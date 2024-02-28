A estrutura utilizada para construir um código assíncrono anteriormente foi a do .then, um método que as Promises disponibilizam:

```
var requisicao = fetch("https://localhost:5000/")
.then(resposta => resposta.json())
.then(respostaConvertida => console.log(respostaConvertida));

```
Esse código faz uma requisição pra uma API através de seu link em conjunto do método fetch e em seguida converte o resultado para JSON. De que maneira podemos reproduzir o mesmo código usando async await?

Selecione uma alternativa

- [ ] ```async function geraRequisicao() {
    var requisicao = fetch(“https://localhost:5000”);
    var respostaConvertida = requisicao.json();
}```

- [x] ```async function geraRequisicao() {
    var requisicao = await fetch(“https://localhost:5000”);
    var respostaConvertida = await requisicao.json();
}```

- [ ] ```async geraRequisicao() {
    var requisicao = fetch(“https://localhost:5000”);
    var respostaConvertida = requisicao.json();
}```

- [ ] ```function geraRequisicao() {
    var requisicao = await fetch(“https://localhost:5000”);
    var respostaConvertida = await requisicao.json();
}```

**Explicações:**

1. A declaração async function define uma função assíncrona, mas esse trecho de código não está aguardando o resultado das Promises.

**2. A declaração async function define uma função assíncrona e o operador await é utilizado para esperar por uma Promise. Dessa maneira, nossa requisição funcionará corretamente.**

3. Ao testar esse trecho de código nos retornaria um erro, pois a declaração de função está com uma estrutura incorreta: é necessário informar que isso é uma função através do function.

4. O operador await é utilizado para esperar por uma Promise. Ele somente pode ser usado apenas dentro de uma função declarada como assíncrona.

Parabéns, você acertou!

