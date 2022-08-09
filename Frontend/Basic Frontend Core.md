# Basic Frontend Core

---

## 1. HTML

HTML adalah singkatan dari **H**yper**t**ext **M**arkup **L**anguage. *Markup* adalah istilah untuk bahasa yang memberikan fitur *document formatting* (e.g link, text, dan picture formatting). Dengan HTML, kita dapat membuat laman web.
Namun, perlu diketahui bahwa HTML **bukan** bahasa pemrograman, karena HTML tidak dapat memberikan fungsionalitas dinamis yang lebih (selain dari document formatting) seperti bahasa pemrograman pada umumnya.

**Example**

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Learn HTML</title>
        <meta/>
    </head>
    <body>
        <h1>Belajar HTML Dasar</h1>
        <p>Hello world</p>
    </body>
</html>
```

* `<!DOCTYPE>` mendeklarasikan tipe document yang kita buat (dalam contoh ini HTML). Hanya boleh dituliskan 1x dibagian paling awal dan case insensitive
* `<html>` merupakan root dari html. menyatakan bahwa seluruh hal yang kita tulis di dalamnya sebagai elemen dari HTML
* `<head>` merupakan bagian yang berisi dari meta(data) dan informasi tambahan bagi laman web
* `<body>` merupakan bagian HTML yang ditampilkan pada laman web
* `<h1>` dan `<p>` merupakan contoh elemen dari html untuk menampilkan teks
<br>

### HTML Elements

elemen HTML adalah seluruh hal dari awal tag pembuka hingga penutup tag.

```html
<h1>...</h1> --> 1 elemen HTML
```

* `<h1>` merupakan tag pembuka
* `...` merupakan konten dari elemen
* `</h1>` tag penutup

Perlu diketahui bahwa tidak semua penulisan elemen HTML berformat `<tag-pembuka>...</tag-penutup>`, contohnya tag image dan line break.

```html
<img src="./awikwok.jpg" alt="awikwok"/> --> 1 elemen HTML
<br> --> 1 elemen HTML
```

<br>

### HTML Tag

tag merupakan awalan dan akhiran (jika memang ada) dari elemen HTML.

|Tag|Fungsi|
|:---|:---|
|`<p>`| Mendeklarasikan teks (paragraf) pada document / laman web|
|`<hn>` -- `<h6>`| Mendeklarasikan teks heading / judul artikel pada document / laman web |
|`<img/>`| Mendeklarasikan elemen gambar pada document / laman web|
|`<form>`| Mendeklarasikan elemen form yang bisa kita submit|

Untuk list lebih lengkap, silahkan kunjungi laman web <https://www.w3schools.com/tags/default.asp>
<br>

### HTML Attributes

Hampir setiap elemen HTML yang ada memiliki atribut. simplenya, atribut adalah informasi tambahan yang bisa kita sisipkan pada tag pembuka suatu elemen. Namun, ada juga elemen yang tidak memiliki atribut apapun, misalnya line break.

```html
<p id="paragraf1"></p> --> "id" merupakan atribut

<img src="./awikwok.jpg" alt="awikwok"/> --> "src" dan "alt" merupakan atribut (khusus untuk elemen image)

<br> --> tidak memiliki atribut
```

Untuk list lebih lengkap, silahkan kunjungi laman web <https://www.w3schools.com/tags/ref_attributes.asp>
<br>

### Core HTML Tags

---

#### Paragraphs

tag `<p>` kita gunakan ketika kita ingin membuat sebuah teks atau paragraf

```html
<p>
    Lorem ipsum dolor amet
</p>
<p>
    Welcome to HTML
