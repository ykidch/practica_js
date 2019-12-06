# Resumen

- **3 maneras de insertar CSS:**
```html
	<tag style="attribute:value; attribute:value; ...">
```
  
```html
	<style>
		h1 {color:red;...}
		.class {...}
		#id {...}
	</style>
```
  
```html
	<link href="path/to/file" type="text/css" rel="stylesheet">
```

-Maneras de insertar JS
	<script>
		...
		código JS
		...
	</script>

	<script src="myscript.js"></script> #se comporta igual que si copias y pegas el código directo en el html

-Documentación
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
e.g. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const
(te dice desde qué versiones de buscadores es compatible)

// comentario
/* */ comentar múltiples líneas

-Declarar una variable: 	var foo = valor;
-Cambiar el valor de una variable (ya declarada): 	foo = valor2;

-Mostrar en línea de comando: console.log(foo);

-Tipos de datos importantes:
	número: 1,2,3
	string: 'abc'
	array: [1,2,3,'a','b','c']   -  array[i] (indexar desde 0)
	objeto: {key1:value1, key2:value2, ...}  - objeto.key

-if, for, while, switch
	if (condición) {
		acción
		}
	else if (condición) {
		acción
		}
	else (condición) {
		acción 
		};

	switch 

	for (var i=min; i<=max; i++) {
		acción
		};

	while (condición) {
		acción
		};

-definir funciones
	function miFuncion(args) {
		...
		return valor;
		}	


-JS interactúa con HTML con el "DOM"

document - todo el contenido de la página
document.getElementById('id')
document.getElementsByClassName('classname') 
document.getElementsByTagName('tagname') 
document.querySelector('#id'/'.classname'/'tagname')
	 - puede ser document.querySelector('tag.class#id')


Element.innerHTML - regresa el HTML dentro del elemento (puedes cambiarlo)
Element.textContent - regresa el contenido sin contar los HTML tags (puedes cambiarlo)

document.createElement('tag') - crea <tag></tag> (pero no lo mete en el DOM)

Para meter elementos en el DOM:
	Element.appendChild(otherElement) - mete otherElement como un hijo de Element, justo antes de </Element>
	Element.insertAdjacentElement(where,otherElement) - inserta otherElement en:
	where = 'beforebegin' - hermano antes de Element
		'afterbegin' - justo después de <Element>
		'beforeend' - justo antes de </Element>
		'afterend' - hermano después de Element 

Quitar elementos:
	Element.removeChild(childElement)
	Element.remove()

Cambiar CSS
	Element.style.attribute = nuevo_valor
	Element.setAttribute('attribute','value')


Eventos:
-document.addEventListener(evento, funcion)

