Nama 				: Hafizh Kennandya Maulana
ID Camp 			: FE4593655
Kelas		 		: FE-2
Referensi Aplikasi	: Sistem Kasir
Menu 				: Memasukan item dan auto calculate total harga

PROGRAM SistemKasir

STORE "total" WITH NUMBER 0									// Variabel integer untuk menampung total harga item
STORE "input" WITH BOOLEAN TRUE								// Variabel boolean penentu untuk menambahkan item

STORE "count" WITH NUMBER 0									// Variabel integer untuk index di dalam looping dan menghitung banyaknya item
WHILE "input"
	DO
	READ AND WRITE "item["count"]["name"]" WITH STRING				// Memasukkan nama item pada array item ke-i dengan tipe data string
	READ AND WRITE "item["count"]["price"]" WITH NUMBER				// Memasukkan harga item pada array item ke-i dengan tipe data number
	STORE "total" WITH CALCULATE "total" PLUS "item["count"]["price"]"	// Menghitung total harga item
	WRITE "input" WITH BOOLEAN								// Memasukkan penentu untuk menambahkan item, true (tambah item) atau false (tidak tambah item)
	STORE "count" WITH "count" PLUS 1							// Melakukan penambahan index untuk penunjuk ke item berikutnya

PRINT "total"											// Menampilkan total harga item
