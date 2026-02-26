# Testing con Junit

Este es un ejemplo sencillo de pruebas unitarias usando Junit 5

Observa que este proyecto no tiene ninguna clase con el método `main`, no nos hace fatal. Además, tampoco tiene ningún `scanner` ni ningún `print`.

Haz un fork de este proyecto en tu repositorio de Github y contesta a las siguientes preguntas:

1. ¿Qué sentido puede tener este proyecto y para que lo podrías usar?

Este proyecto es para la creacion de una calculadora simple que sume, reste, multiplique y divida dos numeros.

2. Revisa las pruebas de la suma y comenta lo que te parezca de interés

Las pruebas de la suma comprueba primero si suma bien dos positivos, la segunda prueba se asegura que no salga un resultado differente al esperado, y la tercera comprueba varias sumas distintas.

3. Realiza un estudio de caja negra de la división e implementa las pruebas en junit: Se realizará en markdown.

Hay dos entradas: **int a** y **int b**. Ambas enteras.
Y los valores de **int a** estan en este rango (-∞, +∞).Mientras que con **int b** sus rangos serian (-∞,0) ,0 y (0,+∞).

La salida debe ser un valor numerico float en el rango (-∞, +∞).Excepto cuando **int b**=0, en este caso devuelve un mensaje de error.

Para representar el rango de **int a** utilizare el valor 6, y para los rangos de **int b** -2, 0 y 2.

|entrada a|entrada b|salida|
|---|---|---|
|6|-2|-3|
|6|0|ERROR|
|6|2|3|

Para hacer las pruebas en junit habria que implementar lo siguiente en el archivo CalculadoraTest.java.(El de dividir con cero no hace falta porque ya esta hecho)
```
    @Test
    void dividirPositivo() {

        int valor1 = 6;
        int valor2 = 2;
        int esperado = 3;

        assertEquals(esperado, Calculadora.dividir(valor1, valor2));
    }

    @Test
    void dividirNegativo() {

        int valor1 = 6;
        int valor2 = -2;
        int esperado = -3;

        assertEquals(esperado, Calculadora.dividir(valor1, valor2));
    }


```





## Instrucciones

El alumno deberá hacer un fork de este proyecto e implementar la solución solicitada (preguntas y código).

>Se deberá utilizar este fichero, y los artefactos de código del proyecto, para resolver el ejercicio.


**Si no se puede acceder al repositorio la evaluación del ejercicio será de 0. No se evaluarán entregas modificadas/entregadas fuera del plazo establecido en la tarea**