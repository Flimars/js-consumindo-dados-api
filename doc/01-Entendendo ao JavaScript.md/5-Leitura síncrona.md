```
function mandarMensagem() {
console.log(“Estou aprendendo a programar.”);
}
console.log(“O javascript é legal.”);
mandarMensagem();
console.log(“Eu gosto de HTML e CSS.”);

```
Com o event loop reproduzindo esse código através do empilhamento de ações na call stack, qual será a ordem que poderemos visualizar essas frases no console?
- [ ] Opção A:
Estou aprendendo a programar.
O javascript é legal.
Eu gosto de HTML e CSS.

- [x] Opção B:
O javascript é legal.
Estou aprendendo a programar.
Eu gosto de HTML e CSS.


É isso aí! O código será lido linha por linha e o console.log de dentro da função será impresso quando a função for chamada, ou seja, entre a frase “O javascript é legal” e a “Eu gosto de HTML e CSS”.

- [ ] Opção C:
O javascript é legal.
Eu gosto de HTML e CSS.
Estou aprendendo a programar.