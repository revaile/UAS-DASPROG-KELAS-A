# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar pemerograman
<br> Nama		: Ade Ripaldi Nuralim
<br>NIM		:	1227050003
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
Array dua dimensi adalah sebutan untuk array yang penomoran index-nya menggunakan 2 buah angka. Analogi lain adalah matriks. Matrixs Merupakan kumpulan-kumpulan bilangan yang disusun secara baris (vertikal) dan kolom (horizontal) bisa disebut juga array dua dimensi (multi-dimensional). Transpose Matriks adalah memperoleh sebuah matriks dengan cara menukar baris menjadi kolom dan kolom menjadi baris dari sebuah matriks. Dalam matematika, matriks terdiri dari kolom dan baris. Kembali, untuk menentukan nilai dari sebuah matriks, kita harus sebut secara berpasangan seperti baris 1 kolom 1, atau baris 2 kolom 3, dst. Konsep seperti inilah yang menjadi dasar dari array 2 dimensi. Untuk membuat array 2 dimensi di dalam bahasa C++, caranya tulis 2 kali tanda kurung siku setelah nama variabel, seperti contoh berikut:
int arr[2][2];
Untuk UAS kali ini kami diminta membuat 2 buah program yaitu program pertama adalah membuat array 2 dimensi dengan baris , kolom dan nilai nya di input lalu ditukarkan antara kolom dan baris sedangkan program ke dua digunakan untuk mencari nilai yang dapat di bagi 3, 7, dan 5.

## Source Code
    #include <iostream>
    #include <conio.h>
    using namespace std;

    int main() {
        //nama dan nim
        cout<<"Ade Ripaldi Nuralim\n"
            <<"1227050003\n"
            <<"----------------------\n";
        //input banyaknya baris dan kolom
        int baris, kolom;
        cout << "Masukkan banyaknya baris: ";
        cin >> baris;
        cout << "Masukkan banyaknya kolom: ";
        cin >> kolom;

        // Membuat array 2 dimensi dengan banyaknya baris dan kolom yang diinput
        int arr[baris][kolom];
        int balik[kolom][baris];

        // Memasukkan data ke dalam array menggunakan loop
        for (int i = 0; i < baris; i++) {
            for (int j = 0; j < kolom; j++) {
                cout << "Masukkan elemen baris ke-" << i << " kolom ke-" << j << ": ";
                cin >> arr[i][j];
            }
        }

        // cetak isi dari array
        cout << "Isi dari array:" << endl;
        for (int i = 0; i < baris; i++) {
            for (int j = 0; j < kolom; j++) {
                cout << arr[i][j] << " ";
            }
            cout << endl;
        }
        for(int i = 0; i < baris; i++){
            for(int j = 0; j < kolom; j++){
                balik[j][i] = arr[i][j];
            }
        }
        // balik isi dari array
        cout << "balik Isi dari array:" << endl;
        for (int i = 0; i < kolom; i++) {
            for (int j = 0; j < baris; j++) {
                cout << balik[i][j] << " ";
            }
            cout << endl;
        }
        getch();
        return 0;
    }


## Output

<img width="244" alt="Cuplikan layar_20221221_110339" src="https://user-images.githubusercontent.com/118891086/208818933-c37dd92b-5e09-4bec-8577-cfefe6597196.png">

## Deskripsi Umum
UAS 2
## Source Code
    #include <iostream>
    #include <conio.h>
    using namespace std;

    int main() {
        // input banyaknya baris dan kolom
        cout<<"Ade Ripaldi Nuralim \n"
            <<"127050003\n"
            <<"----------------------\n";
        int baris, kolom;
        int arr[20][20];
        cout << "Masukkan banyaknya baris: ";cin >> baris;
        cout << "Masukkan banyaknya kolom: ";cin >> kolom;
        cout << "input nilai : "<<endl;
        for (int i = 0; i < baris; i++) {
            for (int j = 0; j < kolom; j++) {
                cout << "Masukkan elemen baris ke-" << i << " kolom ke-" << j << ": ";
                cin >> arr[i][j];
            }
        }
        cout << "Isi dari array:" << endl;
        for (int i = 0; i < baris; i++) {
            for (int j = 0; j < kolom; j++) {
                cout << arr[i][j] << " ";
            }
            cout << endl;

        }

        cout <<"hasil akhir: "<<endl;
        for (int i = 0; i < baris; i++) {
            for (int j = 0; j < kolom; j++) {
                if (arr[i][j] % 3 != 0 && arr[i][j] % 5 != 0 && arr[i][j] % 7 != 0) {
                    cout<<arr[i][j]<<" ";
                }
                else{

                }

            }
        }
        getch();
        return 0;
    }
    
 ## Output
 <img width="257" alt="Cuplikan layar_20221221_111327" src="https://user-images.githubusercontent.com/118891086/208819864-0aaf5b03-7888-4b9c-b35a-61359fec86bd.png">

