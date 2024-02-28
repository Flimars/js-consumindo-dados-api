Transcrição
[00:00:00] Até aqui, aprendemos muitos conceitos JavaScript assíncronos. Nós consumimos uma API, aprendemos a pegar os valores dela, aprendemos a converter o retorno, a tratar erros. Isso é um aprendizado que vai servir para muita coisa, não só para esse problema que estamos tentando resolver.

[00:00:18] Não se esqueça que somos uma dupla de desenvolvedores da Alura e estamos enfrentando um problema do AluraBooks, que é a normalização de dados de cadastro dos usuários.

[00:00:28] Os clientes estavam cadastrando o nome de uma mesma rua de formas diferentes, mesmo sendo vizinhos, queremos evitar que isso aconteça. Então, vamos consumir aquela API e fazer o autocomplete. O cliente vai preencher o CEP e terá como retorno o bairro, a cidade, etc., tudo automaticamente.

[00:00:45] O primeiro passo é selecionarmos o campo de CEP, faremos tudo em volta dele. Vamos ao index.html e depois procuraremos o campo de CEP. Não é isso? Eu tinha passado, ele está próximo à linha 103. E o ID dele é CEP, precisamos só dessa informação.

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
```

[00:01:04] Então, vou procurar e, no final do script.js, eu vou criar uma variável chamada CEP, var cep. Nela, vou colocar document.getElementById('cep'). Depois eu vou adicionar cep.addEventListener("focusout"). Abriu uma janela gigante.

[00:01:20] Então, ("focusout", () => buscaEndereco(cep.value)). O que aconteceu? Eu criei uma variável CEP, atribuí um caminho grande, o document, quer dizer que ele é um documento HTML inteiro.

[00:01:25] Para isso, usei o método getElementById, o que ele faz? Assim como a sua tradução, ele pega um elemento pelo seu ID. O ID que tínhamos olhado no HTML é o CEP. Então, ele puxou todo aquele campo, não somente o valor que o usuário inseriu.

[00:02:13] Procurou o elemento em si, o elemento HTML. Depois, eu pedi para pegar esse elemento HTML e colocar um ouvinte de eventos para ficar cuidando da vida dele e saber quando acontece determinado evento, o defini como focusout, um evento que ocorre quando a pessoa clica na parte de fora.

[00:02:34] Ao escrever o CEP, ela clicou naquele campo. Ele está selecionado, está com o foco ativo. Após escrever, qualquer lugar em que ela clicar vai tirar o foco. Isso é o focusout.

[00:02:46] Quando ele acontece, chama o buscaEndereço, e manda o valor do CEP. Lembra que tínhamos feito essa parte mais dinâmica no promise.all? Ele recebe um parâmetro e altera - conforme o parâmetro que recebe - a URL do viaCEP?

```
     async function buscarEndereco() {
        try {
            var consultaCEP = await fetch(`htpps://viacep.com.br/ws/${cep}/json/`);
            var consultaCEPConvertida = await consultaCEP.json();
            if(consultaCEPConvertida.erro) {
                throw Error('CEP não existente!');
            }
            console.log(consultaCEPConvertida);
        } catch (erro){
            console.log(erro); 
        }
    }

    var cep = document.getElementById('cep');
    cep.addEventListener("focusout", () => buscaEndereco(cep.value));    
```

[00:03:02] Isso é chamado de Template Strings, que é basicamente composto dessas crases e de valores dinâmicos colocados através do cifrão e das chaves ${}. Com isso, nós já passeamos pelo DOM do nosso site.

[00:03:19] Conseguimos encontrar o valor do campo do input, e enviar para fazer essa consulta dinâmica. Mas ainda não colocamos nada, podemos até testar! Vamos colocar, salvar, acessar no navegador e clicar "F5". Vou colocar o CEP padrão que estávamos usando na função: 01001000 e depois tirar o foco do campo de CEP.

[00:03:47] Coloquei e tirei, cada vez que eu coloco algo e tiro, ele faz uma requisição nova. Já está uma consulta muito dinâmica. Agora precisamos fazer com que essas informações que foram retornadas, como logradouro, estado e cidade, sejam completadas automaticamente. E é isso que, no próximo vídeo, vamos trazer!

![Usando focusout](/img/consultaDinamica.png)
___