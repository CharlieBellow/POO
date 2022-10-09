# Polimorfismo

- Quando um objeto estende de outro (herança) talvez haja a necessidade de reescrever uma ou mais características (atributos e métodos) nesse novo objeto.

- Recriaremos então um método (ou mais) da classe herdada.

- Polimorfismo significa muitas formas

- uma classe herda de outra e modifica alguns comportamentos

# Polimorfismo com Javascript

```js
class Atleta {
  peso;
  categoria;
  
  constructor (peso) {
    this.peso = peso
  }

  definirCategoria() {
    if (this.peso <= 50) {
      this.categoria = 'infantil'
    }
    else if (this.peso <= 65) { 
      this.categoria = 'juvenil'
    }
    else {
      this.categoria= 'adulto'
    }
  }
}


class Lutador extends Atleta {
  constructor (peso) { 
    super (peso) 
    //lutador herda a função atleta
  }
  
  // reescrevendo os parâmetros de peso e categoria
  definirCategoria() {
    if (this.peso <= 54) { 
      this.categoria = 'pluma'
    }
    else if (this.peso <= 60) {
      this.categoria = 'leve'
    }
    else if (this.peso <= 75) { 
      this.categoria = 'meio-leve'
    }
    else {
      this.categoria = 'pesado'
    }
  }
}

// uma classe pai e uma classe filha que herda da classe pai e modifica algumas coisas pra que a classe filha faça mais sentido
```