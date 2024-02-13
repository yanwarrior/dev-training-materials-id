# Mengenal Component

Component Angular adalah blok penyusun utama aplikasi Angular.

Component berisi data dan logika interaksi pengguna yang menentukan view dan perilaku view. View di Angular mengacu pada template (HTML).

Component Angular adalah class JavaScript biasa yang ditentukan menggunakan decorator `@Component`. Decorator ini menyediakan view untuk ditampilkan dan metadata tentang component tersebut.

Component bertanggung jawab untuk menyediakan data ke view. Angular menggunakan data binding untuk memindahkan data dari component ke view dan sebaliknya. Data binding dilakukan menggunakan markup HTML khusus, yaitu **Angular Template Syntax**. Component juga mendapat pemberitahuan ketika view berubah.

Aplikasi Angular dapat memiliki banyak component. Setiap component menangani sebagian kecil UI. Component-component ini bekerja sama untuk menghasilkan user interface aplikasi yang lengkap.
