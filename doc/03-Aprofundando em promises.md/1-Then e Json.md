Transcrição
[00:00:00] Lembra que comentei sobre uma entrega, que estávamos esperando receber, e esse status de entrega era como uma promessa? E quando ela era entregue, essa promessa era resolvida, e quando acontecia alguma coisa com o entregador, a promessa era rejeitada?

[00:00:17] Então, em qualquer uma dessas situações, a resposta que vai chegar em nós, é um objeto do tipo Response. E como fazemos para acessar esse objeto? Vamos no trecho de código, que criamos aquela variável consultaCEP. Então, ao final do fetch, você vai colocar: .then ();.

[00:00:37] Em um panorama mais geral, uma promessa sempre vai retornar um objeto do tipo response, seja ela rejeitada ou resolvida. E esse then() funciona assim, como a sua tradução. Ele é basicamente um “então”. Que é: faça o fetch, ele vai lá e faz a requisição.

[00:00:56] E então, com aquela resposta, ele vai fazer alguma operação que vamos colocar dentro do then(). E a resposta, sendo do objeto do Response, não vem da maneira que podemos acessar. Vamos precisar converter. Que é da mesma maneira que, como se aquela encomenda que eu estava comentando, ela tivesse vindo com a voltagem 110V. E as tomadas da sua casa são 220V, e você precisa de um adaptador.

[00:01:24] Ele vai fazer essa conversão de voltagem para você poder usar o seu aparelho. Vamos fazer a mesma coisa que essa resposta. Então, vamos colocar: resposta =>;, porque estamos formando uma arrow function. E a resposta, vamos colocar novamente json(). Salvei, e vamos entender, em termos técnicos, porque aconteceu essa conversão.

[00:01:49] O objeto do tipo Response nos trouxe um corpo de resposta que não conseguíamos acessar. Ele trouxe um amontoado de bytes. Usamos o JSON para ele converter essa resposta em json, que é um formato muito usado no desenvolvimento em JavaScript, porque ele parece um objeto JavaScript.

[00:02:07] Então, vamos conseguir acessá-lo. Mas ainda assim, salvando essa alteração, vamos ver o resultado. Salvei e agora eu vou testar o que retorna para nós. Cliquei na tecla “F5”, ainda não exibiu nada. Porque eu só fiz a conversão, eu não pedi para exibir na tela.

[00:02:22] E seguindo a lógica do then(), sendo “então”, vamos colocar outro then(), quando fecha o anterior. Então, no final vamos incluir .then(). Eu vou pegar novamente uma resposta ou eu vou colocar “r”, (r =>). É novamente uma arrow function: console.log. E vai imprimir esse “r”: console.log(r). Vou salvar e ir no navegador, clicar na tecla “F5”, novamente.

[00:02:48] Ele primeiro fez a promessa, nos disse que ela estava executando, e depois imprimiu o valor dela. Ainda na linha da variável que pedimos o console.log, e imprimiu todos os dados que precisávamos: o bairro, o CEP e o complemento.

[00:03:04] Então, eu vou ajeitar o código. Estou com o script.js aberto. Vou clicar na tecla “Enter” depois do .then, o primeiro. E depois clicar na tecla “Enter” no segundo .then. Agora ele ficou apresentável, um embaixo do outro, fica mais fácil visualizarmos. Tudo se tratando da primeira promessa.

[00:03:21] Com isso, temos uma cadeia de then(), porque fizemos o fetch, fizemos a requisição. Então, com a requisição, nós convertemos. Depois, esse outro “então”, é referente à promessa de antes, da promessa da conversão.

[00:03:36] Então vamos sempre fazer algumas coisas que resultem em outras. Eu tenho uma promessa, “então”, ela vai realizar algum comando quando ela for resolvida ou rejeitada.

[00:03:51] Tem várias coisas que você pode associar, que falando em português e em voz alta, fica fácil de entender. Porque você faz uma associação na sua cabeça com a própria língua portuguesa.

[00:04:04] Mas, e se retornasse o Reject? Ele ainda só retornaria o que nos foi exibido? Como eu faço a impressão desse erro? É legal avisar para o usuário que está com algum problema na requisição que ele solicitou. No próximo vídeo, vamos conhecer o método catch, que vai ajudar a fazer essa impressão de erros.
___