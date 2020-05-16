# Ruby Gems

Toda linguagem de programação tem um gerenciador de pacotes, onde você pode baixar código como bibliotecas de maneira rápida e fácil, e ruby não seria diferente, ruby tem as **Gems**, que já foram instaladas junto com seu Ruby, vamos aprender como usa-las!

Para baixar um pacote abra a sua linha de comando, e digite ``gem install [PACOTE]``, vamos usar como exemplo o pacote binary, com ele seria desse jeito:

``
gem install binary
``

depois disso, podemos usar este pacote binary, que converte números binários para texto e vice e versa (mas que no caso, iremos apenas usar para gerar um número binário aleatório) usando o ``require``, dessa maneira:

```ruby
require 'binary'

puts Binary.random
```

Usamos o ``require`` para importar o binary em nosso arquivo, e APENAS podemos usar este pacote importado com a primeira letra maiúscula, no puts, imprimimos o binary com seu método (função) random, que gera um número aleatório, teste na sua máquina este código.

Simples dessa maneira é o uso do Ruby Gems, que funciona da mesma maneira que o NPM (Javascript) e o Pip (Python) por exemplo, podendo baixar pacotes como bibliotecas da linguagem de maneira fácil.

# Parabéns!

Caso você tenha digitado, testado, experimentado, enfim, todos os códigos e exemplos contidos neste 4Noobs você já sabe o básico do Ruby, divulge este repositório, dê Star, e busque ensinar as pessoas o que você sabe, pois quem mais aprende, é você.

Feito por Ederson Ferreira, contato: edersondeveloper@gmail.com