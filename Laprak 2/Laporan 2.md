# <h1 align="center">Laporan Praktikum Modul X <br> Nama Modul</h1>
<p align="center"> Luthfi Maolana Andhika W - 103112430181 </p>

## Dasar Teori

Materi ini membahas array, pointer, fungsi, dan prosedur dalam C++. Array adalah struktur data untuk menyimpan banyak nilai dalam satu wadah dengan indeks sebagai pengaksesnya. Pointer adalah variabel yang menyimpan alamat dari variabel lain, termasuk elemen array. Fungsi adalah sub-program yang dapat digunakan kembali dan dapat menerima input serta menghasilkan output, seperti fungsi main(). Jika fungsi tidak memiliki input, sering disebut sebagai prosedur.

## Guided

### Soal 1 - Call By Pointer

```go
#include <iostream>
using namespace std;

void tukar(int *px, int *py)  // definisi fungsi
{
    int temp = *px;
    *px = *py;
    *py = temp;
}

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(&a, &b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}
```

> Output
> ![Screenshot bagian x](output/screenshot_soal1.png)
> %% Untuk mencantumkan screenshot, tidak boleh ada spasi di urlnya `()`, penamaan file bebas asal gak sara dan mudah dipahami aja,, dan jangan lupa hapus komen ini yah%%

Program tersebut menggunakan pointer sebagai parameter untuk menukar nilai dua variabel. Fungsi menerima *px dan *py sebagai alamat a dan b, lalu menggunakan temp untuk menukarnya. Di main, tukar(&a, &b) dipanggil agar nilai asli a dan b berubah, sehingga hasilnya tertukar.

### soal 2 - Call By Reference

```go
#include <iostream>
using namespace std;


void tukar(int &x, int &y)
{
    int temp = x;
    x = y;
    y = temp;
}

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(a, b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}
```

> Output
> ![Screenshot bagian x](output/screenshot_soal1.png)
> %% Untuk mencantumkan screenshot, tidak boleh ada spasi di urlnya `()`, penamaan file bebas asal gak sara dan mudah dipahami aja,, dan jangan lupa hapus komen ini yah%%

Program ini mirip dengan sebelumnya, tetapi menggunakan reference. Pada fungsi tukar(int &x, int &y), tanda & berarti variabel tersebut adalah referensi ke nilai asli, sehingga perubahan langsung mengubah variabel aslinya. Cara ini membuat pemanggilan lebih sederhana dibanding pointer.

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
