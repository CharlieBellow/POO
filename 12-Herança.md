# Herança

- Pais e filhos
- Objetos podem herdar, ou estender, características bases
- Uma cópia de atributos e métodos de outra classe

# Código:

```js

class Veiculo { //classe pai

rodas = 4;

mover(direcao){}
virar(direcao){}
}

class Moto extends Veiculo {  // essa classe moto herda as propriedades do veículo    
  constructor() {
    super() // super = puxar atributos e métodos do pal }
    this.rodas = 2 // aqui só mudo de 4 pra 2 rodas
  }
}
```
*  OBS:

- Um objeto pode estender de outro objeto que pode estender de outro objeto

- Fácil reutilização de código

- a Herança facilita a reutilização do código