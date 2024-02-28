Transcrição
[00:00:00] Um usuário pode preencher errado o campo de CEP e é o nosso dever avisar. Antes estávamos só captando e mostrando no console.log esses erros. Como faremos para mostrar na tela?

[00:00:14] Novamente, vamos mexer no DOM, para isso, abriremos o index.html desse projeto no Visual Studio Code. Embaixo do campo de CEP, vamos criar uma div com id="erro", só para ele ocupar o espaço que vai ficar a nossa mensagem.

[00:00:35] Vamos no script.js e antes do try, colocaremos var mensagemErro. Atribuiremos para ele o document.getElementById, esse que acabamos de criar, o erro. E vamos iniciar com nenhuma mensagem. Então, mensagemErro.innerHTML = "". Não vai ter nada dentro dele.

```
     async function buscarEndereco() {
        var mensagemErro = document.getElementById('erro');
        mensagemErro.innerHTML = "";
        try {
            var consultaCEP = await fetch(`htpps://viacep.com.br/ws/${cep}/json/`);
            var consultaCEPConvertida = await consultaCEP.json();
            if(consultaCEPConvertida.erro) {
                throw Error('CEP não existente!');
            }
            var cidade = document.getElementById('cidade');
            var logradouro = document.getElementById('endereco');
            var estado = document.getElementById('estado');

            cidade.valeu = consultaCEPConvertida.localidade;
            logradouro.valeu = consultaCEPConvertida.logradouro;
            estado.value = consultaCEPConvertida.uf;

            console.log(consultaCEPConvertida);
            return consultaCEPConvertida;
        } catch (erro){
            mensagemErro.innerHTML = `<p>CEP inválido. Tente novamente!</p>`
            console.log(erro); 
        }
    }

    var cep = document.getElementById('cep');
    cep.addEventListener("focusout", () => buscaEndereco(cep.value));    
```

[00:01:04] O que estamos fazendo aqui? Estamos selecionando aquela div que acabamos de fazer pelo ID e colocando dentro do HTML, com o innerHTML, uma mensagem vazia. Deve iniciar com vazio, porque se não tem erro, não é para ter nada lá.

[00:01:20] E como faremos para inserir essa mensagem de erro? Usaremos o innerHTML dentro do Catch. Então, no Catch, colocaremos mensagemErro.innerHTML = e o elemento HTML de parágrafo. Você vai usar <p>, e vamos colocar a mensagem CEP inválido. Tente novamente.

![mensagem de erro](/img/cepInvalido.png)

[00:01:46] Vamos fechar com </p>. Agora temos uma mensagem que vai aparecer quando pegar algum erro. Vamos testar? Salvei e vou ao navegador.

[00:01:51] Apertarei "F5" para recarregar e vou colocar aquele CEP que estávamos testando por padrão. Vou tirar um zero para forçar o erro e clicar fora. Ele está pensando. Deu erro e apareceu embaixo: CEP inválido. Tente novamente. Também apareceu no console.log porque eu deixei.

[00:02:24] Já conseguimos informar para o usuário quando acontece algo errada, oferecendo-lhe autonomia para arrumar esse erro e tentar novamente, tentar de outra maneira. O que você acha? Essa mensagem podia ser mais específica, podia explicar mais coisas? Você pode também, com a sua criatividade, colocar uma mensagem diferente.

[00:02:46] Com isso, conseguimos normalizar boa parte do nosso problema dos dados. Agora, quando o usuário digitar o CEP, todos que possuírem o mesmo CEP, a rua, o nome da cidade, o estado, até o bairro, que eu não coloquei e você pode colocar como desafio, tudo será normalizado, igual entre todos os vizinhos e não teremos esse problema que estávamos enfrentando.

[00:03:08] Então, muito obrigada por me acompanhar no desenvolvimento dessa solução para a nossa equipa da Alura. Eu acredito que você vai conseguir usar esse aprendizado em vários outros projetos seus. Eu te espero nas redes sociais, no compartilhamento desse aprendizado que você teve aqui. Até mais!
___

