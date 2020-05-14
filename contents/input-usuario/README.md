# Input do Usuário

Em um programa Ruby, muitas vezes teremos que pegar o input do usuário, que é algo que o usuário irá digitar e passar como uma variável do nosso programa, em Ruby, para pegar o input do usuário, ou stdin (STandart INput) é:

```ruby
print "Qual é o seu nome?: "
nome = gets.chomp

puts "Olá #{nome}, tudo bem?"
```

execute este código na sua máquina, agora tente retirar o .chomp do gets.

Sem o .chomp, após o input do usuário for pego, haverá a quebra de uma linha, que dependendo da sua intenção, pode ser algo negativo, é por isso que na maioria dos casos usamos sempre o .chomp diretamente no gets.

## Proximo =>

[Estruturas de Repetição](../repeticoes/README.md)