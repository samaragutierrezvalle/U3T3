# U3T3
package samara_t3;

import java.util.Scanner;

public class Samara_T3 {

    public static void main(String[] args) {
        Scanner V = new Scanner(System.in);
        ClasePila p = new ClasePila();
        boolean salir = false;
        int dato;
        do {
            salir = false;
            System.out.println(
                    "Metodo de una pila"
                    + "\n[1]insertar"
                    + "\n[2]sacar"
                    + "\n[3]mostrar cima"
                    + "\n[4]generar numeros random"
                    + "\n[5]mostrar si la pila esta vacia"
                    + "\n[6]mostrar pila"
                    + "\n[7]Mostrar tamaño de la pila"
                    + "\n[8]salir");
            int opc = V.nextInt();
            switch (opc) {
                case 1:
                    System.out.println("Ingrese un numero");
                    dato = V.nextInt();
                    p.Agregar(dato);
                    break;
                case 2:
                    if (!p.EstaVacia()) {
                        System.out.println("Numero elimidado: " + p.quitar());
                    } else {
                        System.out.println("La pila esta vacia");
                    }
                    break;
                case 3:
                    if (!p.EstaVacia()) {
                        System.out.println("Ultimo numero agregado: " + p.cima());
                    } else {
                        System.out.println("La pila esta vacia");
                    }
                    break;
                case 4:
                    p.NumerosRandom();
                    System.out.println("Numeros random generados");
                    break;
                case 5:
                    if (p.EstaVacia()) {
                        System.out.println("La pila esta vacia");
                    } else {
                        System.out.println("La pila tiene " + p.tama());
                    }
                    break;
                case 6:
                    if (!p.EstaVacia()) {
                        p.MostrarPila();
                    } else {
                        System.out.println("La pila esta vacia");
                    }
                    break;
                case 7:
                    System.out.println("Tamaño de la pila: " + p.tama());
                    break;
                case 8:
                    salir = true;
                    break;
                default:
                    System.out.println("Opcion no valida");
            }
            System.out.println("");
        } while (!salir);
    }
}
