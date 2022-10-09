# Abstração

Template ou Identidade de uma classe que será construída no futuro

  • Atributos e métodos podem ser criados na classe de Abstração (Superclasse) MAS,

  • A implementação dos métodos e atributos, só poderá ser feita na classe que irá herdar essa Abstração

  # Abstração com código Javascript
```js
  
  // definir
class Parafuso { // Superclasse - Abstrata
  constructor() { // a classe construtura vai sempre verificar se ele é igual a parafuso
    if (this.constructor === Parafuso) 
    throw new Error('Classe abstrata não pode ser instânciada')
    // e se tentar criar outra classe com o nome parafuso, ele vai mostrar esse erro dizendo que não pode criar pq já existe
  }

  get tipo() {
    throw new Error('Método "get tipo()" precisa ser implementado')
    // essa função vai ser chamada dentro das outras função de tipo
  }
}

class Fenda extends Parafuso {
  constructor() { super() } 
  // criei essa classe fenda que herda tudo que ta em parafuso e faz a herança com o super()

  get tipo() { 
    return 'fenda'
  }
}

class Philips extends Parafuso { 
  constructor() { super() }
  
  get tipo() { 
    return 'philips'
  }

class Allen extends Parafuso {}// não tem os métodos e atributos

// criar e usar
new Parafuso() // 'Classe abstrata não pode ser instânciada
let fenda = new Fenda ()
let philips = new Philips() 
let allen = new Allen() // mesmo que eu crie aqui, eu preciso ter os métodos e atributos onde eu crei a classe

console.log(fenda.tipo, philips.tipo) 
console.log(allen.tipo) // 'Método "get tipo()" precisa ser implementado'
```

Nesse exemplo, só existe parafuso se ele for de algum tipo específico como: Fenda, Philips ou Allen

