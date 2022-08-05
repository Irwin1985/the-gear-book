El lenguaje de programación Gear
===================================

Gear es un lenguaje de programación multiparadigma, es imperativo, funcional, orientado a objetos y parcialmente dinámico. Soporta inferencia de tipos y, aunque carece de un sistema de tipado estático, es seguro. Gear fue creado por `Jeroen de Haan <https://github.com/jdehaan2014>`_ quien no solo nos ha regalado un lenguaje maravilloso sino que también se tomó la molestia de crear un libro documentado todo el código de creación del intérprete, sin embargo esta documentación no es una traducción de su libro sino más bien como apuntes que iré documentando mientras escribo mi versión de Gear siguiendo el libro.

Antes de comenzar vamos a conocer la sintaxis de Gear:

::

    // El clásico Hola Mundo
    print('Hola mundo')

Lo anterior es de hecho un programa completo, no hay necesidad de crear un punto de entrada como una función ``main`` ni nada parecido. Un programa puede ser solamente una sentencia (de aquí en adelante ``Statement``).

Otra variante de Hola Mundo puede ser la siguiente:

::

    var helloWorld := func() print('Hola mundo') end
    helloWorld()

O quizá esta otra:

::

    func helloWorld()
        print('Hola mundo')
    end
    helloWorld()

Que tal si nos creamos una función que nos de un saludo de bienvenida:

::

    func saludar(to nombre)
        print('Hola \(nombre)!')
    end
    greetings(to: 'Irwin')

Como puedes ver, los bloques de código de Gear no están basados en llaves sino en palabras tal y como lo hace Pascal y dialectos similares. De hecho la su sintaxis está basada fuertemente en _`Object Pascal <https://es.wikipedia.org/wiki/Object_Pascal>`_ por lo tanto su legibilidad es superior a los lenguajes basados en símbolos.

.. note:: El punto y coma ``;`` no es necesario para separar las sentencias y para las asignaciones hay que utilizar el operador ``:=`` y las comparaciones de igualdad se realizan con el operador ``=``.


Tabla de Contenidos
--------

.. toctree::

   variables
   expresiones
   colecciones
   control-flow
   funciones
   clases
   extensiones
   traits
   arrays
   listas
   rangos
   diccionarios
   enumerables
   ficheros   
