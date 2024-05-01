import java.util.Scanner;

public class Main {
    static void manipulateNumber(int n) {
        // Base case: Sayı negatif veya 0 ise işlemi sonlandır ve geri dön
        if (n <= 0) {
            System.out.println("Son değer: " + n);
            return;
        }

        // Sayıdan 5 çıkar ve son değeri yazdır
        System.out.println("Son değer: " + n);

        // 5 çıkarıldıktan sonra yeni değeri hesapla ve metodu recursive olarak çağır
        int newNumber = n - 5;
        manipulateNumber(newNumber);

        // Sayı negatif veya 0 olduğunda 5 ekleyin ve son değeri yazdırın
        System.out.println("Son değer: " + (newNumber + 5));
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Bir sayı giriniz: ");
        int number = input.nextInt();

        manipulateNumber(number);
    }
}
