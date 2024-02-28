Transcrição
[00:00:00] No último vídeo, eu citei para você que o caso mais comum de uso de Call Backs e de operações assíncronas são as requisições. E nós, da equipe de desenvolvedores da Alura, nos deparamos com um problema nos dados dos usuários que se cadastraram no AluraBooks.

[0:00:19] Esse formulário que estamos construindo já existia, só que ele era um pouco diferente. Verificamos o banco de dados para sabermos como os usuários estavam cadastrados e encontramos vários problemas.

[00:00:32] Por exemplo, um cliente que morava na Rua Getúlio Vargas escreveu o nome inteiro, completo, e o número 1520. No mesmo campo da rua, ele colocou até o número. O Cliente 2 colocou "Rua" abreviada, "Getúlio" abreviado e "Vargas", e o número 1520. O outro colocou "R. Getúlio Vargas", e o outro, só "G. Vargas".

[00:00:55] Quatro clientes moram no mesmo endereço, talvez até no mesmo prédio, e cada um deles escreveu o mesmo endereço de jeitos diferentes. Para normalizar isso, nós pensamos e desenvolvemos um brainstorming.

[00:01:08] Faremos a solução consumindo a API do ViaCEP. Eu vou entrar no site para mostrar a vocês como funciona. Então, ao entrar aqui, há um tutorial de como acessar o webservice de CEP, a validação do CEP, uma explicação dos possíveis erros e os formatos de retorno.

[00:01:27] Usaremos a URL do viacep.com.br/ws/01001000/json para consumir essa API. Basicamente, aquele número com 01001000, vários zeros, é um CEP que eles usaram como padrão. É basicamente ali que vamos colocar o CEP do cliente para trazer o endereço de volta. Foi essa a solução do brainstorming.

[00:01:55] Mas, antes de tudo, o que é uma API? O que é isso que vamos consumir agora? O significado de API é Interface de Programação de Aplicações. Ela permite que dois componentes de software se comuniquem. Chamamos esses dois lados de cliente e servidor.

[00:02:12] Então, a API fica no meio fazendo a conexão. O cliente faz uma solicitação para essa API, ela faz os trâmites e pede ao servidor para retornar a resposta.

[00:02:25] Assim está bem técnico e difícil de entender, então vamos imaginar que você queira pagar um boleto no aplicativo do banco. Quando você acessa o aplicativo no seu celular, você preenche os campos de usuário, conta, dados do banco e a senha.

[00:02:41] No momento que você, cliente, apertou o botão "Entrar", ele está enviando uma solicitação para o servidor. No meio deste processo está a API formalizando a sua requisição para o servidor entender.

[00:02:53] E o servidor vai retornar, através da API, deixando mais organizado, legível, seu saldo, número da conta e nome. Ele vai permitir várias interações: pagar boleto, ver o saldo, transferir, fazer um PIX. Várias coisas.

[00:03:14] Enfim, no meio de todas essas interações, existe a API, aquele link viacep.com.br/ws/ que vamos pegar para conseguir acessar o servidor deles. Mas como fazer essa interação? Através do Fetch API.

[00:03:26] Outra vez no ViaCEP, copiaremos o link viacep.com.br/ws/01001000/json e voltaremos ao código. Você pode tirar totalmente aquela simulação de conversa de chat que tínhamos feito, porque não usaremos mais.

[00:03:40] Primeiro, vamos criar uma variável com o nome de consultaCEP. Vamos adicionar consultaCEP = fetch ('viacep.com.br/ws/01001000/json/').

[00:04:03] Já estamos gerando uma requisição. Vou fazer console.log(consultaCEP). Agora ele vai imprimir o resultado desse Fetch no navegador. Vou salvar e abrir.

[00:04:17] Para isso, vamos à pasta do nosso projeto, "Documentos > dev > Cadastro AluraBooks". Em seguida, abriremos o Index. Com ele já aberto, vamos à Ferramenta do Desenvolvedor, que é o botão direito, "Inspecionar" ou "F12". No Console, verificaremos que ele retornou uma Promise.

[00:04:37] O método Fetch é assíncrono e tem como parâmetro obrigatório a URL da API. Ou seja, usamos o ViaCEP, usando outra opção, obteríamos outro link, e é esse link que é obrigatório, o único parâmetro obrigatório desse método.

[00:04:54] Colocamos esse valor dentro de uma variável para conseguirmos consultar o retorno - consultamos o valor através do console.log. E o que ele retornou para nós? Uma Promise, isto é, uma promessa.

[00:05:07] E o que é isso? Por que não retornou alguma frase ou algum conteúdo, retornou uma promessa? É o que descobriremos no próximo vídeo. Fica aí a curiosidade! Te vejo lá!