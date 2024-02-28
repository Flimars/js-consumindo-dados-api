No último vídeo vimos que é possível detectar eventos nos elementos através do método addEventListener(), que permite chamar funções quando ocorre alguma interação do usuário em específico.

Selecione a alternativa que retorna a frase “Hello World” ao clicar fora do campo de digitação de um formulário:

Selecione uma alternativa

- [ ] ```var campoDeDigitacao = document.getElementById("campoDeDigitacao");
campoDeDigitacao.addEventListener(“clickout", () => console.log(“Hello World”));```

- [ ] ```var campoDeDigitacao = document.getElementById("campoDeDigitacao");
campo.addEventListener("focusout", () => console.log(“Hello World”));```

- [ ] ```var campoDeDigitacao = document.getElementById("campoDeDigitacao");
campoDeDigitacao.addEventListener("focus out", () => console.log(“Hello World”));```

- [x] ```var campoDeDigitacao = document.getElementById("campoDeDigitacao");
campoDeDigitacao.addEventListener("focusout", () => console.log(“Hello World”));```

**Explicações:**

1. Errado! O código até cria a variável recebendo o elemento do campoDeDigitacao, mas o evento “clickout” não existe e isso trará erros na execução do projeto.

2. Errado! Esse trecho de código está criando uma variável com nome “campoDeDigitacao” que recebe o elemento através do seu id, mas está colocando o método addEventListener em outra variável.

3. Não é essa a alternativa certa! Apesar de estar criando uma variável que recebe o elemento através do seu id, o evento “focus out” não existe. Isso acarretará em um erro na execução desse código.

4. Alternativa Correta! Primeiramente estamos criando uma variável que recebe o elemento com id “campoDeDigitacao”, em seguida monitoramos o evento “focusout” (que se refere a retirada de foco desse elemento) para quando ele ocorrer imprimir no console a frase “Hello World”.
___
