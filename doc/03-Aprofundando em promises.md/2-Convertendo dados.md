Observe o trecho de código a seguir:

```
    var requisicao = fetch("https://viacep.com.br/ws/01001000/json/")
        .then(resposta => resposta.json());
```        

Ao fazer uma requisição para uma API com o fetch, é necessário converter os dados recebidos com o método .json(). Por que isso é necessário?

Selecione uma alternativa

- [ ] Pois os dados chegam desformatados e o método json() deixa com um formato mais fácil de visualizar.
- [ ] Pois os dados chegam em outra linguagem de programação e o método json() transforma em JavaScript.
- [x] Pois os dados chegam em formato de bytes e precisamos transformar em outro formato para manipulá-los.
- [ ] Pois os dados chegam criptografados por questões de segurança e não conseguimos acessá-lo.

**Explicações:**

1. Errado! O método .json() transforma os dados em, como seu nome diz, formato JSON. Mas isso não acontece para arrumar a visualização dos dados.

2. Errado! Os dados chegam de uma maneira que é difícil acessar com o JavaScript, mas isso não quer dizer que é em outra linguagem e sim em outra configuração.

3. Correto! O corpo da resposta de uma requisição chega em formato de bytes. Desta forma o .json() transforma o corpo e retorna um json formatado. O formato JSON (JavaScript Object Notation) possui basicamente a mesma sintaxe que a de um objeto JS.

4. Errado! Quase lá! Os dados chegam de uma maneira que não conseguimos acessar, mas não são criptografados e nem abrangem a questão de segurança. Como conseguimos acessar facilmente com o método .json(), seria uma falha de segurança essa facilidade.