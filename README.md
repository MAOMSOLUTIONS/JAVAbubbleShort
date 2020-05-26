# JAVAbubbleShort
import java.util.Scanner;

public class HelloWorld 
{ 

     public static void main(String []args){
        System.out.println("EXAMEN JAVA  - Miguel Ochoa 21 de  Mayo");
        System.out.println("1.- Genera un programa en Java que encuentre los primeros 10 números primos");
        NumeroPrimo(2,100,10);

        System.out.println("3.- Genera un programa en java que ordene la siguiente lista de números 90,5,8,9,4,2,1,10,55,68,74,42,41,45,67 de números de forma ascendente, con un algoritmo tipo bubble-sort");

        ordenaNumeros();

     }
     public static void NumeroPrimo(int desde,int hasta,int contador){
         boolean esPrimo;
         int icontadorAux = 1;
         for(int i = desde; i<= hasta; i++){
             esPrimo = true;
             
             
             for(int j= 2; j <= Math.sqrt(i) && esPrimo; j++){
                 if(i%j==0){
                     esPrimo = false;
                 }
        
             }
             
             
             if(esPrimo){
                 if(icontadorAux <= contador){
                     System.out.println(icontadorAux + "-" + i);
                     icontadorAux++;
                 }
             }
             
         }
     }
     
     public static void ordenaNumeros(){
         int nn;
         Scanner sc = new Scanner(System.in);
         int ArrayN[] = {90,5,8,9,4,2,1,10,55,68,74,42,41,45,67};
          System.out.println("SIN ORDENAR");
          mostrarN(ArrayN);
          System.out.println("ORDENADO bubble-sort");
          bubbleShort(ArrayN);
          
         
     }
     static void bubbleShort(int ArrayN[]){
         for(int i=0;i<ArrayN.length -1 ; i++){
             for(int j=0; j<ArrayN.length -1; j++){
                 if(ArrayN[j] >ArrayN[j+1]){
                     int temp = ArrayN[j+1];
                     ArrayN[j+1] = ArrayN[j];
                     ArrayN[j] = temp; 
                     
                 }
             }
         }
         mostrarN(ArrayN);
         
     }
     
     
     static void mostrarN(int ArrayN[]) {
        System.out.println("|-----------------------|");

        for (int i = 0; i < ArrayN.length; i++) { System.out.print(" Elemento " + (i + 1) + " -----> " + ArrayN[i] + "\n");
        }
        System.out.println("|-----------------------|");
    }
     
}
