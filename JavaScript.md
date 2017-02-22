# JavaScript

###FLUJO DE CONTROL
~~~
if(condicion) {...}
else {...}
~~~

###OPERADORES TERNARIOS
~~~
condicion ? Accion si TRUE : accion si FALSE //Se puede definir una condición de modo muy
~~~
### BUCLES

~~~
for(inicialización; condición; actualización) {…}
~~~

~~~
for(indice in array) {...}
~~~
~~~
while (condición){....}
~~~
~~~
do {…} while (condición);
~~~
~~~
break y continue
~~~

~~~
switch (var1) {
case (1):
document.write(“Página principal”);
break;
case (2):
document.write(“Popup”);
break;
default:
…;
break;
}
~~~
_______________________________________________________________________________

###FUNCIONES
~~~
function nombreFuncion ([param1], …, [paramN]) {
…
return valorRetorno;
}
~~~
~~~
var variable = prompt("mensaje");
document.write('texto');
~~~


### FUNCIONES ÚTILES PARA CADENA DE TEXTO

-   `.toUpperCase()` //Transforma todos los caracteres en mayúsculas.
-   `.toLowerCase()` //Transforma todos los caracteres en minúsculas.
-   `.charAt(posicion)` // Obtiene el carácter que se encuentra en la posición indicada.
-   `.indexOf('caracter')` //Calcula la posición en la que se encuentra el carácter indicado dentro de la cadena de texto.
-   `.lastIndexOf('caracter')` //Calcula la última posición el carácter indicado dentro de la cadena de texto. Si no encuentro devuelve -1.
-   `.substring(inicio, final)` //Extrae una porción de una cadena de texto, "final" opcional, final no incluido.
-   `.split("separador")` //convierte una cadena de texto en un array de cadenas de texto.

### FUNCIONES ÚTILIES PARA ARRAYS
-   `.length` //Calcula el número de elementos de un array
-   `.concat()` //Se emplea para concatenar los elementos de varios arrays.
-   `.join(“separador”)` //Une todos los elementos de un array para formar una cadena de texto. Para unir los elementos se utiliza el carácter separador indicado.
-   `.pop()` // Elimina el último elemento del array y lo devuelve.
-   `.push()` //Añade un elemento al final del array. También es posible añadir más de un elemento a la vez.
-   `.shift()` //Elimina el primer elemento del array y lo devuelve.
-   `.unshift()` //Añade un elemento al principio del array. Se puede añadir más de un elemento a la vez.
-   `.reverse()` //Modifica un array colocando sus elementos en el orden inverso a su posición original.
-   `.toLocaleString()` //Devuelve una cadena formada por los elementos de la matriz.
-   `.toString()` // Devuelve devuelve cadena con los valores separados por comoas
-   `.slice()` //Se utiliza con dos valores de índice (inferior y superior). Devuelve una matriz formada por el elemento del índice inferior hasta el elemento del índice superior (sin incluirlo).
-   `.sort()` //Ordena la matriz en orden creciente.

###FUNCIONES ÚTILES PARA NÚMEROS
-   `.sort()` NaN //Para indicar un valor numérico no definido.
-   `Infinity` //Hace referencia a un valor numérico infinito y positivo (también existe el valor –Infinity para losinfinitos negativos)
-   `isNaN(expresion)` //Evalúa si es un número valido.
-   `.toFixed(digitos)` //Devuelve el número entero con tantos decimales como los indicados por el parámetro digitos y realiza los redondeos necesarios.
-   `typeof` //Devuelve el tipo de dato (typeof 95); //devuelve “number”
   -   `“undefined”` : si la variable es de tipo Undefined.
   -   `“boolean”` : si la variable es de tipo Boolean.
   -   `“number”` : si la variable es de tipo Number.
   -   `“string”` : si la variable es de tipo String.
   -   `“object”` : si la variable es de un tipo de referencia o de tipo NULL.

### CONVERSOR DE DATOS

