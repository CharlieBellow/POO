# Confusão e Solução

## Programação Estruturada x Orientação a Objetos

# Programação Estruturada

• Processa a entrada e manipulação dos dados, até a saida

• Uso de sequências, estruturas de repetições e condições

Uso de uma rotina maior, ou sub-rotinas (funções)

• Não existem restrições às variáveis (variáveis sobreescritas)


# Programação Orientada a Objetos

• Surge para trazer um cuidado ao uso estruturado 

    • Não elimina por completo o uso estruturado

• Conceitos como Objetos e Classes

• Cuidados com variáveis e rotinas (Encapsulamento)

• Melhor reuso de código (Herança)


```js
// funcional 
var valorHora = 50
var tempoEstimado = 20
var desconto = valorHora * tempoEstimado * (10 / 100)
var custoEstimado = valorHora * tempoEstimado - desconto
// o problema aqui é que se eu mudar o valor dessas variáveis pode dar confusão..

console.log(custoEstimado)

// POO
const job = new Job()
job.valorHora = 50
job.tempoEstimado = 20
job.desconto = 10
const custoEstimado = job.calcularEstimativa() // todo o calculo que foi feito lá no exemplo acima foi trocado por essa função calcular estimativa
console.log(custoEstimado)


const prog = new Job()
prog.valorHora = 100
prog.tempoEstimado = 20
prog.desconto = 50
const custoEstimado = prog.calcularEstimativa()
//todo esse rolÊ de travar as variáveis aqui faz com que quando eu precise alterar as variáveis, eu altere de uma maneira organizada


```

# exercício:
quais entidades? ex.: artigo
características do artigo: nome, autor, link ... (this.)
o que fazer com o artigo? categorizar

cria 10 artigos

