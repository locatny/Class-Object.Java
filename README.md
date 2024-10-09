# Class-Object.Java
# Latihan1
![](DiagramPerson,Drawio).png
# Latihan2
# Person.Java
package com.mycompany.classobject;

// Deklarasi class Person
public class Person {
    // Atribut dari class Person
    private final String nama;
    private final String jenisKelamin;
    private final int umur;

    // Konstruktor untuk inisialisasi objek
    public Person(String nama, String jenisKelamin, int umur) {
        this.nama = nama;
        this.jenisKelamin = jenisKelamin;
        this.umur = umur;
    }

    // Method untuk menampilkan informasi objek
    public void tampilkanInfo() {
        System.out.println("Nama: " + this.nama);
        System.out.println("Jenis Kelamin: " + this.jenisKelamin);
        System.out.println("Umur: " + this.umur);
    }
}

# Main.Java

import com.mycompany.classobject.Person;

public class Main {
    public static void main(String[] args) {
        // Membuat objek Anton dan Riko dari class Person
        Person anton = new Person("Anton", "Laki-laki", 20);
        Person riko = new Person("Riko", "Laki-laki", 35);

        // Menampilkan informasi dari masing-masing objek
        System.out.println("Informasi Anton:");
        anton.tampilkanInfo();

        System.out.println("\nInformasi Riko:");
        riko.tampilkanInfo();
    }
}

# Latihan3
# AkunBank.Java
package com.mycompany.bankapp;

// Deklarasi class AkunBank
public class AkunBank {
    // Atribut untuk menyimpan saldo
    private int saldo;

    // Konstruktor untuk inisialisasi saldo awal
    public AkunBank(int saldoAwal) {
        this.saldo = saldoAwal;
    }

    // Method untuk menyimpan uang
    public void simpanUang(int jumlah) {
        saldo += jumlah;
        System.out.println("Simpan uang: Rp. " + jumlah);
    }

    // Method untuk mengambil uang
    public void ambilUang(int jumlah) {
        if (jumlah <= saldo) {
            saldo -= jumlah;
            System.out.println("Ambil uang: Rp. " + jumlah);
        } else {
            System.out.println("Saldo tidak mencukupi untuk penarikan.");
        }
    }

    // Method untuk cek saldo
    public void cekSaldo() {
        System.out.println("Saldo saat ini: Rp. " + saldo);
    }
}

# Main.Java

import com.mycompany.bankapp.AkunBank;

public class Main {
    public static void main(String[] args) {
        // Menampilkan pesan selamat datang
        System.out.println("Selamat Datang di Bank ABC");

        // Membuat objek AkunBank dengan saldo awal Rp. 100000
        AkunBank akunSaya = new AkunBank(100000);

        // Mengecek saldo awal
        akunSaya.cekSaldo();

        // Simpan uang sebesar Rp. 500000
        akunSaya.simpanUang(500000);

        // Mengecek saldo setelah menyimpan uang
        akunSaya.cekSaldo();

        // Ambil uang sebesar Rp. 150000
        akunSaya.ambilUang(150000);

        // Mengecek saldo setelah mengambil uang
        akunSaya.cekSaldo();
    }
}

