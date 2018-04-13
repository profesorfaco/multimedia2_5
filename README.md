Diseño Gráfico · Universidad de Chile

# Multimedia II

### Formatos ligeros para el intercambio de datos. 

Me referiré a 2 formatos: **JSON** y **CSV**. Omitiré, por ahora, a [XML](https://es.wikipedia.org/wiki/Extensible_Markup_Language), [YAML](https://es.wikipedia.org/wiki/YAML) y otros.

JSON es JavaScript Object Notation (Notación de Objetos de JavaScript). CSV es Comma Separated Values (Valores separados por coma). Sus estructuras son muy distintas. Y prefiero mostrárselas con un ejemplo: 

Volver A Comenzar, de Café Tacvba, parte así:

> Si hiciera una lista de mis errores  
De los menores hasta los peores  
Que expusiera todas las heridas,  
Los fracasos, desamores y las mentiras

En JSON, podría escribir mi listado así:

```
{
	"errores": {
		"menores": [
			["herida", "herida", "herida"],
			["fracaso", "fracaso", "fracaso"],
			["desamor", "desamor", "desamor"],
			["mentira", "mentira", "mentira"]
		],
		"peores": [
			["herida", "herida", "herida"],
			["fracaso", "fracaso", "fracaso"],
			["desamor", "desamor", "desamor"],
			["mentira", "mentira", "mentira"]
		]
	}
}
```

En CSV, podría escribirlo así: 

```
error, gravedad, clase
"El error, bien detallado",1,herida
"El error, bien detallado",1,fracaso
"El error, bien detallado",1,desamor
"El error, bien detallado",1,mentira
"El error, bien detallado",2,herida
"El error, bien detallado",2,fracaso
"El error, bien detallado",2,desamor
"El error, bien detallado",2,mentira
…
```

[CSV](https://es.wikipedia.org/wiki/Valores_separados_por_comas) es la simplificación de una hoja de cálculo, en donde encontrarían datos en filas y columnas. En CSV, cada coma representa el fin de una columna y los saltos de línea son las filas.

[JSON](https://www.json.org/json-es.html) se parece mucho a un objeto en JavaScript (tanto que le debe su nombre). Acá es necesario extender la explicación, porque aún no nos asomamos a JavaScript ni menos a la manera en que se escriben sus variables.

### JavaScript

<p>Javascript es un lenguaje de programación que, originalmente, se ejecuta del <a href="https://es.wikipedia.org/wiki/Lado_del_cliente">lado del cliente</a> para crear interactividad dinámica en páginas web. 

Cuando lo programado en [JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide) se ejecuta, no modifica directamente el código fuente de la página web sino que el [DOM](https://es.wikipedia.org/wiki/Document_Object_Model) de la misma. Uno puede seguirle la pista a esta ejecución mediante la [Consola de JavaScript](https://transferwise.com/es/help/article/2247654/tecnico-navegador/como-abrir-la-consola-de-tu-navegador) que incluyen los navegadores.

En programación, una variable está formada por un espacio en el sistema de almacenaje (memoria principal del computador) y un identificador asociado a dicho espacio. Este espacio contendrá una cantidad conocida o desconocida de datos, que pueden ir variando en la medida que el programa se ejecuta (y esta es la razón del nombre).

En JavaScript, el identificador de la variable se define después de `var` y un espacio. Así, por ejemplo, puedo crear una variable fau escribiendo `var fau`. 

En esta variable puedo almacenar distintos tipos de datos; según lo almacenado, corresponde seguir ciertas reglas:

**Para un valor entero (integer) o un valor de punto flotante (float)**, después de la asignación (=) se ingresa solamente el número. `var fau = 84;`

**Para una cadena de caracteres (string)**, después de la asignación (=) se agregan comillas dobles o simples, delimitando comienzo y final de la cadena. `var fau = "Facultad de Arquitectura y Urbanismo de la Universidad de Chile";`

**Para un booleano o variable de tipo lógico**, después de la asignación (=) se ingresa la palabra `true` o `false`, sin comillas. `var fau = false;` De usar comillas, el computador entendería que se está almacenando una cadena de caracteres.

**Para un arreglo (array)**, después de la asignación (=) se agregan paréntesis cuadrados, delimitando comienzo y final del conjunto. `var fau = ["arquitectura", "diseño", "geografía"];` luego, lo que sea parte del arreglo puede ser identificado por su posición. Si quisiera identificar a "diseño", tendría que escribir `fau[1]`, esto porque la primera posición es 0.

**Para un objeto (object)**, después de la asignación (=) se agregan paréntesis de llave, delimitando comienzo y final de un conjunto de pares. En cada par, lo primero denomina a lo que se almacena en el segundo.

```
var fau = {
direccion: "Portugal 84",
carreras: ["arquitectura", "diseño", "geografía"], 
crisis: true
};
```

A un objeto le podemos pedir cada cosa por su nombre. Así, por ejemplo, "Portugal 84" es lo que nos entrega si le pedimos `fau.direccion`. "Geografía" es lo que nos entrega si le pedimos `fau.carreras[2]`.

Como indiqué más arriba, JSON se basa en los objetos de JavaScript. Por eso, cuando necesitemos un dato particular, tenemos que pedirlo por su nombre y/o posición.

A continuación transcribo un [JSON que pueden encontrar en línea](http://api.open-notify.org/astros.json). Este JSON indica cuáles son las personas que se encuentran en el espacio:

```
{
"people": [
	{
	"name": "Anton Shkaplerov",
	"craft": "ISS"
	},
	{
	"name": "Scott Tingle",
	"craft": "ISS"
	},
	{
	"name": "Norishige Kanai",
	"craft": "ISS"
	},
	{
	"name": "Oleg Artemyev",
	"craft": "ISS"
	},
	{
	"name": "Andrew Feustel",
	"craft": "ISS"
	},
	{
	"name": "Richard Arnold",
	"craft": "ISS"
	}
],
"number": 6,
"message": "success"
}
```

Si necesito conocer el número de las personas en el espacio, puedo: 

- pedir el contenido del `number`, o 
- pedir la cantidad de contenidos en el arreglo `people`.

¿Cómo hacer esas peticiones? Eso es lo que revisaremos en las páginas incluidas en el repositorio, donde tenemos JavaScript incluido en las distintas páginas HTML.

- - - - - 

[Clase anterior](https://github.com/profesorfaco/multimedia2_4) | [Siguiente clase](https://github.com/profesorfaco/multimedia2_6)
