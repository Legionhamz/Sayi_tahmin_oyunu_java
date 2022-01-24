# Sayi_tahmin_oyunu_java


import java.util.Scanner;
import java.util.Random;

public class tahminEt {

	public static void main(String[] args) {
		/*	***KURALLAR***
		 *  * 10 deneme hakkınız vardır.
		 *  * Eğer Tekte bilirseniz 100 puan.
		 *  * her yanlış için -10 puan alırsınız.
		 */
		
		Scanner input = new Scanner(System.in);
		System.out.println("Bir sayi giriniz:");
		int tahmin = input.nextInt();
		
		Random rnd = new Random();
		int sayi = rnd.nextInt(101);
		
		int sayac = 10;
		
			int puan = 100;
		
		for(int i = 1; i<=10; i++) {

			
			if (sayi == tahmin) {
				System.out.println(sayi + " sayisini "+ i + " . denemede doğru bildiniz, puanınız: " + puan);
				break;
				
			}
			else if(sayi > tahmin) {
				System.out.println(i + " . Deneme"+" daha büyük bir sayi giriniz: ");
				tahmin = input.nextInt();
				puan -=10;
				
			}
			else if(tahmin > sayi) {
				System.out.println(i + ". Deneme"+" daha küçük bir sayi giriniz: ");
				tahmin = input.nextInt();
				puan -=10;
			}
			else if(i == 11) {
				System.out.println("10 deneme'de bulamadınız.");
			}
			
		}
		
		
	}

}
