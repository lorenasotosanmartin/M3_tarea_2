# Taller: Integración de Funcionalidades Básicas de JavaScript en el Sitio Web del Hospital
## Descripción 
En este proyecto se integran funcionalidades de JavaScript al proyecto "clínica Chillán", solicitando datos al usuario y mostrando información de forma dinámica.

### Integración de funcionalidades JavaScript 
- **Reservar Cita:** En el navegador de nuestro sitio, se encuentra un botón titulado "Reservar cita", al seleccionarlo, se solicitará información al usuario (nombre, teléfono, correo) con el objetivo de que si registran esta información serán contactados por la clínica para reserva su cita. Para ello, se implementaron prompts que solicitan la información al usuario y alertas que le señalan si la información es invalida o correcta. Estos prompts y alertas se encuentran dentro de un iterador do...while, al cual se le indica que le solicite la información al usuario hasta que este ingrese una opción valida. Para verificar que la información es válida o no, se implementaron iteradores if que validan mediante una expresión regular si la información registrada es válida (cumple con ciertas condiciones en su estructura).
Finalmente, si el usuario ingresa correctamente los tres parámetros solicitados mediante una alerta se le indica que será contactado por la clínica. 
- **Servicios:** al ingresar a la página principal, home, se encuentra una sección de bienvenida al sitio web de clínica Chillán junto con un botón titulado "Conoce más", si el botón es seleccionado por el usuario, de forma dinámica, se presentarán en pantalla los servicios disponibles, los cuales, están registrados en un arreglo de objetos en el archivo JavaScript app.js
### Event Loop
Corresponde al mecanismo provisto por JavaScript que le permite ser asíncrono, lo cual, significa que permite que el programa siga respondiendo a otros eventos mientras espera la finalización de operaciones lentas. Para ello utiliza: 
- **Stack:** estructura utilizada para registrar las funciones que se están ejecutando en un momento determinado. Cuando se llama a una función, esta se añade a la cima de la pila, y cuando se completa, se elimina de la pila.
- **Queue:** si se lleva a cabo una operación asíncrona, la función se agregará a la cola y espera ahí para ser ejecuta una vez que la pila esté vacía. Así, el event loop puede continuar atendiendo a otros eventos sin problemas.


el event loop se asegura de que todas las funciones suscritas a ese evento sean llamadas de forma adecuada, para ello vigila continuamente a la pila y a la cola. Si la pila está vacía, mueve la primera función de la cola a la pila para su ejecución.
### Scope de variables 
En el desarrollo de este proyecto se utilizaron variables en JavaScript, las cuales fueron seleccionadas de acuerdo a su función
- **Var:** en el caso de variables que podrían cambiar su valor (redeclaraciones) y que cuenten con alcance global. 
- **Const:** en el caso de variables donde su valor es constante (sin cambios) independiente de las acciones realizadas en el sitio, como es el caso de las expresiones regulares utilizadas en este proyecto.
- **let:** en el caso de variables con un alcance local, en el proyecto, se utilizó dentro de los iteradores for para declarar el índice del array. 

### Operadores 
En el desarrollo de este proyecto se utilizaron algunos operados, que permitieron asignar valores a variables y facilitar la verificación de que la información cumpliera o no con ciertas condiciones. Los operadores utilizados fueron los siguientes:
- **||** : or 
- **=** : asignación de valor a variables
- **===** : comparación estricta (mismo valor y tipo)
- **!** : no 
- **<** : menos a

### Manejo de errores 
Para el manejo de errores en el proyecto se utilizaron: 
-	**Try/catch:** utilizado para manejar el error de ingresar un teléfono invalido (no cumpla con los parámetros solicitados), para lo cual, se ejecutan las instrucciones dentro de la sentencia try y se evalúa si el código presenta errores o no, si encuentra algún error, la sentencia try se detiene y el control se va directamente a catch, si no hay errores, se ignora la sentencia catch y la sentencia finaliza en try.
-	**Debugger:** utilizado para depurar mediante las herramientas de desarrollador de Google Chrome, principalmente, verificando el valor que toman las variables (nombre, teléfono y correo) al ir ejecutándose las líneas de código. Para utilizarlo se utiliza la sentencia debugger donde se desea pausar la ejecución y verificar, luego en las herramientas de desarrollador opción “sources” se puede revisar el “scope de las variables” y mediante los botones que se muestran en la ventana “Paused in debugger” se puede seguir ejecutando las sentencias o ir a la siguiente función. Actualmente, las sentencias debugger utilizadas se encuentran comentadas con el objetivo de no pausar el sitio web, si se desea utilizar solo se deben quitar los signos utilizados para comentar una sentencia (//)

### Visualización del proyecto
Para visualizar este proyecto se necesita que previamente cuentes con la instalación de:
- **Git**: [sitio de descarga] (https://git-scm.com/downloads)
- **Node.js**: [sitio de descarga] (https://nodejs.org/en/download/package-manager)
- **Visual Studio Code**: [sitio de descarga] (https://code.visualstudio.com/download)
  
Para visualizar este proyecto debes clonar este repositorio, mediante el siguiente comando:
```bash
git clone https://github.com/lorenasotosanmartin/tarea_3
```
Luego mediante tu consola (cmd) posicionarte en la carpeta donde alojaste el proyecto y escribir el siguiente comando: 
```bash
npm  init
```
Una vez cuentes con estos pases es recomendable que utilices un editor como Visual Studio Code para visualizar el código de cada archivo de una forma adecuada, para ello, es necesario contar con dos extensiones, las cuales pueden instalar escribiendo su nombre en la sección extensiones de Visual Studio Code y presionar la opción Install, la primera es **Live Server**, la cual, una vez instalada aparecerá una opción en la esquina inferior derecha de Visual Studio Code titulada como **"Go live"** la cual debes presionar, esto permitirá abrir una pestaña en tu navegador predeterminado y podrás visualizar todo el contenido de la página web. la segunda extensión que debes instalar es **Live Sass Server**, esta extensión, una vez instalada, te mostrara la opción **"watch Sass"** en la esquina inferior derecha la cual al ser seleccionada permitirá que se compile el código Sass incluido y ver los estilos creados en la página web. cabe destacar, que ambas opciones deben de ser seleccionadas de forma paralela para visualizar correctamente el sitio web de la clínica.
