# SONIDO EN P5.JS

1. Subir sonidos a p5: 
1.1  Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.
   
1.2 Hacer clic en el icono de + o el menú desplegable junto a Files.  

1.3 Seleccionar Upload file (Subir archivo).  

1.4 Arrastrar el archivo de sonido. Formatos recomendados: .mp3 o .wav  

1.5 Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

2. Declarar y precargar el sonido
   2.1 Creamos una variable global al inicio del código para guardar nuestro sonido.
   2.2 Usamos la función function preload() inicializamos nuestra variable y cargamos el sonido con loadSound()

3. Activar mi sonido: Le damos play al sonido en el function setup con:

nombreVariable.play();

Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.

---

## Métodos de control de sonido

nombreVariable.play() : Reproduce el sonido una vez.  

nombreVariable.loop() : Reproduce el sonido en bucle infinito.  

nombreVariable.stop() : Detiene el sonido por completo.  

nombreVariable.pause() : Pausa el sonido en el segundo actual.  


nombreVariable.setVolume(valor) : Modifica el volumen. Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).  

nombreVariable.rate(valor) : Modifica la velocidad de reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más grave) y 2.0 es el doble (suena más agudo).

--- 

## Métodos de consulta o estados del sonido

nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.  
nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().  
nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().  
nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).  
nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).  
nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0
y 1.0).  
nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el doble).
