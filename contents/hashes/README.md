# Hashes 
Um **Hash** é uma matriz(**array**) associativa(pares-chave-valor) onde a chave e o valor podem ser qualquer objeto, separados pelo simbolo ``=>``.

Ele é indexado em um **Hash** usando as chaves.

Exemplo:
````ruby
    telefone = {:home => 1, :mobile => 2, :work => 3}

    telefone2= { "home" => 1,  "mobile" => 2, "work" => 3}
````
Abrindo o terminal do Ruby ou o Interactive Ruby(irb)

Como podemos trablhar com o **Hash**:

Esta e a forma de indexar o **Hash**, 
````shell
   > telefone[:home]      # => 1

   >telefone2["home"]     # => 1
````
esta devolve o valor associado a chave ``:home`` em otras palavras 1.

````shell
   > telefone.key(1)      # => :home

   > telefone2.key(1)      # => "home"
````
esta devolve o valor associado  á chave com valor 1.

````shell
   > telefone.key?(:home)  # => true

   > telefone2.key?("home")  # => true
````
esta é uma consulta para ver se a chave home existe.
````shell
 > telefone.value?(1)   # => true

 > telefone2.value?(1)   # => true
````
este se utiliza para ver se exite o valor 1.

Não apenas podemos definir um **Hash** implicitamente, mas também podemos fazer isso usando o método ``new``.

```ruby
    browsers = Hash.new  #=> {}
```
Este cria um **Hash** vazio, ai vc se pergunta mais como você poderia adicinar informaçoes, e simples.
````ruby
    browsers[:name] = "Chrome"
````
ou

````ruby
    browsers2["name"] = "Opera"
````
ao executar a variavel vera:

````shell
   > browsers  # => {:name=>"Chrome"}

   > browsers2 # => {"name"=>"Opera"}
````
O que acontece se você quiser acessar uma chave chamada ``data``.
Ele vai me dizer que nil, este nao exite
````shell
   > browsers[:data] #=> nil
````
Como posso resolver essa parte?
Existem duas formas de expecificar um valor por padrao. Este ira executar cuando nao encontre um elemento.

Uma das formas e no momento que estou criando meu **Hash**, desta forma.
````ruby
    browsers = Hash.new("padrao")
````
ou
````ruby
    browsers.default = "Nao encontrado"
````
````shell
 > browsers[:data] #=> "Nao encontrado"
````
isso o torna algo muito bom de usar dentro de um **Hash**, pois é algo que os arrays não suportam.
Os Hashes e uma forma simples de representar estructuras de dados
dentro do Ruby e sao comumente usados ​​como parâmetros nomeados dentro de funçoes dentro de Ruby e Rails

Notaçao:
Em Ruby e muinto comum utilizar 
[Simbolos](../simbolos/README.md) para representar as chaves.
