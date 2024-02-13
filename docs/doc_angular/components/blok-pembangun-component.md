# Blok Pembangun Component

Component terdiri dari tiga blok pembangun utama:

- Template
- Class
- Metadata

## Template (view)

Template mendefinisikan tata letak dan konten tampilan yang akan dilihat oleh pengguna. Tanpa template,  Angular tidak dapat merender apa pun ke DOM.

Template tersebut hanyalah kode HTML dan markup HTML khusus milik Angular (dikenal sebagai Angular Template Syntax).

Kita dapat menambahkan directive, pipe & bahkan component lainnya pada template.

Data yang ditampilkan di template berasal dari component, dimana biasanya data tersebut diperoleh dari service. Kita dapat menjaga agar template tetap sinkron dengan component menggunakan teknik data binding. Template dapat menerapkan event binding atau two way data binding untuk memberi tahu component ketika pengguna mengubah sesuatu pada view.

Ada dua cara untuk menentukan template di Angular:

- Mendefinisikan template secara inline.
- Menyediakan template eksternal.

## Class

Class menyediakan data & logika ke view. Biasanya berisi kode TypeScript yang terkait dengan template (view). Dalam membuat class, kita perlu menggunakan TypeScript.

Class berisi properti dan method. Properti class dapat di-binding ke view menggunakan data binding.

Contoh class Angular sederhana:

```ts
export class AppComponent {
  title: string = "app"
}
```

Berdasarkan konvensi, nama class diakhiri dengan kata `Component` untuk mengidentifikasinya dengan mudah bahwa itu adalah component.

## Metadata

Metadata memberikan informasi tambahan tentang component. Angular menggunakan informasi ini untuk memproses class. Kita menggunakan decorator `@Component` untuk menyediakan metadata ke component.

### Decorator @Component

Decorator adalah fungsi yang digunakan untuk menambahkan metadata ke class. Component dapat ditentukan dengan decorator `@Component`.

Ketika Angular melihat class dengan decorator `@Component`, Angular akan memperlakukan class tersebut sebagai component.

Decorator selalu diawali dengan `@`. Kita harus menempatkan decorator tepat sebelum definisi class. kita juga dapat membuat decorator kita sendiri. Decorator ini mirip dengan atribut di C#.

