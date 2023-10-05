<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

### Actividad 4: Ejercicios de control de flujo con expresiones compuestas

1. 
```java 
 // Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```


### Solucion 


1. 

```java
public class universidad {

    public static void main(String[] args) {
        
        // Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;

System.out.println("--------------------");
System.out.println("EJERCICIO 1: ");
if (edad >=18 && esActivo){
    System.out.println("Es mayor de edad y está activo");

}
System.out.println("--------------------");

System.out.println("EJERCICO 2: ");

if(promedio >=3.5){
    becado = true;
    System.out.println("Tiene beca");

}

if (carrera== "Desarrollo de Software"){
    System.out.println("Estudia desarrollo de software");

}
System.out.println("--------------------");
System.out.println("EJERCICO 3: ");

if (semestre !=3){
System.out.println("No estás en tu último semestre");

}
if (esActivo){
    System.out.println("Estás activo");
}
System.out.println("--------------------");
System.out.println("EJERCICIO 4: ");

if (carrera== "Desarrollo de Software"){
    System.out.println("Tienes una carrera relacionada con desarrollo web");

}
if(promedio >=4.1){
    System.out.println("Tienes un promedio superior a 4");

}
System.out.println("--------------------");
System.out.println("EJERCICIO 5: ");

if (universidad == "Cesde" ){
System.out.println(nombre);
System.out.println(apellido);
System.out.println(identificación);
System.out.println(correo);
System.out.println(carrera);
System.out.println(universidad);
System.out.println(edad);
System.out.println(esActivo);
System.out.println(becado);
System.out.println(género);
System.out.println(promedio);
System.out.println(semestre);
}
System.out.println("--------------------");
System.out.println("EJERCICIO 6: ");

if(universidad == "Cesde"  && promedio >= 4.1 && esActivo){

    System.out.println("Tienes una beca del 50%");
}

System.out.println("--------------------");
System.out.println("EJERCICIO 7: ");

if(promedio >= 4.5){
    System.out.println("Tienes una beca completa para estudiar tu carrera en desarrollo");
}
System.out.println("--------------------");

}

}
```

2. 

```java 
import java.util.Scanner;

public class Inventado por nosotros {

    public static void main(String[] args) {

        Scanner input1 = new Scanner(System.in);
        Scanner input2 = new Scanner(System.in);
        Scanner input3 = new Scanner(System.in);

        System.out.println("--------------------");
        System.out.println("EJERCICIO 1: ");

        System.out.println("Ingresa tu promedio: ");
        double promedio = input.nextDouble();

        if (promedio >= 3) {
            System.out.println("Aprobaste el semestre");
        } else {
            System.out.println("Reprobaste el semestre");
        }

        System.out.println("--------------------");
        System.out.println("EJERCICIO 2: ");

        System.out.println("¿Cual es tu género? ");
        String genre = input2.nextLine();

        if (genre == "Masculino") {
            System.out.println(" género es másculino");
        } else if (genre == "Femenino") {
            System.out.println(" género es femenino");
        }

        System.out.println("--------------------");
        System.out.println("EJERCICIO 3: ");

        System.out.println("¿Es estudiante activo?");
        System.out.println("Ingrese solo 1 para si / 2 no");
        int act = input3.nextInt();

        if (act == 1) {
            System.out.println("Estás matriculado");

        }

        else {
            System.out.println("Debe matricularte");
        }
        System.out.println("--------------------");

        input1.close();
        input2.close();
        input3.close();

    }
}
```

