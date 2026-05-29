# **SOLEMNE 2**
# Poder y Desigualdad

## Autor/a
Alondra Saravia Zenteno

---

##  Descripción objetiva

Este proyecto es una animación interactiva realizada en p5.js que representa visualmente la desigualdad de género a través de un sistema dinámico dividido en dos espacios: uno azul y otro rosado.

En el sketch hay una composición dividida, figuras en ambos lados, textos informativos, frases asociadas a cada género y dos personajes principales (hombre y mujer) que interactúan con el usuario.

Elementos visuales:
- Fondo dividido en dos áreas (azul y rosado)
- Figuras geométricas animadas
- Frases asociadas a estereotipos de género
- Imágenes de un hombre y una mujer
- Texto dinámico con porcentaje de “imposición masculina”
- Sistema de interacción por mousePressed
- Mensajes condicionales según el estado del sistema

---

##  Descripción conceptual

El proyecto plantea un sistema visual que representa la desigualdad de género como una relación de equilibrio inestable entre dos fuerzas. La idea central es que el espacio visual no es fijo, sino que se modifica según la interacción del usuario, evidenciando cómo el poder y la visibilidad pueden cambiar según dinámicas sociales.

### Regla del sistema:
**“A mayor dominio del lado azul, menor espacio y visibilidad del lado rosado.”**

---

##  Relación con la problemática de género

El proyecto se relaciona con la desigualdad de género al representar visualmente cómo el poder, las oportunidades y la visibilidad han sido distribuidos de forma desigual. El lado azul simboliza privilegios asociados al género masculino, mientras que el lado rosado representa las limitaciones y cargas sociales asociadas al género femenino. La interacción del usuario evidencia cómo pequeñas acciones pueden alterar este equilibrio simbólico.

---

## Input / Output / Sistema

###  INPUT 
- Clic del mouse sobre el hombre o la mujer
- Posición del mouse
- Tecla “R” para reiniciar

###  PROCESO
- El sistema detecta la interacción del usuario
- Modifica variables como `divisionX`, `hombreTam` y `mujerTam`
- Aplica funciones como `random()`, `map()` y `dist()`
- Actualiza posiciones, tamaños y transparencias en tiempo real

###  OUTPUT 
- Cambio en la división del espacio
- Aumento o disminución del tamaño de los personajes
- Movimiento de elementos visuales
- Aparición de frases dinámicas
- Cambio de mensajes según el nivel de desigualdad

---

##  Pensamiento computacional

El sistema se basa en reglas condicionales que controlan el comportamiento visual:

- Si el usuario interactúa con el hombre → aumenta el dominio del lado azul
- Si interactúa con la mujer → aumenta el espacio del lado rosado
- Las variables controlan tamaño, posición y equilibrio del sistema

### Interactividad:
El usuario actúa como agente externo que modifica el sistema, generando una simulación de cambio de poder visual.

---

##  Referentes

- **Data visualization**: Representación visual de datos sociales mediante gráficos no tradicionales.
- **Vanessa Beecroft**: Referente en representación del cuerpo y tensiones sociales en el espacio visual.

---

![IDEAS](C:\Users\yoyip\Downloads\Ideas.jpeg)
![BOCETO](C:\Users\yoyip\Downloads\Boceto.jpeg)

---
## Sketch

