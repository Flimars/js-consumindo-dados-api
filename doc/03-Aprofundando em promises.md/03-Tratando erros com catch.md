Transcrição
[00:00:00] No vídeo passado, aprendemos sobre o método then(). O método then(), em português, significa "então". O que ele faz? Ele pega a requisição, e aquele valor, ele faz alguma operação com ele. Faz alguma coisa com a resposta retornada. Mas ele só faz se aquela promessa foi resolvida.

[00:00:20] O que acontece se der algum erro e aquela promessa for rejeitada? Por enquanto, não acontece nada. Vamos precisar aprender outro método para imprimir isso na tela. Você vai no Visual Studio Code, e após o último then que colocamos, está na linha três, vamos colocar .catch().

[00:00:35] Vou selecionar a tecla "Enter", antes do ponto, para ele ficar para baixo e ficar mais fácil de visualizarmos. Então, vamos colocar catch(erro => );, que é outra arrow function, console.log(erro): catch(erro => console.log(erro));

[00:00:47] Se eu testar agora, não vai funcionar, não vai acontecer nada. Quer dizer, vai acontecer. Vai dar certo, então não vai cair no catch. Porque o nosso CEP está digitado corretamente.

[00:01:09] Eu vou tirar um zero do link do fetch, porque eu quero que dê problema mesmo. Vou salvar e testar no navegador. Então, eu fui no nosso formulário de cadastro, em que estamos testando nossos scripts e vou clicar na tecla "F5", para recarregar a página. Está demorando um pouco, está pensando. E deu erro.

[00:01:32] Aqueles erros em vermelho são erros do navegador. Então, se você estiver usando o Chrome, o Opera, ou outra coisa, pode ser que apareça o mesmo erro com outra mensagem, porque não é o erro que estamos tratando.

[00:01:44] Aquele último erro escrito em branco, TypeError: failed to fetch, é aquilo que mandamos imprimir no console.log, através do catch. E toda promise retorna esses dois métodos. Ela retorna o then, caso ela for resolvida. E retorna o catch, caso ela seja recusada.

[00:02:07] Você pode interpretar assim: catch em português significa "pegue". Assim, caso aconteça algum erro, ele pega o erro e imprime na tela. Basicamente podemos entender dessa forma para ficar mais fácil de entender como ele está funcionando.

[00:02:22] E essa mensagem é difícil de entender. TypeError: failed to fetch. Imagine sobre a encomenda que eu estava falando até agora. Se a minha encomenda saiu para entrega e não é entregue na minha casa, eu gostaria de uma mensagem que me avisasse o que aconteceu.

[00:02:35] Se não, eu ia pensar: "Meu Deus, entregou para quem? Entregou para um vizinho? Entregou para alguém errado?". Então, para ajudar esse cliente, para dar influência para outros sites fazerem uma mensagem que possamos entender o que está acontecendo, vamos customizar isso.

[00:02:49] Para fazer isso, vamos no Visual Studio Code, na linha três, em que temos o segundo .then. E depois da flecha, do r =>, vamos abrir chaves, e fechar após o console.log(r).

[00:03:06] Vou clicar na tecla "Enter" duas vezes para facilitar a visualização do que eu estou fazendo. Vou colocar if, uma condicional que significa "se". Se (r.erro) for verdade, eu quero que ele faça alguma operação. Coloquei duas chaves de novo, o que estiver ali dentro é um código. E vou colocar throw Error ('').

[00:03:37] Entre os parênteses: ('Esse cep não existe!') E se não for verdade, então else, ele vai dar o console.log(r). O que aconteceu? Eu vou salvar, só que esse erro também não vai dar certo, porque eu quero um CEP que não existe.

[00:04:02] Então eu vou colocar no fetch, em que tem o CEP, eu vou colocar 01001250. Não deve existir, vou salvar e vamos analisar no navegador o que aconteceu. Vou recarregar.

[00:04:18] Agora ele deu esse erro de que o CEP não existe. Por que eu fiz esse tratamento, do (r.erro)? Vamos no viaCEP comigo. Quando ele fala da validação do CEP, no site do viaCEP, ele nos explica como lidar com erros.

[00:04:33] Então, quando consultado um CEP de formato inválido, por exemplo, nove dígitos, alfa numérico, espaço, o código de retorno da consulta é 400. Ele puxa o erro direto. Ele vai dar a promessa rejeitada e vai cair naquele console.log do catch que fizemos.

[00:04:51] Mas se você reparar, nenhum desses casos, é: caso o CEP não exista. No segundo parágrafo, ele explica como funciona, como ele faz esse tratamento de erro.

[00:05:02] Ele explica que, quando consultado um CEP de formato válido, porém inexistente, o retorno encontrará um valor de erro igual a true. Por isso que tratamos desse jeito. Observe o nosso código. Estou com o Visual Studio Code aberto.

[00:05:17] Então, para CEPs que não existem, ele não vai voltar reject, ele não vai no catch, mas no then. E para pegarmos esse erro, temos que fazer essa condicional.

[00:05:31] Se o retorno foi um erro igual a true, não precisamos informar que é true. Eu só coloquei (r.erro), ele vai imprimir um erro chamado de "Esse cep não existe!". E o catch vai pegar aquele erro que eu coloquei. E caso não esteja incorreto, ele vai continuar, vai dar o else console.log(r) e imprimir sem mandar erro nenhum.

[00:05:55] Quando conseguimos outras maneiras de exibir erros, podemos colocar no throw Error. Desta maneira, faz ainda mais sentido usar o catch, porque ele pega esse erro"

[00:06:05] E com os outros condicionais, podemos dar um jeito de imprimir mensagens customizadas direto no catch, sem ser esse caso do "CEP não existe", que ele passa como Resolve. Então, quem sabe você não faz, como desafio, algumas mensagens customizadas a partir do throw Error, ou só mudando no console.log e fazendo uma condicional lidando com o que está vindo errado.

[00:06:25] A partir disso, aprendemos a fazer mensagens customizadas para erros. E quem sabe, vendo a maneira como se faz, com as condicionais, com o throw Error, você não consegue fazer, como desafio, outros erros que podem cair com essas ações de forçar o erro.

[00:06:41] Coloca outro CEP e veja qual o possível erro que pode vir, e tenta tratar para fazer outras mensagens. Aposto que vai ser um desafio para você treinar e vai ser legal!

[00:06:51] Por enquanto é isso, a maneira de tratar é com o catch. Mas ainda tem um método de promises que não vimos, o finally. E vamos ver no próximo vídeo!
___