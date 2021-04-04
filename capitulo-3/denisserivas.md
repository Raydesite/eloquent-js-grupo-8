# Ejercicios Capítulo 3

**Mínimo** - Escribe una función `min` que tome 2 argumentos y regrese su mínimo

```javascript
function min(x,y) {
	if (x<y) {
		return x
	} else {
		return y
	}
}
console.log(min(0, 10));
// → 0
console.log(min(0, -10));
// → -10
```

**Recursión** - Define una función recursiva `isEven` que corresponda a la siguiente descripción. La función debería aceptar un solo parámetro (un número entero positivo) y regresar un booleano.
- Para cualquier número N, es par si N-2 es par.

```javascript
function isEven(x) {
	if (x==0){
		return true
	} else if (x==1) {
		return false
	} else {
		return isEven(x-2)
    }
}
console.log(isEven(50));
// → true
console.log(isEven(75));
// → false
console.log(isEven(-1));
// → ??
```

**Contando Bs** - Escribe una función `countBs` que tome un string como su único argumento y regrese un número que indique cuantas "B" mayúsculas hay en el string. Luego escribe una función llamada `countChar` que se comporte como `countBs`, excepto que toma un segundo argumento que indica el caracter que se va a contar (en lugar contar las "B" mayúsculas). Reescribe `countBs` para hacer uso de esta nueva función.

```javascript
function countBs(str) {
  return countChar(str,"B")
}

function countChar(str, char) {
	let charCount = 0;
		for (i=0; i < str.length; i++) {
			if (str[i]===char) { charCount++}
		}
	return charCount
}
console.log(countBs("BBC"));
// → 2
console.log(countChar("kakkerlak", "k"));
// → 4
```
