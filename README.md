# Adivinar-numero_1
El usuario tendra que adivinar el numero seleccionado por la maquina en 10 intentos
import java.util.Scanner;
public class Numerito {
    public static void main(String args[]){
        Scanner leer = new Scanner(System.in);
        
        int numero, numeroInt,intentos;
        
        numero =(int)Math.round((Math.random()*99)+1);
        intentos = 1;
        System.out.println("Adivina el numero seleccionado por el programa en menos de 10 intentos");
        do{
            System.out.printf("INTENTO NUMERO %d DE 10\n",intentos);
            System.out.println("Ingrese numero: ");
            numeroInt = leer.nextInt();
            if(intentos > 9){
                System.out.println("PERDISTE NO ENCONSTRASTE EL NUMERO "+ numero);
                break;
            }
            if(numeroInt == numero){
                System.out.println("Lo lograste XD encontras el numero "+ numero);
                break;
            }else{
                if(numero < numeroInt){
                    System.out.println("numero ingresado es mayor que el numero a buscar");
                }else{
                    System.out.println("numero ingresado es menor que el numero a buscar");
                }
            }
            intentos++;
        }while(numeroInt != numero);
        System.out.println("programador: MEVA");
    }
}
