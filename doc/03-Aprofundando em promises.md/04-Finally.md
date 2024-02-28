Transcrição
[00:00:00] Acabamos de conhecer tanto o método then() quanto o método catch. Cada um deles tem a sua função. O then é quando a nossa promessa é resolvida, e o catch é quando a nossa promessa foi rejeitada.

[00:00:12] Mas também tem mais um método que não conhecemos até agora. É isso que vamos fazer na tela para vermos como funciona, e entendê-lo melhor.

[00:00:21] Para usá-lo, vamos depois do catch, quando fechamos os parênteses, vamos selecionar a tecla "Enter", e colocar finally(). Abre e fecha parênteses, e coloca mensagem => console.log('Processamento concluído!'), entre aspas, porque é uma frase que queremos colocar na tela, precisa desses parênteses.

![método finally](/img/finally.png)

[00:00:52] Vou salvar e vamos testar o que acontece. Eu vou no navegador, no nosso cadastro, e clicar na tecla "F5". Agora ele vai fazer, vai carregar, esta lento porque minha internet está lenta hoje.

[00:01:09] Ele deu erro porque tínhamos feito aquela alteração no CEP para forçar o erro, e depois ele deu "Processamento concluído!". Vamos tentar com o CEP certo, para ver o que acontece. Eram três zeros, assim, no fetch colocando aquele que eu sei que existe, o CEP "01001000".
![Ajustando cep certo](/img/finallyCepCerto.png)

![console.log mensagem de conclusão](/img/f12.png)

[00:01:27] Salvei, vou novamente no navegador, clico na tecla "F5", e agora ele carregou, mostrou a resposta, e informou que o processamento foi concluído. Ou seja, ele apareceu tanto quando deu errado, quanto quando deu certo.

[00:01:40] O finally é literalmente a sua tradução também, sendo "Finalmente". Independente da resposta dessa promessa, ele vai imprimir o que colocarmos.

![retorno objeto endereço](/img/newF12.png)

[00:01:51] E quando realmente não nos importamos em qual vai ser esse resultado, temos uma frase padrão que vai retornar na tela. Um exemplo seria se, lembra da encomenda?

[00:02:01] A encomenda de novo, vamos analisar esse caso. Imagine que a transportadora liga ou manda mensagem, um questionário, independente se a encomenda foi entregue ou se ela não foi entregue. Ela pede esse feedback por procedimento padrão dela.

[00:02:14] Seria o mesmo caso, independente da resposta, aquele finally vai acontecer.
___