-   `.tostring()` //Conversor de cadenas.
-   `.parseInt()` //Convierte en un entero (Solo convierte cadenas).
-   `.parseFloat()` //Convierte en números de coma flotante (Solo convierte cadenas).
-   `Boolean(valor)` //Convierte en Booleano el valor indicado.
-   `Number(valor)` //Convierte el valor indicado en un número (entero o de coma flotante).
-   `String(valor)` //Convierte el valor indicado en una cadena.


### EXPRESIONES REGULARES
var espreg = new RegExp(cadenaExg, opcion)
#### Opciones
-   `-g` Para que evalúe toda la cadena y no se detenga en la primera coincidencia (replace)
-   `-i` para que no tenaga en cuenta la diferencia entre mayúsculas y minúsculas.
-   `-gi`  combina las dos opciones.
-   `-” ”` La cacena vacia indiaca que no se debe añicar ninguna de las opciones.
-   Var expreg = /cadenaExpReg/opción

#### CODIFICACIÓN DE LA EXPRESIÓN REGULAR
Estos son los códigos válidos que se pueden utilizar en una expresión regular y su descripción:
^ Indica el inicio de la cadena
$ Indica el final de la cadena.
. Cualquier carácter.
[xyz] Define un grupo de caracteres permitidos
[a-z] Se define que se acepta el grupo de letras minúsculas que van de la a hasta la z.
[A-Z] Se define que se acepta el grupo de letras mayúsculas que van de la A hasta la Z.
[0-9] Se define que se acepta el grupo de números que van de 0 a 9; si fuese [6-8] aceptaría 6,
7 y 8.
[^a-c] Se define que se aceptan todos los caracteres salvo el rango indicado.
* Indica que el carácter precedente se acepta de 0 a n veces.
+ Indica que el carácter precedente se acepta de 1 a n veces.
? Indica que el carácter precedente se acepta de 0 a 1 vez.
{n} Indica que el carácter precedente se acepta sólo n veces.
{n, } Indica que el carácter precedente se acepta al menos n veces.
{n, m} Indica que el carácter precedente se acepta entre n y m veces.
\ Carácter de escape.
\d Indica dígitos, es similar a [0-9]
\D Indica salvo los dígitos, es similar a [^0-9]
\s Indica caracteres de espaciado (espacio, tabulador o salto de página).
\S Indica que es un carácter cualquiera (salvo espacio).
\w Indica cualquier carácter alfanumérico, incluye el guión bajo (_).
\W Indica cualquier carácter salvo un alfanumérico o el guión bajo (_).
\b Principio o final de palabra
\B Frontera entre no palabras

