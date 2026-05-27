# LOOPS, WHILE & FOR
---
**BUCLE**
Serie de instrucciones que se repite indefinidamente mientras no se cumpla una condición previamente establecida.

---
**LOOP**
Es una estructura de control que permite ejecutar un bloque dee intrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.

---
**WHILE**
Los bucles while son útiles para repetir instrucciones mientras una condición sea verdadera.

while(condición boleana){ ejecuta este código si es true}
Mientras(x sea menor po igualque el alto de mi lienzo) {x incrementará 1 cada vez} ejemplo: While (x <=height)  { x=x+1 }

---
**FOR**
Es una formna de repetir un bloque de código cuando se conoce el número de iteraciones. Son útiles para repetir instrucciones un número determinado de veces.

for (inicializacion variable; condicion booleana; actualizacion){ lo que queremos que pase cuando la condicion sea verdadera } // for(let x=0 ; x<= width; x=x+1)

---
**NESTED LOOPS**
Un for dentro de otro for . se cumple primero el loop de adentro.

for(inicialización variable; condición boleana; actualización){
lo que queremos que pase cuando la condición sea verdadera
  for(inicialización variable; condición boleana; actualización){
 }
lo que queremos que pase cuando la condición sea verdadera
}

---
**frameCount**
Variable numerica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de frameCount es 0 dentro del setup(). Se incrementa en 1 cada vez que finaliza la ejecución del código draw()
