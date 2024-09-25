# Nama  : Ahmad Perdana
# NIM   : 09011282328023
# Kelas : SK3B

# TUGAS PRAKTIKUM 5 Job Control

## 1. Eksekusi seluruh profile yang ada : 
## a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : 
### echo “Profile dari /etc/profile” 
![1 B](https://github.com/user-attachments/assets/0d16d214-9308-4edb-bf81-4db0491f7f8e)

## b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : 
### /home/stD02001/.bash_profile 
### /home/. stD02001/.bash_login 
### /home/mahasiswa/.profile 
### /home/mahasiswa/.bashrc
![image](https://github.com/user-attachments/assets/19658130-4eae-450f-bd26-37828bb2f924)

## c.Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: 
### $ su mahasiswa 
### $ exit 
## kemudian gunakan opsi – sebagai berikut : 
### $ su – mahasiswa 
### $ exit 
## Jelaskan perbedaan kedua utilitas tersebut. 
![image](https://github.com/user-attachments/assets/7b8d2b2b-3024-4ff4-97ac-b22da371f34a)
### perbedaan antara su - dan su 
### su mahasiswa: Berpindah ke pengguna "mahasiswa" tanpa mengubah lingkungan.
## su - mahasiswa: Berpindah ke pengguna "mahasiswa" dan mengubah ke lingkungan pengguna tersebut secara penuh.


## 2.Prompt String (PS) 
## a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell
![image](https://github.com/user-attachments/assets/e468827b-1041-4aa4-b04e-93ec6f1463a9)

## b. Eksperimen hasil PS1 : 
![image](https://github.com/user-attachments/assets/a77e64c8-880f-4861-b0a3-4553f8d76fa0)

## 3 Logout 
### Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout 
### Echo “Terima kasih atas sesi yang diberikan”
### Sleep 5 
![image](https://github.com/user-attachments/assets/febe5e89-82bb-4f23-8830-4201c552669b)

## 4  Bash script 
## a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : 
### p1.sh 
### #! /bin/bash 
### echo “Program p1” 
### ls –l 
### p2.sh 
### #! /bin/bash 
### echo “Program p2” 
### who 
### p3.sh 
### #! /bin/bash 
### echo “Program p3” 
### ps x
![image](https://github.com/user-attachments/assets/7e1dd684-071b-42fe-afcb-37bbecb26c7b)

## b. Jalankan script tersebut sebagai berikut : 

### $ ./p1.sh ; ./p3.sh ; ./p2.sh 
![4b](https://github.com/user-attachments/assets/90c8e7c3-df85-4d1c-b7e4-a9df90de0aaa) 
### $ ./p1.sh & 
![4b2](https://github.com/user-attachments/assets/168c9f26-6ae4-4797-b45e-69b232c1479b)
### $ ./p1.sh $ ./p2.sh & ./p3.sh & 
![4b3](https://github.com/user-attachments/assets/70bd097c-8aaf-40ff-b9be-2f821fa6a999)
### $ ( ./p1.sh ; ./p3.sh ) &
![4b4](https://github.com/user-attachments/assets/55aedd62-f6b4-46e5-95a8-a140f2ab67ab)

## 5.Jobs 
### a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. 
### #!/bin/bash 
### while [ true ] 
### do 
### date >> hasil 
### sleep 10 
### done
![5a](https://github.com/user-attachments/assets/73b7ef58-8dbb-4411-96b4-3f8ef03ec557)

## b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut : 
### $ jobs 
### $ find / -print > files 2>/dev/null & 
### $ jobs
![5b](https://github.com/user-attachments/assets/9592cf29-49d8-472c-bff0-80777bb15a5d)

## c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background 
### $ fg %1 
### $ bg 
![5c](https://github.com/user-attachments/assets/c05041ae-bf62-40c4-8e66-08d0543cc306)


## d. Stop program background dengan utilitas kil 
### $ ps x 
### $ kill [Nomor PID] 
![5d](https://github.com/user-attachments/assets/f2eccb04-1ab6-4e87-9d3a-f8cd886c13be)


## 6. History 
## a. Ganti nilai HISTSIZE dari 1000 menjadi 20 
### $ HISTSIZE=20 
### $ h 
!-![image](https://github.com/user-attachments/assets/c37b5e73-346d-47b0-af9b-dbbf97dfbf6f)

## b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan 
### $ !-5 
![image](https://github.com/user-attachments/assets/d30e0d46-ef2e-42aa-8259-e81ff3f17654)

## c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer 
### $ !! 
![image](https://github.com/user-attachments/assets/af77405e-6434-4006-be8e-57e0b28165c4)

## d. Ulangi instruksi pada history bufer nomor 150 
### $ !150 
![image](https://github.com/user-attachments/assets/30539783-eea3-4a61-ac35-bafd23eb6ed0)

## e. Ulangi instruksi dengan prefix “ls” 
### $ !ls
![image](https://github.com/user-attachments/assets/59bdc47f-3782-43c0-b223-c160d294c9a9)
