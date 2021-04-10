# Ejercicios Capitulo 2

Hechos con amor y cariño

------------

## Primer Ejercicio

Escriba un ciclo que haga siete llamadas a console.log para generar el siguiente triángulo: - ingresar resultado del código -

```javascript
 let hashtag = '#'

 for (let hashtag = '#'; hashtag != '########'; hashtag += '#'){
  console.log(hashtag)
} 
```

------------

## Segundo Ejercicio

Escribe un programa que use console.log para imprimir todos los números de 1 a 100, con dos excepciones. Para números divisibles por 3, imprime "Fizz" en lugar del número, y para los números divisibles por 5 (y no 3), imprime "Buzz" en su lugar.

Cuando tengas eso funcionando, modifica tu programa para imprimir "FizzBuzz", para números que sean divisibles entre 3 y 5 (y aún imprimir "Fizz" o "Buzz" para números divisibles por solo uno de ellos).

(Esta es en realidad una pregunta de entrevista que se ha dicho elimina un porcentaje significativo de candidatos a programadores. Así que si la puedes resolver, tu valor en el mercado laboral acaba de subir).

```javascript
function fizzBuzz(){
  for (let i = 0; i <= 100; i++){
    if (i % 3 == 0 && i % 5 == 0) {
      console.log("FizzBuzz")
    } else if (i % 3 == 0) {
      console.log("Fizz")
    } else if (i % 5 == 0) {
      console.log("Fizz")
    } else {
      console.log(i)
    }
  }
}

fizzBuzz()
```

## Tercer Ejercicio

Escribe un programa que cree un string que represente una cuadrícula de 8 × 8, usando caracteres de nueva línea para separar las líneas. En cada posición de la cuadrícula hay un espacio o un carácter "#". Los caracteres deberían de formar un tablero de ajedrez.

Pasar este string a console.log debería mostrar algo como esto: -Resultado del código -

Cuando tengas un programa que genere este patrón, define una vinculación tamaño = 8 y cambia el programa para que funcione con cualquier tamaño, dando como salida una cuadrícula con el alto y ancho dados.

``` javascript
let tablero = "";

let tamaño = 8;

for (let i = 0; i < tamaño; i++){ 
    for (let j = 0; j < tamaño; j++){
        if( ( i + j ) % 2 == 0){
          
            tablero += " ";
          
        } else {
            tablero += "#";
        }
    }
  
    tablero += "\n";
}
console.log(tablero);
```