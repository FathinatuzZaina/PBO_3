# PBO_3
# FATHINATUZ ZAINA (2409116016)
# DESKRIPSI
Program Sistem Informasi Manajemen Donor Darah ini adalah aplikasi sederhana berbasis console yang dirancang untuk mengelola data pendonor dengan fitur CRUD (Create, Read, Update, Delete) serta tambahan pencarian dan filter data. Program ini menerapkan konsep Object-Oriented Programming (OOP) dengan menggunakan encapsulation, inheritance, dan polymorphism. Superclass Person menyimpan atribut umum seperti id, nama, dan umur, kemudian diturunkan ke subclass Donor yang memiliki atribut tambahan golDarah dan subclass Petugas yang memiliki atribut jabatan. Kedua subclass ini melakukan overriding pada method tampilkanInfo() untuk menampilkan informasi sesuai jenis datanya. Class DonorService mengelola logika CRUD pendonor lengkap dengan validasi umur minimal 17 tahun dan validasi golongan darah (A, B, AB, O), sementara data disimpan menggunakan ArrayList. Melalui class Main, pengguna dapat mengakses menu interaktif untuk menambah, menampilkan, mengubah, menghapus, mencari, dan memfilter data pendonor, sekaligus menampilkan contoh data petugas. Dengan struktur ini, program berhasil menunjukkan implementasi konsep OOP secara terstruktur untuk mendukung pengelolaan data donor darah.

# ALUR PROGRAM
1. Saat pengguna memilih menu tambah data, program akan meminta input berupa nama, umur, dan golongan darah. Data yang dimasukkan akan divalidasi, dengan syarat umur minimal 17 tahun dan golongan darah hanya A, B, AB, atau O. Jika data valid, maka donor baru akan disimpan ke dalam daftar dan ditampilkan pesan bahwa data berhasil ditambahkan.
<br>
<div align="center">
  <img width="571" height="370" alt="Screenshot 2025-09-23 215429" src="https://github.com/user-attachments/assets/36366125-569e-4c2b-a784-11b374650d26" />
</div>
<br>
2. Jika pengguna memilih menu untuk menampilkan semua donor, program akan menampilkan seluruh data donor yang sudah tersimpan dalam daftar. Jika belum ada data, program akan memberikan pesan bahwa data pendonor masih kosong.
<br>
<div align="center">
  <img width="615" height="352" alt="Screenshot 2025-09-23 215435" src="https://github.com/user-attachments/assets/4dbd42fb-b4f9-4089-a29c-44d9fa29465c" />
</div>
<br>
3. Menu update memungkinkan pengguna memperbarui data donor yang ada. Program menampilkan daftar donor beserta ID-nya, lalu pengguna diminta memilih ID yang akan diubah. Setelah itu, pengguna dapat memasukkan nama, umur, dan golongan darah baru. Jika umur yang dimasukkan kurang dari 17, program menolak update dan menampilkan pesan kesalahan.
<br>
<div align="center">
  <img width="651" height="445" alt="Screenshot 2025-09-23 215443" src="https://github.com/user-attachments/assets/e73c4e02-77ba-4627-bf75-803066b305fe" />
</div>
<br>
4. Melalui menu hapus, program akan menampilkan daftar donor yang ada, lalu pengguna diminta memasukkan ID donor yang ingin dihapus. Jika ID valid, data akan dihapus dari daftar dan program menampilkan pesan bahwa data berhasil dihapus. Jika ID tidak sesuai, maka program akan menampilkan pesan bahwa data tidak ditemukan.
<br>
<div align="center">
  <img width="640" height="404" alt="Screenshot 2025-09-23 215526" src="https://github.com/user-attachments/assets/215b064f-37b6-4d8c-9710-f31a1b8ab4c1" />
</div>
<br>
5. Saat pengguna memilih menu Cari Donor, program akan meminta input berupa nama atau kata kunci yang ingin dicari. Misalnya ketika pengguna mengetikkan “Zaina”, program akan menampilkan data donor dengan nama tersebut. Bahkan jika pengguna hanya memasukkan sebagian dari nama, seperti “Ina”, program tetap dapat menemukan data karena pencarian dilakukan menggunakan metode substring match pada nama donor. Dengan demikian, fitur ini memudahkan pengguna untuk menemukan data donor meskipun hanya mengetahui sebagian dari nama yang dicari.
<br>
<div align="center">
  <img width="636" height="329" alt="Screenshot 2025-09-23 215457" src="https://github.com/user-attachments/assets/d488ec02-ed8f-4c95-912b-2bb102e09bd3" />
</div>
<br>
<div align="center">
  <img width="623" height="337" alt="Screenshot 2025-09-23 215450" src="https://github.com/user-attachments/assets/bebc99bb-e332-4373-97df-a566cddb7231" />