</p>
```

<br>

#### Heading

tag `<hn>` 1<=n<=6 kita gunakan untuk mendeklarasikan heading / judul artikel

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

<br>

#### Image

tag `<img/>` kita gunakan untuk mendeklarasikan elemen image.

```html
<img src="https://en.wikipedia.org/wiki/Ratio#/media/File:Aspect-ratio-4x3.svg" alt="ratio picture" width="500" height="500"/>
```

* atribut `src` pada elemen image wajib diisi, karena merupakan link ke source image.
* atribut `alt` menyatakan alternative (text) yang akan ditampilkan, jika gambar tidak bisa ditampilkan. atribut ini tidak wajib, Namun dianjurkan (better practice)
<br>

#### Links

Kita bisa membuat teks kita sebagai hyperlink sehingga jika diklik, akan "mengantarkan" kita ke tujuan yang tertera.
link bisa kita deklarasikan dengan tag `<a>`

```html
<a href="https://insta.not4saken.com">Visit not4saken's page!</a>
```

* atribut `href` berisikan url tujuan
<br>

#### lists

pada html, kita juga bisa membuat list (bullet/numbering), yakni dengan outer tag `<ol>` atau `<ul>` dan inner tag `<li>`.
`<ol>` menyatakan *ordered list*, sedangkan `<ul>` menyatakan *unordered list*

```html
<h2>An Unordered HTML List</h2>
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
<h2>An Ordered HTML List</h2>
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```
<br>

#### Tables
```html
<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
  </tr>
</table>
```

* `<tr>` menyatakan table row
* `<th>` menyatakan heading / judul untuk setiap kolom
* `<td>` menyatakan data untuk setiap cell

<br>

#### Forms

Pada HTML, kita juga bisa mendeklarasikan formulir untuk menerima input dari user. kita mendeklarasikannya dengan tag `<form>`.
pada form terdapat beberapa atribut yang harus di isi, yaitu :

* `action`, yang menyatakan aksi ketika data dikirim. biasanya berupa url atau endpoint API
* `method`, yang menyatakan metode pengiriman data. biasanya berupa HTTP `POST` atau `GET`

```html
<form action="api/auth" method="POST">
    <input type="text" name="username">
</form>
```

form hanyalah "kerangka" yang mendefinisikan fitur-fitur form sehingga sistem mengerti bahwa itu adalah form.
Namun, untuk menerima masukan dari user, kita harus mendeklarasikan elemen lain, yakni `<input>` atau `<textarea>`.
pada contoh di atas form menggunakan `<input>` untuk menerima input dari user. `<input>` sendiri memiliki 2 atribut yang harus di isi, yakni:

* `type`, yang menjelaskan tipe masukan dari user. biasanya berupa "text", "password", atau "number"
* `name`, yang akan menjadi key atau identifier dari masing-masing input field. valuenya harus unik (tidak ada 2 atau lebih input dengan name yang sama)
<br>

#### Block-level Element

Sejauh ini kita sudah mengenal berbagai tag untuk membuat elemen html. masing-masing tag mendefinisikan hal yang berbeda. 
Namun, HTML juga memiliki elemen yang berfungsi sebagai "wrapper" sehingga berbagai elemen bisa di-*nest* menjadi satu blok elemen (block-level element).
contohnya adalah tag `<div>`. dengan `<div>`, kita bisa melakukan grouping terhadap elemen-elemen kita sehingga menjadi 1 blok elemen dan kita bisa dengan mudah mengaplikasikan `style` atau behaviour tertentu pada seluruh `children` (subelemen) di dalam `<div>` tersebut.

```html
<div style="background-color:red;"> --> memberi warna red sebagai background dari seluruh elemen
    <h2>Land of Solomon</h2>
    <img src="www.abcdefg.com/image/solomon.jpg" alt="solomon's view from above"/>
    <p>Solomon is located near off-shore...</p>
