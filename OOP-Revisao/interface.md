# Interface

Seta expectativas, serve para definir um padrão de comunicação para minhas outras classes.

Lembrar do uso das interfaces na aplicação que usamos o pattern Repository.

Em um exemplo de serviços de emails onde eu tenho mailchimp, google e etc:  
Não importa quantos serviços eu tiver ou classes diferentes(implementando serviços de email distintos porque esses serviços diferentes terão a mesma assinatura), de onde eu vou consumir é completamente "abstraído" porque quem eu vou me comunicar será a interface. 

Se um dia eu mudar o banco de dados ou a api, tá tudo certo porque eu tenho esse "contrato"/interface que me dá essa segurança.

Todas as classes que eu utilizar o _implements interfaceASDF_ eu preciso obrigatóriamente usar todos os métodos da interface? 
Sim. Como a interface é um contrato que você firma, toda vez que você for implementar algo à partir dela, você vai ter que seguir aquele contrato.
Lembrar do exemplo a tomada de 3 pinos que usamos hoje. Como existe uma norma que diz que os eletrodomésticos virão com uma tomada 3 pinos, as tomadas deverão dar suporte a isso.

para lembrar de pontos importantes sobre interfaces: 
 - Flexibilidade de trocar implementações.
 - Você cria um contrato com a interface. Esse contrato permite seus objetos serem flexíveis.
 - Serviços diferentes terão a mesma assinatura
