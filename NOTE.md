Semua codingan saya melihat dan meniru dari salah satu tutorial di channel youtube
Pada tutorial tersebut membuat table warga, saya membuat table mahasiswa
Kesulitan yang saya dapat saat mengerjakan adalah karena saya belum benar-benar memahami mengenai fungsi-fungsi codingan nya, jadinya saya hanya mengikuti tutorial di yt namun belum memahami betul fungsi-fungsi codingannya
Di youtube pada index.blade.php tertulis <input class="btn btn-danger" type="submit" name="submit" value="Delete" onclick="confirm('Sure?')">, namun tugas saya saya ganti  <input class="btn btn-danger" type="submit" name="submit" value="Hapus" onclick="confirm('Sure?')">. Saya mengganti karena inisiatif saya sendiri dan saya juga tidak mengetahui efeknya apa jika saya megganti dan baru mengetahui ketika bapak dosen memberikan contoh kepada salah satu teman saya ketika presentasi. 

Langkah-langkah:
1. jalankan perintah create-project laravel/laravel laravel9 (nama projek) di command prompt untuk membuat projek baru.
2. Lalu masuk ke folder kita dengan jalankan perintah cd laravel9(nama projek yang telah kita buat) di command prompt
3. Buka Xampp lalu klik start pada apache dan mysql 
4. Buat database baru di localhost/phpmyadmin dan beri nama sesuai keinginan kita
5. Buka visual code lalu masuk ke .env dan ganti nama databese menjadi nama database yang telah kita buat
6. lalu jalankan perintah php artisan serve
7. jalankan perintah php artisan migrate
8. Buat migration untuk tabel baru kita dengan menjalankan perintah php artisan make:migration create_mahasiswa_table dan tambahkan field yang kita butuhkan dalam table mahasiswa tersebut
9. Membuat model mahasiswa dengan menjalankan perintah php artisan make:model Mahasiswa
10. Membuat route /mahasiswa
11. Membuat controller mahasiswa untuk mengelola codingan data mahasiswa dengan menjalankan perintah php artisan make:controller MahasiswaController 
Dalam MahasiswaController.php import use App\Models\Mahasiswa; dan membuat public function index
Dalam web.php import use App\Http\Controllers\MahasiswaController;
12. Membuat folder mahasiswa di view lalu membuat file index.blade.php
13. Membuat tampilan tabel di index.blade.php
14. Membut route /create di web.php
15. Membuat public function create di MahasisswaController untuk menampilkan form insert data
16. Membuat view create.blade.php di folder mahasiswa
17. Membuat tombol untuk insert data di index.blade.php
18. Membuat form create mahasiswa di create.blade.php
19. Membuat tombol save di create.blade.php dan menentukan method yang digunakan adalah method POST dan memberikan action /mahasiswa/store
20. Membuat route /store dna menggunakan routing post
21. Membuat function store di MahasiswaController.php
Di dalam model mahasiswa kita tambahkan protected $guarded unutk keamanan agar field dapat di isi secara masal
22. Membuat kolom baru dinamakan aksi di index.blade.php untuk mengedit
23. Membuat route /edit
24. Membuat function edit
25. Membuat file edit.blade.php di dalam folder mahasiswa di views untuk membuat form edit
26. Dalam edit.blade.php actionnya diubah menjadi "/mahasiswa/{{$mahasiswa->id}}" dan menggunakan method "POST". 
Dan menambahkan @method ('put') agar ketika form action dieksekusi menggunakan method put
27. Membuat route/warga/(id) dengan method get dan functionnya update
28. Membuat function update di MahasiswaController.php
29. Membuat tombol delete/hapus di indexx.blade.php dengan menggunakan method post dan action di arahkan ke /mahasiswa dan print id
30. Membuat route delete
31. Membuat Public function destroy
