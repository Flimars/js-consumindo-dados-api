Transcrição
[00:00:00] Anteriormente, estávamos discutindo sobre os termos síncrono e assíncrono, mas onde é que isso funciona na vida real? Quando começou a pandemia, tudo se tornou home office, as aulas se tornaram online e as reuniões de trabalho também eram online.

[00:00:14] Participávamos de muitas videochamadas, seja na aula, em que a professora falava da casa dela e ouvíamos da nossa casa, seja no trabalho, onde o pessoal atualizava seus status, o que eles estavam fazendo, e você falava o seu também, ou até no happy hour com seus amigos.

[00:00:31] Chamamos essas atividades em vídeo de videochamadas, síncronas, ou seja, quando você está falando ao mesmo tempo, simultaneamente, com os seus colegas, seus amigos.

[00:00:41] A comunicação assíncrona também era bem comum, por exemplo, as mensagens de texto, quando você mandava um "Oi" para o seu colega e ele demorava horas para responder. Quem não tem aquele amigo que demora muito tempo para te responder? Essa é a comunicação assíncrona.

[00:00:57] Então, quando você manda uma mensagem e seu amigo que demora três horas para te responder, quais são as opções? Você para de fazer suas coisas, tudo que você tem para fazer, ou você se ocupa para fazer outras tarefas até chegar essa resposta dele?

[00:01:15] Isso é o que acontece em um sistema JavaScript também. Você pode ter o sistema síncrono, que é o padrão dele: responder uma tarefa após a outra. Por exemplo, uma imagem carrega, depois a outra carrega e depois a outra carrega e assim por diante, seguindo um fluxo.

[00:01:31] Também temos como fazer um sistema assíncrono, com tarefas acontecendo, sendo concluídas uma após a outra, mas também com outras em segundo plano ou afastadas para carregar depois.

[00:01:43] Vamos aplicar esse procedimento do JavaScript síncrono, o padrão, considerando a história da conversa do seu amigo que demora 10 anos para responder. Para isso, abriremos novamente o Visual Studio Code e o script.js.

[00:01:59] Agora precisamos criar outro console.log que represente essa conversa. Primeiro vamos colocar ("Mandando oi pro amigo!"). Em seguida, criaremos uma função chamada mandaMensagem.

[00:02:17] Prosseguindo, escreveremos function mandaMensagem() {}, usando os "bigodinhos" que bastante gente usa. Vamos colocar mais console.log ali dentro para simular outros elementos dessa conversa. Então, mandaremos ("Tudo bem?").

[000:02:35] Faremos outro console.log("Vou te mandar uma solicitação!"). Agora vou colocar pontos e vírgulas. Por fim, outro console.log. Estou colocando aqui uma conversa fictícia. ("Solicitação recebida!") e fechando essa função mandaMensagem.

[00:02:57] Para chamar essa função, escreveremos o mandaMensagem e adicionaremos outro console.log que vai acontecer depois da função. Vai ser ("Tchau tchau!"), só para dizer que acabou a conversa. Vamos abrir no navegador e verificar o resultado.

[00:03:14] Então, eu vou abrir a pasta que está o projeto, "Documentos > dev > Cadastro AluraBooks", o index.html e a "Ferramenta do Desenvolvedor" novamente. Usaremos "F12" ou botão direito e "Inspecionar". Por fim, acessaremos "Console".

[00:03:31] Tudo que escrevi aparece. Vou colocar o código do lado do Console para comparamos com o primeiro Console, o "Mandando oi pro amigo!".

[00:03:44] Ele começou, depois foi para outra linha, que é o mandaMensagem. Não é a função. A função só acontece quando ela é chamada. Então, na linha nove, chamamos um mandaMensagem que rodou os três console.log que estão na função e depois foi para o "Tchau tchau!". Ou seja, está acontecendo uma coisa por vez.

[00:04:01] Imagina se essa conversa fosse muito mais longa, com console.log maiores, quanto tempo perderíamos nela. Não seria muito melhor fazer ela acontecer em segundo plano, para realizarmos nossas tarefas enquanto ela acontece?

[00:04:17] Essa é a base do assíncrono que aprenderemos durante o curso. Entenderemos como funciona essa leitura - tanto de códigos síncronos, quanto assíncronos - no próximo vídeo. Até lá!