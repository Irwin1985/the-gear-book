Expresiones
============

**Gear** presenta los operadores aritméticos básicos que conoce de otros lenguajes:

**Aritmética básica**

- Adición
+----------------------+---------------+-------------------------+------------------------+
|     Muestra          | Resultado     | Ejemplo                 | Resultado              | 
+----------------------+---------------+-------------------------+------------------------+
| ``Number + Number``  |   ``Number``  | ``8 + 9``               | ``17``                 |
+----------------------+---------------+-------------------------+------------------------+
| ``String + Number``  |   ``String``  | ``'Hello ' + 42``       | ``'Hello 42'``         |
+----------------------+---------------+-------------------------+------------------------+
| ``String + String``  |   ``String``  | ``'Hello ' + 'world'``  | ``'Hello world'``      |
+----------------------+---------------+-------------------------+------------------------+
| ``String + Number``  |   ``String``  | ``'Hello ' + "!``       | ``'Hello!'``           |
+----------------------+---------------+-------------------------+------------------------+
| ``String + Boolean`` |   ``String``  | ``'It''s ' + True``     | ``'It's True'``        |
+----------------------+---------------+-------------------------+------------------------+

- Sustracción
+----------------------+---------------+-------------------------+------------------------+
|     Muestra          | Resultado     | Ejemplo                 | Resultado              | 
+----------------------+---------------+-------------------------+------------------------+
| ``Number - Number``  |   ``Number``  | ``8 - 9``               | ``-1``                 |
+----------------------+---------------+-------------------------+------------------------+

- Multiplicación
+----------------------+---------------+-------------------------+------------------------+
|     Muestra          | Resultado     | Ejemplo                 | Resultado              | 
+----------------------+---------------+-------------------------+------------------------+
| ``Number * Number``  |   ``Number``  | ``8 * 9``               | ``72``                 |
+----------------------+---------------+-------------------------+------------------------+

- División
+----------------------+---------------+-------------------------+------------------------+
|     Muestra          | Resultado     | Ejemplo                 | Resultado              | 
+----------------------+---------------+-------------------------+------------------------+
| ``Number / Number``  |   ``Number``  | ``72 / 9``               | ``8``                 |
+----------------------+---------------+-------------------------+------------------------+

- Resto o Módulo
+----------------------+---------------+-------------------------+------------------------+
|     Muestra          | Resultado     | Ejemplo                 | Resultado              | 
+----------------------+---------------+-------------------------+------------------------+
| ``Number % Number``  |   ``Number``  | ``72 % 7``               | ``2``                 |
+----------------------+---------------+-------------------------+------------------------+

Además existen otros operadores que trabajan solo con números:

:: 

  -4       // Negación
  4 << 2   // Desplazamiento de bytes a la izquierda => 16
  36 >> 2  // Desplazamiento de bytes a la derecha => 9
  4 ^ 3    // Potencia => 64


Operadores especiales para Arrays:

:: 

  [1, 2, 3] >< [4, 5, 6] // Suma de arrays => [1, 2, 3, 4, 5, 6]
  [1, 2, 3] :: [4, 5, 6] // Multiplicación de arrays => 32


Operadores lógicos:

:: 

  !True         // Negación
  True & False  // Conjunción
  True | False  // Disyunción
  True ~ False  // Or exclusivo

Operadores Relacionales:

::

  a = b   // igualdad
  a <> b  // desigualdad
  a >= b  // mayor o igual que
  a > b   // mayor que
  a <= b  // menor o igual que
  a < b   // menor que
  a in b  // a es un elemento de b
  a is b  // a es una instancia de b


Expresión If
============

La expresión ``if`` debe ser tratada como cualquier otra expresión en **Gear** con lo cual pueden ser asignados a variables:

::

  let a := 7, b := 13
  let max := if a > b then a else b
  print('Maximo = \(max)')


Expresión Match
===============

  
