# Examen Parcial - elhadjiniang646

**Usuario GitHub:** elhadjiniang646
**Fecha:** 4 de noviembre de 2025
**Retos tenidos en cuenta:** Reto 003

---

## Instrucciones

A continuación encontrarás fragmentos de código extraídos de tus entregas. Cada fragmento contiene una o más situaciones relacionadas con los conceptos vistos en clase.

Para cada pregunta debes:
1) Identificar a qué se refiere la observación
2) Explicar si es o no un error y por qué
3) Proponer la corrección

Nota: Responde 5 de las 9 preguntas (en función a lo indicado en el examen).



---

## Pregunta 1

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
final double PERSIANA_ABIERTA = 0.7;
final double PERSIANA_CERRADA = 0.6;
```

¿Qué observas en este código?
Bueno en este codigo se observa la declaracion de variables estaticos de tipo double. En java para cuadno vas a usar una variable que no se va cambiar usas final y el nombre de la variable se hace en mayuscula y si mas de una palabra se separa con un guillon bajo.Pero en esta declaracion se observa que los nombres de las variables no estan bien nombradas por que se puede crear confusion. Por que un poco mas adelante del desarollo vamos hay que unas variables de String que vamos a necesitar que normalmente se tendrian que nombrar como asi. 
Entonces corrigiendolo yo pondria **final double PROBABILIDAD_PERSIANA_ABIERTA = 0.7;** , **final double PROBABILIDAD_PERSIANA_CERRADA = 0.6;**
                  


---

## Pregunta 2

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
for (int i = 0; i <= horasTotales; i++) {
    abierta = Math.random() < PERSIANA_ABIERTA;
    encendida = Math.random() < PERSIANA_CERRADA;
    hora++;
    if (hora == 24) {
        hora = 1;
        dia = dia + 1;
        // ...
    }
}
```

¿Qué observas en este código?
En este codigo se oberva que dos bucles y el bucle if esta dentro del for, yo habia implementado este codigo para, primero imprimir la ventana si esta abierta o cerrada dependiendo de su probabilidad despues hay el bucle if que habia implementado para programar la hora, hacer de tal manera que cuando la hora se a igual a 24 se reinicie empezando de 1 y que el dia suba 1. Pero la implementacion no es correcta porque mas adelante que al imprimir no se imprime bien, entonces una buena implementacion seria usar bucles for para cada una el asi : **"for(int dia = 1; dia < 7; dia ++){for(int hora =1; hora <24 ; hora ++) }"** y las variables ***abierta** y ***encendida***
dentro del bucle hora.



---

## Pregunta 3

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
for (int piso = 1; piso < 7; piso++) {
    for (int columna = 1; columna < piso; columna++) {
        System.out.print(!abierta ? VENTANA_CERRADA : encendida ? LUZ_ENCENDIDA : LUZ_APAGADA );
    }
}
```

¿Qué observas en este código?
En este bloque de codigo se observa que hay un bucle dentro de otro  y un System.out.println para imprimir el escena dependiendo de lo que occura en base a las probabilidades.El primer error que se detecta es el magic number, si derrepente de pone 7 puden haber confusiones y no saber de donde viene entonces para no crear confudiones seria mas adecuado declarar una variabl estatico tipo int que se llame **NUMERO_PISOS** y asi la modificacion del codigo se podra hacer correctamente. Segunda observacion que se constata es en el segundo for y dentro de la condicion **"(int columna=1; columna < piso ; columna ++)"** aqui la parte **"columana < piso "** no esta bien porque normalmente tiene que parcourir el numero de columnas que son 6, entonces los mas adecuado seria declarar al igual que el anterior una variable estatico que se llame **NUMERO_COLUMNAS**.
Y lo que esta dentro del system como explicado antes es el que se encargar de imprimir la escena parcurriendo los bucles y imprime en funcion de los pisos y columnas.
 
---

## Pregunta 4

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
System.out.println("Dia " + dia + " - " + hora + ":00h ");
```

¿Qué observas en este código?

---

## Pregunta 5

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
class Edificio {
    public static void main(String[] args) {
        // ...
        };
    };
}
```

¿Qué observas en este código?
Aqui se observa la declaracion de la clase Edificio que esta bien declarada con la primera letra en mayuscula y luego el la clase main igualmente bien declarad. Pero aqui se observa un eroor que en llave de sobra. Seguramente esta por error.
Normañmente deberia ser // class Edificio {
    public static void main(String[] args) {
        // ...
        };
    };
---

## Pregunta 6

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
for (int i = 0; i <= horasTotales; i++) {
    abierta = Math.random() < PERSIANA_ABIERTA;
    encendida = Math.random() < PERSIANA_CERRADA;

    hora++;

    if (hora == 24) {
        hora = 1;
```

¿Qué observas en este código?

---

## Pregunta 7

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
for (int piso = 1; piso < 7; piso++) {
    for (int columna = 1; columna < piso; columna++) {
        System.out.print(!abierta ? VENTANA_CERRADA : encendida ? LUZ_ENCENDIDA : LUZ_APAGADA );
    }
    ;
}
;
```

¿Qué observas en este código?

---

## Pregunta 8

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
System.out.println(

           "------------------------------------\r\n" +
            "     ==========================\r\n" +
            "   ==============================\r\n" +
         " ==================================\r\n" +

            "Dia " + dia + " - " + hora + ":00h ");
```

¿Qué observas en este código?
En este codigo se observa el uso del System para imprimir la parte baja del hotel pero esta mal implementada, lo bueno seria crear una condicion que immprima esta base del hotel como **"if(piso == 7 ){ ..,}"**,
y la ultima linea deberia ser declarada aparte.

---

## Pregunta 9

Archivo: `Edificio.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/bca521c60726a8fabc73ebc9281552231873d9fb/entregas/elhadjiNiang/src/reto003/Edificio.java) (Reto 003)

```java
for (int i = 0; i <= horasTotales; i++) {
    abierta = Math.random() < PERSIANA_ABIERTA;
    encendida = Math.random() < PERSIANA_CERRADA;
    // ...
}
};
```

¿Qué observas en este código?


