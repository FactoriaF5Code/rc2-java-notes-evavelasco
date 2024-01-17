Un applet es una pequeña aplicación Java, la cual esta disponible en un servidor web del cual nos la descargamos y ejecutamos dentro de una página web. Algunas de sus características son:

-Tamaño pequeño, esto es debido a que se requiere su descarga a través de la red. Aunque existen applets de gran tamaño.
-Uso de interfaces gráficos, utiliza las clases AWT y Swing, las cuales dotan al interface del applet de una gran versatilidad y operabilidad para el usuario.
-… Podríamos decir que es un componente, ya que va a ir incluido dentro de otras aplicaciones.

**Creando un applet**
Lo primero que hay que tener en cuenta es que la definición de los applet se encuentra dentro de la librería **java.applet**, la cual deberemos de importar para poder utilizarla. Además necesitaremos de la librería **java.awt** que es la que gestionará los recursos gráficos que se incluyan dentro del applet. La librería **java.applet** cuenta con una clase abstracta Applet, de la que deberemos de heredar en la clase principal de nuestra aplicación.

`import java.applet.\*;
public class miApplet extends Applet {
//variables y métodos
}`

**Ciclo de vida del applet**

Un applet de Java pasa por diversos estados:

1.El applet se carga por primera vez, es decir, se inicializa. Esto sucede cuando el usuario entra en la página por primera vez.

2.Seguidamente el applet empieza a funcionar.

3.En el caso de que el usuario abandone la página, para desaplazarse a otra, lo que se hace es detener al applet, pero no descargarlo de memoria.

4.Si el usuario recarga la página donde se encuentra el applet, este se descarga de memoria el applet actual y sus recursos asociados. Posteriormente se carga una nueva instancia del applet.

5.Cuando se cierra el navegador o la aplicación que visualiza el applet, se detiene la ejecución y se libera el applet de memoria.
Cada uno de los estados lleva asociado un método:

`public void init ( ) { ... }`
Este método se llama cuando se inicializa el applet por primera vez. En este método es aconsejable fijar el tamaño (ancho y alto) del applet. Además se suelen instanciar los elementos que utilice el applet, ya sean botones, cajas de texto, imágenes,…

`public void start ( ) { ... }`
Es el método que arranca la ejecución del applet cada vez que se visita, siempre y cuando el applet esté expuesto a la visión del usuario.

`public void stop ( ) { ... }`

Para la ejecución del applet. Se ejecuta cuando el applet desaparece de la pantalla.

`public void destroy ( ) { ... }`
Destruye el applet cuando este ya no se vaya a utilizar. En este método deberemos de poner a null todas las variables que maneje el applet para que puedan ser descargadas de memoria por el Garbage Collector (GC), que es el encargado de liberar memoria dentro de la JVM (Java Virtual Machine).

**Código HTML de un applet**

Para poder visualizar un applet dentro de una página web deberemos de introducir su código HTML correspondiente, este se referencia mediante la etiqueta applet.

Esta etiqueta cuenta con una serie de atributos:

**code**, indica el fichero .class que representa el applet.
**height**, indica el alto del área donde se representará el applet.
**width**, representa el ancho del área donde se representa el applet.
Veamos el código que cargaría el applet codificado anteriormente: miApplet.html

`<applet code="MiApplet.class" width="350" height="350">
Mi Primer Applet en Java
</applet>`

**Utilizar el visor de applets (Appletviewer)**
En vez de utilizar un navegador web, podemos visualizar el applet mediante una de las herramientas que se incorpora en el kit de desarrollo de Java SUN. Esta herramienta es el **appletviewer**. Esta herramienta se ejecutará en línea de comandos. Para poder ver nuestra aplicación deberemos de poner en línea de comandos:

`jdk1.4binappletviewer miApplet.html`
