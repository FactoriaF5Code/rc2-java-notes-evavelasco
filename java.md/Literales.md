Los valores literales son aquellos que podemos asignar a las variables, dependiendo de las variables podremos asignar unos valores u otros.



**LITERALES DE ENTEROS**

Los enteros que podemos utilizar serán byte, short, int y long. Los literales que les asignemos siempre será un número entero.

`byte variableByte = 12;`
`short variableShort = 12;`
`int variableInt = 12;`
`long variableLong = 12;`

**LITERALES DE DECIMALES**

Los dos tipos de datos de decimales que podemos manejar son float y double,y se utiliza un punto para separar la parte entera de la decimal.

`float variableFloat = 12.2;`
`double variableDouble = 12.2;`

**LITERALES DE CARACTERES Y CADENAS**

Tanto los caracteres del tipo de dato char, como las cadenas del tipo de datos String contienen caracteres Unicode UTF-16.

Los caracteres UTF-16 se pueden escribir directamente en la cadena o si nuestro editor de textos no nos permite el manejo de esa codificación los podemos poner escapados en el formato.

'uCODIGOUNICODE'

Por ejemplo la letra como la ñ se escaparía de la siguiente forma:

'u00F1'

Para utilizarla en una cadena de texto “España” podríamos poner

String pais = "Espau00F1a";
Para los caracteres utilizaremos comillas simples para delimitarlos, mientras que para las cadenas utilizaremos comillas dobles.

`char variableChar = ‘a’;
`String variableString = “cadena”;`

Además en las cadenas podemos utilizar una serie de secuencias de escape, las cuales empiezan por una barra invertida y siguen con un modificador:

Secuencia	Significado
b	retroceso
t	tabular la cadena
n	salto de línea
f	form feed
r	retorno de carro
'	comilla simple
"	comilla doble
\	barra invertida


 **LITERALES SUBRAYADOS**

 Se puede utilizar el subrayado para realizar separaciones entre números para una mejor visualización, no se puede usar al principio o al final del número, alrededor de un punto decimal, ni entre el número y un literal de entero o decimal.