# Objeto:

> Objeto é um trem! :ok_hand: (que tem características, comportamentos e estado)

É uma instancia de uma classe. Quando eu instancio uma classe, eu crio um objeto. 

Coisa material ou abstrata que pode ser percebida pelos sentidos e descrita por meio das suas _características_, _comportamentos_ e _estado_ atual. Objetos podem ser físicos ou abstratos.

Controle remoto:
  - características/atributos: cor, modelo
  - Comportamento: pause, trocar canais, volume(aumentar ou diminuir)
  - Estado: novo, ligado ou desligado, com ou sem bateria

Compromisso:
  - características/atributos: dia, hora, tipo de roupa para ir
  - Comportamento: marcado, desmarcado, adiado, cancelado
  - Estado: combinado, suspenso, remarcado

## Visibilidade de atributos e métodos

A visibilidade padrão do PHP é pública, mas podemos definir explicitamente a visibilidade de cada um deles e entender isso é muito importante para entender o conceito de encapsulamento.

Atributos privados e protegidos você não pode mexer a não ser que você esteja dentro da própria classe. Dentro das classes o ideal é que você tenha ou crie métodos públicos que acessam atributos privados ou protegidos. Levando em consideração esse contexto de atributos privados e protegidos, lembrar: seu acesso ao comportamento é público, mas seu acesso aos atributos são protegidos!

## Métodos acessores - getter, setter e construtor 
Pelo que eu entendi é basicamente uma continuação sobre a visibilidade de atributos e métodos. Porque ele está batendo bastante na tecla de dar acesso a um atributo, mas sem dar acesso direto a esse atributo. Tem a ver com boas práticas por ter uma segurança adicional de não deixar tudo liberado e acabar vendo a aplicação virar uma bagunça.
Além disso, a questão de trabalhar com essas formas de acessar o objeto é que você abstrai dentro desses métodos a forma como você irá acessar os atributos/métodos dele. 

### Resumão:

**Getters:** Métodos acessores conseguem acessar um determinado atributo mantendo a segurança de acesso a ele.  
**Setters:** Métodos modificadores/mutantes(hue) modificam coisas que estão dentro do objeto garantindo a segurança do atributo. Com eles, você consegue alterar atributos privados.
**Construct:** Quando eu instanciar um objeto ele já inicia executando esse comando. Foi usado o exemplo de você iniciar sua classe já chamando o método tampar ou já definindo um atributo por padrão. Além disso, ele pode receber esses parâmetros que irão definir atributos na classe(modelo, cor e ponta, por exemplo)

