<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

Actividad: Ejecicios Array - ArrayList
1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.
Ejemplo Array

~~~ java

import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        //toString Retorna una representación de los contenidos del arreglo especificado.
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        //.length limita la iteracion a la longitud del arreglo mientras la variable suma con el operador += van sumando numeros en cada iteracion y asignandoselos de nuevo a la var suma
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        //.length limita la iteracion a la longitud del arreglo mientras la var maximo compara los numeros en cada iteracion
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        //Arrays.sort ordena los elementos de un arreglo (array) localmente y devuelve el arreglo ordenado
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}

~~~

Ejemplo Array list

~~~ java
  // se importan librerias array list y scanner
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {
    // se llama al metodo notas
    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);
    // condicion para la iteracion y cierre de programa
    while(true) {
      // se crea un menu de opciones
      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");
      // se crea var tipo entero para capturar la opcion del usuario 
      int opcion = scan.nextInt();
      // se crea la salida de opciones del menu 
      if (opcion == 1) {
        // si opcion 1 entonces se llama al metodo agregar notas quien captura letras y numeros 
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        // sino si se llama el metodo mostrar notas quien imprime la informacion      alfanumerica obtenida por medio del scanner del metodo agregar notas
        mostrarNotas(notas);
      } else {
        // false cierra el programa si la opcion obtenida es diferente a la opcion 1 o 2
        break;
      }

    }

  }
// se crea el metodo agregar notas array list  tipo string y se le indica el scannner
  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    // se imprimen las opciones de salida de la opcion del menu 1 para capturar los datos alfanumericos de las notas y se declaran las var para capturar los datos
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    // se llama al metodo notas
    notas.add(titulo + " - " + contenido);

  }
  // se crea el metodo mostrar notas
  public static void mostrarNotas(ArrayList<String> notas) {
      // se crea la condicion en la variable n string que guarda la inf de notas add
    for(String n : notas) {
      // se le indica que cuando en alguna parte del programa llamen al metodo notas va a imprimir n = arraylist notas
      System.out.println(n);
    }

  }

}

~~~

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.


### Respuesta

__Ejemplos array__

~~~ java

import java.util.ArrayList; 
import java.util.Scanner;

// leer 5 numeros y mostrarlos en el mismo orden introducido

class Main {
  public static void main(String[] args) {
Scanner entrada = new Scanner(System.in);
    // se crea un arreglo de tipo entero y se pone limite de 5 
    int [] array = new int[5];
    //se crea un ciclo for para el contador de las iteraciones, se limita a 5 y se le indica que incremente 
    for (int c = 0; c < 5; c++) {
      // se le pide al usuario que ingrese un numero 
      System.out.println("Ingrese un numero: ");
      //se captura por medio del scanner los datos ingresados por el usuaro
      array[c] = entrada.nextInt();
    }
    System.out.println("Los numeros son: ");
    // se crea otro ciclo for para trabajar el array con los mismos parametros
    for(int c = 0; c < 5; c++) {
      //se imprime cada iteracion del contador
      System.out.println(array[c]);
    }

  }
}

~~~

### Respuesta

__Ejemplos array__

~~~ java

import java.util.ArrayList; 
import java.util.Scanner;

// realiza un programa que pida 6 numeros enteros y que luego muestre esos numeros junto con la palabra par o impar segun proceda

class Main {
  public static void main(String[] args) {
    
Scanner entrada = new Scanner(System.in);
 // se crea un nuevo arreglo llamado numero de tipo entero y se limita a 6 posiciones
  int [] numero = new int [6];
    // se le pide al usuario que ingrese 6 numeros
    System.out.println("ingrese 6 numeros: ");
    // se crea un ciclo for se inicia en 0 se limita a 6 y se le pide que incremente en 1 para capturar los datos ingresado
    for (int c = 0; c < 6; c++) 
    {
      // se llama al arreglo numero para capturar los datos ingresados por el usuario
      numero[c] = entrada.nextInt();
    }
    // se crea un ciclo for para trabajar con el arreglo
    for (int c = 0; c < 6; c++) 
    {
      // se indica que si el residuo del numero dividido por 2 es igual a 0 imprima que el numero es par
       if (numero[c] % 2 == 0) {
         System.out.println("el numero es par: " + numero [c]);
         // se indica que de lo contra si el residuo no es igual a 0 imprima que el impar
       } else {
         System.out.println("el numero es impar: " + numero [c]);
       }
    }

    
  }
}

~~~


### Respuesta

__Ejemplos array__

~~~ java


import java.util.ArrayList; 
import java.util.Scanner;

// invertir el array

class Main {
  public static void main(String[] args) {
    
Scanner entrada = new Scanner(System.in);
    // se crea el arreglo de tipo entero llamado arreglo y se limita a 8 posiciones
    int [] arreglo = new int [8];
    //se crea un ciclo for se inicia en 0 se limita a 8 iteraciones y se le pide que incremente 
    for (int c = 0; c < 8; c++)
      {
        // se llama al arreglo para capturar los datos ingresados por el usuario con el metodo scanner
        arreglo [c] = entrada.nextInt();
      }
    // se imprime un titulo 
    System.out.println("invertido");
    // se crea un ciclo for para trabajar en el arreglo, se le pide que inicie en la posicion 7 que se repita mientras sea mayor o igual a la posicion 0 y que se decremente en cada iteracion de esta forma se invierte el contador del ciclo
    for (int c = 7; c >= 0; c--)
    {
      // se imprime cada iteracion desde la posicion 7 hasta la posicion 0
      System.out.println(arreglo[c]);
    }
  }
}

~~~


### Respuesta

__Ejemplos array__

~~~ java



import java.util.ArrayList; 
import java.util.Scanner;

// Escribe un progama que lea 8 numeros por teclado y que los almacene en un array, rota los elementos de ese array, cambia de posicion +1 los elementos guardados y luego imprime el recorrido  

class Main {
  public static void main(String[] args) {
Scanner entrada = new Scanner(System.in);
    // se crea el array entero llamado numero con 8 posiciones
    int [] numero = new int [8];
    int c;
    //se pide al usuario que ingrese 8 numeros
    System.out.println("ingrese 8 numeros: ");
    // se inicia el ciclo for para capturar los numeros ingresados
    for(c=0; c<8; c++)
      {
        numero[c] = entrada.nextInt();
      }
  // separacion 
    System.out.println("           array original ");
    System.out.println(" ");
    // ciclo for para imprimir posiciones
      for(c=0; c<8; c++)
        {
          System.out.printf(" | " + c);
        }
    //separacion
    System.out.println(" | ");
    System.out.println(" ---------------------------------");
    // ciclo for para imprimir datos ingresados
    for (c=0; c<8; c++)
    {
      System.out.printf(" | " + numero[c]);
    }
    System.out.println(" | ");
    //rotar de posicion, se crea aux como funcion de array para cambiar los valores de posicion de 0 a 7 empezando desde la posicion 7 mientras sea mayor a 0 y en decremento
    int aux = numero[7];
    for (c=7;c>0;c--)
      {
        
        numero[c] = numero[c-1];
      }
    // se indica que array numero afecta a aux
    numero[0] = aux;
    //array con el recorrido
    System.out.println(" ");
    System.out.println("       array con el recorrido");
    System.out.println(" ");
  
    for (c=0;c<8;c++)
      {
        System.out.printf(" | " + c);
      }
    System.out.println(" | ");
    System.out.println(" ---------------------------------");
    for (c=0;c<8;c++)
      {
        System.out.printf(" | " + numero[c]);
      }
    System.out.println(" | ");
}

}


~~~

