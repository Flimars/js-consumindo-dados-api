## Then ou Async Await?

Quando produzimos um código assíncrono com o uso do .then nós fazemos uso de callback dentro deles. O maior problema com callbacks é que eles não são bem dimensionados mesmo para códigos assíncronos moderadamente complexos, onde temos vários .then em seguida do outro. O código resultante geralmente se torna difícil de ler, fácil de quebrar e difícil de depurar. Isso é o que chamamos de callback hell.

Para resolver isso, foi desenvolvido outra forma de construir um código assíncrono: o async await, que funciona de forma semelhante ao then mas o código fica mais “bonito”. Esse “embelezamento” em códigos é o que chamamos de syntax sugar.

Em ciência da computação, syntax sugar ou açúcar sintático (em tradução literal), é a sintaxe dentro de uma linguagem de programação que foi concebido para tornar as coisas mais fáceis de ler ou expressar. Isso torna a linguagem "mais doce" para uso humano: as coisas podem ser expressas de forma mais clara, de forma mais concisa, ou em um estilo alternativo que alguns podem preferir.

O async/await apesar de ser uma opção mais "legível" ao .then() é importante frisar que não são logicamente equivalentes: o async/await faz o processamento de forma sequencial, Promises com .then() são processadas em paralelo, o que faz com que este método seja mais rápido. O async/await simplifica a escrita e a interpretação do código, mas não é tão flexível e só funciona com uma Promise por vez.

O artigo [“Async/await no JavaScript: o que é e quando usar a programação assíncrona?”](https://www.alura.com.br/artigos/async-await-no-javascript-o-que-e-e-quando-usar?_gl=1*axkcr*_ga*NzEzNDU5MTcuMTY4MjYxMzY2NA..*_ga_1EPWSW3PCS*MTcwOTEzNDYwMC45OS4xLjE3MDkxMzU5NTEuMC4wLjA.*_fplc*Y3IlMkIlMkZxVzMlMkJqSWZralRVYnl2aWIwcU1qeG15Zm8lMkIzTzlUTm5qdFZzSDZxQkRzSUhWWTVSRkxuM2NPNTBYQllZSEp1Z0dUeG1kSFJGeW5JVkIzT01IT1NPOVg1aUN0Yk5oRUMyODRjVElQU2FDTmFvd1MzY1hjeXUlMkJrc2VtdyUzRCUzRA..) pode te ajudar a entender ambos os casos e suas diferenças.
___