```
// VARIABLES

let divisionX = 650; // Guarda la posición de la división entre el lado azul y rosado en 650px.
let hombreX = 250; // Guarda la posición horizontal (X) del hombre en 250px.
let mujerX = 780; // Guarda la posición horizontal (X) de la mujer en 780px.
let hombreTam = 1; // Controla el tamaño del hombre mediante scale().Aumenta cuando el usuario hace click sobre él.
let mujerTam = 1; // Controla el tamaño de la mujer.Disminuye cuando el hombre gana dominio.
let colorTexto; // Guarda el color utilizado en los textos del sketch.
let imgHombre; // Variable donde se almacena la imagen del hombre.
let imgMujer; // Variable donde se almacena la imagen de la mujer.

// FRASES

let frasesHombre = [
  // Frases relacionadas a privilegios masculinos.
  "Más liderazgo",
  "Mayor autoridad",
  "Más oportunidades",
  "Mejor salario",
  "Preferencia laboral",
];

let frasesMujer = [
  // Frases relacionadas a desigualdad femenina.
  "Menos valorada",
  "Menor salario",
  "Poca oportunidad",
  "Doble esfuerzo",
  "Subestimada",
];

// FORMAS ANIMADAS

let formasAzules = []; // Variable que almacena las figuras animadas del lado azul.
let formasRosadas = []; // Variable que almacena las figuras animadas del lado rosado.

function preload() {
  imgHombre = loadImage("hombre.png"); // Carga la imagen del hombre desde la carpeta del sketch.

  imgMujer = loadImage("mujer.png"); // Carga la imagen de la mujer desde la carpeta del sketch.
}

function setup() {
  createCanvas(1000, 600); // Crea el lienzo principal de 1000px x 600px.
  textAlign(CENTER); // Centra todos los textos.
  colorTexto = color(255); // Define el color blanco para los textos.

  // FORMAS AZULES

  for (let i = 0; i < 20; i++) {
    //// El ciclo for repite el bloque de código 20 veces, utilizando la variable i como contador, para crear automáticamente múltiples figuras animadas con diferentes posiciones, tamaños y movimientos.

    formasAzules.push({
      x: random(0, 500),
      // Posición X aleatoria de cada figura azul.

      y: random(height),
      // Posición Y aleatoria usando el alto del canvas.

      tam: random(20, 60),
      // Tamaño aleatorio de la figura.

      vel: random(1, 4),
      // Velocidad de movimiento horizontal.

      rot: random(360),
      // Rotación inicial aleatoria.

      tipo: int(random(2)),
      // Define si será rectángulo o triángulo.
    });
  }

  // FORMAS ROSADAS

  for (let i = 0; i < 20; i++) {
    // Este ciclo for ejecuta el código 20 veces seguidas, aumentando la variable i en cada repetición, para generar distintas figuras animadas dentro del espacio.

    formasRosadas.push({
      x: random(700, width),
      // Genera una posición X aleatoria entre 700 y el ancho del canvas.

      y: random(height),
      // Genera una posición Y aleatoria entre 0 y el alto del canvas.

      tamX: random(20, 70),
      // Genera un ancho aleatorio entre 20 y 70 píxeles.

      tamY: random(20, 50),
      // Genera un alto aleatorio entre 20 y 50 píxeles.

      alpha: random(100, 255),
      // Genera una transparencia aleatoria entre 100 y 255.

      vel: random(0.5, 2),
      // Genera una velocidad aleatoria entre 0.5 y 2.
    });
  }
}

function draw() {
  background(240); // Color de fondo general.

  // FONDO AZUL

  noStroke(); // Deja las figuras sin bordes.
  fill(50, 120, 255); // Color de rrelleno en RGB
  rect(0, 0, divisionX, height); // Dibuja un rectangulo azul desde la posición 0,0 hasta la división y la altura del lienzo.

  // FONDO ROSADO

  fill(255, 170, 210); // Color de relleno en RGB
  rect(divisionX, 0, width - divisionX, height); // Dibuja un rectángulo rosado desde la división,0 hasta el ancho del lienzo - la división x el alto.

  // FORMAS AZULES

  for (let i = 0; i < formasAzules.length; i++) {
    let f = formasAzules[i]; // Este ciclo recorre todas las figuras del arreglo formasAzules y guarda cada una temporalmente en la variable f para poder dibujarla y animarla.

    push();
    translate(f.x, f.y); // Mueve el origen a la posición de la figura.
    rotate(radians(f.rot)); // Rota la figura según su ángulo.
    fill(80, 170, 255, 150); // Relleno en RBG con transparencia.

    // RECTÁNGULO
    if (f.tipo == 0) {
      rect(0, 0, f.tam, f.tam);
    } else {
      // TRIÁNGULO
      triangle(
        -f.tam / 2,
        f.tam / 2,

        0,
        -f.tam / 2,

        f.tam / 2,
        f.tam / 2
      ); // La condicional revisa el valor de f.tipo: si es 0 dibuja un rectángulo usando rect(), y si no, dibuja un triángulo usando triangle(), ambos con el tamaño almacenado en f.tam.
    }

    pop();
    f.x += f.vel; // Movimiento horizontal.
    f.rot += 2; // Rotación continua.
    if (f.x > divisionX) {
      // Reinicia figura si sale del área azul.
      f.x = random(0, 200);
      f.y = random(height); // Cuando la figura sale del área azul, se le asigna una nueva posición aleatoria en X e Y para que vuelva a aparecer dentro del canvas.
    }
  }

  // FORMAS ROSADAS

  for (let i = 0; i < formasRosadas.length; i++) {
    let p = formasRosadas[i]; // p representa cada figura rosada individual. La condición i < formasRosadas.length hace que el ciclo se repita mientras existan figuras dentro del arreglo formasRosadas.

    fill(255, 255, 255, p.alpha); // Color de relleno en RGB con transparencia
    ellipse(p.x, p.y, p.tamX, p.tamY); // Crea una ellipse en las coordenadas (x,y,ancho,alto)
    p.alpha -= p.vel; // p.alpha -= p.vel reduce poco a poco la transparencia de la figura según su velocidad, haciendo que desaparezca gradualmente.

    if (p.alpha <= 0) {
      p.x = random(divisionX, width);
      p.y = random(height);
      p.alpha = 255; // La condicional revisa si la transparencia de la figura llegó a 0 y, cuando desaparece, le asigna una nueva posición aleatoria y vuelve su transparencia al máximo para que reaparezca.
    }
  }

  // TITULO

  fill(colorTexto); // Color blanco para el texto.
  textSize(34); // Tamaño del texto en 34px.
  text("PODER Y DESIGUALDAD", width / 2, 50); // Dibuja el título "PODER Y DESIGUALDAD" en el canvas, posicionándolo horizontalmente al centro usando width / 2 y a 50 píxeles desde arriba.
  textSize(18); // Tamaño del texto en 18px.
  text("Haz click sobre el hombre o la mujer", width / 2, 80); // Centra el texto horizontalmente en el canvas y ubicándolo a 80 píxeles desde la parte superior.

  // MAP()

  let fuerzaTexto = map(divisionX, 500, 850, 50, 100); // Transforma el valor de divisionX desde un rango entre 500 y 850 a un nuevo rango entre 50 y 100, creando un porcentaje visual para representar el dominio azul.
  textSize(20); // Tamaño del texto de 20px.
  text("Imposición masculina: " + int(fuerzaTexto) + "%", 200, 120); // Muestra el porcentaje de imposición masculina calculado con map(), ubicando el texto en la posición X = 200 e Y = 120.

  // FRASES HOMBRE

  fill(255); // Color blanco para el texto.
  textSize(map(hombreTam, 1, 1.8, 14, 26)); // El tamaño del texto aumenta según el tamaño del hombre.

  for (let i = 0; i < frasesHombre.length; i++) {
    let xH = random(80, divisionX - 120); // Recorre todas las frases de frasesHombre y xH genera una posición horizontal aleatoria entre 80 y la división - 120 dentro del área azul para mostrar cada frase en distintas ubicaciones.
    let yH = random(140, 450); // yH guarda una posición vertical aleatoria entre 140 y 450 para ubicar las frases del hombre en distintas alturas.
    text(frasesHombre[i], xH, yH); // Dibuja cada frase del arreglo frasesHombre usando la posición aleatoria almacenada en xH e yH.
  }

  // FRASES MUJER

  fill(120, 0, 60); // Color de relleno del texto en RGB.
  textSize(map(mujerTam, 1, 0.4, 18, 10)); // Transforma el valor de mujerTam para ajustar dinámicamente el tamaño del texto entre 18 y 10 píxeles según el tamaño de la mujer.

  for (let i = 0; i < frasesMujer.length; i++) {
    let xM = random(divisionX + 50, width - 80); // Recorre todas las frases de frasesMujer y xM genera una posición horizontal aleatoria dentro del área rosada para distribuir las frases.

    let yM = random(140, 450); // yM guarda una posición vertical aleatoria entre 140 y 450 para ubicar las frases de la mujer en diferentes alturas.

    text(frasesMujer[i], xM, yM); // Dibuja cada frase utilizando las posiciones aleatorias guardadas en xM e yM.
  }

  // HOMBRE

  push();
  translate(hombreX, 320); // Posiciona la imagen del hombre.
  scale(hombreTam); // Escala la imagen del hombre.
  image(imgHombre, -60, -120, 120, 220); // Dibuja la imagen almacenada en imgHombre, posicionándola respecto al translate(), con un ancho de 120px y un alto de 220px.
  pop();

  // MUJER

  push();
  translate(mujerX, 340); // Posiciona la imagen de la mujer.
  scale(mujerTam); // Escala la imagen de la mujer.
  image(imgMujer, -60, -120, 120, 220); // Dibuja la imagen almacenada en imgMujer, posicionándola respecto al translate(), con un ancho de 120px y un alto de 220px.
  pop();

  // TEXTO LADOS

  fill(255); // Color blanco para el texto.
  textSize(28); // Tamaño del texto de 28px.
  text("HOMBRE", divisionX / 2, 520); // Ubica la palabra horizontalmente al centro del área azul usando divisionX / 2 y a 520 píxeles de altura.
  fill(120, 0, 60); // Color para el texto.
  text("MUJER", divisionX + (width - divisionX) / 2, 520); // Ubica la palabra al centro del área rosada calculando la mitad del espacio restante del canvas y posicionándola a 520 píxeles de altura.

  // CONDICIONALES

  if (divisionX > 750) {
    fill(255);
    text("Mayor dominio masculino", 220, 560); // Si la división es mayor a 750 inserta la frase "mayor dominio masculino"
  } else if (divisionX > 600) {
    fill(255);
    text("Desigualdad visible", 220, 560); // Si la división es mayor a 600 inserta la frase "Desigualdad visible"
  } else {
    fill(255);
    text("La mujer recupera espacio", 220, 560); // Si no es así, inserta la frase "La mujer recupera espacio"
  }
}

// INTERACCIÓN

function mousePressed() {
  // CLICK HOMBRE

  let dHombre = dist(mouseX, mouseY, hombreX, 240); // Calcula la distancia entre el mouse y el hombre.

  if (dHombre < 80) {
    divisionX += 50; // El área azul aumenta.
    hombreX += 20; // El hombre avanza.
    hombreTam += 0.08; // El hombre crece.
    mujerX += 50; // La mujer se desplaza.
    mujerTam -= 0.08; // La mujer disminuye.

    // Límites máximos y mínimos.
    if (divisionX > 850) {
      divisionX = 850; // Evita que divisionX supere 850, fijando ese valor como límite máximo.
    }

    if (hombreTam > 1.8) {
      hombreTam = 1.8; // Limita el tamaño del hombre para que no supere 1.8, evitando que crezca.
    }

    if (mujerX > 930) {
      mujerX = 930; // Evita que la posición de la mujer en X supere 930, manteniéndola dentro del límite derecho del canvas.
    }

    if (mujerTam < 0.4) {
      mujerTam = 0.4; // Evita que el tamaño de la mujer sea menor a 0.4, estableciendo un límite mínimo para que no desaparezca visualmente.
    }
  }

  // CLICK MUJER

  let dMujer = dist(mouseX, mouseY, mujerX, 260); // Calcula la distancia entre el mouse y la posición de la mujer para detectar si el usuario hizo clic cerca de ella.

  if (dMujer < 80) {
    divisionX -= 30; // Si la distancia entre el mouse y la mujer es menor a 80, se reduce divisionX en 30 para disminuir el espacio del lado azul y aumentar el lado rosado.

    mujerX -= 20; // Mueve la imagen de la mujer 20 píxeles hacia la izquierda, ajustando su posición dentro del canvas.

    mujerTam += 0.05; // Aumenta gradualmente el tamaño de la mujer cada vez que se activa la condición, haciendo que crezca visualmente.

    // Límites para evitar que el rosado supere al azul.
    if (divisionX < 500) {
      divisionX = 500; // Evita que divisionX sea menor a 500, fijando ese valor como límite mínimo para impedir que el área rosada supere al área azul.
    }

    if (mujerX < divisionX + 100) {
      mujerX = divisionX + 100; // Evita que la mujer se mueva demasiado hacia la izquierda, asegurando que siempre se mantenga al menos 100 píxeles dentro del área rosada respecto a la división.
    }

    if (mujerTam > 1) {
      mujerTam = 1; // Limita el tamaño de la mujer para que no supere 1, evitando que crezca demasiado.
    }
  }
}

// REINICIAR

function keyPressed() {
  // Reinicia el sketch al presionar R.
  if (key == "r" || key == "R") {
    divisionX = 650;
    hombreX = 250;
    mujerX = 780;
    hombreTam = 1;
    mujerTam = 1; // Detecta cuando se presiona la tecla "r" o "R" y reinicia las variables principales del sketch a sus valores iniciales, restaurando la posición y tamaño de los elementos.
  }
} 

```



---
