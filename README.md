# Program-dengan-Prinsip-Rekursif-Menara-Hanoi-
package Rekursif;
/**
 * @author Azaria Dhea Rismaya
 */
import java.util.Scanner;
public class MenaraHanoi {

    public static void pindahDisk (int n, char dariMenara, char keMenara, 
            char bantuanMenara) {
        if ( n==1)
            System.out.println("Pindahkan disk " + n + " dari " + dariMenara 
                    + " ke " + keMenara);
        else {
           pindahDisk(n - 1, dariMenara, bantuanMenara, keMenara);
            System.out.println("Pindahkan disk " + n + " dari " + dariMenara 
                    + " ke " + keMenara);
            pindahDisk(n - 1, bantuanMenara, keMenara, dariMenara);
        }
    }
    public static void main(String[] args) {
        Scanner input = new Scanner (System.in);
        int n;
        
        System.out.print("Masukkan jumlah disk: ");
        n = input.nextInt();
        System.out.println("Perpindahan yang dilakukan adalah: ");
        pindahDisk(n, 'A', 'B', 'C');
    }   
}
