# Arrays

Arrays é um tipo de dado que podemos guardar vários dados de tipos iguais ou diferentes dentro dele, vamos por exemplo, criar um Array com alguns nomes:

```ruby
nomes = ["Pedro", "Maria", "José", "Gabriela"]

# podemos usar também nomes = Array["Pedro", "Maria", "José", "Gabriela"]

puts nomes
```

Cada nome contido neste Array tem um índice, que começa em 0, assim o primeiro nome tem como índice 0, o segundo 1 e assim por diante, por exemplo, para mostrarmos "Pedro", "José" e "Gabriela" na tela seria:

```ruby
nomes = ["Pedro", "Maria", "José", "Gabriela"]

puts nomes[0]
puts nomes[2]

puts nomes[-1]
# Colocando o -1, o Ruby pegará o ultimo item, que é Gabriela
```

Para criar um Array vazio (apenas com Nils) é simples, faça:

```ruby
meu_array = Array.new(5)

puts meu_array
```

Podemos por passar por cada item dentro de um array sem usar estruturas de repetição como For e While dessa maneira:

```ruby
nomes = ["Pedro", "Maria", "José", "Gabriela"]

nomes.each { | nome | puts "#{nome} é meu Amigo(a)!" }
```

Apenas coloque o .each (cada) depois do nome do Array, adicione um {} e entre essas chaves, adicione o nome da variável que será utilizada para armazenar o nome atual, pois essa função irá passar por cada item (nome no caso) de um Array entre dois pipes (| |, aperte a tecla que faz o contra-barra, que fica ao lado do shift junto com o shift.), depois disso podemos colocar o que iremos fazer com o nome atual, que no caso é só um puts simples.

## Manipulando Arrays

### Take

Pega um certo número de itens a partir do início do Array, a partir do 1

```ruby
livro = ["Harry Potter", 400, false]

puts livro.take(2)
# output: "Harry Potter", 400
```

### Sample

Pega um item aleatório de um Array

```ruby
chance = ["Sim", "Talvez", "Não"]

puts chance.sample
```

Podemos sortear mais de um por vez:

```ruby
chance = ["Concerteza", "Sim", "Talvez", "Não", "Negativo"]

puts chance.sample(2)
```

### Include

O include pode ser usado em qualquer variável ou dado em Ruby, como Strings, mas em Arrays ele pesquisa se o item pedido tem no Array, respondendo com true ou false

```ruby
veiculos = ["Celta", "Harley Davidson", "Boing"]

puts veiculos.include? "Celta"
# output: true

puts veiculos.include? "Tanque"
# output: false
```

### Sort e Reverse

Sort organiza o Array enquanto Reverse deixa ele na ordem contrária, dessa maneira:

```ruby
letras = ["k", "h", "a", "c", "x", "z"]

puts letras.sort
# output: [a, c, h, k, x, z]

puts letras.reverse
# output: [z, x, c, a, h, k]
```

### Uniq

Uniq remove elementos duplicados de um Array

```ruby
comprei = ["Arroz", "Arroz", "Desodorante", "Feijão", "Desodorante", "Feijão"]

puts comprei.uniq
# [Arroz, Desodorante, Feijão]
```

### Join

Join converte um Array em String e pede um caractere para separar cada item, como um espaço.

```ruby
precos = [19.90, 10, 2.33, 0.99]

puts precos.join(" ")
```

Há outras dezenas de funções em Arrays, mas essas são as básicas.

# Fontes:

[Lista das Funções em Arrays](https://www.digitalocean.com/community/tutorials/how-to-use-array-methods-in-ruby)

[Dicas extras sobre Arrays](https://mixandgo.com/learn/how-to-use-ruby-each)

## Proximo =>
[Funções](../funcoes/README.md)