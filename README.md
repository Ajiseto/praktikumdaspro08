ini adalah repository pertama saya
nama :  Adjie seto hidayatullah
nim  :  264107020225
kelas:  Ti-1i





import java.util.Scanner;

public class ProgramPenjualan {
    public static void main(String[] args) {
        
        int hargaPerCup = 18000;
        int jumlahCup, uangBayar;
        int totalHarga, diskon, totalBayar;
        int kembalian, kurang;

        
        Scanner input = new Scanner(System.in);

        
        System.out.print("Masukkan jumlah cup: ");
        jumlahCup = input.nextInt();<img width="786" height="182" alt="Screenshot 2026-11-03 174752" src="https://github.com/user-attachments/assets/0287a566-0d81-4cf7-9c70-ef1b754e97d5" />

        
        System.out.print("Masukkan uang bayar: ");
        uangBayar = input.nextInt();

        
        totalHarga = jumlahCup * hargaPerCup;
        diskon = 0;

       
        if (totalHarga >= 100000) {
            diskon = totalHarga * 10 / 100;
        }

       
        totalBayar = totalHarga - diskon;

        
        System.out.println("\n--- Rincian Pembayaran ---");
        System.out.println("Total Harga : Rp " + totalHarga);
        System.out.println("Diskon      : Rp " + diskon);
        System.out.println("Total Bayar : Rp " + totalBayar);
        System.out.println("--------------------------");

        
        if (uangBayar >= totalBayar) {
            kembalian = uangBayar - totalBayar;
            System.out.println("Kembalian: Rp " + kembalian);
        } else {
            kurang = totalBayar - uangBayar;
            System.out.println("Uang tidak cukup, kurang Rp " + kurang);
        }


        input.close();
    }
}
