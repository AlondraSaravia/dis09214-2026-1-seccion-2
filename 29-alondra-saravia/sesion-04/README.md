# Datos dinámicos {Variables}

## Posición del mouse

```
mouseX;
mouseY;
(mouseX,mouseY)
ellipse(mouseX,mouseY,100,100)
```

* Variables que determinan la posición del mouse en X e Y.
---

## Variables integradas en P5

* Para declarar una variable usamos *let*
* Nos sirve para tener un código más ordenado
* Agrupar muchas variables dentro de una variable
* Los objetos funcionan como un contenedor que organiza la información mediantes pares de *clave y valor*. Luego se accede a la información mediante notación de punto.

---

ramdom(); devolver un número aleatorio en un rango definido
- random(); número decimal entre 0 y 1.
- random(máximo); número entre 0 y un máximo elegido (random(100))
- random(mínimo,máximo); se le da un valor min y uno max.

(width, height); valores definidos en el createCanvas.
(windowWidth, windowHeight); permite ajustar el tamaño del lienzo al de la ventana del navegador.

map(); nos permite convertir un valor de un rango a otro, toma un n° que está en una escala y lo traduce proporcionalmente a otra escala.
- map(valor,min_original,max_original,min_nuevo,max_nuevo)
