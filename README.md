# Código da Questão 2

import java.util.Scanner;

/**
 *
 * @author 326125802
 */
public class Questão2 {

    /**
     * @param args the command line arguments
     */
   
        
 

 
    public static boolean existe(int[] vetor, int tamanho, int valor) {

        for (int i = 0; i < tamanho; i++) {

            if (vetor[i] == valor) {

                return true;

            }

        }

        return false;

    }
 
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
 
        System.out.print("Digite o valor de n: ");

        int n = sc.nextInt();
 
        int[] x = new int[n];

        int[] y = new int[n];

        int[] z = new int[2 * n]; // tamanho máximo possível
 
        int tamanhoZ = 0;
 
        // Leitura do vetor X

        System.out.println("Digite os elementos do vetor X:");

        for (int i = 0; i < n; i++) {

            x[i] = sc.nextInt();
 
            if (!existe(z, tamanhoZ, x[i])) {

                z[tamanhoZ] = x[i];

                tamanhoZ++;

            }

        }
 
        // Leitura do vetor Y

        System.out.println("Digite os elementos do vetor Y:");

        for (int i = 0; i < n; i++) {

            y[i] = sc.nextInt();
 
            if (!existe(z, tamanhoZ, y[i])) {

                z[tamanhoZ] = y[i];

                tamanhoZ++;

            }

        }
 
        // Exibir vetor união

        System.out.println("Vetor união (Z):");

        for (int i = 0; i < tamanhoZ; i++) {

            System.out.print(z[i] + " ");

        }
 
        sc.close();

    }

}
