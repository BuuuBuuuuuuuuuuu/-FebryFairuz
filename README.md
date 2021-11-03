# -FebryFairuz
UTS
public class Tabungan {
   private int saldo;

   public Tabungan(int saldo) {
      this.saldo = saldo;
   }
   public int getSaldo() {
      return saldo;
   }
   public int simpanUang(int jumlah) {
      return saldo = saldo + jumlah;
   }
   public boolean ambilUang(int jumlah) {
      if (saldo – jumlah < 0) {
         return false;
      } else {
         saldo -= jumlah;
         return true;
      }
   }
}

public class Nasabah {
   private String namaAwal;
   private String namaAkhir;
   private Tabungan tabungan;

   public Nasabah(String namaAwal, String namaAkhir) {
      this.namaAwal = namaAwal;
      this.namaAkhir = namaAkhir;
   }
   public String getNamaAwal() {
      return namaAwal;
   }
   public String getNamaAkhir() {
      return namaAkhir;
   }
   public Tabungan getTabungan() {
      return tabungan;
   }
   public void setTabungan(Tabungan tabungan) {
      this.tabungan = tabungan;
   }
}

public class latihan91 {
   public static void main(String[] args) {
      int tmp;
      boolean status;
      Nasabah nasabah = new Nasabah("Agus","Daryanto");
      System.out.println("Nasabah atas nama "+ nasabah.getNamaAwal()+nasabah.getNamaAkhir());
         nasabah.setTabungan(new Tabungan (5000));
      tmp = nasabah.getTabungan().getSaldo();
      System.out.println("Saldo awal : "+tmp);
      nasabah.getTabungan().simpanUang(3000);
      System.out.println("Jumlah uang yang disimpan 3000");
      status=nasabah.getTabungan().ambilUang(6000);
      System.out.println("Jumlah uang yang diambil 6000");
      if(status)
         System.out.println(" OK");
      else
         System.out.println(" Gagal");
      nasabah.getTabungan().simpanUang(3500);
      System.out.println("Jumlah uang yang disimpan 3500");
      status=nasabah.getTabungan().ambilUang(4000);
      System.out.println("Jumlah uang yang diambil 4000");
      if(status)
         System.out.println(" OK");
      else
         System.out.println(" Gagal");
      status=nasabah.getTabungan().ambilUang(1600);
      System.out.println("Jumlah uang yang diambil 1600");
      if(status)
         System.out.println(" OK");
      else
         System.out.println(" Gagal");
      nasabah.getTabungan().simpanUang(2000);
      System.out.println("Jumlah uang yang disimpan 2000");
      tmp=nasabah.getTabungan().getSaldo();
      System.out.println("Saldo sekarang = "+tmp);
   }
}
