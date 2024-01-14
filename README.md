# UAS PEMROGRAMAN MOBILE 1
Nama &nbsp; &nbsp;: Ihsan Hadimulya<br>
NIM&nbsp; &nbsp; &nbsp; : 312210047<br>
Kelas&ensp; &nbsp; : TI.22.A.1<br>
Dosen &nbsp; : Donny Maulana, S.Kom., M.M.S.I.<br><br>

## PERINTAH TUGAS
<p align="justify">Perintah tugas kali ini adalah mengumpulkan semua hasil yang sudah dibuat dari pertemuan pertama sampai akhir, hasil - hasil tersebut digabungkan dalam satu Aplikasi. Berikut ini semua code yang telah Saya buat.</p>

## PENJELASAN APLIKASI
Sebelumnya saya akan menjelaskan terlebih dahulu, ada apa saja didalam aplikasi ini. Berikut ini adalah daftarnya :
- Activity Hello World , di activity ini adalah awal dari pengenalan terhadap software Android studio. Didalam activity ini hanya terdapat kalimat yang bertuliskan "Hello_World"
- Activity Count ,  activity ini berisi program penghitungan bilangan fibonnaci yang sebelumnya telah diperintahkan untuk dibuat,
- Activity Scroll Movie , activity ini berisi sinopsis film dokumenter ICE COLD, sinopsis yang banyak digunakan untuk pembelajaran fungsi scroll didalam aplikasi android ini.
- Activity TwoActivity ,  twoactivity ini adalah sebuah program perpesanan atau chatting, yang menggunakan dua activity.
- Program Open Alarm , nah program ini berbeda dari sebelumnya, disini tidak menggunakan layout activity.xml karena program ini hanya berfungsi sebagai pembuka dan pengatur alarm dalam sebuah smartphone android.
- Program Open Map ,  sama seperti program alarm, program open map ini hanya berupa sebuah tombol yang berfungsi sebagai pembuka aplikasi google maps yang tersedia di dalam smartphone Android.
- Activity Fragment , activity ini adalah sebuah activity yang terdiri dari beberapa fragment. Disini fragmentnya berperan sebagai penampil film dengan genre yang berbeda, seperti action, comedy, dan romance.

### Semua Source Code
<p align="justify">Disini saya tidak akan menampilkan source codenya disini, karena akan terlalu banyak dan memakan tempat dan hanya membuat pusing melihatnya. Saya sudah push semua file dari project yang sudah saya buat dan jika menginginkan bisa mendownload beberapa file yang dibutuhkan saja atau clone repository ini sepenuhnya. Sebagai gantinya, Saya hanya akan menjelaskan sedikit dari apa saja yang sudah saya kerjakan.</p>

- Source Code Splash Launcher
  - SplashScreen.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/SplashScreen.java)<br>
    <p align="justify">Didalamnya berisi code java, untuk menjalankan fungsi splash launcher. Lebih jelasnya splash launcher ini adalah menampilkan gambar/logo/icon ketika kita pertama kali membuka aplikasi, atau sebelum menuju kehalaman utama.</p>
  - backgroundlauncher.xml [Lihat File](TugasUAS/app/src/main/res/drawable/backgroundlauncher.xml)<br>
    Ini adalah logo yang saya gunakan, Saya menggunakan logo dari channel youtube yang saya punya yaitu CREATIVEGG.
  - Hasil Run<br>
    Berikut ini adalah hasil run nya :<br>
    
https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/123f5194-2c55-4b92-a469-30ee7635af6e

<br><br>

- Source Code Utama
  - MainActivity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/MainActivity.java)<br>
    <p align="justify">Di MainActivity ini berisi program java yang memiliki fungsi penghubung dari semua activity yang disebut intent dan fungsi tombol open alarm dan open map. Saya beri nama file ini Main karena disinilah fungsi paling awal dari halaman awal.</p>
  - activity_main.xml [Lihat File](TugasUAS/app/src/main/res/layout/activity_main.xml)<br>
    <p align="justify">Ini adalah layout dari halaman awal aplikasi ini. Layout ini terhubung dengan MainActivity.java tadi. Dilayout ini menampilkan semua tombol tombol dari berbagai activity dan program yang sudah dijelaskan diatas. Beginilah tampilan dari layoutnya :</p> <br>
    
    ![image](https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/a581874e-e647-4b21-8f19-4f90125967a3)
    > Iconnya disini sudah Saya usahakan agar sesuai dengan identitas dari activitynya.
  - AndroidManifest.xml [Lihat File](TugasUAS/app/src/main/AndroidManifest.xml)<br>
    <p align="justify">Di AndroidManifest.xml ini berfungsi untuk mengaktifkan permission yang dibutuhkan dibeberapa activity. Selain itu, AndroidManifest.xml ini juga harus dilakukan pengeditan jika kita menambah sebuah tombol atau activity baru yang berhubungan dengan intent, agar activity tersebut dapat dibuka nantinya.</p>
  - string.xml [Lihat File](TugasUAS/app/src/main/res/values/strings.xml)<br>
    String.xml ini adalah sebuah values, values ini berisi teks-teks dari tombol - isi - atau apapun itu yang berhubungan dengan teks.
  - colors.xml [Lihat File](TugasUAS/app/src/main/res/values/colors.xml)<br>
    <p align="justify">Sama seperti string, colors.xml ini juga merupakan sebuah values, tapi bedanya values ini berisi code-code warna yang sudah dibuat menjadi ID atau identitas yang bertujuan untuk memudahkan dalam pemanggilan warnanya di dalam coding.</p><br><br>