</div>
```
---

### Semantic HTML

Setelah kita mengenal block-level element `<div>`, kita mungkin jadi lebih mengerti bagaimana menyusun elemen-elemen html pada laman web. kita tinggal menyatukan elemen-elemen tertentu dalam `<div>` dan meletakannya seusai dengan keinginan kita. Dengan begitu, layouting menjadi mudah. 
Namun, ternyata, selalu membungkus elemen ke dalam tag `<div>` bukanlah best practice. karena, dengan begitu, ketika browser kita mengurai dokumen yang berisi banyak sekali `<div>`, maka tiap bagian akan menjadi abstrak / ambigu (div). Oleh karena itu, munculah paradigma "Semantic HTML".
<br>

Semantic HTML mengajarkan kita untuk tidak selalu menggunakan tag `<div>` dalam membungkus elemen, tetapi sesuaikan dengan kebutuhan. misal ketika membuat navbar, gunakan `<nav>` untuk membungkus elemen yang ada. lalu, konten utama web kita, kita bungkus dengan `<main>` instead of `<div>`, dsb. dengan begitu, komposisi / struktur dokumen web kita akan menjadi lebih baik.

![semantic html layout](https://miro.medium.com/max/1400/1*VU3WvCvNzu5KfLnrXi4BVA.jpeg)
taken from https://medium.com/codex/what-is-semantic-markup-and-why-you-should-use-it-44777543c29c

<br>
<br>
<br>

## 2. CSS

Kita telah mengenal HTML. dengan HTML kita bisa membuat konten untuk laman web kita. Namun, HTML hanya bisa mendefinisikan elemen-elemen / konten.
Ketika membuat web, kita tentunya ingin laman web kita menjadi menarik. oleh karena itu, kita membutuhkan CSS untuk memberi styling pada laman kita.
CSS merupakan singkatan dari **C**ascading **S**tlye **S**heet. Dengan CSS, kita bisa memberikan style (layouting, warna, ukuran, dll) sehingga laman web kita menjadi lebih estetik.

__Analogi html + css + js__
![html,css,js analogy](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/06/HTML-vs-CSS-vs-JavaScript-512x300.png)
taken from https://www.edureka.co/blog/javascript-tutorial/

<br>

__HTML+CSS vs HTML-only__
![htmlcss vs html only](https://c.jorcus.com/wp-content/uploads/2020/05/21125641/CSS-vs-no-CSS.jpg)
taken from https://jorcus.com/getting-started-with-css/

<br>

__syntax__
![css syntax](https://www.w3schools.com/css/img_selector.gif)

<br>

**How to Apply CSS to HTML?**
![how to apply css to html](https://gitlab.com/it-force/amfm/-/raw/master/gambar/img6.PNG)

<br>

**Where to Apply CSS?**

#### 1. inline

```html
<p style="font-weight:bold;color:red">HELLO</p>
```
* pada inline css, css kita tuliskan pada atribut "style". dengan format `property:value`, dan setiap css dipisah dengan `;`

#### 2. internal

CSS bisa kita deklarasikan dengan tag `<style>` pada HTML kita. Namun, kita perlu reference (selector) terhadap elemen yang ingin dikustomisasi, dengan atribut `class` atau `id`.

```html
<head>
    <style>
        #title {                    --> gunakan prefix "#" untuk selector id
            color:red;
            font-weight:bold;
            text-align:center
        }
        .content {                  --> gunakan prefix "." untuk selector class
            font-size: 12px;
            text-align:left;
        }
    </style>
</head>
<body>
    <div>
        <h1 id="title">HELLO</h1>
        <p class="content">WORLD</p>
    </div>
