Variables, Constantes y Valores
===============================

En **Gear** una variable es declarada bien como variable o constante. Las variables de declaran usando la palabra reservada *var* mientras que las constantes se declaran con *let*.

Veamos algunos ejemplos:

:: 

  var planet := 'Neptune'
  let Pi := 3.1415926
  var radius := 2
  var area := Pi * radius^2
  var ready := False
  let A := "A
  var initial := Null


Cada declaración es precedida por su respectiva palabra reservada, habrás notado que estoy usando la palabra *declaración* en lugar de *sentencia*; ahora ¿Qué pasaría si quitásemos las palabras reservadas? pues nos quedaría algo como esto ``planet := 'Neptune'`` con lo cual ya no sería una declaración sino una *asignación* y ambas son de tipo *statement*. Más adelante lo verás más claro cuando hablemos de las reglas gramaticales, por ahora quédate con el concepto de *declaración* de variables.

.. note:: En las declaraciones de arriba no hay ninguna información de tipos de datos, esto es porque Gear internamente puede *inferirlos* según el valor que le hayamos asignado a las variables, por ejemplo ``planet`` es de tipo ``String`` porque su valor asignado es ``'Neptune'``, del mismo modo ``Pi`` es ``Number``, ``ready`` es ``Boolean`` e ``initial`` es ``Null``.

.. note:: Si una constante adquiere un valor inicial ``Null`` este no podrá ser modificado durante todo el ciclo de vida de dicha constante, a esto se le conoce como *inmutabilidad*. Las variables por el contrario son *mutables* con lo cual una vez enlazadas a un tipo, estas podrán cambiar su contenido siempre y cuando sea del mismo tipo.

Declaración múltiple de variables:

:: 

  var x := 1, y := 2, s := 'Saturn'
  let v := 4, w := 5, p := 'Pluto'

Valores
=======

Además de variables y constantes también existen los *valores* que pueden ser declarados con la palabra reservada *val*. Una variable de tipo *valor* se calcula siempre al momento de ser usada, la diferencia contra una variable mutable es que estas últimas una vez enlazan su valor este permanece igual hasta que se asigne uno nuevo o no mientras que los *valores* son calculados al momento de ser usados en una *expresión*.

Vamos a verlo más claro con unos ejemplos:

:: 

  let Pi := 3.1415926
  var radius := 2
  var area := Pi * radius^2
  print(area) // imprime 12.5663704
  radius := 1
  print(area) // imprime 12.5663704
  
.. note:: Los 2 ``print(area)`` arrojan el mismo valor, esto es porque ``radius`` es una *variable* pero ¿Qué pasa si lo cambiamos por *value*?

:: 

  let Pi := 3.1415926
  var radius := 2
  val area
    var result := Pi * raius^2
    return result
  end
  
  print(area) // imprime 12.5663704
  radius := 1
  print(area) // ahora imprime 3.1415926

.. note:: La variable ``area`` se recalcula automaticamente y al haber cambiado ``radius := 1`` imprime un nuevo valor tras el último recálculo.

El cuerpo de un *value* es muy flexible y permite cualquier código de *sentencia* o *declaración*. Si el *value* está compuesto por una expresión sencilla entonces esto es válido:

::

  val area := Pi * radius^2
  
.. note:: Solo está permitida una expresión simple como la anterior, las expresiones múltiples no están permitidas.

Al cambiar el valor de ``radius`` estamos haciendo una *asignación*. Una *asignación* es muy parecida a una *declaración* pero con ausencia de la palabra reservada *var* o *let* según el caso. El rol de una *asignación* es cambiar el valor de una variable mutable, las asignaciones para *constantes* y *values* están prohibidas.

**Gear** admite los tipos de constantes regulares ``number``, ``string``, ``char`` y ``boolean``. Los tipos no están explícitamente disponibles como tales; son internos al intérprete. En principio, los valores no se convierten implícitamente a otro tipo, con una excepción. Puedes agregar cualquier valor a un ``string`` porque  el valor agregado será siempre conviertido en ``string``.


Strings y Character
===================

Un ``string`` es un texto encerrado en comillas simples. Ejemplo:

:: 

  let helloWorld := 'Hello world!'
  var code := '123'

Si queremos que un ``string`` contenga una comilla simple entonces necesitaremos repetir la comilla simple:

:: 

  let label := 'it''s me'
  print(label) // imprime: it's me
  
Un ``string`` puede ser concatenado con otro usando el operador ``+``:

:: 

  let hi := 'Hello ' + 'world' + '!' // 'Hello world!'

``number`` y ``boolean`` también pueden ser concatenados a un ``string``:

:: 

  let hiNumber := 'Hello ' + 42 // 'Hello 42'
  let truth := 'It is ' + True // 'It is True'


Character
=========

Los caracteres se forman anteponiendo una comilla doble al caracter deseado:

:: 

  "a // representa al caracter 'a'
  "1 // representa al caracter '1'

Los caracteres también pueden ser concatenados al tipo ``string``:

:: 

  let helloWorld := 'Hello world' + "! // Hello world!
  
Concatenar cadenas de texto con el operador ``+`` no siempre es legible, veamos este ejemplo:

::

  let bananas