- Source Code Activity Hello World
  - HelloActivity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/HelloActivity.java)<br>
    Disini saya tidak mengubah apapun isi dari javanya, dengan kata lain saya buat default sedari awal dibuat.
  - activity_hello.xml [Lihat File](TugasUAS/app/src/main/res/layout/activity_hello.xml)<br>
    <p align="justify">Seperti yang sudah diketahui ini merupakan layout yang terhubung dengan java nya. Saya hanya menambahkan textview untuk menampilkan android:text "hello_world" nya (text sudah ada di string.xml), selain itu saya juga mengubah warna text dan menambahkan background agar terlihat lebih menarik.</p>
  - Hasil Run<br>
    Berikut adalah hasil run nya :<br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/054f30de-31d8-43ca-a7d5-74ec8e0cb802

<br><br>

- Source Code Activity Count
  - CountActivity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/CountActivity.java)<br>
    Tentunya disini berisi code java untuk menjalankan fungsi perhitungan dari rumus fibonnaci. Bilangan fibonnaci adalah bilangan yang rumusnya adalah menambah sebuah bilangan dengan        bilangan sebelumnya. Contohnya 1, 1, 2, 3, 5, 8...
  - activity_count.xml [Lihat File](TugasUAS/app/src/main/res/layout/activity_count.xml)<br>
    Ini adalah layout dari activity count, ada beberapa tombol disini seperti set limit, count, dan reset. Angka yang ditampilkan juga sudah menggunakan code warna, agar setiap angka         yang ditampilkan memiliki warna yang berbeda dengan angka sebelumnya.
  - Hasil Run<br>
    Berikut adalah hasil run nya :<br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/c80d6b3f-3c2e-4177-804d-c91675139b65

<br><br>

- Source Code Activity Scroll Movie
  - SianidaActivity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/SianidaActivity.java)<br>
    Disini saya tidak mengubah apapun isi dari javanya, dengan kata lain saya buat default sedari awal dibuat.
  - activity_sianida.xml [Lihat File](TugasUAS/app/src/main/res/layout/activity_sianida.xml)<br>
    <p align="justify">Layout inilah yang mempengaruhi dan memberikan alasan kenapa di javanya tidak ada perubahan. Disini, digunakan sebuah scrollview yang bisa menjadikan text yang begitu panjang dan tidak muat dalam satu layar penuh, maka dengan ini kita bisa membaca semua isi kontennya hanya dengan cara scroll layar.</p>
  - Hasil Run<br>
    Berikut adalah hasil run nya :<br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/70779eef-1c2f-4886-9f51-d310ac4d0125

<br><br>

- Source Code Activity TwoActivity
  - TwoActActivity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/TwoactActivity.java) & TwoAct2Activity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/Twoact2Activity.java)<br>
    <p align="justify">Kedua java berisi fungsi untuk menjalankan program perpesanan. Kedua java tersebut memiliki peran masing-masing, yang pertama untuk pengirim dan yang kedua untuk fungsi ketika pesan berhasil terkirim.</p>
  - activity_twoact [Lihat File](TugasUAS/app/src/main/res/layout/activity_twoact.xml) & activity_twoact2 [Lihat File](TugasUAS/app/src/main/res/layout/activity_twoact2.xml)<br>
    Kedua layout ini merupakan tampilannya, yang pertama berfungsi menampilkan saat mengirim pesan dan yang kedua menampilkan saat pesan berhasil terkirim.
  - Hasil Run<br>
    Berikut adalah hasil run nya :<br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/4f7542d0-9643-4733-935f-1e9910692f78

<br><br>

