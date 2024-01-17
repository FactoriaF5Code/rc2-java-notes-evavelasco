Una cadena de texto no deja de ser más que la sucesión de un conjunto de caracteres alfanuméricos, signos de puntuación y espacios en blanco con más o menos sentido.
Todas ellas serán representadas en java con la clase **String** y **StringBuffer**
Para encontrar la clase **String** dentro de las librerías de Java tendremos que ir a **java.lang.String**

**Creando una cadena**
Para crear una cadena tenemos dos opciones:

Instanciamos la clase **String**. Que sería una creación explicita de la clase
`String sMiCadena = new String("Cadena de Texto");`

Crear implícitamente la cadena de texto. Es decir, simplemente le asignamos el valor al objeto.
`String sMiCadena = "Cadena de Texto";`

En este caso, Java, creará un objeto **String** para tratar esta cadena.

**Crear una cadena vacía**
Para poder crear la cadena vacía nos bastará con asignarle el valor de “”, o bien, utilizar el constructor vacío.

`String sMiCadena = "";
String sMiCadena = new String();`

**FUNCIONES BASICAS CON CADENAS**
Métodos que nos permiten manipular la cadena de texto.

**Información básica de la cadena**

**.length()** Nos devuelve el tamaño que tiene la cadena.

**char charAt(int index)** Devuelve el carácter indicado como índice. El primer carácter de la cadena será el del índice 0. Junto con el método **.length()** podemos recuperar todos los caracteres de la cadena de texto. Hay que tener cuidado. Ya que si intentamos acceder a un índice de carácter que no existe nos devolverá una excepción **IndexOutOfBoundsException.
**

**Comparación de Cadenas**

**boolean equals(Object anObject)** Nos permite comparar si dos cadenas de texto son iguales. En el caso de que sean iguales devolverá como valor “true”. En caso contrario devolverá “false”. Este método tiene en cuenta si los caracteres van en mayúsculas o en minúsculas. Si queremos omitir esta validación tenemos dos opciones. La primera es convertir las cadenas a mayúsculas o minúsculas con los métodos **.toUpperCase()** y **.toLowerCase()** respectivamente.La segunda opción es utilizar el método **.equalsIgnoreCase()** que omite si el carácter está en mayúsculas o en minúsculas.

**boolean equalsIgnoreCase(String anotherString)**
Compara dos cadenas de caracteres omitiendo si los caracteres están en mayúsculas o en minúsculas.

**int compareTo(String anotherString)**Este método es un poco más avanzado que el anterior, el cual, solo nos indicaba si las cadenas eran iguales o diferentes En este caso compara a las cadenas léxicamente. Para ello se basa en el valor Unicode de los caracteres. Se devuelve un entero menor de 0 si la cadena sobre la que se parte es léxicamente menor que la cadena pasada como argumento. Si las dos cadenas son iguales léxicamente se devuelve un 0. Si la cadena es mayor que la pasada como argumento se devuelve un número entero positivo.

**Búsqueda de caracteres**
Tenemos un conjunto de métodos que nos permiten buscar caracteres dentro de cadenas de texto:

**int indexOf(int ch)** Nos devuelve la posición de un carácter dentro de la cadena de texto. En el caso de que el carácter buscado no exista nos devolverá un -1. Si lo encuentra nos devuelve un número entero con la posición que ocupa en la cadena.

**int indexOf(int ch, int fromIndex)** Realiza la misma operación que el anterior método, pero en vez de hacerlo a lo largo de toda la cadena lo hace desde el índice (fromIndex) que le indiquemos.

**int lastIndexOf(int ch)** Nos indica cual es la última posición que ocupa un carácter dentro de una cadena. Si el carácter no está en la cadena devuelve un -1.
**int lastIndexOf(int ch, int fromIndex)**Lo mismo que el anterior, pero a partir de una posición indicada como argumento.

**Búsqueda de subcadenas**

**int indexOf(String str)** Busca una cadena dentro de la cadena origen. Devuelve un entero con el índice a partir del cual está la cadena localizada. Si no encuentra la cadena devuelve un -1.

**int indexOf(String str, int fromIndex)** Misma funcionalidad que**indexOf(String str)**, pero a partir de un índice indicado como argumento del método.

**int lastIndexOf(String str)** Si la cadena que buscamos se repite varias veces en la cadena origen podemos utilizar este método que nos indicará el índice donde empieza la última repetición de la cadena buscada.

**lastIndexOf(String str, int fromIndex)** Lo mismo que el anterior, pero a partir de un índice pasado como argumento.

**boolean startsWith(String prefix)** La verdad es que este método podía obviarse y utilizarse el **indexOf()**, con el cual, en el caso de que nos devolviese un 0, sabríamos que es el inicio de la cadena.

**boolean startsWith(String prefix, int toffset)** Más elaborado que el anterior, y quizás, y a mi entender con un poco menos de significado que el anterior.

**boolean endsWith(String suffix)** De igual manera que sucedía con el método .**startsWith()** podríamos utilizar una mezcla entre los métodos **.indexOf()** y
**.length()** para reproducir el comportamiento de **.endsWith()**.

**Métodos con subcadenas**

**String substring(int beginIndex)** Este método nos devolverá la cadena que se encuentra entre el índice pasado como argumento (beginIndex) hasta el final de la cadena origen

**String substring(int beginIndex, int endIndex)** Si se da el caso que la cadena que queramos recuperar no llega hasta el final de la cadena origen, que será lo normal, podemos utilizar este método indicando el índice inicial y final del cual queremos obtener la cadena

**Manejo de caracteres**
Otro conjunto de métodos que nos permite jugar con los caracteres de la cadena de texto. Para ponerles en mayúsculas, minúsculas, quitarles los espacios en blanco, reemplazar caracteres,….

**String toLowerCase();** Convierte todos los caracteres en minúsculas.

**String toUpperCase();** Convierte todos los caracteres a mayúsculas.

**String trim();** Elimina los espacios en blanco de la cadena.

**String replace(char oldChar, char newChar)** Este método lo utilizaremos cuando lo que queramos hacer sea el remplazar un carácter por otro. Se reemplazarán todos los caracteres encontrados.

**Conversión a String: valueOf()**
Un potente conjunto de métodos de la clase **String** nos permite convertir a cadena cualquier tipo de dato básico: int, float, double,

**String valueOf(boolean b);**

**String valueOf(int i);**

**String valueOf(long l);**

**String valueOf(float f);**

**String valueOf(double d);**

**String valueOf(Object obj);**
