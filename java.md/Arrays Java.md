Un array Java es una estructura de datos que nos permite almacenar una ristra de datos de un mismo tipo. El tamaño de los arrays se declara en un primer momento y no puede cambiar en tiempo de ejecución como puede producirse en otros lenguajes.

La declaración de un array en Java y su inicialización se realiza de la siguiente manera:

`tipo_dato nombre_array[];
nombre_array = new tipo_dato[tamaño];`

Los arrays Java se numeran desde el elemento cero, que sería el primer elemento, hasta el tamaño-1 que sería el último elemento.

Para acceder a un elemento especifico utilizaremos los corchetes de la siguiente forma.
`arrayCaracteres[numero_elemento];`

**Tamaño del array: .length**

Este atributo nos devuelve el número de elementos que posee el array

**Matrices o Arrays de varios subindices**
Para declarar e inicializar un array de varios subíndices lo haremos de la siguiente manera:

`tipo_dato nombre_array[][];
nombre_array = new tipo_dato[tamaño][tamaño];`

**Inicialización de Arrays en Java**
Existe una forma de inicializar un array en Java con el contenido, amoldándose su tamaño al número de elementos a los que le inicialicemos. Para inicializar un array Java utilizaremos las llaves de la siguiente forma:

`tipo_dato array[] = {elemento1,elemento2,...,elementoN};`
