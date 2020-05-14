# Estruturas de Repetição

As estruturas de repetição são úteis para fazer um trecho de código ser repetido por um número determinado ou indeterminado de vezes.

## While

While (enquanto) repete algo enquanto uma condição não ser falsa, como no exemplo abaixo

```ruby
print "Digite a palavra chave!: "
palavra = gets.chomp

while palavra != "abracadabra" do
    print "ERROU!, tente novamente!: "
    palavra = gets.chomp
end

puts "\nParabéns, você encontrou a palavra chave!"
```

no código acima, é perguntado qual é a palavra chave, e a palavra que o usuário digitar será a palavra chave, mas **enquanto** ela não for (!=) abracadabra, o programa continuará perguntando a palavra chave, mas caso o usuário digite abracadabra irá aparecer uma mensagem parabenizando-o, o ``\n`` antes a string é uma quebra de linha, indo para a linha de baixo, pois usamos o print acima, que não quebra linha no final, também poderiamos tirar o .chomp do gets, assim não precisariamos colocar o ``\n``.

## For

O for é uma estrutura de repetição útil para quando precisarmos repetir algo por um número de vezes pré determinado, como no exemplo abaixo:

```ruby
print "Quantos segundos demorará para os fogos estourarem?: "
segundos = gets.chomp.to_i

for tempo in 0 .. segundos do

    if tempo == segundos 
	    break    
    end
    # Caso o tempo seja igual aos segundos iria aparecer 0 segundos que faltam para os fogos estourarem, por isso foi utilizado o break, que quebra a estrutura de repetição caso o tempo seja igual aos segundos.

    puts "Faltam #{segundos - tempo} segundos para os fogos estourarem!"
end

puts "ESTOUROU!"
```

É perguntado ao usuário quantos segundos ele quer que demore para os fogos estourarem, e esse valor é pego em um for, o tempo é uma variável que diz qual é o índice do for, como podemos ver no ``0 .. segundos`` o for irá ir de 0 até o valor de segundos que o usuário selecionou, e o for irá se repetir até acabarem os segundos ou no caso, o tempo ser igual ao de segundos, que está explicado no comentário o motivo.

Brinque um pouco com o for e o while, são as duas estruturas de repetição básicas do ruby, há outras duas, mas que para começar no ruby, não serão úteis.