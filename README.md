# studycase1_124250196.cpp
no 1. 
#include <iostream>
#include <string>
using namespace std;

struct Buku {
    string nama;
    int harga;
};

int main() {
    Buku daftarBuku[5] = {
        {"Algoritma", 75000},
        {"BasisData", 85000},
        {"Jaringan", 90000},
        {"Pemrograman", 80000},
        {"StrukturData", 95000}
    };

    string cari;
    bool ditemukan = false;

    cout << "Masukkan nama buku yang dicari: ";
    cin >> cari;

    for(int i = 0; i < 5; i++) {
        if(daftarBuku[i].nama == cari) {
            cout << "Harga buku: " << daftarBuku[i].harga << endl;
            ditemukan = true;
            break;
        }
    }

    if(!ditemukan) {
        cout << "Buku tidak ditemukan." << endl;
    }

    return 0;
}


no 2. 
#include <iostream>
using namespace std;

struct Buku {
    string nama;
    int harga;
};

int main() {
    Buku daftarBuku[5] = {
        {"Algoritma", 75000},
        {"BasisData", 85000},
        {"Jaringan", 90000},
        {"Pemrograman", 80000},
        {"StrukturData", 95000}
    };

    string cari;
    int awal = 0, akhir = 4, tengah;
    bool ditemukan = false;

    cout << "Masukkan nama buku yang dicari: ";
    cin >> cari;

    while(awal <= akhir) {
        tengah = (awal + akhir) / 2;

        if(daftarBuku[tengah].nama == cari) {
            cout << "Harga buku: " << daftarBuku[tengah].harga << endl;
            ditemukan = true;
            break;
        }
        else if(cari < daftarBuku[tengah].nama) {
            akhir = tengah - 1;
        }
        else {
            awal = tengah + 1;
        }
    }

    if(!ditemukan) {
        cout << "Buku tidak ditemukan." << endl;
    }

    return 0;
}
