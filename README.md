# tugas-6-job-control
VI. Tugas 
## 1. Eksekusi seluruh profile yang ada : 
### a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : echo “Profile dari /etc/profile” 
<img width="664" height="453" alt="pk5 1a" src="https://github.com/user-attachments/assets/3bc83cf5-5f0f-4939-b551-3b954c940beb" />
<img width="684" height="466" alt="pk5 1aa" src="https://github.com/user-attachments/assets/905c5f0f-98f7-4f90-a7d3-1548564a14c2" />

### b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : 
#### /home/stD02001/.bash_profile 
#### /home/. stD02001/.bash_login 
#### /home/mahasiswa/.profile   
#### /home/mahasiswa/.bashrc 
<img width="696" height="475" alt="pk5 1bb" src="https://github.com/user-attachments/assets/4fc4e2f4-b9bb-4386-b2e1-d59e9a2e8315" />
<img width="671" height="442" alt="pk5 1b" src="https://github.com/user-attachments/assets/d08a3058-c15f-406c-a7fa-687faf14f81b" />
<img width="681" height="477" alt="pk5 1bbb" src="https://github.com/user-attachments/assets/103f2e92-f7e1-47a0-a12e-e158bec3d25f" />

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap   file tersebut, cantumkan mahasiswa/.bash_profile : instruksi echo, misalnya pada /home/ echo “Profile dari .bash_profile” Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.   

### c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: $ su mahasiswa $ exit kemudian gunakan opsi – sebagai berikut : $ su – mahasiswa $ exit Jelaskan perbedaan kedua utilitas tersebut.
<img width="658" height="297" alt="pk5 1c" src="https://github.com/user-attachments/assets/ad1bc2b2-effc-43f0-9d8e-6c3df951f33d" />

## su username :	Beralih ke pengguna lain tanpa memulai lingkungan login secara penuh.
## su - username:	Beralih ke pengguna lain dengan lingkungan login, termasuk pengaturan lingkungan dan pembacaan file profile login yang sesuai.
## 2. Prompt String (PS) 
### a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell PS1=’> ‘   export PS1 
<img width="665" height="76" alt="pk5 2a" src="https://github.com/user-attachments/assets/f6a707e6-da65-48d3-938d-9fcbd2e8bdd1" />

### b. Eksperimen hasil PS1 : $ PS1=“\! > “   69 > PS1=”\d > “   Mon Sep 23 > PS1=”\t > “   10:10:20 > PS1=”Saya=\u > “  Saya=mahasiswa > PS1=”\w >”  ~ > PS1=\h >” 
<img width="675" height="148" alt="pk5 2b" src="https://github.com/user-attachments/assets/38245304-d299-48c1-bf8d-0f37eeaed20f" />

## 3. Logout Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout Echo “Terima kasih atas sesi yang diberikan”  Sleep 5   clear   
<img width="659" height="454" alt="pk5 3aaa" src="https://github.com/user-attachments/assets/eddf3c87-5b0a-4b3b-b687-20cf8cd414c6" />
<img width="670" height="438" alt="pk5 3aa" src="https://github.com/user-attachments/assets/cacb74b1-e780-4229-9209-939319ca89da" />
<img width="679" height="469" alt="pk5 3a" src="https://github.com/user-attachments/assets/0fe16b6c-efce-411c-bd36-de6aae38d73b" />

## 4. Bash script 
### a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : p1.sh   #! /bin/bash   echo “Program p1” ls –l p2.sh   #! /bin/bash   echo “Program p2” who p3.sh   #! /bin/bash   echo “Program p3” ps x 
<img width="677" height="623" alt="pk5 4a" src="https://github.com/user-attachments/assets/32c37a5d-c47c-44a1-8df6-8f307593aad8" />

### b. Jalankan script tersebut sebagai berikut : $ ./p1.sh ; ./p3.sh ; ./p2.sh $ ./p1.sh & $ ./p1.sh $ ./p2.sh & ./p3.sh & $ ./p1.sh ; ./p3.sh ) & 
<img width="673" height="618" alt="pk5 4bbb" src="https://github.com/user-attachments/assets/71fbdde2-6e8d-46e9-9ff3-3105408013b0" />
<img width="662" height="620" alt="pk5 4bb" src="https://github.com/user-attachments/assets/48b15e04-d3cb-4fe4-ad62-acf74d362751" />
<img width="665" height="622" alt="pk5 4b" src="https://github.com/user-attachments/assets/695a0a79-2852-4079-a226-052eeabff506" />

## 5. Jobs 
### a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. #!/bin/bash   while [ true ]  do   date >> hasil  sleep 10 done   
<img width="644" height="100" alt="pk5 5a" src="https://github.com/user-attachments/assets/97c96161-9d8c-49fd-8ba8-52f01e6c2568" />

### b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut : $ jobs $ find / -print > files 2>/dev/null & $ jobs 
<img width="655" height="92" alt="pk5 5b" src="https://github.com/user-attachments/assets/bda3b30e-c157-42b6-974e-890dc35cbf5a" />

### c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background $ fg %1 $ bg 
<img width="667" height="178" alt="pk5 5c" src="https://github.com/user-attachments/assets/229cb579-4083-40d7-82f0-fa8f11b0629b" />

### d. Stop program background dengan utilitas kill $ ps x $ kill [Nomor PID] 
<img width="685" height="607" alt="pk5 5d" src="https://github.com/user-attachments/assets/4a9a841c-0191-44b2-81f7-3a94e778fe5b" />
<img width="673" height="90" alt="pk5 5dd" src="https://github.com/user-attachments/assets/a32eb05d-58c9-460d-a63f-02955ac8ba0e" />

## 6. History 
### a. Ganti nilai HISTSIZE dari 1000 menjadi 20 $ HISTSIZE=20 $ h 
### b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan $ !-5 
### c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer $ !! 
### d. Ulangi instruksi pada history bufer nomor 150 $ !150 e. Ulangi instruksi dengan prefix “ls” $ !ls
<img width="681" height="556" alt="pk5 6a" src="https://github.com/user-attachments/assets/d2680c25-ff51-407a-a4f7-505a9ca10837" />
<img width="671" height="437" alt="pk5 6b" src="https://github.com/user-attachments/assets/8b8f5b67-ebcb-4bf9-96ae-1829c9a8f1e3" />
<img width="671" height="264" alt="pk5 6bb" src="https://github.com/user-attachments/assets/00755a07-c00e-47e6-96ab-a84ba4eb94ac" />
<img width="678" height="149" alt="pk5 6bbb" src="https://github.com/user-attachments/assets/941bf233-d381-41af-8915-e4044312a281" />
<img width="683" height="166" alt="pk5 6d,e" src="https://github.com/user-attachments/assets/fda07f2a-3d9b-4d1e-8b17-1b6de450b1ee" />