</body>
```

## 3. JavaScript (DOM Manipulation)

Setelah mempelajari HTML dan CSS, kita sudah bisa membuat laman web yang sangat basic dan cukup estetik. Namun, pada kenyataannya, setiap laman web yang sering kita kunjungi pasti penuh dengan fitur-fitur atau fungsionalitas yang cukup kompleks, misal menghapus teks, mengubah tulisan atau warna ketika sebuah button kita klik, dsb.
Fungsionalitas ini tidak bisa dilakukann oleh HTML maupun CSS, karena keduanya bukanlah bahasa pemrograman. Oleh karena itu, kita butuh JavaScript untuk melakukan fungsionalitas ini (DOM Manipulation).
<br>

__DOM__
![DOM Tree](https://www.w3schools.com/js/pic_htmltree.gif)
DOM merupakan singkatan dari **D**ocument **O**bject **M**odel. DOM merupakan sebuah platform atau interface yang *language-agnostic* yang memungkinkan script program mengakses dan atau mengubah konten, struktur dan ,style document secara dinamis.
<br>

Dengan memanfaatkan JavaScript HTML DOM Manipulation, kita bisa melakukan beberapa fungsionalitas terhadap HTML kita, seperti :
 * Mengubah konten dari elemen HTML
 * Mengubah style (CSS) dari elemen tertentu
 * Mengatur logic web ketika terjadi event HTML DOM
 * Menambah atau menghapus elemen HTML

<br>

Pada JS DOM terdapat dua hal penting yang harus diketahui, yakni **DOM Method** dan **DOM Property**. DOM method memungkinkan kita untuk melakukan aksi tertentu, sedangkan DOM property adalah nilai yang bisa kita dapatkan dan atau ubah.

### Menemukan atau Mendapatkan Element HTML (referencing).
Sebelum kita memanipulasi sebuah elemen html, kita harus mendapatkan (referencing) elemen html tersebut terlebih dahulu. JavaScript memiliki beberapa cara untuk melakukannya, yakni :
* document.getElementById(INSERT_ID_STRING)
* document.getElementsByClassName(INSERT_CLASSNAME_STRING)
* document.getElementsByTagName(INSERT_TAG_STRING)
<br>

Setelah mendapatkan reference ke elemen yang kita inginkan, baru kita bisa memanipulasi elemen HTML tersebut.

**example**

```html
<head>
   <script>
      const pageTitle = document.getElementByID("title");   // menemukan (referencing) elemen dengan id "title"
      pageTitle.innerHTML = "THIS TITLE HAS BEEN CHANGED";  // Mengubah (memanipulasi) konten dari heading
   </script> 
</head>
<body>
    <div>
        <h1 id="title">HELLO</h1>
        <p class="content">WORLD</p>
    </div>
</body>
```
untuk list lebih lengkapnya, silahkan kunjungi laman web https://www.w3schools.com/jsref/default.asp

<br>

### DOM Events and Event Listeners
Kita juga bisa melakukan manipulasi DOM ketika terjadi sesuatu aksi (Event). Dengan begitu, kita bisa melakukan fungsionalitas dalam kondisi tertentu secara otomatis. beberapa event listener yang basic adalah :
* `onclick`, listener ketika terjadi event mouseclick.
* `onmouseover`, listener ketika terjadi event mouse hover
* `onchange`, listener ketika terjadi perubahan pada konten elemen.

<br>

**example**
```html
<head>
   <script>
      function changeTitle(e){
        const pageTitle = document.getElementByID("title");   // menemukan (referencing) elemen dengan id "title"
        pageTitle.innerHTML = "WORLD";  // Mengubah (memanipulasi) konten dari heading
        e.innerHTML = "title changed!"; // mengubah teks pada button.
      }
   </script> 
</head>
<body>
    <div>
        <h1 id="title">HELLO</h1>
        <button class="content" type="button" onclick="changeTitle(this)">change title</button> --> menggunakan onclick event listener
    </div>
</body>
```
<br>

selain builtin event listener dari tag, kita juga bisa menambahkan event listener , dengan menggunakan `element.addEventListener("EVENTNAME", callback_function)`

**example**
```html
<head>
   <script>
    //menggunakan event listener untuk mengeksekusi setName(), ketika halaman web telah terload sepenuhnya
      window.addEventListener("DOMContentLoaded", setName) 
      function setName(){
        const target = document.getElementById("name");
        target.innerHTML = "USER69"
      }
   </script> 
</head>
<body>
    <div>
        <h1 id="title">HELLO <span></span></h1>
    </div>
</body>

untuk list lebih lengkapnya, silahkan kunjungi laman web https://www.w3schools.com/jsref/dom_obj_event.asp
<br>

reference:
1. https://pragusga.gitlab.io/bismit/HTML.html by Mas Taufik Bismit 2021
2. HTML https://www.w3schools.com/html/
3. CSS https://www.w3schools.com/css/
4. JS DOM 
