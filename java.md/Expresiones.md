**EXPRESIONES, SENTENCIAS Y BLOQUES EN JAVA**

**EXPRESIONES**
Conjunto de variables, operadores e invocaciones de métodos que se construyen para poder ser evaluadas retornando un resultado. Cuando tengamos expresiones de evaluación complejas es recomendable que utilicemos paréntesis para saber cual es el orden de ejecución de operaciones.
Ej.
`int valor = 1;`
`if (valor 1 > valor2) { ... }`

**SENTENCIAS**
Es la unidad minima de ejecución de un programa(conjunto de sentencias que acaban resolviendo un problema).Al final de cada una de las sentencias encontraremos un punto y coma.

Tenemos los siguientes tipos de sentencias:

**Sentencias de declaración**
`int valor = 2;`

**Sentencias de asignación**
`valor = 2;`

**Sentencias de incremento o decremento**
`valor++;`

**Invocaciones a métodos**
`System.out.println("Hola Mundo");`

**Creaciones de objetos**
`Circulo miCirculo = new Circulo(2,3);`

**Sentencias de control de flujo**
`if (valor>1) { … }`

**BLOQUES**
Un bloque es un conjunto de sentencias los cuales están delimitados por llaves.

`if (expresion) {`
`// Bloque 1`
``} else {`
` // Bloque 2}`
