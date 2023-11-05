<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->

# Actividad: Ejercicios de Lógica de Programación
Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

### Respuesta

~~~java

public class Main {

    public static void main(String[] args) {
        int[] numeros = {1, 2, 3, 4, 5, 2, 3, 4, 6, 7, 7};

        boolean hayRepetidos = false;

        for (int i = 0; i < numeros.length; i++) {
            for (int j = i + 1; j < numeros.length; j++) {
                if (numeros[i] == numeros[j]) {
                    hayRepetidos = true;
                    System.out.println("Número repetido: " + numeros[i]);
                    break; // Si se encuentra un número repetido, se sale del bucle interno
                }
            }
        }

        if (!hayRepetidos) {
            System.out.println("No hay números repetidos.");
        }
    }
}

~~~


Desarrollar un algoritmo que realice la conversión de binario a decimal.

### Respuesta

~~~ java

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingresa un número binario: ");
        String binario = scanner.nextLine();
        scanner.close();

        int decimal = 0;
        int longitud = binario.length();

        for (int i = 0; i < longitud; i++) {
            char digito = binario.charAt(i);

            if (digito == '1') {
                decimal = decimal * 2 + 1;
            } else if (digito == '0') {
                decimal = decimal * 2;
            } else {
                System.out.println("Número binario inválido.");
               
            }
        }

        System.out.println("El número decimal equivalente es: " + decimal);
    }
}

~~~






