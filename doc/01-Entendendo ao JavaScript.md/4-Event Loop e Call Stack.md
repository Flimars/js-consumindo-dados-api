Transcrição
[00:00:00] Anteriormente, discutimos como funciona a comunicação síncrona, a comunicação assíncrona e ainda colocamos em código uma simulação de um chat entre colegas e amigos.

[00:00:10] Quando fizemos isso, eu comentei que, por padrão, o JavaScript é um sistema síncrono. Mas como funciona essa leitura de ação por ação, uma após a outra, por trás dos panos no JavaScript? Vamos entender isso agora.

[00:00:25] Basicamente, podemos separar em três partes o que acontece no nosso código: o Event Loop, o Call Stack e o Task Queue. Vamos analisar o código que fizemos antes.

[00:00:40] Quando chamamos o primeiro console.log, ele vai ser enviado lá para o Call Stack, “Essa ação foi enviada para o Call Stack”. Em seguida, aparecerá uma chamada da função. Conforme havia comentado, a criação da função fica ali, mas ela só é chamada quando chamamos no código.

[00:00:58] Então, o mandaMensagem() é a chamada e ele fica no Call Stack até terminar o que precisa fazer: imprimir três console.log.

[00:01:10] Então, cada um deles vai ser chamado, terminar de acontecer e sair. O próximo console.log será chamado, impresso na tela e depois vai sair. Por fim, o terceiro console.log vai aparecer e sair.

[00:01:25] Assim, a chamada da função termina sua atuação ali, o que tinha para fazer, e vai sair do Call Stack. Só após terminar tudo que tinha para fazer, vai sair da Call Stack. Então, será chamado o último console.log, o "Tchau tchau!". Imprimiu na tela, sumiu. Basicamente é isso que acontece no sistema síncrono.

[00:01:48] Agora sabemos mais a fundo o que é cada parte. O Event Loop é como um segurança na festa e vai guiando para qual porta a pessoa tem que entrar, qual é o acesso dela e quando ela deve acontecer. Então ele fica o tempo inteiro no código olhando o que vai ser chamado para a Call Stack.

[00:02:06] Na Call Stack vão todas as coisas que devem acontecer na tela. Então ele chama uma coisa por vez do código, essa é a função dele. O Event Loop manda para lá o nosso código, as partes VIPs que têm que acontecer primeiro. Elas entram primeiro ali na fila.

[00:02:24] Por padrão, tudo vem vazio. Mas também temos a Task Queue, que vai dar conta do nosso sistema síncrono. É a outra fila que o guarda vai fazer a segurança. No próximo vídeo, estudaremos melhor esse assunto e entenderemos também visualmente como funciona essa parte. Até lá!