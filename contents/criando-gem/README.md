# Criando a sua própria Gem

Como vimos anteriormente, as Gems são pacotes, como bibliotecas e programas, agora vamos aprender como criar nossa própria Gem, no caso será um projeto simples, uma biblioteca que mostra na tela "Olá Mundo!".

Primeiro crie o arquivo `olamundo.gemspec`, e uma pasta chamada `lib`, agora dentro de ``lib`` crie o arquivo ``olamundo.rb``.

Agora vamos editar ``lib/olamundo.rb`` e escreva:

```ruby
class Hello
  def self.hi
    puts "Olá Mundo!"
  end
end
```

Fizemos o seguinte, criamos uma classe chamada ``Hello`` e uma função dentro dela, chamada hi, que mostra na tela "Olá Mundo!"

Agora vamos editar o ``olamundo.gemspec`` e escrever:

```ruby
Gem::Specification.new do |s|
  s.name        = 'olamundo'
  s.version     = '0.0.0'
  s.date        = '2020-05-29'
  s.summary     = "Ola Mundo!"
  s.description = "um simples Olá Mundo!"
  s.authors     = ["Seu Nome"]
  s.email       = 'seu@email.com'
  s.files       = ["lib/olamundo.rb"]
  s.homepage    =
    'https://rubygems.org/gems/olamundo'
  s.license       = 'MIT'
end
```

Agora insira os seus dados acima, este é apenas um arquivo de exemplo.

agora vamos executar os comandos para montar essa Gem e enviar ela.

Primeiro crie a sua conta no [Ruby Gems](https://guides.rubygems.org), depois use ``curl -u [SEU USUÁŔIO] https://rubygems.org/api/v1/api_key.yaml >
~/.gem/credentials; chmod 0600 ~/.gem/credentials`` para logar na sua conta no seu computador.

Execute `` gem build olamundo.gemspec``, o arquivo ``olamundo.gem`` será criado, agora use ``gem push olamundo-0.0.0.gem``, pronto! sua Gem foi criada e enviada!

# Parabéns!

Caso você tenha digitado, testado, experimentado, enfim, todos os códigos e exemplos contidos neste 4Noobs você já sabe o básico do Ruby, divulge este repositório, dê Star, e busque ensinar as pessoas o que você sabe, pois quem mais aprende, é você.

Feito por Ederson Ferreira, contato: edersondeveloper@gmail.com