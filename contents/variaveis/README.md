# Variáveis e tipos primitivos

As variáveis são espaço na memória com um nome, onde podemos guardar um valor e usar esse valor ao longo do programa, para declararmos uma variável em Ruby, é simples.

```ruby
nome = "Pedro"
```

Tipos primivos, ou tipos de data, são os valores possíveis que podem ser guardados dentro de uma variável, os tipos simples e mais comuns são:

- Strings (texto)
- Int (números inteiros)
- Float (números decimais)
- Boolean (verdadeiro ou falso)
- Nil (Nulo)

---

## String

As strings são os textos e palavras, como "Hello World" ou pedro, temos duas maneiras de declarar strings em ruby

```ruby
nome = "João"
Amigo = 'Felipe'
```

## Int

Variáveis Int contém um número inteiro dentro delas, como exatamente 5 e 3, para declararmos uma variável tipo int em ruby é:

```ruby
idade = 24
coisas_na_bolsa = 5
```

## Float

Variáveis tipo Float em ruby contém um número com ponto flutuante, ou decimal, para declararmos uma variável tipo Float em ruby é:

```ruby
dinheiro = 40.5
altura = 1.78
```

Inclusive, se declararmos um número que é inteiro, mas colocarmos um ".8" no final do número ele se torna float, para isso vamos usar um recurso interessante no ruby se colocarmos um ".class" no final da variável, por exemplo.

```ruby
idade = 18

puts idade.class
```

com isso, o ruby irá mostrar "Integer", que é Int, inclusive, podemos colocar um () no final do class, com isso, teste esse código na sua máquina.

```ruby
idade = 18

puts (idade.class)

idade = 18.0

puts idade.class()
```

Você pode ver que nas primeiras duas linhas, declaramos uma variável de tipo Int e mandamos mostrar o tipo dela que é int, mas na terceira e quarta linha podemos ver que declaramos o mesmo valor do ponto de vista matemático, mas para o ruby, é outro, pois colocamos o ".0" no final do número, assim, o Ruby irá achar que este número é um Float, isso será muito útil quando aprendermos sobre os operadores em Ruby.

## Boolean 

Uma variável tipo Boolean pode ser verdadeira ou falsa, em ruby, true ou false, como no exemplo abaixo:

```ruby
lampada = false
vivo = true
```

a utilidade dos Booleans é que podemos usar para determinar se o programa já passou até certo ponto, o usuário marcou algum checkbox dentre outras coisas.

## Nil

Nil é um tipo primitivo menos usado, ele representa um valor nulo, apenas isso, que pode ser modificado para um outro tipo primitivo, como Int ou String.

## Usando variáveis junto com puts/print

Podemos mostrar uma variável junto com um puts ou um print de duas maneiras como abaixo:

```ruby
nome = "João"

puts "Olá " + nome

puts "Tudo bem #{nome}, como vai?"
```

Os dois puts irão mostrar o nome, que é João, mais uma outra string, como "Olá" e "Tudo Bem", mas o primeiro é a maneira mais comum, com soma ou concatenação de Strings enquanto o segundo usa algo chamado normalmente na programação de F Strings, onde podemos colocar uma variável dentro de uma string de maneira mais simples, apenas coloque um jogo da velha, e entre as chaves {} coloque o nome da variável e pronto, iremos ter um código mais bonito e limpo.

## Proximo =>

[Comentários em Ruby](../comentarios/README.md)
