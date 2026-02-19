# Testing con Junit

Este es un ejemplo sencillo de pruebas unitarias usando Junit 5

Observa que este proyecto no tiene ninguna clase con el método `main`, no nos hace fatal. Además, tampoco tiene ningún `scanner` ni ningún `print`.

Haz un fork de este proyecto en tu repositorio de Github y contesta a las siguientes preguntas:

1. ¿Qué sentido puede tener este proyecto y para que lo podrías usar?
Este proyecto es para la creacion de una calculadora simple que sume, reste, multiplique y divida dos numeros.

2. Revisa las pruebas de la suma y comenta lo que te parezca de interés
Las pruebas de la suma comprueba primero si suma bien dos positivos, la segunda prueba se asegura que no salga un resultado differente al esperado, y la tercera comprueba varias sumas distintas.

3. Realiza un estudio de caja negra de la división e implementa las pruebas en junit: Se realizará en markdown.

Las pruebas de una caja negra en este caso seria comprobar:
- si positivo(a) entre positivo(b) = resutado correcto positivo
- si positivo(b) entre positivo(a) = resutado distinto correcto positivo
- si negativo(a) entre positivo(b) = resutado correcto negativo
- si negativo(a) entre negativo(b) = resutado correcto positivo
- si 0 entre positivo = 0
- si 0 entre negativo = 0

``` 
    @Test
    void dividir() {
        assertAll("Dividir",
                () -> assertEquals(3, Calculadora.dividir(6, 2), "6/2=3"),
                () -> assertEquals(0.33, Calculadora.dividir(2, 6), "2/6=0.33"),
                () -> assertEquals(-3, Calculadora.dividir(6, -2), "6/(-2)= -3");
                () -> assertEquals(3, Calculadora.dividir(-6, -2), "(-6)/(-2) = 3");
                () -> assertEquals(0, Calculadora.dividir(0, 2), "0/2 =0");
                () -> assertEquals(0, Calculadora.dividir(0, -2), "0/(-2) = 0"));
    }
```




## Instrucciones

El alumno deberá hacer un fork de este proyecto e implementar la solución solicitada (preguntas y código).

>Se deberá utilizar este fichero, y los artefactos de código del proyecto, para resolver el ejercicio.


**Si no se puede acceder al repositorio la evaluación del ejercicio será de 0. No se evaluarán entregas modificadas/entregadas fuera del plazo establecido en la tarea**