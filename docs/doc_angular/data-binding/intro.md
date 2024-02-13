# Mengenal Data Binding

Data binding adalah teknik di mana data tetap sinkron antara component dan view. Setiap kali pengguna memperbarui data di view, Angular akan memperbarui component. Saat component mendapatkan data baru, Angular juga akan memperbarui view-nya.

Data binding di Angular secara garis besar dapat diklasifikasikan menjadi dua kelompok. One way data binding atau two way data binding.

## One Way Data Binding

Dalam one way data data binding, data mengalir hanya satu arah, baik dari view ke component atau component ke view.

### Dari Component ke View

Untuk membinding data dari component ke view, kita dapat menggunakan interpolasi dan properti binding.

### Dari View ke Component

Untuk membinding data dari view ke component, kita dapat menggunakan event binding.

## Two Way Data Binding

Two way data binding berarti bahwa perubahan yang dibuat pada model kita di component akan di-share ke view dan setiap perubahan yang dibuat di dalam view akan segera diperbarui di component yang yang terkait.

Two way data binding biasanya digunakan di dalam form entri data. Setiap kali pengguna membuat perubahan pada inputan, Angular akan memperbarui model kita di component. Demikian pula sebaliknya, saat kita memperbarui model dengan data baru, Angular juga akan memperbarui view-nya.

Two way data binding menggunakan sintaks khusus yang dikenal sebagai **banana in a box** `[()]`.

Sintaks tersebut berfungsi memiliki dua fungsionalitas, yaitu property binding & event binding. Namun untuk menggunakannya, properti harus memiliki event change dengan nama `<propertyName>Change`. Tapi, Angular sudah menyediakan directive khusus bernama `ngModel` yang mengatur two-way data binding lebih mudah.


