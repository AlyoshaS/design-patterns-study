# Orientação a objetos

> esse pode ser um indice com os conteúdos da parte de revisão. e enquanto eu não separo um lugar específico para algumas coisas posso colocar as anotações aqui.

*Bases:* 
- Palestra do [Marcel dos Santos](https://twitter.com/marcelgsantos): [Projetando Softwares Orientado a objetos com qualidade](https://www.youtube.com/watch?v=LZ2ouAttbvM)
- Curso Programação Orientada a Objetos com PHP do Guanabara no [Curso em Vídeo](https://www.youtube.com/watch?v=KlIL63MeyMY&list=PLHz_AreHm4dmGuLII3tsvryMMD7VgcT7x&index=1)]

Vantagens da Orientação a objetos:

- Confiável: O isolamento entre as partes gera software seguro. Ao alterar uma parte, nenhuma outra é afetada. 
- Oportuno: Ao dividir tudo em partes, várias delas podem ser desenvolvidas em paralelo
- Manutenível: Atualizarum software é mais fácil. Uma pequena modificação vai beneficiar todas as partes que usarem o objeto
- Extensível: O princípio da extensibilidade diz que o software não é estático. Ele deve crescer para permanecer útil
- Reutilizável O próprio nome já descreve (:, mas a base é você poder reaproveitar objetos, classes, interfaces criadas para um projeto A em um projeto B futuro. O Guanabara cita um exemplo de você modelar uma classe aluno para uma escola e poder reaproveitar a mesma classe em um outro projeto, por exemplo, de uma academia(que também tem alunos)  
- Natural: todo software orientado a objeto ele tem que ser natural. O princípio diz que uma coisa natural é mais fácil de você entender. Você se preocupa mais na funcionalidade do que nos detalhes de implementação.

**Abstração:** Trata a representação de um conceito da vida real dentro do sistema. Por exemplo um usuário dentro do seu sistema/app - quais são as características que o seu usuário precisa ter? ele precisa de cpf, data de nascimento ou só nome e email?
Levando em consideração que um usuário é uma pessoa, você precisa ter na sua classe todos atributos que uma pessoa tem? quais são os métodos que você precisa no contexto de um sistema? tipo, a pessoa precisa do método TOMAR CERVEJA dentro do teu sistema?

Em relação ao estado, qual o estado importante pra você naquele contexto? tem algo sobre estar feliz ou triste? isso é uma informação importante? ou você precisa só saber se seu usuário tá online ou offline? realizou ou não uma compra? etc

*PS: lembrar do controle remoto.*  
  - estado: desligado/ligado  
  - consigo usar: pause, canais, volume  
  - caraterísticas: cor, modelo..  


