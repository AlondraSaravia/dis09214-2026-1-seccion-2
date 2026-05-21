# sesión 03 - 27/03

---

# P5.JS

## Algoritmo

Características fundamentales:

* Precisión: cada paso claro.
* Orden: Los pasos llevan una secuencia lógica.
* Finitud: Tiene que terminar en algún momento; no puede ser infinito.
* Definición: Si sigues el mismo algoritmo dos veces con los mismos datos,
deberías obtener siempre el mismo resultado.

---

## Estructura

* Input: información para empezar.
* Proceso: Los pasos lógicos que transforman esa entrada.
* Output: Resultado.

---

## Diagrama de flujo

* Representación gráfica de un algoritmo.
* Se  usa como herramienta de planificación para visualizar la lógica de un programa.
* Se usan componentes estandar para que sea usado en cualquier programador.

---

## Lenguajes de programación 

**Propósito General:**

*  Python
*  Java
*  C++
*  C#

**Desarrollo web:**

*  JavaScript
*  TypeScript
*  PHP
*  Ruby

**Sistemas y bajo nivel:**

*  C
*  Rust
*  Go

**Análisis de datos:**

* R
* Python
* Julia

**Móvil:**

* iOS
* Android

---

## P5.Js

Es una biblioteca de JavaScrip, que usa toda la potencia y sintaxis, pero con un vocabulario espacializado para dibujar, animar y crear visuales.

## Funciones maestras 

```

setup (){ Aquí se configura el entorno inicial

}

draw (){ Se ejecuta un bucle 60 veces por seg aprox. Se ceran movimientos y responde a la interaccion en tiempo real.

}

createCanvas (width, height); se crea el lienzo en pixeles.

background (R,G,B); asigna color de fondo en RGB

```

---

### Figuras geométricas 2D

* point(x,y)
* line(x1,y1,x2,y2)
* rect(x,y,ancho,alto): desde la esquina superior izquierda
* ellipse(x,y,ancho,alto): desde el centro
* circle(x,y,diámetro)
* square(x,y,lado)
* triangle(x1,y1,x2,y2,x3,y3)
* quad(x1,y1,x2,y2,x3,y3,x4,y4)

### Tamaño del borde

* strokeWeight(); tamaño de borde.  
* noStroke(); no borde.

### Color borde

* stroke(); RGB

### Forma del borde/línea

* strokeCap(); ROUND, SQUARE, PROJECT.

### Relleno de color 

* fill(); RBG

### Figuras geométricas 2D avanzadas

* arc(x,y,w,h,start,stop); se activa **angleMode(DEGREES)** en setup.








