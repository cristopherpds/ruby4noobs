# Funções

Já usamos várias funções durante este 4Noobs, como include e sample na página anterior, as funções são muito úteis para automatizar o código, não repetir e facilitar a leitura, para criarmos uma função que mostra um nome na tela é simples:

```ruby
def nome_tela
    puts "Olá Pedro!"
end

nome_tela()
```

Apenas use def [NOME DA FUNÇÃO], abra um end e neste meio coloque o código da função, depois disso execute ela, que no caso é ``nome_tela()``, caso não coloque a executação da função, ela não será executada, pois ela precisa ser chamada para seu código ser usado.

Mas e se quisermos passar um nome específico para ser mostrado? Simples:

```ruby
def nome_tela(nome)
    puts "Olá #{nome}!"
end

nome_tela("João")
nome_tela("Maria")
```

apenas colocamos um () depois do nome da função e a variável ``nome`` que irá representar o nome que iremos passar na chamada á função, depois é só executar e pronto! Agora teste, execute a função sem passar o nome.

Irá ocorrer isso:

```
irb(main):034:0> nome_tela()
Traceback (most recent call last):
        6: from /home/ederson/.asdf/installs/ruby/2.7.1/bin/irb:23:in `<main>'
        5: from /home/ederson/.asdf/installs/ruby/2.7.1/bin/irb:23:in `load'
        4: from /home/ederson/.asdf/installs/ruby/2.7.1/lib/ruby/gems/2.7.0/gems/irb-1.2.3/exe/irb:11:in `<top (required)>'
        3: from (irb):33
        2: from (irb):34:in `rescue in irb_binding'
        1: from (irb):27:in `nome_tela'
ArgumentError (wrong number of arguments (given 0, expected 1))
```

O erro diz que a função esperava um argumento, e passamos nenhum, para resolvermos isso é simples:

```ruby
def nome_tela(nome = "Desconhecido")
    puts "Olá #{nome}!"
end

nome_tela("Fabricio")
nome_tela()
```

como podemos ver, na função, depois de nome temos um ``= desconhecido``, caso não passemos o nome a função assumirá que ele é Desconhecido.

## Retorno da função

A função abaixo pega dois números e multiplica eles, olhe abaixo:

```ruby
def multiplica(num1 = 0, num2 = 1)
    multiplicado = num1 * num2

    return multiplicado
end

puts multiplica(2,2)
```

Há uma palavra especial na função, chamada Return, o return expressa qual será o retorno da função, é util para assumirmos o valor de uma variável ser uma certa função ou em outros casos mas neste caso específico, ele não faria muita diferença, mas vamos pensar nesse agora:

```ruby
def fazer_op(operacao = "soma", num1 = 1, num2 = 1)

    case operacao
        when "soma"
            return num1 + num2

        when "subtração"
            return num1 - num2
        
        when "multiplicação"
            return num1 * num2

        when "divisão"
            return num1 / num2
        
        else
            return "ERRO!"
    end
end

puts fazer_op("soma", 3, 4)
```

Analise o código acima, a função fazer_op recebe 3 parâmetros, a operação, o primeiro e o segundo número, é usado um case para saber se a operação é uma soma, subtração, multiplicação ou uma divisão, e para cada um desses casos, se for verdadeiro a função retornará o num1 sendo operado pelo num2, e se nenhum desses casos for verdadeiro, a função retorn um erro, o return é essencial para funções.