Transcrição
[00:00:00] Fizemos a requisição com o Fetch API para a API do viaCEP e tivemos uma Promise como retorno. Mas o que é uma Promise? A Promise é uma promessa de que algo vai acontecer. Como retorno, ela pode ser resolvida ou rejeitada.

[00:00:19] Isso permite que métodos assíncronos se tornem síncronos. Ou seja, ao invés de retornar um valor específico, o valor final, como ainda não chegou lá, ele retorna uma promessa que esse valor uma hora vai chegar. Podemos comparar essa situação, essas promessas, com uma encomenda ou com algo que gostamos muito de fazer: comprar na internet.

[00:00:43] Quando o nosso pedido sai para a entrega, ele gera uma Promise, isto é, uma promessa de que o pedido será entregue ou pode acontecer algum problema e o entregador não conseguir chegar até a sua casa para entregar esse produto.

![Alt text](/img/retorno-da-Promise.png)

[00:01:00] Repare como uma promessa pode ser comparada com situações do nosso cotidiano. Falando sobre a anatomia da Promise para entendermos corretamente seu funcionamento, ela é composta de uma função com os parâmetros Resolve e Reject.


[00:01:18] Se essa promessa foi resolvida, ela vai ser chamada de função Resolve e enviará uma mensagem ou fará alguma ação que você definiu que fosse acontecer.

![Alt text](/img/promise.png)

[00:01:30] Na Promise de entrega, quando acontece a entrega da encomenda, mandamos uma mensagem avisando que a pessoa recebeu a encomenda. Se ela não recebeu, chamamos a função de Reject e enviamos uma mensagem indicando que não foi possível essa entrega.

[00:01:48] Na maioria dos casos, não construímos uma Promise do zero. Ela é gerada a partir de algo síncrono que, no caso, é o nosso Fetch API. Ele está fazendo uma Promise por trás dos panos que foi gerada através da nossa requisição.

[00:02:02] Pode acontecer de a requisição demorar para carregar. Então, ao invés de dar um valor final de erro, ele gera uma promessa, e no futuro teremos o resultado da requisição.

[00:02:15] Uma última curiosidade dentro dessa anatomia da Promise: perceba que estamos enviando uma função como parâmetro para ela e aparecem Callbacks. E é isso que o Resolve e Reject são, dois Callbacks da função da Promise.

[00:02:30] Vamos voltar ao código. O Console está mostrando essa Promise que recebemos do Fetch API. Eu abri a Promise. Existem três tipos de categoria.

[00:02:44] O Protótipo diz que é uma Promise, está afirmando que o que tem ali é uma promessa. O estado dessa Promise é rejeitada. Em seguida, temos o Promise Result, que é o resultado da Promise. Ele deu erro, ou seja, caiu no Reject da promessa. Esse erro não deveria acontecer. Como fazemos para contornar essa situação? Não é isso que eu quero!

[00:03:03] Então, vamos lá no Visual Studio Code. No Fetch API, antes do link [viacep.com.br](https://viacep.com.br/), vamos colocar . Salvei, vou voltar no formulário e clicar "F5" só para ele recarregar o script. Agora ele mudou, não está mais dando erro nenhum e o estado da Promise virou o Fulfilled, significa que está completa. Se analisarmos, existem três tipos de estados que podem aparecer.

[00:03:32] O Fulfilled, que quer dizer que está completa. O Reject, que é o que deu antes e o Pending, que quer dizer que ainda não concluiu. Além disso, o PromiseResult também mudou, ele retornou o objeto do tipo Response, com vários elementos dentro: o body, o bodyUsed e headers. Eles não nos dizem respeito agora. Sobre o objeto Response, para o acessarmos, precisamos usar os métodos das Promises, que vão retornar outras Promises.

[00:04:00] Esses métodos são: o Then, o Catch e o Finally. Eles nos permitirão mostrar na tela todo esse valor do que estamos recebendo, mas, vamos entendê-los melhor na aula que vem. Te vejo lá!