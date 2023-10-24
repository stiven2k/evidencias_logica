<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->


### Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

- Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

### Solucion 
1. 

```java 

import java.util.Scanner;
import java.text.DecimalFormat;

public class Main {
    public static void main(String[] args) {
        DecimalFormat decimalFormat = new DecimalFormat("#,###");
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        double montoDeposito = scanner.nextDouble();

        System.out.print("Ingrese la tasa de interés anual (%): ");
        double tasaInteresAnual = scanner.nextDouble();

        System.out.print("Ingrese el plazo en meses: ");
        int plazoMeses = scanner.nextInt();

        // Calcular el interés y el monto total al vencimiento
        double tasaInteresMensual = tasaInteresAnual / 12 / 100;
        double interesMensual = montoDeposito * tasaInteresMensual;
        double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);

        // Mostrar el resumen del CDT
        System.out.println("Resumen del CDT:");
        System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
        System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
        System.out.println("- Plazo en meses: " + plazoMeses);
        System.out.println("- Interés mensual: $" + interesMensual);
        System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
    }
}
``` 

``` java
import java.util.Scanner;
import java.text.DecimalFormat;
 ```

-  Scanner se utiliza para leer la entrada del usuario desde la consola.

- DecimalFormat se utiliza para formatear números con separadores de miles y decimales.

```java
public class Main {
```

- El programa comienza con la declaración de la clase Main.

```java
DecimalFormat decimalFormat = new DecimalFormat("#,###");
Scanner scanner = new Scanner(System.in);
```

- Se crea un objeto DecimalFormat para formatear números y un objeto Scanner para leer la entrada del usuario.


```java
System.out.println("Bienvenido al calculador de CDT!");
System.out.print("Ingrese el monto del depósito: ");
double montoDeposito = scanner.nextDouble();

System.out.print("Ingrese la tasa de interés anual (%): ");
double tasaInteresAnual = scanner.nextDouble();

System.out.print("Ingrese el plazo en meses: ");
int plazoMeses = scanner.nextInt();
```

- El programa solicita al usuario ingresar el monto del depósito, la tasa de interés anual y el plazo en meses.

```java 
double tasaInteresMensual = tasaInteresAnual / 12 / 100;
double interesMensual = montoDeposito * tasaInteresMensual;
double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);
``` 
- tasaInteresMensual se calcula dividiendo la tasa de interés anual entre 12 y luego dividiendo por 100 para obtener la tasa mensual en decimales.
interesMensual representa el interés ganado cada mes.
montoTotalVencimiento representa el monto total al vencimiento del CDT.

``` java
System.out.println("Resumen del CDT:");
System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
System.out.println("- Plazo en meses: " + plazoMeses);
System.out.println("- Interés mensual: $" + interesMensual);
System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
``` 
- El programa muestra un resumen del CDT, incluyendo el monto del depósito, la tasa de interés anual, el plazo en meses, el interés mensual y el monto total al vencimiento. Los números se formatean para que sean más legibles usando DecimalFormat.

```java 
scanner.close();
```
-  Al final del programa, se cierra el objeto Scanner para liberar recursos.















2. 

```java 
import java.util.Scanner;

public class IMC {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double weight, height, imc;
      
      // Solicita el peso y la altura
      System.out.print("Ingrese su peso en kilogramos: ");
      weight = input.nextDouble();
      System.out.print("Ingrese su altura en metros: ");
      height = input.nextDouble();

      // Calcula el IMC
      imc = weight / (height * height);

      // Muestra el resultado en la consola
      System.out.printf("Su IMC es %.2f", imc);
   }
}
```

```java 
import java.util.Scanner;
```
- El programa utiliza la clase Scanner para leer la entrada del usuario.

```java 
double weight, height, imc;
```
- Se declaran tres variables de tipo double para almacenar el peso, la altura y el IMC respectivamente.

```java 
Scanner input = new Scanner(System.in);
System.out.print("Ingrese su peso en kilogramos: ");
weight = input.nextDouble();
System.out.print("Ingrese su altura en metros: ");
height = input.nextDouble();
```

- El programa solicita al usuario que ingrese su peso en kilogramos y su altura en metros. Estos valores son leídos y almacenados en las variables weight y height respectivamente.

```java 
imc = weight / (height * height);
```

- El IMC se calcula utilizando la fórmula IMC = peso / (altura * altura). El resultado se almacena en la variable imc.

```java 
System.out.printf("Su IMC es %.2f", imc);
```


- El programa muestra el resultado del IMC en la consola utilizando System.out.printf para formatear el número con dos decimales.

Cierre del Scanner:

```java
input.close();
```
- Al final del programa, se cierra el objeto Scanner para liberar recursos.
