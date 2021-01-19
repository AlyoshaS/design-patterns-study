Visibilidade1 -> É basicamente o que eu vou/preciso expor da minha classe
pro mundo externo. Esse conceito se relaciona com o Encapsulamento

visibilidade -> tudo que eu preciso usar no index, acessar e testar aqui
é o que eu vou manter público na minha classe

modelagem, como vc desenhou sua arquitetura. Método público é como filho(sobre controle)

o controle da exposição do que será público ou não te permitirá alterar 
internamente uma classe sem o conhecimento de quem a usa
(exemplo do carro/motor - disponivel frear acelera)

se eu criar uma classe e tudo público é uma boa prática ou não?
a partir do momento que você estuda encapsulamento, você começa a perceber que não faz sentido dar visibilidade pra todos os métodos dentro da minha classe.
O que perdemos com essa abordagem:
- você perde o controle da sua classe e o que as outras pessoas estão usando
dela. (lib: se eu retirar um método de lá, vou ter que avisar antecipadamente pros meus usuários e remover só em um release seguro - Imagina cê quebrar a aplicação
de um usuário seu sem avisar? Quanto problema você vai gerar pra ele?

acelerar e frear -> vc mexer no seu código sem alterar a interface pública(quem tá usando nem vai saber que vc trocou qualquer coisa/ mudou internamente a estrutura da 
sua classe). exemplo de se trocar o motor.

segurança: dar acesso a algo que o usuario não pode ter acesso
no exemplo de um carro: o que eu preciso(BEEM ABSTRAÍDO) acessar no meu carro? acelerar e frear, saber que posso chegar a 200km, quantos litros de gasolina vou utilizar e etc. 
Vamos supor que eu exponho tudo do carro pra pessoa fuçar onde ela quiser, se ele fizer uma gambiarra elétrica, uma das coisas que podem acontecer é o carro explodir.
Trazendo pro nosso contexto de software, pode mexer em algum método que você não sabe o que vai acontecer ou não conseguiu prever enquanto estava desenvolvendo. 
Segurança não é só sobre cybersecurity.

você pode alterar a regra de negócio no vacilo de deixar algo público

carrinho de compra onde você consegue alterar o valor do desconto que o cupom dá na mão (10 reais e vc coloca porcentagem, por exemplo) 

idade e colocar -10, seu objeto não tá seguro // vai quebrar a regra de negócio. (value object/entity)

uma vez que vc valida os dados do objeto na criação dele(construct) 
você vai ter um objeto num estado válido sempre e não vai precisar se preocupar
em validar ele em cada camada que ce for usálo(persistir no banco, consultar api, logs, envios de email)
no new ele tem que lançar uma excessão ou estar válido.


e vc evita duplicidade de código -> ex: você não precisa validar aquele dado em diversos lugares
Objeto não tem que saber quem controla ele.

propriedade que a gente guarda estado de um objeto é sempre privado e é por isso
que usamos getter e setters -> entra na parte de construct dele, se vc faz um construct com o que vc precisa exatamente do objeto, cê não vai precisar alterar essedado sempre

Se eu tenho getter e setters sem validação ou sem comportamento, é quase uma classe com todas as propriedades públicas ou um array

objeto anemico / dominio ricos passo 3 objeto anemico

Você tornar público só o que é essencial.

$eve = ["nome"=> "eve" , "idade"=> 31, "email"=> "lala@gmail.com"];

definição de value object 
email- tipar como email 

entidade diferencia sobre identidade

valor deve ser imutável

7.4 ja posso tipar todos os 

named constructor fromArray
construtor nomeado



Herança