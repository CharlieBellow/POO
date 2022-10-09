# Encapsulamento

Dirigir carro vs conhecer o motor do carro

  • Colocar numa cápsula

  • Agrupamento de funções e variáveis

  • Esconder detalhes de implementação

  • Camada de segurança para os atributos e métodos


# Encapsulamento no código JavaSccript

```js

// Estrutural

let altura = 50
let largura = 60

function calcularArea() { 
  return altura * largura 
}

let area = calcularArea()

// Orientado a objetos

// cria uma classe chamada poligono
class Poligono {
  // a primeira função é o construtor onde eu vou passar os os argumentos da classe:
  constructor(altura, largura) { // cria objetos que representam essa classe
    // o this se refere ao objeto poligono(let poligono = new Poligono(50, 60)) que vai ser criado abaixo
    this.altura = altura // então esse objeto que será criado, vai receber a altura que foi passada como argumento nessa função constructor
    this.largura = largura // aqui está recebendo a largura igual ao caso de cima
  }
  // essa função está sendo criada apenas para retornar a função que será criada lá embaixo. ela serve pra chamar a função calcularArea(), pq a função calcularArea() então com a # e por isso ela não vai ser mostrada para o usuário final, acho que é por isso que se faz necessária essa função "pública" pra chamar uma função restrita
  get area () {
    return this.#calcularArea()
  }

  // finalmente chegamos na função que vai fazer alguma coisa! Ela vai calcular a largura * altura, igual ao exemplo anterior, mas aqui como é orientado a objetos precisa ser assim cheio de coisa sem sentido! kkkkk

  #calcularArea() {
    return this.altura * this.largura
    // aqui fazemos referência novamente ao tal objeto que nem sequer foi criado. mas já entendi que é nesse objeto que vamos passar os valores de altura e largura que vamos calcular
  }
}


  // criando o objeto!
  let poligono = new Poligono(50, 60) // criando o objeto poligono através da classe poligono
  // criei o objeto e passei os valores que gostaria de calcular. mas qual é a vantagem de criar ele se eu posso alterar lá no outro exemplo o valor das variáveis e dá no mesmo?

  console.log(poligono) // vendo o que tem na classe poligono e o resultado é um objeto com os elementos altura e largura e com os parametros que passei no objeto que acabei de criar: {"altura": 50, "largura": 60}

  // se eu quiser ver o calculo dessa área, eu tenho que pegar esse objeto poligono e relacionar com a função que calcula a area. mas como ela tá restrita, usamos a função area que vai chamar a função calcularArea e vai fazer o calculo. aí fica assim:
  console.log(poligono.area)


```