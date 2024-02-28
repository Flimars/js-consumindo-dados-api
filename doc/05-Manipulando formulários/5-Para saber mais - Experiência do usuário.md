## Experiência do usuário

Dentro da área de experiência do usuário, os designers estudam as [heurísticas de Nielsen](https://www.alura.com.br/artigos/10-heuristicas-de-nielsen-uma-formula-pra-evitar-erros-basicos-de-usabilidade?_gl=1*1lxf6x5*_ga*NzEzNDU5MTcuMTY4MjYxMzY2NA..*_ga_1EPWSW3PCS*MTcwOTEzODAyOS4xMDAuMS4xNzA5MTQwMTMyLjAuMC4w*_fplc*Y3IlMkIlMkZxVzMlMkJqSWZralRVYnl2aWIwcU1qeG15Zm8lMkIzTzlUTm5qdFZzSDZxQkRzSUhWWTVSRkxuM2NPNTBYQllZSEp1Z0dUeG1kSFJGeW5JVkIzT01IT1NPOVg1aUN0Yk5oRUMyODRjVElQU2FDTmFvd1MzY1hjeXUlMkJrc2VtdyUzRCUzRA..), que ajudam a projetar uma boa interface e por consequência uma ótima experiência de uso, durante o desenvolvimento desse projeto foi pensado em duas delas:

- Prevenção de erros

Não é uma boa ideia deixar seu usuário errar sem explicar previamente o motivo do erro. Melhor do que isso, tente criar uma interface que permita ao usuário não errar. Para isso, aplicamos o mecanismo de auto completar o endereço de acordo com o CEP do usuário, evitando que os dados sejam enviados errados e ele não consiga receber seu pedido.

- Ajude os usuários a reconhecerem, diagnosticarem e recuperarem-se de erros.

As mensagens de erros tem que ser claras e próximas do conteúdo ou ação que causou o erro. Por isso, aplicamos uma mensagem que aparece abaixo do campo de CEP caso o usuário digite ele incorretamente. Isso ajudará a detectar e resolver possíveis problemas.
___

Para ambas heurísticas, a solução foi aplicada com a manipulação do DOM. O Document Object Model (DOM) é uma interface de programação para os documentos HTML e XML. Representa a página de forma que os programas possam alterar a estrutura do documento, alterar o estilo e conteúdo. O DOM representa o documento com nós e objetos, dessa forma, as linguagens de programação podem se conectar à página. Para entender mais sobre isso, aprenda outras maneiras de transformar seu HTML através do JavaScript com o instrutor Pedro Marins curso [“JavaScript: manipulando o DOM”](https://cursos.alura.com.br/course/javascript-manipulando-dom).