#### METODOS REGEXP
test(): Evalua si una cadena cumple la expresión.
exec(): Devuelve la primera coincidencia de una cadena.
String.match(RegExp): Devuelve una matriz con todos los elementos encontrados.
String.split(RegExp): Devuelve una matriz de resultados compuesta por todos los elementos
detectados entre los separadores.
String.replace(RegExp): devuelve una nueva cadena con los caracteres reemplazados, si es que se
encontraron, sino sería una cadena idéntica a la original.
Var nuevoTexto = textoCadena.replace(expresionRegular, caracterReemplazo);
Temporizadores
Timer= setTimeout (“fn()”, lapso);
clearTimeout(Timer);
Variable=setInterval("Nombre de la funcion a repetir()", tiempo);
clearInterval(Variable);
Funciones Fecha
getDate(): Devuelve el día del mes actual como un entero entre 1 y 31.
getDay(): Devuelve el día de la semana actual como un entero entre 0 y 6.
getFullYear():Devuelve el año como un numero de cuatro dígitos.
getHours():Devuelve la hora del día actual como un entero entre 0 y 23.
getMinutes(): Devuelve los minutos de la hora actual como un entero entre 0 y 59.
getMonth(): Devuelve el mes del año actual como un entero entre 0 y 11.
getSeconds(): Devuelve los segundos del minuto actual como un entero entre 0 y 59.
getTime(): Devuelve el tiempo transcurrido en milisegundos desde el 1 de enero de 1970 hasta el momento
actual.
setDate(día_mes): Pone el día del mes actual en el objeto Date que estemos usando.
setHours(horas): Pone la hora del día actual en el objeto Date que estemos usando.
setMinutes(minutos): Pone los minutos de la hora actual en el objeto Date que estemos usando.
setMonth(mes): Pone el mes del año actual en el objeto Date que estemos usando.
setSeconds(segundos): Pone los segundos del minuto actual en el objeto Date que estemos usando.
setTime(milisegundos): Pone la fecha. Le indicamos los milisegundos que han pasado desde el 1 de enero
de 1970 en el objeto Date que estemos usando.
setFullYear(año): Pone el año actual en el objeto Date que estemos usando.
toGMTString(): Devuelve una cadena que usa las convenciones de Internet con la zona horaria GMT.
IES La Senia 2 DAW
Samuel Castro Domínguez DWEC
Objetos
this.newMethod = objeto que queremos eredar;
this.newMethod(variables contructor);
delete this.newMethod;
onclick="funcion()"
Crear un objeto
function nombreDelObjeto() {
var propiedadesDelObjeto;
}
nombreDelObjeto.prototype. nombreDeLaFuncion = function() {
return;
};
nombreDelObjeto..prototype = {
nombreDeLaFuncion: function(parametros) {
operaciones;
return;
},
…..
},
Heredar
objetoDelQueQueremosHeredar.call(parametros);
objeto.prototype = new objetoDelQueQueremosHeredar();
DOM
Nodos
.nodeName  → nombre del nodo / nombre de etiqueta / nombre del atributo / tipos de nodos (String).
.childNodes[0].nodeValue; → Devuelve el texto del nodo (String).
.nodeType → devuelve el tipo de nodo, como un número, del nodo especificado (Number).
.childNodes → Lista de todos los hijos (NodeList).
.firstChild → Puntero al primer nodo de la lista de childNodes (Node).
.lastChild → Puntero al ultimo nodo de la lista de childNodes (Node).
.nextSibling → Devuelve el nodo hermano siguiente, si no hay devuelve null (Node).
.previousSibling → Devuelve el nodo hermano anterior, si no hay devuelve null. (Node).
.hasChildNodes() → Si contiene nodos (Boolean).
.Attributes → Contiene objetos Attr que representan los atributos de un elemento.
.appendChild(nodo) → Añade un nodo al final.
IES La Senia 2 DAW
Samuel Castro Domínguez DWEC
.removeChild(nodo) → Elimina un nodo.
.remplaceChild(nuevo_nodo, nodo_antiguo) → Sustituye el nodo antiguo por el nuevo.
.insertBefore (nuevo_nodo, nodo_ref) → Añade un nodo nuevo por delante del de ref.
.setAttribute(“atributo”,”valor”) → Añade o modifica un atributo.
.style. → Para obtener el valor de cualquier propiedad CSS del nodo.
.className → para acceder al atributo class de HTML  +=
.innerHTML → devuelve el contenido HTML (HTML interna).
Crear un nodo
document.createElement("tipo_de_elemento");
document.createTextNode("texto");
.appendChild(Nodo);
Eventos
Atributos de la ventana de eventos
onclick Clic del ratón en el elemento
ondblclick Doble clic sobre el elemento
ondrag Cuando se arrastra un elemento
ondragend Ejecutarse al final de una operación de arrastre
ondragenter Ejecutarse cuando un elemento ha sido arrastrado a un destino de colocación válido
ondragleave Ejecutarse cuando un elemento deja un destino de colocación válido
ondragover Ejecutarse cuando un elemento está siendo arrastrado en un destino de colocación válido
ondragstart Ejecutarse en el inicio de una operación de arrastre
ondrop Ejecutarse cuando se cayó elemento arrastrado
onmousedown Cuando se pulsa un botón del ratón sobre un elemento
onmousemove Se activa cuando el puntero del ratón se mueve mientras está sobre un elemento
onmouseout Se activa cuando el puntero del ratón se mueve fuera de un elemento
onmouseover Se activa cuando el puntero del ratón se mueve sobre un elemento
onmouseup Cuando se suelta un botón del ratón sobre un elemento
onscroll Se ejecuta cuando se está desplazando la barra de desplazamiento de un elemento
onwheel Se activa cuando la rueda del ratón hacia arriba o hacia abajo Rodillos sobre un elemento