Transcrição
[00:00:00] Lembra da consulta que você estava tentando marcar? Quando você ligou para o consultório e falou com a secretária, ela gerou uma promessa para você. Ela tentou pegar um horário e não tinha, deu uma promessa rejeitada, não tinha. Ela precisou te avisar que não tinha, ela pegou essa informação e repassou para você.

[00:00:21] Tem dois termos que vamos usar bastante nesse vídeo, o try, "tentar", e o catch, sendo o "pegar". Vamos aplicar essa forma de acontecer um reject no código.

[00:00:33] Vamos abrir o Visual Studio Code, e no início, antes da declaração da variável consultaCEP, você vai colocar try, sendo o “tentar”, abre e fecha chaves. Vamos pegar o fechamento e colocar abaixo do console.log. E depois colocar catch (erro), abre e fecha chaves.

```
    async function buscarEndereco() {
        try {
            var consultaCEP = await fetch('htpps://viacep.com.br/ws/01001000/json/');
            var consultaCEPConvertida = await consultaCEP.json();
            console.log(consultaCEPConvertida);
        } catch (erro){
            console.log(erro); 
        }
    }

    buscaEndereco();

```

[00:00:55] Dentro dessas chaves, vamos colocar console.log(erro). Vamos salvar, e analisar o resultado no navegador. Na tela de cadastro, em que estávamos com o formulário do AluraBooks.

[00:01:11] Vou clicar na tecla "F5", está dando tudo certo. Agora vamos testar o que eu fiz do try e catch. Vamos minimizar o Visual Studio Code, no navegador, na tela de cadastro e clicar na tecla "F5". Continua aparecendo o endereço, mas isso porque nosso CEP está certo.

[00:01:27] Eu vou tirar um zero do Fetch API só para forçar esse erro. Salvei e vou clicar na tecla "F5", está demorando um pouco. Ele retornou aqueles dois erros, em vermelho, que eu até comentei - erro do navegador, não e não do código. E ele imprimiu o failed to fetch, o erro que gerou do código.

[00:01:48] Estamos captando o erro, e a partir daquele ciclo que aconteceu na consulta, é bem fácil de entender fazendo essa tradução. Porque ele vai tentar fazer tudo aquilo para captar o endereço, aquela lista que diz endereço, cidade, estado, etc. Senão, ele vai pegar o erro e mostrar na tela.

[00:02:07] É até mais fácil de compreender como funciona, desse jeito. E lembra que quando estávamos vendo sobre o tratamento de erros, com o then e o catch, vimos que a viaCEP, ela manda um erro diferente.

[00:02:20] Caso sejam CEPs com os dígitos que são necessários, mas ele não exista, eles mandam um erro igual a true. Eles não mandam um erro 400, mas sim dessa maneira, então precisaremos fazer uma condicional novamente.

[00:02:34] Dentro do try, antes do console.log, vamos colocar if (consultaCEPConvertida.erro), abrir e fechar chaves. Dentro, vamos colocar throw Error('CEP não existente!'). Fecha as chaves embaixo, e o console.log embaixo, porque se não tiver erro, ele vai continuar.

[00:03:10] Vamos salvar e colocar um CEP que sabemos que vai dar esse erro: 01001250, na linha três. Salvei e vamos forçar esse erro. Vamos no navegador, clicar na tecla "F5", e retornou "CEP não existente!". Com isso, já conseguimos fazer uma mensagem de erro customizada.

```
     async function buscarEndereco() {
        try {
            var consultaCEP = await fetch('htpps://viacep.com.br/ws/01001250/json/');
            var consultaCEPConvertida = await consultaCEP.json();
            if(consultaCEPConvertida.erro) {
                throw Error('CEP não existente!');
            }
            console.log(consultaCEPConvertida);
        } catch (erro){
            console.log(erro); 
        }
    }

    buscaEndereco();
```
![f12-console-error](/img/f12-console-error.png)

[00:03:31] Essa parte em específico é bem parecida. Forçamos um erro e, se acontecer essa situação para exibir esse erro, ele vai pegar com o catch e imprimir na tela. Essa é basicamente a estrutura, não é muito diferente do que vimos antes, mas não conhecíamos o try, e nesse caso, é ele que temos que usar, em conjunto ao catch.

[00:03:52] Porém, e se quiséssemos fazer várias requisições em simultâneo? Por exemplo, fazer um acompanhamento mensal no dentista. Como faríamos várias requisições ao mesmo tempo, sem utilizar "Ctrl + C" e "Ctrl + V" na mesma função e aplicar arranjos? Veremos no próximo vídeo uma maneira de fazermos isso! Até lá!
___