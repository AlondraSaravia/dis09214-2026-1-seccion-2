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

El proyecto se relaciona con la desigualdad de género al representar visualmente cómo el poder, las oportunidades y la visibilidad han sido históricamente distribuidos de forma desigual. El lado azul simboliza privilegios asociados al género masculino, mientras que el lado rosado representa las limitaciones y cargas sociales asociadas al género femenino.La interacción del usuario evidencia cómo pequeñas acciones pueden alterar este equilibrio simbólico.

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

- **Arte generativo (Generative Art)**: Uso de reglas y aleatoriedad para crear composiciones dinámicas.
- **Data visualization**: Representación visual de datos sociales mediante gráficos no tradicionales.
- **Vanessa Beecroft**: Referente en representación del cuerpo y tensiones sociales en el espacio visual.
- **Arte conceptual feminista**: Obras que abordan desigualdad de género y roles sociales.
- **p5.js (Processing)**: Entorno de programación creativa utilizado para construir sistemas interactivos.

---

![IDEAS](C:\Users\yoyip\Downloads\Ideas.jpeg)
![BOCETO](C:\Users\yoyip\Downloads\Boceto.jpeg)

---

##  Diagrama de flujo

![Diagrama de flujo del sistema](diagrama.png)

---
