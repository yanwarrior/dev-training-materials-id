# Interpolasi

Interpolasi digunakan untuk memasukkan ekspresi sebagai bagian dari literal string ke template HTML. Angular mengevaluasi ekspresi menjadi string di dalam template. Interpolasi juga dikenal dengan nama **string interpolation**.

Angular menggunakan `{{ }}` (kurung kurawal ganda) pada template untuk menunjukkan interpolasi:

```jsx
{{ ekspresi }}
```

Isi di dalam tanda kurung tersebut disebut sebagai **template expression**.

Angular akan mengevaluasi template expression tersebut dan mengubahnya menjadi string. Setiap kali template expression berubah, Angular akan memperbarui view-nya kembali.

## Contoh Implementasi Interpolasi

Buka file `app.component.html` dan tambahkan kode berikut:

```jsx
{{ title }}
```

Buka file `app.component.ts` dan tambahkan kode berikut:

```js
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Angular Interpolation Example';
}
```

Jalankan aplikasi dan kita akan melihat pesan "Angular Interpolation Example" tampil di browser.

Pada contoh di atas `title` adalah template expression yang berasal dari component. Angular mengevaluasi `{{ title }}` dan menggantinya dengan nilai properti `title` dari component.

Jika kita mengubah `title` di class component, Angular akan memperbarui view-nya.

Kita dapat menggunakan interpolasi untuk memanggil method apa saja dari class component atau kita juga bisa menggnunakannya melakukan beberapa operasi matematika dan lain sebagainya.

> Perlu diingat, interpolation adalah one way data binding. Interpolasi tidak direkomendasikan untuk mengubah state dari component!

## Contoh Lain Interpolasi

**Memanggil method dari component:**

template:

```jsx
{{ getTitle() }}
```

component:

```ts
title = 'Angular Interpolation Example';

getTitle(): string {
  return this.title;
}
```

**Menggabungkan string:**

```jsx
<p>Welcome to {{title}}</p>
<p>{{ 'Hello & Welcome to '+ ' Angular Interpolation '}}</p>
<p>Welcome {{firstName}}, {{lastName}}</p>
<p>Welcome {{getFirstName()}}, {{getLastName()}}</p>
```

**Melakukan operasi matematika:**

template:

```jsx
<h2>Mathematical Operations</h2>
 
<p>100x80 = {{100*80}}</p>
<p>Largest: {{max(100, 200)}}</p>
```

component:

```ts
max(first: number, second: number): number {
  return Math.max(first, second);
}
```

### Binding Properti Element

Kita dapat menggunakan interpolasi untuk mem-binding properti element HTML, component atau directive. 

Pada kode berikut, kita mem-binding properti `style.color` dari elemen `<p>`. Kita dapat mem-binding properti apa pun di element asalkan properti tersebut menerima string sebagai nilainya:

```html
<p>Show me <span class = "{{giveMeRed}}">red</span></p>
<p style.color={{giveMeRed}}>This is red</p>
```

**Mem-binding image source:**

```html
<div><img src="{{itemImageUrl}}"></div>
```

**Membinding atribut `href`:**

```html
<div><img src="{{itemImageUrl}}"></div>
```



