
# <h1 align="center">Laporan Praktikum Modul X <br> Single Linked List 2</h1>
<p align="center"> Luthfi Maolana Andhika W - 103112430181 </p>

## Dasar Teori

Pada materi ini menjelaskan tentang Singly linked list terutama searching dalam singly Linked List. Penelusuran daftar tertaut biasanya dilakukan untuk mencari simpul tertentu, dan membaca atau mengubah konten simpul, menghapus simpul, atau menyisipkan simpul tepat sebelum atau sesudah simpul tersebut.

## Unguided

### Soal 1

```go
#include <iostream>

using namespace std;

struct Buku{

  string judul, pengarang;
  int tahunTerbit;

  Buku *next;

};

Buku *head, *tail, *cur, *newNode, *del, *before;

void createSingleLinkedList(string judul, string pengarang, int tB){
  head = new Buku();
  head->judul = judul;
  head->pengarang = pengarang;
  head->tahunTerbit = tB;
  head->next = NULL;
  tail = head;
}


int countSingleLinkedList(){
  cur = head;
  int jumlah = 0;
  while( cur != NULL ){
    jumlah++;
    cur = cur->next;
  }
  return jumlah;
}

void addFirst(string judul, string pengarang, int tB){
  newNode = new Buku();
  newNode->judul = judul;
  newNode->pengarang = pengarang;
  newNode->tahunTerbit = tB;
  newNode->next = head;
  head = newNode;
}

void addLast(string judul, string pengarang, int tB){
  newNode = new Buku();
  newNode->judul = judul;
  newNode->pengarang = pengarang;
  newNode->tahunTerbit = tB;
  newNode->next = NULL;
  tail->next = newNode;
  tail = newNode;
}

void addMiddle(string judul, string pengarang, int tB, int posisi){
  if( posisi < 1 || posisi > countSingleLinkedList() ){
    cout << "Posisi diluar jangkauan" << endl;
  }else if( posisi == 1){
    cout << "Posisi bukan posisi tengah" << endl;
  }else{
    newNode = new Buku();
    newNode->judul = judul;
    newNode->pengarang = pengarang;
    newNode->tahunTerbit = tB;

    cur = head;
    int nomor = 1;
    while( nomor < posisi - 1 ){
      cur = cur->next;
      nomor++;
    }
    newNode->next = cur->next;
    cur->next = newNode;
  }
}


void removeFirst(){
  del = head;
  head = head->next;
  delete del;
}

void removeLast(){
  del = tail;
  cur = head;
  while( cur->next != tail ){
    cur = cur->next;
  }
  tail = cur;
  tail->next = NULL;
  delete del;
}

void removeMiddle(int posisi){
  if( posisi < 1 || posisi > countSingleLinkedList() ){
    cout << "Posisi diluar jangkauan" << endl;
  }else if( posisi == 1){
    cout << "Posisi bukan posisi tengah" << endl;
  }else{
    int nomor = 1;
    cur = head;
    while( nomor <= posisi ){
      if( nomor == posisi-1 ){
        before = cur;
      }
      if( nomor == posisi ){
        del = cur;
      }
      cur = cur->next;
      nomor++;
    }
    before->next = cur;
    delete del;
  }
}

void changeFirst(string judul, string pengarang, int tB){
  head->judul = judul;
  head->pengarang = pengarang;
  head->tahunTerbit = tB;
}

void changeLast(string judul, string pengarang, int tB){
  tail->judul = judul;
  tail->pengarang = pengarang;
  tail->tahunTerbit = tB;
}

void changeMiddle(string judul, string pengarang, int tB, int posisi){
  if( posisi < 1 || posisi > countSingleLinkedList() ){
    cout << "Posisi diluar jangkauan" << endl;
  }else if( posisi == 1 || posisi == countSingleLinkedList() ){
    cout << "Posisi bukan posisi tengah" << endl;
  }else{
    cur = head;
    int nomor = 1;
    while( nomor < posisi ){
      cur = cur->next;
      nomor++;
    }
    cur->judul = judul;
    cur->pengarang = pengarang;
    cur->tahunTerbit = tB;
  }
}

void printSingleLinkedList(){
  cout << "Jumlah data ada : " << countSingleLinkedList() << endl;
  cur = head;
  while( cur != NULL ){
    cout << "Judul Buku : " << cur->judul << endl;
    cout << "Pengarang Buku : " << cur->pengarang << endl;
    cout << "Tahun Terbit Buku : " << cur->tahunTerbit << endl;

    cur = cur->next;
  }
}

int main(){

  createSingleLinkedList("Kata", "Geez & Aan", 2018);

  printSingleLinkedList();

  cout << "\n\n" << endl;

  addFirst("Dia adalah Kakakku", "Tere Liye", 2009);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  addLast("Aroma Karsa", "Dee Lestari", 2018);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  removeFirst();

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  addLast("11.11", "Fiersa Besari", 2018);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  removeLast();

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  changeFirst("Berhenti di Kamu", "Gia Pratama", 2018);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  addMiddle("Bumi Manusia", "Pramoedya Anata Toer", 2005, 2);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  addMiddle("Negeri 5 Menara", "Ahmad Fuadi", 2009, 2);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  removeMiddle(5);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

  changeMiddle("Sang Pemimpi", "Andrea Hirata", 2006, 2);

  printSingleLinkedList();
  
  cout << "\n\n" << endl;

}
```

> ![foto](foto/UG1.png)

Program ini membuat dan mengelola single linked list berisi data buku, lalu di main() dilakukan serangkaian operasi seperti menambah buku di awal, tengah, atau akhir; menghapus buku pertama, terakhir, atau posisi tertentu; mengubah data buku; serta mencetak seluruh isi list setelah setiap operasi, sehingga setiap langkah perubahan pada linked list bisa terlihat hasilnya.

## Referensi

1. https://youtu.be/VVemCxif9vg?si=fB6hGUa7R2x5Dx1k (diakses 8 Desember 2025)
