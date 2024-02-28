Transcrição
[00:00:00] No último vídeo, estávamos testando o código que simulamos em JavaScript, da conversa entre amigos e colegas, só que eles eram síncronos e a leitura funcionou através do Event Loop e do Call Stack.

[00:00:13] No sistema do JavaScript, havia uma parte de Task Queue que não vimos funcionar e agora a colocaremos em prática. Naquele código que fizemos antes, a função mandaMensagem() agora vai começar com o setTimeOut, depois abriremos parênteses, faremo a chamada da função com mandaMensagem, 5000) e fecharemos parênteses.

[00:00:37] Agora testaremos o funcionamento no nosso sistema do Event Loop. Ele vai chamar a primeira linha, o primeiro console.log e colocar na Call Stack. Então, imprimiu na tela, chegou a hora dele sair de lá.

[00:00:52] Agora o Event Loop vai chamar o setTimeOut, que funciona diferente. Ele é um setTimeOut de cinco segundos, portanto, não vai acontecer agora, será enviado para o Task Queue. O Event Loop vai colocá-lo em outra fila e continuará com o código funcionando da mesma maneira.

[00:01:10] Agora, em vez de chamar a função, ele chamará o último console.log. Então, o console.log do "Tchau tchau!" é o que acontece agora. Quando ele terminar, vai esperar passar cinco segundos que dissemos para ele esperar e depois chamará a função mandaMensagem para o Call Stack.

[00:01:30] Agora ele vai fazer o comportamento normal: chamar o primeiro console.log, que será empilhado em cima da função; imprimir na tela; e sair. Vamos colocar o segundo console.log que está dentro da função. Aconteceu, foi embora. Colocou o terceiro, também aconteceu e foi embora.

[00:01:48] Após terminar de rodar a função inteira, ela vai sair do Call Stack. Quando a função terminar, ela também vai sair do Call Stack. Rodou o nosso código inteiro e já é possível notar a diferença.

[00:01:59]. Acrescentamos a função setTimeOut do JavaScript que faz acontecer algo depois de um certo tempo que definirmos. Então, ele calcula em milissegundos. Eu coloquei 5000 para ser 5 segundos.

[00:02:16] Podemos deixar algo no canto fazendo a sua função para depois ser chamado. Isso também acontece no cotidiano.

[00:02:27] Imagina que você está lavando a louça e faz a divisão de quais itens serão lavados antes. Eu faço assim: lavo primeiro os meus copos. Se a panela está muito suja, eu coloco uma água e deixo por algum tempo de molho para ajudar na lavagem.

[00:02:43] Enquanto isso, eu não paro toda a minha louça para esperar a panela, vou lavar os pratos, os talheres e tudo o que estiver na pia. Depois eu pego a panela e lavar de novo.

[00:02:56] Basicamente, funciona isso. Você deixa ali no canto para ele se preparar e depois puxa de volta para rodar na sua tela. Essa função do mandaMensagem está sendo enviada como um parâmetro do setTimeOut. Isso é chamado de Call Back. No próximo vídeo, estudaremos melhor esse assunto. Até lá!