</div>
<br>
6. Menu filter memberikan kesempatan bagi pengguna untuk menampilkan donor sesuai golongan darah tertentu. Program meminta input golongan darah, lalu menampilkan semua donor yang memiliki golongan darah tersebut. Jika tidak ada donor dengan golongan yang diminta, program akan menampilkan pesan bahwa data tidak tersedia.
<br>
<div align="center">
  <img width="671" height="325" alt="Screenshot 2025-09-23 215505" src="https://github.com/user-attachments/assets/c88b6429-24ad-4c2b-9999-6cc38888735e" />
</div>
<br>
<div align="center">
  <img width="660" height="335" alt="Screenshot 2025-09-23 215512" src="https://github.com/user-attachments/assets/e7aa8c2c-f15e-4ac6-9efe-e5b15b91c1f3" />
</div>
<br>
7. Selain data donor, program juga menampilkan data petugas melalui menu khusus. Data ini ditampilkan untuk memperlihatkan implementasi inheritance, di mana petugas merupakan subclass dengan atribut tambahan jabatan.
<br>
<div align="center">
  <img width="672" height="352" alt="Screenshot 2025-09-23 215519" src="https://github.com/user-attachments/assets/3ae8ebbf-ba38-495a-87f3-db0ba4ea8f91" />
</div>
<br>
8. Jika pengguna memilih menu keluar, program menampilkan pesan terima kasih lalu menghentikan seluruh proses. Dengan demikian, seluruh interaksi program berakhir dengan rapi.
<br>
<div align="center">
  <img width="857" height="367" alt="Screenshot 2025-09-23 215533" src="https://github.com/user-attachments/assets/dde7242c-3fb6-45bd-bacf-7864d1ea4457" />
</div>


