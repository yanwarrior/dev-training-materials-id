# Properti Penting Metadata Component

Ada beberapa properti yang wajib kita ketahui di dalam metadata:

- Selector
- Provider
- Directive
- Styles/styleUrls
- template/templateUrl

## Selector

Selector menentukan selector CSS yang sederhana. Angular mencari selector CSS di template dan merender component-nya di sana.

## Provider

Provider adalah service Angular yang akan digunakan oleh component kita. Service memberikan fungsionalitas tambahan kepada component atau service lainnya.

## Directive

Tempat menyisipkan directive yang akan digunakan oleh component kita.

## `styles` dan `styleUrls`

Style CSS atau stylesheet yang dibutuhkan oleh component. Di sini kita bisa menggunakan stylesheet eksternal (menggunakan `styleUrls`) atau inline style (menggunakan `styles`). Style yang digunakan di sini khusus untuk component tersebut.

## `template` dan `templateUrl`

Template HTML yang akan membentuk tampilan yang nantinya akan dilihat oleh pengguna. Properti ini seolah memberi tahu Angular cara merender tampilan component. Template bisa dalam bentuk inline (menggunakan `template`) atau kita bisa menggunakan template eksternal (menggunakan `templateUrl`). Component hanya dapat memiliki satu template. Kita bisa menggunakan template inline atau template eksternal atau bahkan tidak kedua-duanya.

