Transcrição
[00:00:00] Olá! Boas-vindas ao treinamento sobre consumo de API e tratamento de dados que retornam a partir dela. O meu nome é Mônica Hillman, mas você pode me chamar de Moni Hillman. Eu serei a instrutora que vai te guiar nessa jornada de aprendizado.

[00:00:13] Vamos contextualizar a nossa história. Nós somos uma dupla de desenvolvedores da Alura, especificamente do produto AluraBooks, uma plataforma de venda de livros técnicos. Nós trabalhamos com a linguagem JavaScript.

[00:00:26] Durante nosso desenvolvimento, encontramos um problema nos dados dos usuários do AluraBooks. Vários usuários moravam na mesma rua e cada um deles estava escrevendo o nome dessa rua de formas diferentes. Isso impediu que os nossos cientistas de dados fizessem uma análise mais aprofundada sobre os nossos clientes.

[00:00:45] Faremos um brainstorming para construir uma solução, passando por vários termos e conceitos sobre o JavaScript. Os termos são: JavaScript assíncrono e síncrono, Event Loop, Call Stack e Task Queue.

[00:01:01] Esses quatro assuntos específicos vão nos ajudar a entender o funcionamento do JavaScript. A partir disso, aprenderemos sobre Callbacks, Fetch API e Promises e, em seguida, sobre assincronicidade, assunto relacionado ao JavaScript assíncrono e às requisições, que é o consumo da API.

[00:01:23] Esses três tópicos nos gerarão mais dúvidas, especialmente sobre: Then; JSON; tratamento de erros com catch; e Finally, que são métodos das Promises, termo que acabamos de mencionar.

[00:01:38] Também aprenderemos sobre Async Await, sobre tratamento de erros com Async e Promise All. Isso vai nos ajudar a entender funções assíncronas, assim, continuaremos o nosso aprendizado sobre assincronicidade.

[00:01:52] Por fim, vamos aprender um pouquinho sobre getElementById, sobre Value e sobre addEventListener. Usaremos esses três tópicos para manipularmos o DOM e chegar na solução esperada. Repare que passaremos por vários tópicos para chegarmos na solução.

[00:02:11] Mas, afinal, qual vai ser a solução? Começaremos pegando o formulário de cadastro de clientes da AluraBooks. Depois, vamos consumir a API do ViaCEP. Quando o nosso usuário for se cadastrar e colocar o CEP, vai puxar já o nome da rua, o nome da cidade e o estado automaticamente.

[00:02:29] A partir de agora, teremos todos os nomes de rua escritos da mesma maneira, e isso vai facilitar muito a vida dos nossos cientistas de dados. Vamos testar e verificar a solução final.

[00:02:43] Estou com a tela de cadastro do AluraBooks aberta e eu vou até o CEP. Vou colocar um CEP padrão que vai devolver um endereço de São Paulo. Em seguida, vou clicar no campo de "CEP" e apertar “zoom” para vermos melhor.
![Dados do Cadastro](/img/image-1.png)
[00:02:57] Agora, adicionaremos um "01001000" e tiraremos o mouse do campo de CEP. Selecionando fora, ele completa automaticamente o endereço da Praça da Sé, cidade de São Paulo e o estado de São Paulo.
![campos do Formulário](/img/image.png)
[00:03:11] O próximo passo é enviar esse formulário. Ele vai pedir para eu completar tudo e poderemos testar depois. O ponto principal, é: conseguimos resolver o problema dos nossos cientistas de dados. Agora ele completa automaticamente o endereço, a cidade e o estado.

[00:03:24] Se você quer passar por toda essa trilha de aprendizado comigo e resolver esse problema do AluraBooks, além de outros projetos pessoais seus, te convido a participar do treinamento. Te vejo nos próximos vídeos!

