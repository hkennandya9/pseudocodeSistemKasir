Nama 				: Hafizh Kennandya Maulana</br>
ID Camp 		: FE4593655</br>
Kelas		 		: FE-2</br>
Referensi Aplikasi	: Sistem Kasir</br>
Menu 				: Memasukan item dan auto calculate total harga</br>

PROGRAM SistemKasir

STORE "total" WITH NUMBER 0
STORE "input" WITH BOOLEAN TRUE

STORE "count" WITH NUMBER 0
WHILE "input"
	DO
	READ AND WRITE "item["count"]["name"]" WITH STRING
	READ AND WRITE "item["count"]["price"]" WITH NUMBER
	STORE "total" WITH CALCULATE "total" PLUS "item["count"]["price"]"
	WRITE "input" WITH BOOLEAN
	STORE "count" WITH "count" PLUS 1

PRINT "total"
