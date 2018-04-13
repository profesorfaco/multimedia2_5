Diseño Gráfico · Universidad de Chile

# Multimedia II

### Formatos ligeros para el intercambio de datos. 

Me referiré a 2 formatos: **JSON** y **CSV**. Omitiré, por ahora, a [XML](https://es.wikipedia.org/wiki/Extensible_Markup_Language), [YAML](https://es.wikipedia.org/wiki/YAML), [KML](https://es.wikipedia.org/wiki/KML) y otros.

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

CSV es la simplificación de una hoja de cálculo, en donde encontrarían datos en filas y columnas. En CSV, cada coma representa el fin de una columna y los saltos de línea son las filas.

JSON se parece mucho a un objeto en JavaScript (tanto que le debe su nombre). Acá es necesario extender la explicación, porque aún no nos asomamos a JavaScript ni menos a la manera en que se escriben sus variables.

### JavaScript

<p>Javascript es un lenguaje de programación que, originalmente, se ejecuta del <a href="https://es.wikipedia.org/wiki/Lado_del_cliente">lado del cliente</a> para crear interactividad dinámica en páginas web. 

Cuando [JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide) se ejecuta, no modifica directamente el código fuente de la página web sino que el [DOM](https://es.wikipedia.org/wiki/Document_Object_Model) de la misma. Uno puede seguirle la pista a esta ejecución mediante la [Consola de JavaScript](https://transferwise.com/es/help/article/2247654/tecnico-navegador/como-abrir-la-consola-de-tu-navegador) que incluyen los navegadores.


- - - - - 

[Clase anterior](https://github.com/profesorfaco/multimedia2_2) | [Siguiente clase](https://github.com/profesorfaco/multimedia2_4)
