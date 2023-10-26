<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 8

<!-- Su documentación aquí -->

### Actividad: Ejecicios de métodos en Java

Implementar los siguientes métodos:

- Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

## Solucion

-

```java

public class Main {
    public static void main(String[] args) {
        int num1 = 10;
        int num2 = 20;
        int resultado = encontrarMayor(num1, num2);
        System.out.println("El número mayor es: " + resultado);
    }

    public static int encontrarMayor(int numero1, int numero2) {
        if (numero1 > numero2) {
            return numero1;
        } else {
            return numero2;
        }
    }
}
```

-

```java

public class ContadorVocales {
    public static void main(String[] args) {
        String texto = "Hola, ¿mundo como estan?";
        int numeroDeVocales = contarVocales(texto);
        System.out.println("Número de vocales en el texto: " + numeroDeVocales);
    }

    public static int contarVocales(String texto) {
        int contador = 0;

        texto = texto.toLowerCase();
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);

            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }
        return contador;
    }
}
```

-

```java

public class CambiarMayusculasMinisculas {
    public static void main(String[] args) {
        String texto = "Hola";
        String textoModificado = cambiarMayusculasMinisculas(texto);
        System.out.println("Texto modificado: " + textoModificado);
    }

    public static String cambiarMayusculasMinisculas(String texto) {

        StringBuilder resultado = new StringBuilder();
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {

                resultado.append(caracter);
            }
        }
        return resultado.toString();
    }
}
```

-

```java

public class ContadorPalabras {
    public static void main(String[] args) {
        String texto = "Hola, esto es una cadena de texto ";
        int numeroDePalabras = contarPalabras(texto);
        System.out.println("Número de palabras en el texto: " + numeroDePalabras);
    }

    public static int contarPalabras(String texto) {

        String[] palabras = texto.split("\\s+");

        return palabras.length;
    }
}
```

-

```java

import java.util.Arrays;

public class OrdenarPalabras {
    public static void main(String[] args) {
        String texto = "Hola, esto es un ejemplo de texto.";
        String textoOrdenado = ordenarPalabras(texto);
        System.out.println("Palabras ordenadas alfabéticamente: " + textoOrdenado);
    }

    public static String ordenarPalabras(String texto) {

        String[] palabras = texto.split("\\s+");

        Arrays.sort(palabras);

        return String.join(" ", palabras);
    }
}
```
