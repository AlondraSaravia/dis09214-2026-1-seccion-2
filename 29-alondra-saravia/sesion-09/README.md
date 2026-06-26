# ARRAYS (listas)

Un contenedor con compartimentos numerados donde puedes
guardar múltiples datos bajo un mismo nombre. Es una lista que
mantiene varios datos ordenados. Los arreglos (Arrays) son muy
útiles para almacenar datos relacionados y pueden contener
datos de cualquier tipo.

sintaxis: let nombreArray = [e0,e1,e2,e3,e4,e5];

let nombreArray= [e0, e1, e2, e3, e4, e5]; 
let colores= ["red","orange","yellow";"green","blue"]

- para llamar alguno de los valores de Array:
  - nombreArray [n° elemento]
  - background(Colores[1]); // Esto pintara el fondo del lienzo de color anaranjado.

---

# CLASS 

Una clase (class) es un molde o plantilla abstracta que define la
estructura, los datos (propiedades) y los comportamientos
(métodos) que tendrá un tipo de objeto específico.

La sintaxis básica de una clase
en JavaScript se estructura
siempre en tres partes dentro
de un bloque de llaves:
1. La palabra clave class +
nombre que le quiera dar.
2. El método constructor
(donde se definen las
propiedades del objeto
usando .this)
3. Las funciones
personalizadas que definen lo
que hace el objeto.

class NombreDeLaClase {  

//El constructor (parámetros opcionales para personalizar al nacer)  

constructor(propiedad1, propiedad2){  

this.variableInterna1 = propiedad1; // ´this´ vinvula el dato al objeto  

this.variableInterna2 = propeidad2;  

}  

//funciones iternas (sin escribir la palabra ´function´)  

primerMetodo(){  

// código para el comportamiento del objeto  

}  

segundoMetodo()}  

//más codigo aquí  

}  

}
