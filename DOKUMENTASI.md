# Post-Test-3-ASD

**1. MODUL**
![1](https://user-images.githubusercontent.com/125839542/225788966-7841ed6e-3a4d-40bd-b3e4-e38eb5820c1b.png)
Kode Python ini menggunakan modul os, time, dan prettytable untuk membuat tabel dengan header kolom yang sudah ditentukan. os.system('cls') digunakan untuk membersihkan layar terminal pada sistem operasi Windows. Objek tabel dari kelas PrettyTable dibuat dan header kolom ditentukan. Dokumentasi kode harus menjelaskan tujuan kode tersebut, modul dan kelas yang digunakan, penjelasan pada setiap baris kode dan variabel yang digunakan, serta contoh penggunaan kode tersebut.

**2. CLASS**
![2](https://user-images.githubusercontent.com/125839542/225789148-b18953a3-efd6-4408-a8c7-f73c87e25270.png)
Kode ini menggunakan implementasi dari kelas linkedList yang memiliki tiga atribut utama, yaitu head, history, dan Node. Kelas Node digunakan untuk mendefinisikan sebuah node dalam linked list, yang memiliki atribut-atribut seperti jam, tujuan, nomor, nextNode, dan prevNode. Atribut-atribut ini merepresentasikan informasi yang disimpan pada setiap node, seperti jam keberangkatan, tujuan perjalanan, dan nomor penerbangan. Kelas linkedList memiliki beberapa method yang akan dijelaskan sebagai berikut.

**3. VIEW**
![3](https://user-images.githubusercontent.com/125839542/225789495-d90e7a8e-52f8-4b38-9867-e6985953bfca.png)
Method view() digunakan untuk menampilkan informasi jadwal keberangkatan dalam bentuk tabel. Method ini memeriksa apakah linked list kosong atau tidak dengan memeriksa apakah atribut head berisi nilai atau tidak. Jika head kosong, maka method akan menampilkan pesan "JADWAL KOSONG". Jika head tidak kosong, method akan melakukan iterasi pada setiap node dalam linked list dan menambahkan informasi node tersebut ke dalam sebuah tabel menggunakan modul "prettytable". Setiap node akan ditambahkan ke dalam tabel sebagai sebuah baris dengan nomor urut, jam keberangkatan, tujuan perjalanan, dan nomor penerbangan. Setelah semua node ditambahkan ke dalam tabel, method akan menampilkan tabel ke layar dengan menggunakan fungsi get_string() dari modul prettytable.

**4. VIEWHISTORY**
![4](https://user-images.githubusercontent.com/125839542/225789665-cb0e3bee-c308-4b84-ab41-81da63bd4611.png)
Method viewHistory() berfungsi untuk menampilkan riwayat perubahan pada linked list yang disimpan dalam atribut history. Pertama, method memeriksa apakah atribut history berisi nilai atau tidak. Jika history kosong, maka method akan menampilkan pesan "HISTORI KOSONG". Jika tidak kosong, method akan membuat sebuah objek tabel menggunakan modul prettytable untuk menampilkan setiap riwayat perubahan. Kemudian, method melakukan iterasi pada setiap elemen dalam history dan menambahkan setiap riwayat ke dalam tabel sebagai sebuah baris dengan nomor urut. Setelah semua riwayat ditambahkan ke dalam tabel, method menampilkan tabel ke layar dengan menggunakan fungsi print(). Agar isi tabel tampil dengan rapi, method menggunakan fungsi align() untuk mengatur penjajaran kolom menjadi rata kiri.

**5. ADDFIRST**
![5](https://user-images.githubusercontent.com/125839542/225789792-1bc0ec65-3e21-479d-b653-ef8ef33cf87d.png)
Method addFirst() berfungsi untuk menambahkan sebuah node baru di awal linked list. Pertama, method menambahkan riwayat penambahan node baru ke dalam atribut history dengan format "Menambah | jam | tujuan | nomor | di awal list", di mana nilai jam, tujuan, dan nomor adalah parameter yang diberikan. Kemudian, method membuat sebuah objek newNode dengan menggunakan class Node dan memberikan nilai parameter jam, tujuan, dan nomor sebagai atribut dari objek tersebut. Jika head kosong, maka method akan menjadikan newNode sebagai head. Jika head tidak kosong, maka method akan menambahkan newNode ke awal linked list dengan mengatur next node dari newNode menjadi head dan prev node dari head menjadi newNode, lalu menjadikan newNode sebagai head baru.

**6. ADDEND**
![6](https://user-images.githubusercontent.com/125839542/225789867-95d18e0c-5f06-4227-93b4-a4cf47c54238.png)
Method addEnd() berfungsi untuk menambahkan sebuah node baru di akhir linked list. Pertama, method menambahkan riwayat penambahan node baru ke dalam atribut history dengan format "Menambah | jam | tujuan | nomor | di akhir list", di mana nilai jam, tujuan, dan nomor adalah parameter yang diberikan. Kemudian, method membuat sebuah objek newNode dengan menggunakan class Node dan memberikan nilai parameter jam, tujuan, dan nomor sebagai atribut dari objek tersebut. Jika head kosong, maka method akan memanggil method addFirst() untuk menambahkan newNode sebagai head. Jika head tidak kosong, maka method akan mencari node terakhir dalam linked list dengan melakukan iterasi pada setiap node dari head hingga node terakhir, kemudian menambahkan newNode sebagai node selanjutnya dari node terakhir dan mengatur prev node dari newNode menjadi node terakhir tersebut.

**7. UPDATE**
![7](https://user-images.githubusercontent.com/125839542/225790042-ed36184d-5af7-441a-96db-ee1211815862.png)
![7 2](https://user-images.githubusercontent.com/125839542/225790087-f1c7142c-1ec7-4d10-9bec-efda1cdda143.png)
![7 3](https://user-images.githubusercontent.com/125839542/225790109-14765131-79a3-4e0c-9d72-43dfe8de14c3.png)
![7 4](https://user-images.githubusercontent.com/125839542/225790127-7bcc3b22-17d7-4e83-9356-dbc141ccfdc8.png)
Method Update berfungsi untuk mengubah nilai atribut jam, tujuan, atau nomor kereta pada node tertentu dalam linked list. Method menerima dua parameter, yaitu position yang menentukan posisi node yang akan diubah (dimulai dari 1) dan newValue yang merupakan nilai baru. Pertama, method menginisialisasi pointer dengan head dan melakukan iterasi pada setiap node dari head hingga node yang memiliki nomor urut sesuai dengan parameter position. Jika pointer telah mencapai node dengan nomor urut position, maka method akan mengubah nilai atribut dari node tersebut dengan nilai newValue dan menambahkan riwayat perubahan ke dalam atribut history dengan format "Mengubah atribut | nialilama | menjadi | nilai baru |". Jika pointer tidak menemukan node dengan nomor urut position, maka method akan mencetak pesan kesalahan dan mengembalikan nilai 0. Jika pointer telah mengubah nilai atribut jam pada node yang tepat, maka method akan mencetak pesan berhasil dan mengembalikan nilai 1.

**8. DELETE**
![8](https://user-images.githubusercontent.com/125839542/225790401-11dddc6e-2860-404a-8185-c6df49a3aa87.png)
Method delete() menghapus data pada sebuah linked list yang disimpan dalam sebuah class. Fungsi delete() ini menerima sebuah parameter position yang menunjukkan posisi node yang akan dihapus dari linked list. Jika linked list masih kosong, maka akan ditampilkan pesan "JADWAL KOSONG". Jika posisi yang diberikan adalah 1, maka node pertama akan dihapus. Selain itu, program akan mencari node pada posisi yang diberikan dan menghapusnya. Setelah node dihapus, program akan menambahkan sebuah riwayat baru ke dalam atribut history berupa string yang berisi informasi tentang node yang dihapus. Akhirnya, fungsi ini akan mengembalikan nilai 1 jika node berhasil dihapus, dan 0 jika tidak.

**9. MENAMBAH ISI LIST**
![9](https://user-images.githubusercontent.com/125839542/225790562-a332ec47-6c70-4327-b1e1-33354c536ff0.png)
Saat dijalankan, program langsung menjalankan kode diatas yang melakukan penambahan ini dari list dengan tribut-atribut tersebut.

**10. MAIN()**
![10](https://user-images.githubusercontent.com/125839542/225790839-70d9de0a-d8a0-4d21-b185-dd8b5e3ce03a.png)
Fungsi main() digunakan sebagai menu pilihan untuk mengakses fitur-fitur program. Setelah menampilkan menu, program akan meminta input dari user untuk memilih fitur yang diinginkan. Jika input yang dimasukkan tidak valid, program akan mencetak pesan "Pilih dari pilihan yang tersedia" dan meminta input ulang hingga input yang valid dimasukkan.

**11. OPSI 1**
![11](https://user-images.githubusercontent.com/125839542/225791022-106ebd7a-d5e0-436b-92e8-953d9a406524.png)
Jika pengguna memilih opsi 1, maka program akan menampilkan pesan "Memproses...", kemudian program akan berjeda selama 1 detik menggunakan fungsi time.sleep(1). Setelah itu, layar konsol akan dibersihkan dengan menggunakan perintah os.system('cls'), kemudian program akan menampilkan judul "JADWAL KEBERANGKATAN KERETA" dan menampilkan seluruh data jadwal keberangkatan yang tersimpan dalam linked list mylist dengan menggunakan fungsi mylist.view().

**12. OPSI 2**
![12](https://user-images.githubusercontent.com/125839542/225791086-31136cd2-3bd8-4de7-a898-babceae132c7.png)
Jika pengguna memilih opsi 2, maka program akan menampilkan pesan "Memproses..." dan menunggu selama satu detik, tampilan konsol dikosongkan menggunakan fungsi os.system('cls'). Kemudian, pilihan "MENAMBAHKAN JADWAL KEBERANGKATAN" dan daftar jadwal saat ini ditampilkan menggunakan mylist.view(). Selanjutnya, pengguna diminta untuk memasukkan informasi jadwal keberangkatan yang baru, yaitu jam keberangkatan, tujuan, dan nomor kereta menggunakan input(). Data jadwal baru kemudian ditambahkan ke awal linked list menggunakan mylist.addFirst(). Akhirnya, data jadwal yang baru ditampilkan kembali menggunakan mylist.view().

**13. OPSI 3**
![13](https://user-images.githubusercontent.com/125839542/225791195-990d1871-38b0-412f-821b-f4a864e3a3ad.png)
Setelah opsi nomor 3 dipilih, maka program akan menampilkan pesan "Memproses...", kemudian akan menunggu selama 1 detik dengan menggunakan fungsi time.sleep(1). Setelah itu, program akan menampilkan jadwal keberangkatan kereta dengan menggunakan fungsi mylist.view(). Kemudian program akan menampilkan pesan "Data akan ditambahkan pada No.(nomor terakhir + 1)", dan akan meminta pengguna memasukkan jam keberangkatan, tujuan, dan nomor kereta. Data baru akan ditambahkan ke dalam linked list pada posisi terakhir menggunakan fungsi mylist.addEnd(arv, des, num), dan program akan menampilkan pesan "Data telah ditambahkan" diikuti dengan jadwal keberangkatan kereta yang baru saja diperbarui menggunakan fungsi mylist.view().

**14. OPSI 4**
![14](https://user-images.githubusercontent.com/125839542/225791535-c5fa4759-2fb2-4e1c-932c-83a9896f4917.png)
Jika pengguna memilih opsi 4 pada menu utama, maka program akan menampilkan pilihan untuk memperbarui jam keberangkatan, tujuan keberangkatan, atau nomor kereta. Setelah pengguna memilih opsi yang diinginkan, program akan menampilkan daftar jadwal keberangkatan yang tersedia dan meminta pengguna untuk memilih nomor urut jadwal yang akan diperbarui. Selanjutnya, program akan meminta pengguna untuk memasukkan data baru untuk jadwal keberangkatan yang dipilih dan mengkonfirmasi pembaruan tersebut. Akhirnya, program akan menampilkan daftar jadwal keberangkatan yang telah diperbarui.

**15. OPSI 5**
![15](https://user-images.githubusercontent.com/125839542/225791611-d0a9f2e9-2c0c-48fb-8290-81e44125aa24.png)
Pada opsi 5, program akan menampilkan daftar jadwal keberangkatan yang sudah ada dan meminta pengguna untuk memasukkan nomor urut dari jadwal yang ingin dihapus. Jika nomor urut yang dimasukkan oleh pengguna terdapat pada daftar, program akan menghapus jadwal tersebut dan menampilkan daftar jadwal yang baru. Namun, jika nomor urut yang dimasukkan tidak ditemukan, program akan menampilkan pesan error dan meminta pengguna untuk mencoba lagi.

**16. OPSI 6**
![16](https://user-images.githubusercontent.com/125839542/225791715-6b16dac2-cd5b-4157-b715-84e2636df354.png)
Saat pengguna memilih opsi 6, program akan menampilkan pesan "Memproses..." dan menunggu selama 1 detik sebelum menampilkan pesan "HISTORI PERUBAHAN TERHADAP JADWAL". Kemudian, program akan menampilkan histori perubahan tersebut dengan memanggil fungsi viewHistory dari objek mylist.









