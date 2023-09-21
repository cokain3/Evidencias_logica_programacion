<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->

# Actividad 5: Ejercicios de bucles
## Resolver los siguientes ejercicios:

- __Ejercicios - while__
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

### Respuesta  

``` java copy
    import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

        int multiplicar;
    System.out.println("Ingrese un numero para conocer sus multiplos");
    multiplicar = scanner.nextInt();

    int multi =1;

    while (multi<=10) {
      System.out.println(multiplicar + " x " + multi + " = " + multiplicar * multi);
      multi++;
    }
  }
}

```


 2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

### Respuesta  

``` java copy

import java.util.Scanner;
class HelloWorld {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

    System.out.println("Ingrese una cadena de caracteres");
    String cadena = scanner.nextLine();

    int i =  0;
    int contadorNumeros = 0;

    while (i < cadena.length()) {
    int caracter = cadena.charAt(i);
      if (caracter == '0' || caracter == '1' || caracter == '2' || caracter == '3' || caracter == '4' || caracter == '5' || caracter == '6' || caracter == '7' || caracter == '8' || caracter == '9') {
        contadorNumeros++;
      }
      i++;
    }

  System.out.println("La cadena de caracteres ingresada contiene " + contadorNumeros + "numeros.");
    }
}

```

- __Ejercicios - do while__
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

### Respuesta  

``` java copy

import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    
    Scanner scanner = new Scanner(System.in);

   System.out.println("Ingrese un número negativo para detener el programa.");
        
    int parar = scanner.nextInt();

    if (parar >=0) {
      int i = 1;

      do {
        System.out.println(i);
        i++;
      } while (i <= 100);
    }  while (parar < 0) {
      System.out.println("Se ha detenido el programa");
      break;
    } 
    
  }
}

```

 2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

### Respuesta  

``` java copy

import java.util.Scanner;

class Main {
  public static void main(final String[] args) {
    
   Scanner scanner = new Scanner(System.in);

   int multi;

    System.out.println("presione 0 para cerrar el programa");
    System.out.println("que numero desea multiplicar?");
    multi = scanner.nextInt();
    
    int multiplicar = 1;
    
     if (multi >= 1) {
      do {
        System.out.println(multi + " x " + multiplicar + " = " + multi * multiplicar );
        multiplicar++;
        
      } while (multiplicar <= 100); 
       
         
       } while ( multi != 0);
      
     }
  }
  
```

- __Ejercicios - for__
1. Imprimir los números impares del 1 al 50.

### Respuesta  

``` java copy


```

 2. Imprimir los números primos del 1 al 100

### Respuesta  

``` java copy


```




