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

*PS: lembrar do controle remoto.*  
  - estado: desligado/ligado  
  - consigo usar: pause, canais, volume  
  - caraterísticas: cor, modelo..  

## Pilares da programação orientada a objetos

### Abstração

Trata a representação de um conceito da vida real dentro do sistema. Por exemplo um usuário dentro do seu sistema/app - quais são as características que o seu usuário precisa ter? ele precisa de cpf, data de nascimento ou só nome e email?
Levando em consideração que um usuário é uma pessoa, você precisa ter na sua classe todos atributos que uma pessoa tem? quais são os métodos que você precisa no contexto de um sistema? tipo, a pessoa precisa do método TOMAR CERVEJA dentro do teu sistema?

Em relação ao estado, qual o estado importante pra você naquele contexto? tem algo sobre estar feliz ou triste? isso é uma informação importante? ou você precisa só saber se seu usuário tá online ou offline? realizou ou não uma compra? etc

### Encapsulamento

Ocultar partes independentes da implementação, permitindo construir partes invisíveis ao mundo exterior. Você pode conversar com essa capsula. A conversa, a troca de informações da capsula com o mundo externo, chamamos de mensagem. Você não vai "entrar" nessa capsula, você irá apenas trocar mensagens com ela. Um código encapsulado usa interfaces(moldes) e esses moldes padrão vão fazer com que não importa como eu vou fazer o código o resultado será sempre o mesmo.

Encapsular não é obrigatório, mas é uma boa prática para produzir classes mais eficientes.

Um objeto bem encapsulado, possui uma interface bem definida!

A ideia do encapsulamento é você proteger sua classe do mundo externo e que todas as trocas de mensagens aconteçam por meio da sua interface.

Vantagens de encapsular:

1 - Tornar mudanças invisíveis (se eu precisar mudar um software por dentro e ele estiver bem encapsulado, mantendo a interface eu posso trocar "a pilha" contanto que a "energia" seja mandada no mesmo padrão. E o mesmo vale pra quando estamos pensando em banco de dados, apis utilizadas).

2 - Facilitar reutilização de código (core do drupal tem bons exemplos de bom encapsulamento)

3 - Reduzir efeitos colaterais

**E o que é uma interface?** Lista de serviços fornecidos por um componente. É o contato com o mundo exterior, que define o que pode ser feito com um objeto dessa classe. Ela seta expectativas, serve para definir um padrão de comunicação para minhas outras classes.

Interface pública é aquele meio externo pra gente deixar que o objeto interaja com o mundo exterior

Em um exemplo de serviços de emails onde eu tenho mailchimp, google e etc:  
Não importa quantos serviços eu tiver ou classes diferentes(implementando serviços de email distintos porque esses serviços diferentes terão a mesma assinatura), de onde eu vou consumir é completamente "abstraído" porque quem eu vou me comunicar será a interface. Ela deixará disponível para mim o tipo de comunicação que eu preciso para interagir com aquela classe, mas não especificamente implementará essa comunicação. A implementação da comunicação estará na classe.
Encapsulamento trata disso: eu manter a forma como vou me comunicar exposta, mas os detalhes da implementação ficam escondidos. Nesse exemplo do email, na minha interface eu posso ter um método enviarEmail exposto, mas só na classe que eu vou codar esse método de enviar email. 

Se um dia eu mudar o banco de dados ou a api, tá tudo certo porque eu tenho esse "contrato"/interface que me dá essa segurança.

Todas as classes que eu utilizar o _implements interfaceASDF_ eu preciso obrigatóriamente usar todos os métodos da interface? 
Sim. Como a interface é um contrato que você firma, toda vez que você for implementar algo à partir dela, você vai ter que seguir aquele contrato. Lembrar da conversa sobre interfaces com o Marcel na mentoria: o exemplo a tomada de 3 pinos que usamos hoje. Como existe uma norma que diz que os eletrodomésticos virão com uma tomada 3 pinos, as tomadas deverão dar suporte a isso.

para lembrar de pontos importantes sobre interfaces: 
 - Flexibilidade de trocar implementações.
 - Você cria um contrato com a interface. Esse contrato permite seus objetos serem flexíveis.
 - Serviços diferentes terão a mesma assinatura

**Método abstrato** é previsto, mas não é implementado. É aquele método que não será desenvolvido na interface, nós só mostramos na interface que vai existir um método X ou Y para que você consiga trocar mensagens com aquele objeto, mas o método em si ficará na classe.