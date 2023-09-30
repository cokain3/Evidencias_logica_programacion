<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

# Actividad: Ejecicios de métodos en Java
## Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

### Respuesta

~~~ java

 * @author Player01 
 */
public class Metodos {

        public static int obtenerMayor(int numero1, int numero2) {
        if (numero1 > numero2) {
            return numero1;
        } else {
            return numero2;
        }
    }

    public static void main(String[] args) {
        int numero1 = 5;
        int numero2 = 10;
        
        int mayor = obtenerMayor(numero1, numero2);
        System.out.println("El número mayor entre " + numero1 + " y " + numero2 + " es: " + mayor);
    }
}

~~~

2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

~~~ java

 *
 * @author Player01
 */
public class Metodos {

public static int contarVocales(String texto) {
        int contador = 0;
        texto = texto.toLowerCase(); // Convertir el texto a minúsculas para contar las vocales sin importar la capitalización
        
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }
        
        return contador;
    }

    public static void main(String[] args) {
        String texto = "Hola, este es un ejemplo de conteo de vocales.";
        int cantidadDeVocales = contarVocales(texto);
        System.out.println("El número de vocales en el texto es: " + cantidadDeVocales);
    }
}

~~~

3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

~~~ java

 * @author Player01
 */
public class Metodos {

public static String cambiarMayusculasMinisculas(String texto) {
        StringBuilder resultado = new StringBuilder();
        
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter); // Mantener caracteres no alfabéticos sin cambios
            }
        }
        
        return resultado.toString();
    }

    public static void main(String[] args) {
        String texto = "Hola Mundo 123";
        String textoModificado = cambiarMayusculasMinisculas(texto);
        System.out.println("Texto original: " + texto);
        System.out.println("Texto modificado: " + textoModificado);
    }
}

~~~

4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

~~~ java

 *
 * @author Player01
 */
public class Metodos {


    public static int contarPalabras(String texto) {
        // Divide la cadena en palabras utilizando un espacio en blanco como separador
        String[] palabras = texto.split("\\s+");
        // Devuelve el número de elementos en el array, que representa la cantidad de palabras
        return palabras.length;
    }

    public static void main(String[] args) {
        String texto = "Esto es un ejemplo de conteo de palabras.";
        int cantidadDePalabras = contarPalabras(texto);
        System.out.println("El número de palabras en el texto es: " + cantidadDePalabras);
    }
}


~~~

5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

~~~ java

 *
 * @author Player01
 */
public class Metodos {

public static String ordenarPalabras(String texto) {
        // Divide la cadena en palabras utilizando un espacio en blanco como separador
        String[] palabras = texto.split("\\s+");
        
        // Ordena las palabras alfabéticamente
        Arrays.sort(palabras);
        
        // Une las palabras ordenadas en una nueva cadena
        StringBuilder resultado = new StringBuilder();
        for (String palabra : palabras) {
            resultado.append(palabra).append(" ");
        }
        
        // Elimina el espacio en blanco adicional al final y devuelve la cadena resultante
        return resultado.toString().trim();
    }

    public static void main(String[] args) {
        String texto = "Manzana Banana Cereza";
        String textoOrdenado = ordenarPalabras(texto);
        System.out.println("Texto original: " + texto);
        System.out.println("Texto ordenado alfabéticamente: " + textoOrdenado);
    }
}

~~~


