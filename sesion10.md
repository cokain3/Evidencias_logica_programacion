<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

1. Crear un programa en Java para calcular el interés de un CDT
Un CDT (Certificado de Depósito a Término) es un producto financiero en el que un inversor deposita una cantidad de dinero en un banco por un plazo determinado y a cambio recibe una tasa de interés fija. Al final del plazo, el inversor recupera su inversión inicial más los intereses generados. Aquí hay un ejemplo de cómo crear un programa en Java para calcular el interés de un CDT:

~~~java
//se importan librerias de scanner y formato decimal
import java.util.Scanner;
import java.text.DecimalFormat;

public class Main {
    //se crea el metodo array vacio
    public static void main(String[] args) {
        //se crea el array utilizando la libreria formato decimal
        DecimalFormat decimalFormat = new DecimalFormat("#,###");
        Scanner scanner = new Scanner(System.in);
        //se imprime un mensaje de bienvenida al usuario
        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        //se capturan los datos ingresados
        double montoDeposito = scanner.nextDouble();
        //se pide al usuario ingresar la tasa de interes anual
        System.out.print("Ingrese la tasa de interés anual (%): ");
        //se captura el valor ingresado
        double tasaInteresAnual = scanner.nextDouble();
        //se le pide al usuario ingresar plazo en emeses
        System.out.print("Ingrese el plazo en meses: ");
        //se captura el dato ingresado
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

~~~


4. Calcular la cantidad de materiales necesarios para construir una pared de ladrillos
Cálculo de la cantidad de materiales para la construcción: Este ejercicio consiste en calcular la cantidad de materiales necesarios para construir una estructura. Para ello, se debe tener en cuenta las dimensiones de la estructura y la cantidad de materiales necesarios por unidad de área o de volumen. Algunos ejemplos de cálculos de materiales son el cálculo de la cantidad de ladrillos necesarios para construir una pared, o el cálculo de la cantidad de concreto necesario para una losa o columna.

    Ejemplo en Java de cómo calcular la cantidad de materiales necesarios para construir una pared de ladrillos:

~~~java

import java.util.Scanner;

public class CantidadLadrillos {
    //se define el metodo vacio tipo string
   public static void main(String[] args) {
    //se llama al scanner
      Scanner input = new Scanner(System.in);
      //se crean las variables de tipo double para capturar los valores ingresados y realizar la operacion
      double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;
      
      // Solicita las dimensiones de la pared
      System.out.print("Ingrese el largo de la pared en metros: ");
      //se capturan los datos ingresados
      largo = input.nextDouble();
      System.out.print("Ingrese el alto de la pared en metros: ");
      //se capturan los datos ingresados
      alto = input.nextDouble();
      System.out.print("Ingrese el ancho de la pared en metros: ");
      //se capturan los datos ingresados
      ancho = input.nextDouble();

      // Solicita las dimensiones del ladrillo
      System.out.print("Ingrese el largo del ladrillo en metros: ");
      //se capturan los datos ingresados
      largoLadrillo = input.nextDouble();
      System.out.print("Ingrese el alto del ladrillo en metros: ");
      //se capturan los datos ingresados
      altoLadrillo = input.nextDouble();
      System.out.print("Ingrese el ancho del ladrillo en metros: ");
      //se capturan los datos ingresados
      anchoLadrillo = input.nextDouble();

      // Calcula el área de la pared y del ladrillo
      areaPared = largo * alto;
      double areaLadrillo = largoLadrillo * altoLadrillo;

      // Calcula la cantidad de ladrillos necesarios
      cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));

      // Muestra el resultado en la consola
      System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);
   }
}

~~~