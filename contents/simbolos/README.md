# Simbolos
- Um símbolo é o objeto mais básico que você pode criar em Ruby: é um nome e um ID interno. Os símbolos são úteis porque, dado um símbolo, ele se refere ao mesmo objeto em todo o programa. Portanto, eles são mais eficientes do que strings: duas strings com o mesmo nome são dois objetos diferentes. Isso economiza tempo e memória.

- Um símbolo é criado adicionando-se dois pontos a um literal ou string.


````ruby
        puts "ola".object_id   # => 21066960
        puts "ola".object_id   # => 21066730
        puts :ola.object_id    # => 132178
        puts :ola.object_id    # => 132178
````

Cada vez que uma string é usada, um novo objeto é criado. Então, quando usar uma string e quando usar um símbolo?

- Se o conteúdo do objeto for importante, use uma string.
- Se a identidade do objeto for importante, use um símbolo.

Ruby usa uma tabela de símbolos interna com os nomes de variáveis, objetos, métodos, classes ... Por exemplo, se houver um método chamado ``control_movie``, o símbolo é criado automaticamente ``:control_movie``. Para ver a tabela de símbolos ``Symbol.all_symbols``.

Como veremos a seguir, os símbolos são particularmente úteis para [Hashes](../hashes/README.md).

