# Ler e Escrever aquivos

A leitura e escrita de arquivos é algo útil dependendo do caso, como guardar rankings, nomes,etc.

## Leitura

para ler um arquivo usando Ruby é simples:

**nomes.txt**
``
Felipe
Gabriel
Andressa
Maria
``

```ruby
arquivo = File.open("nomes.txt")

puts arquivo.read()

arquivo.close()
```

O código acima irá abrir um arquivo chamado ``nomes.txt`` e mostrar seu conteúdo na tela, logo depois, fechar o arquivo para liberar memória, é simples, mas, e se quisermos mostrar apenas uma linha específica? Simples:

```ruby
arquivo = File.open("nomes.txt")

linhas = arquivo.readlines.map(&:chomp)

puts linhas[0]

arquivo.close()
```

abrimos o arquivo e usamos o readlines, essa função mostra uma única linha do arquivo, e usamos um .map passando como parâmetro ``&:chomp``, você não precisa entender o que foi feito agora, mas a variável linhas tem todas as linhas em um Array, com a primeira linha sendo 0, a segunda 1 e assim por diante, mude o índice do Array linhas que será mostrado no puts e veja a mudança.

## Escrita

Para escrita temos duas opções, ou apagamos o conteúdo do arquivo (ou criamos esse arquivo) e escrevemos algo nele, ou adicionamos algo no final de um arquivo, para a primeira opção iremos usar o ``File.write`` chamado, dessa maneira:

```ruby
conteudo = "Eu comprei\nUm Hambúrger\nNa loja"

arquivo = File.write("historia.txt", conteudo)

# historia.txt será:
# Eu Comprei
# Um Hambúrguer
# Na loja
```

Escrevemos o conteúdo que será escrito dentro de uma variável, chamamos o ``File.write``, passando o arquivo que será escrito e o conteúdo, simples.

Para adicionarmos um conteúdo no final de um arquivo também usaremos o ``File.write``, de maneira muito parecida:

```ruby
conteudo = "\nComi em casa\nEra muito Bom\nValeu a pena!"

arquivo = File.write("historia.txt", conteudo, mode: "a")

# historia.txt será:
# Eu comprei
# Um Hambúrger
# Na loja
# Comi em casa
# Era muito Bom
# Valeu a pena!
```

Escrevemos o conteúdo, e usamos o ``File.write`` passando como argumento um mode, que no caso é a, de append que significa em uma tradução livre adicionar.

## Proximo =>
[Ruby Gems](../gems/README.md)