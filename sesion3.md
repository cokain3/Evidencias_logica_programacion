<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->

# Actividad 3: Ejercicios de operaciones básicas en Java.

1. __Suma y multiplicación:__ Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.
### Respuesta

~~~java copy
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    
    Scanner scanner = new Scanner(System.in);
    
    System.out.println("Ingrese el primer numero: ");
      int num1 = scanner.nextInt();
    System.out.println("Ingrese el segundo numero: ");
      int num2 = scanner.nextInt();
    int suma = (num1+num2);
    int multi = (num1*num2);
    System.out.println("La suma de los numeros es " + suma + " y la 
    multiplicacion de los es " + multi);
   
  }
}
~~~

2. __Resta y división:__ Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

### Respuesta

~~~java copy
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    
    Scanner scanner = new Scanner(System.in);
    
    System.out.println("Ingrese el primer numero: ");
      int num1 = scanner.nextInt();
    System.out.println("Ingrese el segundo numero: ");
      int num2 = scanner.nextInt();
    int suma = (num1-num2);
    int multi = (num1/num2);
    System.out.println("La resta de los numeros es " + suma + " y la division es " + multi);
   
  }
}

~~~


3. __Operaciones combinadas:__ Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

### Respuesta

~~~java copy
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    
    Scanner scanner = new Scanner(System.in);
    
    System.out.println("Ingrese el primer numero: ");
      int num1 = scanner.nextInt();
    System.out.println("Ingrese el segundo numero: ");
      int num2 = scanner.nextInt();
    System.out.println("Ingrese el tercer numero: ");
    int num3 = scanner.nextInt();
    int suma = (num1+num2+num3);
    int multi = ((num1*num2/num3));
    System.out.println("La suma de los numeros es " + suma + " y la multiplicacion del numero 1 y 2 y su posterior division por el tercero  es " + multi);
   
  }
}

~~~

4. __Operaciones con decimales:__ Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

### Respuesta

~~~java copy
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    
    Scanner scanner = new Scanner(System.in);
    
    System.out.println("Ingrese el primer numero decimal: ");
      float num1 = scanner.nextFloat();
    System.out.println("Ingrese el segundo numero: ");
      float num2 = scanner.nextFloat();
    double suma = (num1+num2);
    double resta = (num1-num2);
    double multi = (num1*num2);
    double division = (num1/num2);
    System.out.println("La suma de los numeros es " + suma + " la resta es " + resta + " la multiplicacion es " + multi + " y la division es " + division);
   
  }
}

~~~

5. __Incremento y decremento:__ Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

### Respuesta

~~~java copy

public class Mavenproject1 {

    public static void main(String[] args) {
        int num = 10;
        int x = num += 1;
        int y = num -= 2;

        System.out.println("incremento es igual a: " + x + " y decremento es igual a: " + y);
    }
}


~~~

6. __Operador de asignación compuesta:__ Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

### Respuesta

~~~java copy

public class Eje8 {

    public static void main(String[] args) {
        
        int num = 10;
        int x = num += 5;

        System.out.println("el valor de x es: " + x);
    }
}
~~~

7. __Operadores lógicos:__ Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

### Respuesta

~~~java copy

import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese 'si' o 'no' para las siguientes preguntas:");
        
        System.out.print("¿Estás estudiando? ");
        String respuesta1 = scanner.next();

        System.out.print("¿Te gusta estudiar? ");
        String respuesta2 = scanner.next();

        
        boolean valor1 = respuesta1.equalsIgnoreCase("si");
        boolean valor2 = respuesta2.equalsIgnoreCase("si");

        
        if (valor1 && valor2) {
            System.out.println("Felicitaciones");
        } 
        
        else if (valor1 || valor2) {
            System.out.println("Intentalo y esfuerzate");
        } 
        
        else if (!valor1) {
            System.out.println("Lastima");
        } 
        
        else if (!valor2) {
            System.out.println(";C");
        } 
        
        else {
            System.out.println("Por favor, ingrese 'si' o 'no' para los valores.");
        }

      
  }
}

~~~

8. __Operador ternario:__ Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

### Respuesta

~~~java copy

import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese un número entero: ");
        int numero = scanner.nextInt();

        String resultado = (numero >= 0) ? "positivo" : "negativo";

        System.out.println("El número ingresado es " + resultado + ".");
    
      
  }
}

~~~


