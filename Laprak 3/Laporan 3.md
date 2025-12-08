# <h1 align="center">Laporan Praktikum Modul X <br> ABSTARCT DATA TYPE</h1>
<p align="center"> Luthfi Maolana Andhika W - 103112430181 </p>

## Dasar Teori

Abstract data type adalah sebuah model dari tipe data yang ditentukan dalam sudut pandang pengguna. adt menjelaskan apa yang dilakukan oleh tipe data. Komponen utama ADT ada dua yaitu data yang akan disimpan dan operasinya. Contoh ADT umum adalah Stack(pop,peek,isEmpty,isFull), Queue, List, Tree, Map/Dictionary

## Guided

### soal 1

File MAHASISWA_H_INCLUDED berfungsi sebagai kontrak (interface) untuk modul mahasiswa dalam program C++, dilindungi oleh header guard untuk mencegah pendefinisian ganda. File ini mendefinisikan struktur data mahasiswa yang terdiri dari NIM (char nim[10]), dan dua nilai integer (nilai1 dan nilai2). Selain struktur, file ini mendeklarasikan dua prototipe fungsi: void inputMhs(mahasiswa &m) yang memungkinkan pengguna mengisi data mahasiswa (menggunakan referensi untuk memodifikasi objek), dan float rata2(mahasiswa m) yang bertugas menghitung dan mengembalikan hasil rata-rata dari kedua nilai tersebut dalam tipe data floating point.

```go
#ifndef MAHASISWA_H_INCLUDED
#define MAHASISWA_H_INCLUDED

struct mahasiswa
{
 char nim[10];
 int nilai1, nilai2;
};

void inputMhs(mahasiswa &m);
float rata2(mahasiswa m);

#endif

////////////////////////////////////////////////////////////////////////////////////////////////////////

#include "mahasiswa.h"
#include <iostream>
using namespace std;

void inputMhs(mahasiswa &m)
{
cout << "input nama = ";
cin >> (m) .nim;
cout << "input nilai = ";
cin >> (m) .nilai1;
cout << "input niali2 = ";
cin >> m .nilai2;

}
float rata2(mahasiswa m)
{
return float(m.nilai1 + m.nilai2) / 2;
}

```

> Output
> ![foto](foto/Guided1.png)

Penjelasan ttg kode kalian disini




## Unguided

### Soal 1

copy paste soal nomor 1 disini

```go
package main

func main() {
	fmt.Println("Kode kalian disini")
	fmt.Println("JANGAN MASUKIN >>SCREENSHOT<< KODE KALIAN DISINI")
	fmt.Println("KALAU ADA -20 POIN LAPRAK")
}
```

> Output
> ![Screenshot bagian x](output/screenshot_soal1.png)
> %% Untuk mencantumkan screenshot, tidak boleh ada spasi di urlnya `()`, penamaan file bebas asal gak sara dan mudah dipahami aja,, dan jangan lupa hapus komen ini yah%%

Penjelasan ttg kode kalian disini

### Soal 2

soal nomor 2A

```go
package main

func main() {
	fmt.Println("kode untuk soal nomor 2A")
}
```

> Output
> ![Screenshot bagian x](output/screenshot_soal2A.png)

penjelasan kode

Kalau adalanjutan di lanjut disini aja

soal nomor 2B

```go
package main

func main() {
	fmt.Println("kode untuk soal nomor 2B")
}
```

> Output
> ![Screenshot bagian x](output/screenshot_soal2B.png)

penjelasan bedanya sesuai soal

## Referensi

1. https://en.wikipedia.org/wiki/Data_structure (diakses blablabla)
