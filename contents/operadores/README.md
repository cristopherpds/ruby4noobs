# Operadores

Em Ruby, temos alguns tipos de operadores, são com eles que podemos fazer contas matemáticas, comparações,etc. Os operadores são:

- Operadores Aritméticos (matemáticos)
- Operadores Comparativos
- Operadores Atributativos
  
## Operadores Aritméticos
 
São os operadores usados para contas e cálculos, como soma e multiplicação, que podem ser usados dessa maneira:

```ruby
saldo = 400
puts saldo

salario = 1300
puts saldo + salario
# Será mostrado o saldo que é 400 mais 1300, que resultará em 1700
```

Os operadores aritméticos em Ruby são:

| Operador | Descrição                  | Uso                 |
|:---------|:--------------------------:|--------------------:|
| +        | Soma ou concatenação       | ``saldo + salario`` |
| -        | Subtração                  | ``saldo - compras`` |
| *        | Multiplicação              | ``custo * 2``       |
| /        | Divisão                    | ``peso / 2``        |
| **       | Potenciação                | ``altura ** 2``     |
| %        | Módulo ou resto da divisão | ``idade % 2``       |

Lembrando que potênciação é quando você eleva um número isso significa que 10 * 10, 10 ** 2 e 10² são a mesma coisa, mas em ruby é necessário usar o **

Módulo é o resto de uma divisão, ele é útil para descobrir se um número é par ou ímpar, teste o módulo com alguns números pares e ímpares e veja o resultado, para ser mais simples, abra sua linha de comando e digite ``irb``, você entrará no Ruby Interativo, onde poderá testar comandos mais facilmente.

Agora, teste fazer:

```ruby
puts 10 / 7
# 1

puts 10 / 7.0
# 1.4285714285714286
```

Caso quem esteja sendo divido, ou sendo operado, seja um int, e quem divide ou opera também é int o resultado será um int, mas se quem é divido ou operado é int, mas quem divide ou opera é float, o resultado será float, pois ruby segue o tipo das variáveis o valores, tome cuidado com isso, o cálculo pode sair errado caso erre o tipo primitivo das variáveis.

## Operadores Comparativos

Os operadores comparativos são utilizados para comparar dois ou mais variáveis ou fatores para fazer alguma coisa com esse resultado, que pode ser verdadeiro (true) ou falso (false), como no exemplo abaixo:

```ruby
idade = 18
puts idade == 18
# True

salario = 1300
puts salario < 1000
# False
```

Esses operadores serão úteis quando aprendermos as estruturas condicionais, segue a lista dos mais usados:

| Operador | Descrição                  | Uso                   | 
|:---------|:--------------------------:|----------------------:|
| =        | Igual                      | ``idade == 18``       |
| !=       | Diferente                  | ``continuar != false``|
| >        | Maior                      | ``salario > 1000``    |
| <        | Menor                      | ``altura < 1.60``     |
| >=       | Maior ou igual             | ``peso >= 80``        |
| <=       | Menor ou igual             | ``quartos <= 4``      |

Brinque um pouco com cada um para aprender seu funcionamento usando o ``irb`` ou digitando o código em seu editor de texto ou IDE.

# Operadores Atributativos

Os operadores atributativos são úteis para fazer uma operação matemática rapidamente, como multiplicar por 5 de maneira rápida e menos complexa, dessa maneira:

```ruby
saldo = 1000
salario = 1500

# Maneira antiga
saldo_maneira_antiga = salario + saldo

# Maneira atributativa
saldo += salario
```

Lista dos operadores atributativos:

| Operador | Descrição                  | Uso                   | Igual á                           |
|:---------|:--------------------------:|:---------------------:|----------------------------------:|
| +=       | Mais igual                 | ``saldo += 1000``     |``saldo = saldo + 1000``           |
| -=       | Menos igual                | ``vida -= 15``        | ``vida = vida - 15``              |
| *=       | Vezes igual                | ``velocidade *= 2``   | ``velocidade = velocidade * 2``   |
| /=       | Divido igual               | ``comprimento /= 5``  | ``comprimento = comprimento / 2`` |
| %=       | Módulo igual               | ``numero %= 2``       | ``numero = numero % 2``           |
| **=      | Elevado igual              | ``altura **= 2``      | ``altura = altura ** 2``          |

---

Estes são os 3 tipos de operadores em Ruby, serão úteis e a maioria sempre será utilizada em seus programas.

## Proximo =>
[Estruturas Condicionais](../condicionais/README.md)