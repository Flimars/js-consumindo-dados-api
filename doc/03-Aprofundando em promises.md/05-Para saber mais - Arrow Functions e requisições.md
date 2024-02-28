## Arrow Functions
Dê uma olhada na estrutura do nosso código dentro do primeiro método .then dessa requisição: .then(resposta => resposta.json()). O conteúdo que está ali presente é uma função, mas construída de uma maneira diferente se torna uma arrow function. A versão ES6 do ECMAScript trouxe uma nova forma mais sucinta de trabalhar com funções chamada de Arrow Functions, por causa da sintaxe que lembra uma flecha: () =>.

Em uma função tradicional, caso você crie uma variável dentro dela, seu contexto é referente a função onde ela está. Para entender melhor: se você usar a palavra chave “.this”, você está se referindo a essa função em si.

Já em uma arrow function temos um contexto externo. Por exemplo, se essa arrow function for criada dentro de outra função seu contexto será aquela função que ela está dentro. Caso a função for aplicada fora de outra função, seu contexto será global, o código inteiro.

Quer aprender mais sobre esse termo? O nosso parceiro Marco Bruno te ensina em seu vídeo:

<iframe width="560" height="315" src="https://www.youtube.com/embed/3EkS9-P3cIM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[YouTube: Como funciona Arrow Function](https://youtu.be/3EkS9-P3cIM)


Retornos de requisições
Quando estamos realizando uma requisição para a API, estamos trocando mensagens HTTP’s. [HTTP](https://www.alura.com.br/artigos/desmistificando-o-protocolo-http-parte-1?_gl=1*2afvz7*_ga*NzEzNDU5MTcuMTY4MjYxMzY2NA..*_ga_1EPWSW3PCS*MTcwOTExNTgyMC45OC4xLjE3MDkxMjk5NzQuMC4wLjA.*_fplc*Y3IlMkIlMkZxVzMlMkJqSWZralRVYnl2aWIwcU1qeG15Zm8lMkIzTzlUTm5qdFZzSDZxQkRzSUhWWTVSRkxuM2NPNTBYQllZSEp1Z0dUeG1kSFJGeW5JVkIzT01IT1NPOVg1aUN0Yk5oRUMyODRjVElQU2FDTmFvd1MzY1hjeXUlMkJrc2VtdyUzRCUzRA..) é um protocolo, uma forma de conversa entre duas máquinas, que permite transferir hiper-texto de um lado a outro. Daí o nome Hyper Text Transport Protocol.

Uma requisição é composta de uma request (solicitação) e uma response (resposta). Request e Response são dois tipos de mensagem diferentes quando falamos de HTTP. A especificação HTTP diz exatamente o que podemos colocar dentro de cada um destes tipos de mensagem para que todos que "falem" o idioma HTTP consigam trocar informações corretamente.

Em uma response é retornado um response code (código de resposta) e um motivo, que dá significado ao código. A estrutura padrão desse código tem três dígitos, sendo o primeiro referente a classificação dele. Elas são:

1XX: Informativo – a solicitação foi aceita ou está em andamento;
2XX: Confirmação – a solicitação foi concluída ou entendida;
3XX: Redirecionamento – faltou alguma coisa na solicitação;
4XX: Erro do cliente – houve um erro na solicitação;
5XX: Erro no servidor – houve uma falha no servidor durante a solicitação.
Durante essa aula nós conhecemos um deles: quando consultado um CEP de formato inválido na API do ViaCEP ela nos retornará o código 400 (Bad Request).

Caso você queira saber mais sobre os tipos de código de resposta do protocolo HTTP recomendo a aplicação [HTTP Cat](https://http.cat/) que demonstra de forma descontraída as diferentes categorias que podemos encontrar. Para entender melhor sobre o funcionamento das requisições, temos o curso [“HTTP: Entendendo a web por baixo dos panos”](https://cursos.alura.com.br/course/http-fundamentos) do instrutor Fábio Pimentel.
___

Além de todos esses conhecimentos novos, fizemos com sucesso uma requisição com os métodos das promises .then e .catch. Pra reforçar ainda mais o seu aprendizado, recomendo o artigo [“Começando com fetch no JavaScript”](https://www.alura.com.br/artigos/comecando-com-fetch-no-javascript?_gl=1*14umm86*_ga*NzEzNDU5MTcuMTY4MjYxMzY2NA..*_ga_1EPWSW3PCS*MTcwOTExNTgyMC45OC4xLjE3MDkxMjk5NzQuMC4wLjA.*_fplc*Y3IlMkIlMkZxVzMlMkJqSWZralRVYnl2aWIwcU1qeG15Zm8lMkIzTzlUTm5qdFZzSDZxQkRzSUhWWTVSRkxuM2NPNTBYQllZSEp1Z0dUeG1kSFJGeW5JVkIzT01IT1NPOVg1aUN0Yk5oRUMyODRjVElQU2FDTmFvd1MzY1hjeXUlMkJrc2VtdyUzRCUzRA..) e o Alura+ da instrutora Juliana Negreiros onde ela explica brevemente sobre [“JavaScript assíncrono e fetch”](https://cursos.alura.com.br/extra/alura-mais/javascript-assincrono-e-fetch-c93).
___