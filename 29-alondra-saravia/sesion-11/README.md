# DISEÑO RESPONSIVO (windowResized)

1. Crear un canvas con dimensiones dinámicas: usaremos las variables integradas en el sistema (windowWidth, WindowHeight) estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.
function setup () {  
createCanvas(windowWidth, windowHeight);  
}
2. Crear un evento windowResized(): si el usuario estira o encoge la ventana del navegador, el liezo se adaptará.  
function windowResized () {
resizeCanvas (windowWidth, windowHeight).
3. Usar valor4es relativos: Ahora p5.js actualiza estas variables width y height automáticamente con el tamaño actual del lienzo. Entonces ahora todos los valores de posición y tamaño que ocupemos los tenemos que pensar en relación proporcional a esas variables.
Usaremos fracciones y proporciones:
Ej: Centro del lienzo: (width / 2 , height / 2)
Ej: A un cuarto de la pantalla en eje x: ( width * 0.25)
4. Incluir un factor de referencia: Creamos una variable global (referencia) y la asignamos para que calcule el mínimo. Observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.
5. Usar translate - push y pop: En lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para "mover el origen del mundo”. Y siempre utilizando push() y pop() para cada figura o elemento.

---

# AGREGAR IMAGENES

1. Subir imágen a p5:
   1.1: Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.
   1.2 Hacer clic en el icono de + o el menú desplegable junto a Files.
   1.3 Seleccionar Upload file (Subir archivo).
   1.4 Arrastrar la imagen o buscarla en el computador.
   1.5 Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

2. Declarar y precargar la imágen:
   2.1 Creamos una variable global al inicio del código para guardar la imágen
   2.2 Usamos la función dentro del preload y cargamos la imagen con loadImage()

3. Dibujar y dimensionar en el draw: La imagen se dibuja usando la función image()
Esta función requiere mínimo 3 argumentos, pero
acepta 5 si queremos controlar su tamaño de
forma responsiva.

SINTAXIS:

image(nombreVariableImagen, x, y, ancho, alto);

---

loadPixels() entrar en los pixeles.

Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la memoria de acceso rápido (RAM). Se comunica directamente con la tarjeta gráfica píxel por píxel en tiempo real.  


loadPixels() crea un "puente" temporal para que puedas analizar la información de forma masiva y fluida.

get(x, y) — Lectura (El "Ojo")  

• Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.  

• Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).  

• Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una copia de respaldo completa del lienzo. set(x, y, nuevoColor) — Escritura (El "Pincel")  

• Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por completo el color que existía ahí.  

• Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo aspecto de la imagen.
updatePixels() — La Actualización  

• Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la pantalla.  

• ¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios en un borrador secreto. updatePixels() es el comando que efectivamente "publica" y renderiza el resultado final en el lienzo para que el usuario pueda verlo.
