Transcrição
[00:00:00] Não há só uma maneira de fazer um código assíncrono. Do mesmo jeito que não existem só esses casos na realidade de situações assíncronas que eu comentei até agora.

[00:00:10] Vamos imaginar que você queira marcar uma consulta com o dentista na terça-feira. Você vai ligar para a secretária do consultório, ela vai atender, vai dizer que ela vai procurar um horário naquele dia, gerando uma promessa com você. Essa promessa, essa busca por horários, pode ser resolvida achando esse horário disponível e ela pode ser rejeitada, não tendo horário nenhum.

[00:00:32] Mas vamos supor que tem vários horários para terça-feira. Você só declarou querer na terça, não especificou o horário. A secretária ia ter que procurar cada horário e ver se dá para você comparecer. Por exemplo. "Eu tenho horários às 2h. Você pode vir?" Aí você vai responder sim ou não. "Eu tenho horário às 5h. Você pode vir?"

[00:00:51] Imagine que vai ter várias then. E dentro de cada then do nosso código, temos uma Arrow Function. O que tínhamos aprendido no início desse curso sobre funções enviadas como parâmetros para outras funções? Que são os callbacks.

[00:01:08] Quando temos vários "então", temos vários callbacks. E esse termo e essa situação é bem conhecida com o termo de Callback Hell - o Inferno de callbacks. Quando temos vários then() com várias funções. Não é uma condição de fácil leitura.

[00:01:27] Temos outra maneira de fazer essa programação assíncrona, e é isso que vamos transformar agora no código que estávamos fazendo, para ficar mais fácil a leitura.

[00:01:37] Eu quero você abra o Visual Studio Code, e vamos apagar todos aquele then, finally e catch que tínhamos feito. Vamos voltar à estaca zero. Também vou arrumar o CEP, porque eu tinha colocado um CEP errado. Então coloquei "01001000". Salvei.

[00:01:53] Vamos aprender outra maneira, do início, de como fazer um código assíncrono. Quero que você selecione a tecla "Enter" nessa declaração da variável consultaCEP, para criarmos uma função.

![Do Começo](/img/apenasFecth.png)

[00:02:04] Para criarmos uma função, vamos usar async function buscaEndereco, abre e fecha parênteses, abre e fecha chaves. Você vai fechar as chaves após o var consultaCEP. E você vai usar a palavra await antes do fetch.

[00:02:21] Agora, ao invés de darmos um console.log(consultaCEP), porque agora não queremos chamar a variável. O que queremos é chamar a função. Eu vou chamar a função com buscaEndereco(), abre e fecha chaves, porque ele chama ela e a coloca na Call Stack.

[00:02:39] E eu vou fazer o console.log dentro dessa função. console.log(consultaCEP). Vou salvar, e vamos ver o que acontece. Eu vou ao navegador e selecionar a tecla "F5" na tela de cadastro. Agora eu fiz a solicitação. Note, ele já me mandou até o objeto response. Bem mais rápido do que foi o outro.

[00:03:03] Essa questão do Async/Await foi declarada pela ES em 2017 para facilitar a leitura dos códigos assíncronos. Porque, apesar de ser assíncrono, ele é construído como um código síncrono. Ou seja, parece que é feito linha por linha, mesmo que, no fundo, ele esteja esperando uma coisa acontecer antes de fazer a outra.

[00:03:21] Apenas definindo a função como async, podemos usar essa palavra await. Ou seja, se você tentar colocar esse await em qualquer lugar que não seja uma função assíncrona, vai dar problema. Ele vai te cobrar que ela só é aceita dentro de uma função assíncrona.

[00:03:35] Agora estamos com o mesmo problema que deu no início. Lembra que eu mencionei sobre o conversor? Precisamos converter esse retorno do fetch em JSON. Eu vou inserir na linha 3, var consultaCEPConvertida = await consultaCEP.json. E vou imprimir isso no lugar, consultaCEPConvertida no console.log.

![método async](/img/async.png)

[00:04:00] Vou salvar, e vamos analisar no navegador o resultado. Vou clicar na tecla "F5" e pronto! Agora ele está retornando o endereço que queríamos com sucesso, em três linhas dentro dessa função. Antes eu tinha feito dois then e usados outras funções. Dessa maneira que executamos agora, parece que é bem mais fácil, não é? Uma coisa, um passo por vez.

![retorno do método async](/img/returnAsync.png)

[00:04:21] E como eu trato o erro? Porque no then tinha o catch. E como eu faço com Async/Await para resolver isso? É isso que veremos no próximo vídeo. Até lá!
___