# SOURCE CODE
    /*
     * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
     */
    
    package com.mycompany.donor;
    
    import java.util.ArrayList;
    import java.util.Scanner;
    
    class Person {
        private static int counter = 1;
        private final int id;
        private String nama;
        private int umur;
    
        public Person(String nama, int umur) {
            this.id = counter++;
            this.nama = nama;
            this.umur = umur;
        }
    
        // Getter & Setter (Encapsulation)
        public int getId() {
            return id;
        }
    
        public String getNama() {
            return nama;
        }
    
        public void setNama(String nama) {
            this.nama = nama;
        }
    
        public int getUmur() {
            return umur;
        }
    
        public void setUmur(int umur) {
            this.umur = umur;
        }
    
        // Method bisa dioverride di subclass
        public void tampilkanInfo() {
            System.out.println("ID: " + id + " | Nama: " + nama + " | Umur: " + umur);
        }
    }
    
    class Donor extends Person {
        private String golDarah;
    
        public Donor(String nama, int umur, String golDarah) {
            super(nama, umur);
            this.golDarah = golDarah;
        }
    
        public String getGolDarah() {
            return golDarah;
        }
    
        public void setGolDarah(String golDarah) {
            this.golDarah = golDarah;
        }
        
        @Override
        public void tampilkanInfo() {
            System.out.println("ID: " + getId() + " | Nama: " + getNama() +
                    " | Umur: " + getUmur() +
                    " | Golongan Darah: " + golDarah);
        }
    }
    
    class Petugas extends Person {
        private String jabatan;
    
        public Petugas(String nama, int umur, String jabatan) {
            super(nama, umur);
            this.jabatan = jabatan;
        }
    
        public String getJabatan() {
            return jabatan;
        }
    
        public void setJabatan(String jabatan) {
            this.jabatan = jabatan;
        }
    
        // Overriding method tampilkanInfo
        @Override
        public void tampilkanInfo() {
            System.out.println("ID: " + getId() + " | Nama: " + getNama() +
                    " | Umur: " + getUmur() +
                    " | Jabatan: " + jabatan);
        }
    }
    
    class DonorService {
        private final ArrayList<Donor> daftarDonor = new ArrayList<>();
        private final Scanner input = new Scanner(System.in);
    
        private boolean validasiUmur(int umur) {
            return umur >= 17;
        }
    
        private boolean validasiGolongan(String gol) {
            return gol.equalsIgnoreCase("A") ||
                   gol.equalsIgnoreCase("B") ||
                   gol.equalsIgnoreCase("AB") ||
                   gol.equalsIgnoreCase("O");
        }
    
        public void tambahDonor() {
            System.out.print("Masukkan Nama: ");
            String nama = input.nextLine();
    
            System.out.print("Masukkan Umur: ");
            int umur = input.nextInt();
            input.nextLine();
    
            if (!validasiUmur(umur)) {
                System.out.println("Umur minimal 17 tahun untuk donor!");
                return;
            }
    
            System.out.print("Masukkan Golongan Darah (A/B/AB/O): ");
            String gol = input.nextLine();
    
            if (!validasiGolongan(gol)) {
                System.out.println("Golongan darah tidak valid!");
                return;
            }
    
            daftarDonor.add(new Donor(nama, umur, gol.toUpperCase()));
            System.out.println("Data donor berhasil ditambahkan!");
        }
    
        public void tampilkanDonor() {
            System.out.println("\n=== Daftar Data Pendonor ===");
            if (daftarDonor.isEmpty()) {
                System.out.println("Belum ada data pendonor.");
            } else {
                for (Donor d : daftarDonor) {
                    d.tampilkanInfo(); // Polymorphism (Overriding)
                }
            }
        }
    
        public void updateDonor() {
            tampilkanDonor();
            if (daftarDonor.isEmpty()) return;
    
            System.out.print("Masukkan ID pendonor yang ingin diupdate: ");
            int id = input.nextInt();
            input.nextLine();
    
            Donor donor = cariDonorById(id);
            if (donor != null) {
                System.out.print("Masukkan Nama Baru: ");
                String namaBaru = input.nextLine();
                System.out.print("Masukkan Umur Baru: ");
                int umurBaru = input.nextInt();
                input.nextLine();
    
                if (!validasiUmur(umurBaru)) {
                    System.out.println("Umur minimal 17 tahun untuk donor!");
                    return;
                }
    
                System.out.print("Masukkan Golongan Darah Baru (A/B/AB/O): ");
                String golBaru = input.nextLine();
    
                if (!validasiGolongan(golBaru)) {
                    System.out.println("Golongan darah tidak valid!");
                    return;
                }
    
                donor.setNama(namaBaru);
                donor.setUmur(umurBaru);
                donor.setGolDarah(golBaru.toUpperCase());
    
                System.out.println("Data pendonor berhasil diupdate!");
            } else {
                System.out.println("Pendonor dengan ID tersebut tidak ditemukan!");
            }
        }
    
        public void hapusDonor() {
            tampilkanDonor();
            if (daftarDonor.isEmpty()) return;
    
            System.out.print("Masukkan ID pendonor yang ingin dihapus: ");
            int id = input.nextInt();
            input.nextLine();
    
            Donor donor = cariDonorById(id);
            if (donor != null) {
                daftarDonor.remove(donor);
                System.out.println("Data pendonor berhasil dihapus!");
            } else {
                System.out.println("Pendonor dengan ID tersebut tidak ditemukan!");
            }
        }
    
        public void cariDonor() {
            System.out.print("Masukkan Nama yang ingin dicari: ");
            String keyword = input.nextLine().toLowerCase();
    
            boolean ditemukan = false;
            for (Donor d : daftarDonor) {
                if (d.getNama().toLowerCase().contains(keyword)) {
                    d.tampilkanInfo();
                    ditemukan = true;
                }
            }
    
            if (!ditemukan) {
                System.out.println("Tidak ada pendonor dengan nama tersebut.");
            }
        }
    
        public void filterByGolongan() {
            System.out.print("Masukkan Golongan Darah yang ingin difilter (A/B/AB/O): ");
            String gol = input.nextLine().toUpperCase();
    
            if (!validasiGolongan(gol)) {
                System.out.println("Golongan darah tidak valid!");
                return;
            }
    
            boolean ditemukan = false;
            for (Donor d : daftarDonor) {
                if (d.getGolDarah().equalsIgnoreCase(gol)) {
                    d.tampilkanInfo();
                    ditemukan = true;
                }
            }
    
            if (!ditemukan) {
                System.out.println("Tidak ada pendonor dengan golongan darah " + gol);
            }
        }
    
        private Donor cariDonorById(int id) {
            for (Donor d : daftarDonor) {
                if (d.getId() == id) {
                    return d;
                }
            }
            return null;
        }
    }
    
    public class Main {
        public static void main(String[] args) {
            DonorService service = new DonorService();
            Scanner input = new Scanner(System.in);
            int pilihan;
    
            do {
                System.out.println("\n=== Sistem Informasi Manajemen Donor Darah ===");
                System.out.println("1. Tambah Data Donor");
                System.out.println("2. Tampilkan Semua Donor");
                System.out.println("3. Update Data Donor");
                System.out.println("4. Hapus Data Donor");
                System.out.println("5. Cari Pendonor berdasarkan Nama");
                System.out.println("6. Filter Pendonor berdasarkan Golongan Darah");
                System.out.println("7. Data Petugas");
                System.out.println("8. Keluar");
                System.out.print("Pilih menu: ");
                pilihan = input.nextInt();
                input.nextLine();
    
                switch (pilihan) {
                    case 1 -> service.tambahDonor();
                    case 2 -> service.tampilkanDonor();
                    case 3 -> service.updateDonor();
                    case 4 -> service.hapusDonor();
                    case 5 -> service.cariDonor();
                    case 6 -> service.filterByGolongan();
                    case 7 -> {
                        Petugas p = new Petugas("Siti Aminah", 35, "Dokter");
                        System.out.println("\n=== Data Petugas ===");
                        p.tampilkanInfo(); // Overriding berjalan
                    }
                    case 8 -> System.out.println("Terima kasih telah menggunakan program ini!");
                    default -> System.out.println("Pilihan tidak valid, coba lagi.");
                }
            } while (pilihan != 8);
        }
    }
