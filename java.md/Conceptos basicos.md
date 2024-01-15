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

CLASE:
Las clases representan los prototipados de los objetos que tenemos en el mundo real. Es decir, ES UNA GENERALIZACION DE UN CONJUNTO DE OBJETOS. A su vez, LOS OBJETOS SERAN INSTANCIAS DE UNA DETERMINADA CLASE.

/_Ejemplo definición de un triángulo con 2 propiedades base y altura definidas como private,lo cual hace que no puedan ser visibles desde fuera._/
`class Triangulo {`
`private long base;`
`private long altura;`

/\*método constructor. Es el método que tiene el mismo nombre que la clase: Triangulo () y que nos sirve para inicializar las propiedades desde el exterior.\*/

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
