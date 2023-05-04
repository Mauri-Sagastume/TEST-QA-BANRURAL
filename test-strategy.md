Errores encontrados:

-Línea de código 44:
En esta línea de códido que es la que genera el número aleatoreamente está generando un decimal entre 0 y 10 y debe de
generar un número entero entre 1 y 100 utilizando la función "Math.floor(Math.random()*100)+1"

El error está en que la función está escrita como "Math.floor(Math.random())+1" y falta el *100

Entonces corregido quedaría --> randomNumber = Math.floor(Math.random()*100)+1;

-Línea de código 46:
En esta línea de código que es dónde definimos la constante "ATTEMPTS" nos damos cuenta que cuándo la definieron constante
la palabra "ATTEMPTS" está mal escrita, está escrita cómo "ATTEMPS" faltando una "T" y corregir todas las líneas donde se haya usado la constante

Error --> const ATTEMPS = 5;

Corregido quedaría como --> const ATTEMPTS = 5;

-Línea de código 49:
En esta línea de código donde se daclara la constante "lowOrHi" se olvidó incluir el punto al inicio del selector CSS.

Error --> const lowOrHi = document.querySelector('lowOrHi');

Corregido queda como --> const lowOrHi = document.querySelector('.lowOrHi');

-Línea de código 87:
En esta línea se añade un un evento al boton "guessSubmit", se añade por medio de "addEventListener" y vemos que está mal escrito y corregir el "addEventListener" en dónde lo hayamos usado en el programa.

Error --> guessSubmit.addeventListener('click', checkGuess);

Corregido queda así --> guessSubmit.addEventListener('click', checkGuess);

-En la función checkGuess:
Esta función debe verificar si el valor ingresado por el usuario es un número entero utilizando la funcion "Number.isInteger()"

Entonces podemos decir que falta hacer una validación con condicional "if"

Error: Falta de un condicional para que valide si el usuario ingresó un número entero.

Corregido queda cómo: La función "checkGuess" hasta esta parte.

let userGuess = guessField.value;
  if (guessCount === 1) {
    guesses.textContent = 'Número aleatorio anterior: ';
  }
  guesses.textContent += userGuess + ' ';

Después de esa sección de código vamos a escribir lo siguiente:

if (!Number.isInteger(Number(userGuess))) {
    alert('Por favor ingresar un número entero válido!');
    guessField.value = '';
    return;
  }

-Línea de código 83 y 85:
Está dentro de la función "checkGuess"
El mensaje que muestra al usuario por haberse confundido de número y el número que debe ingresar nuevamente debe ser más grande, ese mensaje está erroneo y el color no es el especificado, aparece como color verde y en realidad el color correcto debe ser negro

Error --> lowOrHi.textContent = 'El número es mayor!';
Error --> lowOrHi.textContent = 'El número es menor!';

Corregido --> lowOrHi.textContent = 'Incorrecto! El número es mayor!';
Corregido --> lowOrHi.textContent = 'Incorrecto! El número es menor!';

-Línea de código 71 y 72:
La palabra a mostrar que es "Perdiste" está mal escrita, está así "Pérdistes" y debe ser cómo antes mencionado y aparte el color que debe mostrarse es "rojo" y se está mostrando en "negro".

Error --> lastResult.textContent = '!!!Pérdistes!!!';
Error --> lastResult.style.backgroundColor = 'black';

Corregido --> lastResult.textContent = '!!!Perdiste!!!';
Corregido --> lastResult.style.backgroundColor = 'red';

-Función reset game, línea 114:
En la función resetGame, la línea que genera el nuevo número aleatorio está mal escrita. Debe ser randomNumber = Math.floor(Math.random() * 100) + 1;

Error --> randomNuber = Math.floor(Math.random())+1" y falta el *100

Corregido --> randomNumber = Math.floor(Math.random() * 100) + 1;

-Línea de código 77:
Cuándo se muestra el mensaje de "Felicitaciones! Adivinaste el número!" Estaba con color rojo y el color correcto debe ser "verde"

Error --> lastResult.style.backgroundColor = 'red';

Corregido --> lastResult.style.backgroundColor = 'green';