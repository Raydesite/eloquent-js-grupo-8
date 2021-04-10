# Ejercicios Capitulo 3

Hechos con amor y cariño

## Primer Ejercicio

Escribe una función min que tome dos argumentos y retorne su mínimo.

```javascript
function min(nro1, nro2){
  if (nro1 < nro2){
    return nro1
  }
  else if (nro2 < nro1) {
    return nro2
  }
}

min(0,10)
// 0

min(0,-10)
// -10
```

------------

## Segundo Ejercicio

Define una función recursiva esPar que corresponda a esta descripción. La función debe aceptar un solo parámetro (un número entero, positivo) y devolver un Booleano.

Pruébalo con 50 y 75. Observa cómo se comporta con -1. Por qué? Puedes pensar en una forma de arreglar esto?

```javascript
function esPar(numero) {
  numero = Math.abs(numero)
  if (numero % 2 == 0) {
    return true
  } else if (numero === 0) {
    return true
  } else if (numero === 1) {
    return false
  } else {
    return esPar(numero - 2)
  }
}


esPar(50)
esPar(75)
esPar(-1)
```

## Tercer Ejercicio 

Puedes obtener el N-ésimo carácter, o letra, de un string escribiendo "string"[N]. El valor devuelto será un string que contiene solo un carácter (por ejemplo, "f"). El primer carácter tiene posición cero, lo que hace que el último se encuentre en la posición string.length - 1. En otras palabras, un string de dos caracteres tiene una longitud de 2, y sus carácteres tendrán las posiciones 0 y 1.

Escribe una función contarFs que tome un string como su único argumento y devuelva un número que indica cuántos caracteres “F” en mayúsculas haya en el string.

Despues, escribe una función llamada contarCaracteres que se comporte como contarFs, excepto que toma un segundo argumento que indica el carácter que debe ser contado (en lugar de contar solo caracteres “F” en mayúscula). Reescribe contarFs para que haga uso de esta nueva función.

``` javascript
function countFs(str) {
  return countChar(str,"F")
}

function countChar(str, char) {
    let charCount = 0;
        for (i=0; i < str.length; i++) {
            if (str[i]===char) charCount++
        }
    return charCount
}
console.log(countFs("FFC"));
// → 2
console.log(countChar("kakkerlak", "k"));
// → 4
```