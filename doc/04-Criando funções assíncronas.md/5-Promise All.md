Transcrição
[00:00:00] Vamos supor que você queira fazer um acompanhamento mensal com esse dentista que estávamos marcando consulta. Você teria que fazer várias requisições, solicitando dias e horários diferentes. Isso não é diferente do que acontece nessas nossas consultas e contatos com a API.

[00:00:18] Por exemplo, no do viaCEP que estamos consumindo. Pode ser que você queira ver vários CEPs ao mesmo tempo. Como você faria isso? Vamos descobrir agora, em conjunto com o promise.all.

[00:00:32] Porém, primeiro vamos transformar essa função em algo que está esperando receber um parâmetro, um valor de parâmetro. Na primeira linha, vamos ter async function buscaEndereco(). Dentro dos parênteses, você vai colocar a palavra CEP, ou qualquer uma que você quiser, isso não vai importar muito.

[00:00:51] No fetch, vamos colocar no lugar em que tinha as aspas simples ou aspas duplas, crase. Coloquei no início e no final. E onde tinha o valor do CEP, agora vamos colocar um cifrão (“$”), abre e fecha chaves. Dentro delas, vamos colocar aquele valor que esperamos receber como parâmetro.

[00:01:13] Como eu tinha colocado o CEP, também vou colocar ${cep}. Depois, vamos colocar um retorno, que vai retornar o (consultaCEPConvertida). Vamos incluir após o console.log, na linha oito. Clicamos na tecla "Enter", então vai ser na linha nove.

[00:01:31] Vou colocar return consultaCEPConvertida. Ele vai retornar para quem estiver chamando essa função, esse valor. No final, antes da chamada da função, vamos colocar let ceps =, vamos incluir um array de CEPs aleatórios. Vou colocar aquele que estávamos usando: 01001000.

[00:01:56] Vírgula, abre chaves de novo, e vamos colocar a mesma coisa, mas terminando em um: 01001001. Eu tenho o meu array de CEPs, e vamos fazer um array de conjunto de CEPs. Ele vai fazer várias buscas. Para isso, vamos incluir ceps.map(). E dentro do map faremos uma arrow function igual as que fizemos nos outros lugares.

[00:02:22] Vamos colocar valores =>. Ele vai pegar o endereço, buscaEndereco(), e dentro dos parênteses ele vai colocar esses valores que ele estava pegando. Então, aqui ele vai fazer um novo array com o que retornar daquela função buscaEndereco, para cada um dos valores de dentro do CEP. Esses valores vão ser promessas, e precisamos resolver essas promessas.

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

    let ceps = ['01001000','01001001'];
    let conjuntoCeps = ceps.map(valores => buscaEndereco(valores));

```

[00:02:51] E para isso, usaremos o promise.all. O promise.all(conjuntoCeps), ele vai resolver o array de promessas, e vamos pedir para imprimir com o then. then(respostas => console.log(respostas)). Porque eu quero imprimir o que ele vai ter resolvido.

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

    let ceps = ['01001000','01001001'];
    let conjuntoCeps = ceps.map(valores => buscaEndereco(valores));
    Promise.all(conjuntoCeps).then(respostas => console.log(respostas));
    
```

[00:03:20] Salvei e vamos testar no navegador. Cliquei na tecla "F5", ele fez cada uma das situações separadamente. Cada vez que ele chamou a função, ele passou naquele console.log de dentro da função. Depois imprimimos o promise.all, o resultado dele.

![Alt text](/img/promiseAll.png)

[00:03:39] Ele retornou um array com as duas promessas resolvidas. Para entender melhor o que aconteceu, podemos tentar imprimir aquele conjunto CEPs, aquele que chamou duas vezes a função buscaEndereco, para verificar o que acontece antes de botar o promise.all.

![Alt text](/img/promiseAll2.png)

[00:03:54] Então, console.log(conjuntoCeps). Salvei, vou no navegador e vou atualizar. Lembra que antes tinha aparecido os dois resultados do endereço, e depois um array com as duas promises revolvidas.

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

    let ceps = ['01001000','01001001'];
    let conjuntoCeps = ceps.map(valores => buscaEndereco(valores));
    console.log(conjuntoCeps);
    Promise.all(conjuntoCeps).then(respostas => console.log(respostas));
    
```

[00:04:11] Quando colocamos o console.log, para ele agir antes do promise.all, ele retornou duas Promises. Elas não estavam resolvidas e com todo o corpo possível para visualizarmos na tela.

![Promise.All](/img/promise-all.png)

[00:04:21] É isso que o promise.all fez, ele nos ajudou a fazer várias requisições ao mesmo tempo. Entendendo para que funciona o promise.all, já podemos tirar essa chamada gigante, que não vamos fazer várias requisições para resolver esse problema que estamos tentando solucionar para a API do viaCEP, sendo aquela normalização de dados.

[00:04:40] Eu vou apagar essas linhas que eu fiz fora da função. E o que precisamos fazer agora? Nós já temos uma busca dinâmica, que ele pega um parâmetro e altera na URL. Mas só mostramos no console, na Ferramenta do Desenvolvedor.

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

[00:04:57] Como faremos para colocar isso lá no formulário, para facilitar o cadastro do usuário quando ele estiver preenchendo? Vamos manipular o DOM para chegar em um resultado muito legal, que quando o usuário coloca o CEP dele, os outros campos são completados automaticamente. Vamos aprender isso na próxima aula. Até lá!
___