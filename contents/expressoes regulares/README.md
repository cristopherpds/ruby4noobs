# Expressões regulares

- As expressões regulares, embora enigmáticas, são uma ferramenta poderosa para trabalhar com texto. Eles são usados ​​para reconhecer padrões e processar texto. **Uma expressão regular** é uma forma de especificar um padrão de caractere, que será pesquisado em uma string. Em Ruby, as expressões regulares são criadas entre ``//``: são objetos do tipo **Regexp** e podem ser manipuladas como tal.

````shell
   > //.class  # => Regexp
````

A maneira mais simples de descobrir se uma expressão (também funciona com strings) está dentro de uma string é usar o método ``match`` ou o operador ``=~``:

````ruby
    m1 = /Ruby/.match("O futuro é Ruby")
    puts m1         # => "Ruby" desde que ela encontrou a palavra
    puts m1.class   # => retorna MatchData; retorna "nil" se não for encontrado
    
    # operador {{**=~**}}:
    m2 = "O futuro é ruby" =~ /Ruby/
    puts m2 # => 11 -> posição onde a palavra "Ruby" começa
````

## Construindo expressões regulares

Qualquer caractere que fique entre barras é pesquisado exatamente:

````
    /a/ # procura a letra a e qualquer palavra que a contenha
````
Alguns caracteres tem um significado especial em expressoes regulares. Para evitar que sejam processados ​​e para poder pesquisá-los, a **sequencia de escape** ``\`` é usada.

````
    /\?/
````
O ``\`` significa "não trate o próximo caractere como especial." Os caracteres especiais incluem: ``^, $ ,? ,., /, \, [,], {,}, (,), + e *``.

## O curinga. (ponto)
Às vezes, qualquer caracter é pesquisado em uma determinada posiçao. Isso é conseguido graças ao. (ponto). Um ponto, localiza qualquer caractere exceto o retorno de carro.

````
    /.assado/
````
Pesquise por 'mazado' e 'cazado'. Ele também encontra '%azado' e '8azado'. É por isso que você deve ter cuidado ao usar o ponto: ele pode dar mais resultados do que você deseja. No entanto, você pode colocar restriçoes nos resultados, especificando as classes de caracteres pesquisadas.

## Classes de caracteres

Uma classe de caracteres é uma lista explícita de caracteres. Para isso, sao utilizados os colchetes: ``[]``

````
    /[mc]azado/
````
Desta forma, especificamos a pesquisa por 'azado' precedida de 'c' ou 'm': pesquisamos apenas por 'mazado' ou 'cazado'.

Dentro dos colchetes, voce pode especificar um intervalo de pesquisa.

````
    /[a-z]/ # encontra qualquer letra minúscula
    /[A-Fa-f0-9]/ # encontra qualquer número hexadecimal
````
Às vezes, voce precisa encontrar qualquer caractere, exceto aqueles de uma lista específica. Este tipo de pesquisa é feito negando, usando ``^`` no início da classe.

````
    /[^A-Fa-f0-9]/ #encontre qualquer caractere exceto hexadecimais
````

## Abreviaçoes para classes de caracteres

Para encontrar qualquer cifra decimal, essas duas expressões são equivalentes:
````
    /[0-9]/  
    /\d/
````
Duas outras abreviações são:
- **\w** corresponde a qualquer dígito, letra ou sublinhado (_).
- **\s** corresponde a qualquer espaço em branco de caractere, como um espaço, uma tabulação e um retorno de carro.

Todas as abreviaturas anteriores também tem uma forma negada. Para fazer isso, a mesma letra em maiúscula:
````
    /\D/ # encontra qualquer caractere que não seja um número
    /\W/ # encontra qualquer caractere que não seja uma letra ou sublinhado
    /\S/ # encontra um caractere que não é um espaço em branco.
````

Caso queira criar suas expressoes regulares prove [aqui](https://rubular.com/)