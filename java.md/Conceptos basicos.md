**OBJETO:**

Elemento de software que intenta representar un objeto del mundo real. Tiene su estado (o estados) y su comportamiento. Esto se modula mediante propiedades (o variables) y métodos.
Incluso un objeto puede contener a su vez a otro tipo de objeto.

El uso de objetos nos proporciona los siguientes beneficios:

1.Modularidad, el objeto y sus propiedades pueden ser pasados por diferentes estructuras del código fuente, pero el objeto es el mismo.
2.Encapsular datos, ocultamos la implementación de propiedades del objeto ya que accederemos a traves de los método del objeto.
3.Reutilización de código, podemos tener diferentes instancias de un objeto de tal manera que esas diferentes instancias estan compartiendo el mismo código.
4.Reemplazo, podemos reemplazar un objeto por otro siempre y cuano estos objetos tengan el mismo comportamiento.

**ENCAPSULACION DE DATOS:**

Las interacciones con los objetos se hacen mediante los método. Es decir, si queremos conocer información del estado del objeto deberemos llamar a uno de sus métodos y no directamente a las propiedades.

EJEMPLO
OBJETO ||||||||ESTADOS||||||||| ACCIONES
Televisor||||| Encendida ||||||||Encender
|||||||||||||||Apagada ||||||||||Apagar
||||||||||||En el canal 1 |||||Cambiar de canal

**CLASE:**
Las clases representan los prototipados de los objetos que tenemos en el mundo real. Es decir, ES UNA GENERALIZACION DE UN CONJUNTO DE OBJETOS. A su vez, LOS OBJETOS SERAN INSTANCIAS DE UNA DETERMINADA CLASE.

//Ejemplo definición de un triángulo con 2 propiedades base y altura definidas como private,lo cual hace que no puedan ser visibles desde fuera.//
`class Triangulo {`
`private long base;`
`private long altura;`

\\Método constructor. Es el método que tiene el mismo nombre que la clase: Triangulo () y que nos sirve para inicializar las propiedades desde el exterior.\\

    `public Triangulo(long base, long altura) {`
        `this.base = base;`
        `this.altura = altura;`
    `}`

/_Hemos creado un método que nos calcula el área de un triángulo (base x altura / 2). Este método ya es público y podrá ser invocado de forma externa._/
`public long area() {`
`return (base\*altura)/2;}`

/\*Creamos diferentes objetos del tipo Triángulo. A estos objetos les pasamos diferentes valores.\*/

`Triangulo t1 = new Triangulo(2.0,3.0);`
`Triangulo t2 = new Triangulo(4.0,7.0);`

/_Invocamos el método que nos devuelve el área del triángulo del objeto en concreto_/

`t1.area(); // Área 3.0`
`t2.area(); // Área 14.0`

**INTERFACE:**
Es una forma de establecer un contrato entre dos elementos. Un interface indica qué acciones son las que una determinada clase nos va a ofrecer cuando vayamos a utilizarla.
Cuando implementamos una interface deberemos implementar todas las acciones(métodos) que este contenga.
Ej.Aqui definimos un interface Figura y definimos los métodos que seran obligatorios
`interface Figura {`
` public long area();`
`public long perimetro();}`

Y cuando que una clase implemente un determinado interface deberemos utilizar el **operador implements** indicando en nombre de la interface a implementar

\*Si un triángulo queremos que implemente el interface Figura lo definiremos asi:\*

_/ y asi la clase Triángulo implementa los métodos expresados arriba(calcular área y perimetro)/_

`public Triangulo implements Figura {`
...
``}`

**PAQUETE**
Es una forma de organizar elementos de software mediante un espacio de nombres, que nos facilita encontrar o referirnos a un elemento.
Se definen mediante el modificador **package** seguido del nombre del paquete y lo definiremos en la primera linea de cada una de las clases.

Ej.
`package net.manualweb.java.ejemplos;`

El lenguaje Java nos proporciona un conjunto de paquetes por defecto(API Java) en los que se pueden encontrar multiples utilidades del lenguaje.

**HERENCIA**

Es una forma de estructurar el lenguaje. Podemos indicar que una clase hereda de la otra, es decir, extiende las capacidades(propiedades y métodos) que tenga y añade nuevas acciones y propiedades.

Ej.
/\_el triángulo puede heredar de una clase poligono/\*

`public class Triangulo extends Poligono {...}`

La herencia entre clases se indica mediante el operador **extends**

*/Cuando ahora indiquemos que la clase *Triángulo* hereda de la clase *Poligono\*

`public class Triangulo extends Poligono {`
...

`public Triangulo (long base, long altura, int[] lados) {`
`` super(lados);`
        `this.base = base;`
        `this`.altura = altura; ``

        Una de las cosas que tienes que saber en la herencia es que en el constructor de la clase que hereda (o clase hija) deberas de llamar al constructor de la clase padre con el método especial ***super()***
