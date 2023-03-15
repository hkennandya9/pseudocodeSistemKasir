Nama 				: Hafizh Kennandya Maulana</br>
ID Camp 		: FE4593655</br>
Kelas		 		: FE-2</br>
Referensi Aplikasi	: Sistem Kasir</br>
Menu 				: Memasukan item dan auto calculate total harga</br>

> PROGRAM SistemKasir</br>

> STORE "total" WITH NUMBER 0</br>
> STORE "input" WITH BOOLEAN TRUE</br>

> STORE "count" WITH NUMBER 0</br>
> WHILE "input"</br>
>> DO
>> READ AND WRITE "item["count"]["name"]" WITH STRING</br>
>> READ AND WRITE "item["count"]["price"]" WITH NUMBER</br>
>> STORE "total" WITH CALCULATE "total" PLUS "item["count"]["price"]"</br>
>> WRITE "input" WITH BOOLEAN</br>
>> STORE "count" WITH "count" PLUS 1</br>

> PRINT "total"</br>