- Source Code Program Alarm
  - Karena program ini hanya merupakan tombol, maka hanya tinggal menambahkan baris code berikut :<br>
    ```
    # Tambahkan code ini didalam protected void OnCreate :
          findViewById(R.id.btnSetAlarm).setOnClickListener(v -> {
              // Panggil metode untuk mengatur alarm
              setAlarm();
          });
      }

    # Lalu code tambahkan fungsi intent untuk tombolnya :
      private void setAlarm() {
          Intent alarm = new Intent(AlarmClock.ACTION_SET_ALARM);
          startActivity(alarm);
      }
    ```
  - Tidak hanya itu, perlu ditambahkan juga beberapa baris code di AndroidManifest.xml, seperti ini:
    ```
    <uses-permission
          android:name="com.android.alarm.permission.SET_ALARM" />
  
    dan
        <action android:name="android.intent.action.SET_ALARM" />

    ```
  - Hasil Run<br>
    Berikut adalah hasil run nya :<br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/13a8223e-6984-4696-b750-30c62c9aef11

<br><br>

- Source Code Program Open Map
  - Sama halnya seperti program alarm yang hanya menggunakan fungsi sebuah tombol, maka hanya code inilah yang diperlukan untuk dapat menjalankan dan membuka maps nya.
    ```
    # Tambahkan code ini didalam protected void OnCreate :
    ImageButton btnshowMap = findViewById(R.id.btnshowMap);
        btnshowMap.setOnClickListener(v -> {
            Intent map = new Intent(Intent.ACTION_VIEW, Uri.parse("geo:-6.324307,107.169273"));
            map.setPackage("com.google.android.apps.maps");
            startActivity(map);
        });
    ```
  - Hasil Run<br>
    Berikut adalah hasil run nya :<br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/bac81232-d106-4890-ba58-2bab1215568f

<br><br>

- Source Code Activity Fragment <br>
  <p align="justify">Berbeda dari activity sebelumnya, di activity ini memerlukan banyak java dan layout, karena activity ini terdiri dari beberapa halaman. Perintah tugas dari activity ini adalah, membuat sebuah program atau aplikasi menampilkan daftar film sesuai dengan genre nya. Dan genre yang diperintahkan untuk dibuat ada tiga buah, yakni Action, Comedy, dan Romance.</p>
  
  - FragmentActivity.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/FragmentActivity.java)<br>
    Java yang ini berfungsi sebagai fungsi dari halaman utamanya. Didalamnya terdapat code untuk switch atau berpindah antar fragment dari action/comedy/romance. Nah agar code fragment tersebut dapat berjalan, perlu ditambahkan sebuah depedencies baru di build.gradlenya, berikut dependenciesnya :<br>
    
    ```
    implementation("androidx.fragment:fragment:$fragmentVersion")
    ```
    > Perlu diingat jika menambahkan dependencies baru, perlu dilakukan sync terlebih dahulu.

  - activity_fragment.xml [Lihat File](TugasUAS/app/src/main/res/layout/activity_fragment.xml)<br>
    Inilah layout yang terhubung dengan FragmentActivity.java, layout ini adalah tampilan basic atau tampilan utama yang masih kosong, didalamnya terdapat 3 tombol untuk berpindah antar fragment nya. Berikut ini tampilannya :<br>

    ![image](https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/1eac1dde-3762-4064-a70e-85c2b5b80574) <br>

  - FirstFragment.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/FirstFragment.java) , SecondFragment.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/SecondFragment.java) , ThirdFragment.java [Lihat File](TugasUAS/app/src/main/java/com/example/tugassepuluh/ThirdFragment.java) <br>
    <p align="justify">Nah ketiga java ini didalamnya terdapat fungsi untuk menampilkan list film yang ada, dan fungsi memutar trailer video ketika poster atau gambar filmnya ditekan. Video tersebut berasal dari link youtube yang saya tambahkan sesuai dengan film apa yang ada di masing masing fragment nya. Untuk menggunakan fungsi ini perlu ditambahkan depedencies di build.gradle nya. Saya menggunakan library yang bernama youtube player dari pierfrancescosoffritti, berikut dependenciesnya :</p><br>
    
    ```
    implementation("com.pierfrancescosoffritti.androidyoutubeplayer:core:11.0.1")
    ```
    > Perlu diingat jika menambahkan dependencies baru, perlu dilakukan sync terlebih dahulu.

  - fragment_first.xml [Lihat File](TugasUAS/app/src/main/res/layout/fragment_first.xml) , fragment_second.xml [Lihat File](TugasUAS/app/src/main/res/layout/fragment_second.xml) , fragment_third.xml [Lihat File](TugasUAS/app/src/main/res/layout/fragment_third.xml) <br>
    Ketiga xml ini merupakan layout atau tampilan dari masing-masing fragment, didalamnya menampilkan daftar film sesuai dengan genrenya. Layout ini terhubung dengan ketiga java diatas.
  - Hasil Run <br>
    Berikut adalah hasil run nya : <br>

https://github.com/DYRHEEEN/Tugas-UAS-Mobile-1/assets/151630441/2698f3d6-dee6-4c02-8810-b073784f6668

<br><br>
