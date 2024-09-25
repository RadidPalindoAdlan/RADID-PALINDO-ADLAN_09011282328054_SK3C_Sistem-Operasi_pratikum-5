# RADID-PALINDO-ADLAN_09011282328054_SK3C_Sistem-Operasi_pratikum-5

<hr>

## 1. Eksekusi seluruh profile yang ada :
## a.Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :  
- echo “Profile dari /etc/profile” 
<img src="1a1.png" style="width:100"/>
<img src="1a.png" style="width:100"/>

## b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :  
- /home/stD02001/.bash_profile  
- /home/. stD02001/.bash_login  
- /home/mahasiswa/.profile  
- /home/mahasiswa/.bashrc  
## Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  
## file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  
- echo “Profile dari .bash_profile”  
## Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.  
<img src="1b.png" style="width:100"/>
<img src="1b1.png" style="width:100"/>
<img src="1b2.png" style="width:100"/>
<img src="1b3.png" style="width:100"/>
<img src="1b4.png" style="width:100"/>

## c.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:  
- $ su mahasiswa  
- $ exit  
## kemudian gunakan opsi – sebagai berikut :  
- $ su – mahasiswa  
- $ exit  
## Jelaskan perbedaan kedua utilitas tersebut.  
<img src="1c.png" style="width:100"/>

## 2.  Prompt String (PS)  
## a.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:  Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell  
- PS1=‟> „  
- export PS1
<img src="2a.png" style="width:100"/>
<img src="2a1.png" style="width:100"/>

## b. Eksperimen hasil PS1 : 
- $ PS1=“\! > “  
- 69 > PS1=”\d > “  
- Mon Sep 23 > PS1=”\t > “  
- 10:10:20 > PS1=”Saya=\u > “  
- Saya=mahasiswa > PS1=”\w >”  
- ~ > PS1=\h >”
<img src="2b.png" style="width:100"/>

## 3.  Logout  
## Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  
- Echo “Terima kasih atas sesi yang diberikan”  
- Sleep 5  
- clear
<img src="3.png" style="width:100"/>
<img src="3.1.png" style="width:100"/>

## 4.Bash script  
## a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
<img src="4a.png" style="width:100"/>

## p1.sh  
- #! /bin/bash  
- echo “Program p1”  
- ls –l
  
  <img src="4a1.png" style="width:100"/>
  
## p2.sh  
- #! /bin/bash  
- echo “Program p2”  
- who
- 
  <img src="4a2.png" style="width:100"/>
  
## p3.sh  
- #! /bin/bash  
- echo “Program p3”  
- ps x
  
  <img src="4a3.png" style="width:100"/>
  
## b.  Jalankan script tersebut sebagai berikut :  
- $  ./p1.sh ; ./p3.sh ; ./p2.sh
  <img src="4b1.png" style="width:100"/>
  
- $  ./p1.sh &
  <img src="4b2.png" style="width:100"/>
   
- $  ./p1.sh $ ./p2.sh & ./p3.sh &
  <img src="4b3.png" style="width:100"/>
  
- $  ( ./p1.sh ; ./p3.sh ) &
  <img src="4b4.png" style="width:100"/>

## 5. Jobs  
## a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.  
- #!/bin/bash  
- while [ true ]  
- do  
  - date >> hasil  
  - sleep 10  
- done
 <img src="5a.png" style="width:100"/>
 <img src="5a1.png" style="width:100"/>

  
## b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :  
- $ jobs  
- $ find / -print > files 2>/dev/null &  
- $ jobs  
 <img src="5b.png" style="width:100"/>


## c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background  
- $ fg %1  
- $ bg  
 <img src="5c.png" style="width:100"/>


## d.  Stop program background dengan utilitas kil  
- $ ps x  
 <img src="5d1.png" style="width:100"/>


- $ kill [Nomor PID] 
 <img src="5d2.png" style="width:100"/>


## 6. History  
## a. Ganti nilai HISTSIZE dari 1000 menjadi 20  
- $ HISTSIZE=20  
- $ h  
 <img src="6a.png" style="width:100"/>


## b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan  
- $ !-5  
<img src="6b.png" style="width:100"/>


## c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  
- $ !!  
<img src="6c.png" style="width:100"/>


## d.  Ulangi instruksi pada history bufer nomor 150  
- $ !150  
 <img src="6d.png" style="width:100"/>


## e.  Ulangi instruksi dengan prefix “ls”  
- $ !ls 
<img src="6e.png" style="width:100"/>
