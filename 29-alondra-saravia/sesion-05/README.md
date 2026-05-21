# Transformaciones y Condicionales 

**ÁNGULOS:**

angleMode();

angleMode(RADIANS); por defecto p5 usa radiantes para medir ángulos

angleMode(DEGREES); para cambiar a grados se usa esto en el *setup*

---

**ROTACIÓN:**

rotate(); 

rotate(valor radiantes o en grados);

- Sirve para rotar elementos.
- Rota en el punto de origen (0,0)
- se recomienda usar con *translate();* y en otros casos con *rectMode(CENTER);*

---

**TRASLADAR:**

translate();

translate(x,y);

- sirve para trasladar un punto de origen a una nueva coordenada.

---

**GUARDAR Y RESTAURAR:**

push();
pop();

- Funciones que trabajan juntas como un *"sistema de memoria temporal"* para el estilo y las transformaciones del lienzo.

---

**ESCALA:**

scale();

scale(x,y)

- Ajusta la escala del sistema de coordenadas actual por el factor especificado

---

# CONDICIONALES

*EXPRESIÓN BOOLEANA:* es cualquier enunciado, dato o instrucción que al ser evaluado, solo puede arrojar dos valores posibles *(True)* o *(False)*.

Para construirlo se necesitan 3 elementos:

- *Operandos o Valores:* Datos básicos que se evaluan
   - Variables: x,y o mouseX,mouseY etc
   - Constantes o literales: valores fijos como 5, hola, true o false

- *Operadores de comparación:* Permiten contrastar 2 valores
   - == (igual a)
   - != (diferente de)
   - < o > (mayor o menor que)
   - <= o >= (mayor o igual / menor o igual)

- *Operadores lógicos:* Combinar expresiones
   - AND (&&): Es verdadero solo si ambas partes son verdaderas.
   - OR (||): Es verdadero si al menos una parte es correcta.
   - NOT (!): Invierte el valor (falso).

---

*SENTENCIA CONDICIONAL (IF - ELSE IF - ELSE)*

- If (condición) {ejecuta este código si es true}
  
- If (condición) {ejecuta este código si es true}
  else if (condición 2) {ejecuta este códigp si es true}
  else {ejecuta este código si ambas condiciones son falsas}
