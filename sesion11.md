<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->

### Actividad: Ejercicios de Lógica de Programación


1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.


### Solucion 

```java
public class Ejercicio1 {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2};

        // Creamos una variable para almacenar el número que aparece más de una vez
        int numeroRepetido = 0;

        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            for (int j = 0; j < i; j++) {
                if (numeros[i] == numeros[j]) {
                    // El número actual ya ha aparecido
                    numeroRepetido = numeros[i];
                    break;
                }
            }
        }

        // Si el número repetido es distinto de 0, lo imprimimos
        if (numeroRepetido != 0) {
            System.out.println("El número repetido es: " + numeroRepetido);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

1. 

```java 
import java.util.HashMap;
import java.util.Map;

public class Ejercicio1 {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2, 4, 6, 3, 7, 8, 8};

        // Creamos un HashMap para almacenar la frecuencia de aparición de cada número
        Map<Integer, Integer> frecuenciaNumeros = new HashMap<>();

        // Recorremos el conjunto de números y contamos la frecuencia de cada número
        for (int numero : numeros) {
            frecuenciaNumeros.put(numero, frecuenciaNumeros.getOrDefault(numero, 0) + 1);
        }

        // Mostramos los números que aparecen más de una vez
        boolean hayNumerosRepetidos = false;
        System.out.println("Números repetidos:");
        for (Map.Entry<Integer, Integer> entry : frecuenciaNumeros.entrySet()) {
            if (entry.getValue() > 1) {
                System.out.println(entry.getKey());
                hayNumerosRepetidos = true;
            }
        }

        // Si no hay números repetidos, mostramos un mensaje indicando eso
        if (!hayNumerosRepetidos) {
            System.out.println("No hay ningún número repetido");
        }
    }
}
```
2. 

```java 
public class Ejercicio2 {

    public static void main(String[] args) {
        
        int numeroDecimal = 20;

        
        String numeroBinario = "";

        
        for (int i = numeroDecimal; i > 0; i /= 2) {

            
            int resto = i % 2;

            
            numeroBinario = resto + numeroBinario;
        }

        
        System.out.println("El número binario es: " + numeroBinario);
    }
}
```
