# ESTADOS Y CÁMARA WEB

1. Crear y definir variable estados: Al principio de tu código (fuera de las funciones), debes crear una variable que guarde en qué pantalla nos encontramos. Empezará en 0.
2. Configurar el lienzo: Creamos el lienzo de fondo donde va a ocurrir toda la magia.
3. Crear estructura del estado: Aquí usamos un switch dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.
4. Programar visualmente cada estado: Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.
5. La logica del cambio y el reinicio: Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.

--- 

# HAY MUCHAS FORMAS DIFERENTES DE CAMBIAR DE UN ESTADO A OTRO

1. Interacción con el Teclado
 1.1 Enter
 1.2 Por teclas específicas (ej. Números): Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.
2. Botones reales en la pantalla: En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando la librería de p5.js.
3. Zonas de clic (botones dibujados con rect o ellipse)
4. Interacciones automáticas (por tiempo).

---

# Cámara web

createCapture(VIDEO);
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.
2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.
