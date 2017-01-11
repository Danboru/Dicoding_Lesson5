# Dicoding_Lesson5

Komponen Layout

Layout adalah komponen dasar dalam pembentukan UI dan merupakan container utama untuk komponen-komponen lain pada tampilan aplikasi Android.  Dalam satu tampilan aplikasi Android bisa terdapat lebih dari satu Layout dengan adanya sebuah file XML layout sebagai parent, dan dimungkinkan adanya nested layout dalam satu file UI XML. Penjelasan mengenai XML Layout dapat dibaca pada http://developer.android.com/guide/topics/ui/declaring-layout.html

* Terdapat empat jenis layout utama di Android :

  * Linear Layout
  * Relative Layout
  * Frame Layout
  * Grid Layout
Pembedanya adalah pada posisi penempatan komponen-komponen (child view) didalamnya, sebagai berikut:

Linear Layout

Akan menempatkan komponen-komponen didalamnya secara horizontal atau vertical (menyamping atau menurun). LinearLayout memiliki atribut weight untuk masing-masing child view yang terdapat didalam LinearLayout yang berguna untuk mengontrol porsi ukuran view secara Relatif dalam sebuah ruang (space) yang tersedia.

![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture11.png?raw=true)

Relative Layout

Layout yang paling fleksibel dikarenakan posisi dari masing-masing komponen didalamnya dapat mengacu secara relatif pada komponen yang lainnya dan juga dapat mengacu secara relatif ke batas layar.

![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture12.png?raw=true)

Frame Layout

Layout ini adalah layout yang paling sederhana. Layout ini akan membuat komponen yang ada didalamnya menjadi menumpuk atau saling menutupi satu dengan yang lainnya (layering). Komponen yang paling pertama pada layout ini akan berada dibawah komponen-komponen diatasnya. Pada materi penggunaan fragment di materi sebelumnya, FrameLayout memiliki kemampuan untuk menjadi container untuk fragment-fragment didalam sebuah Activity. Berikut ilustrasi dari penggunaan FrameLayout terhadap child view yang dimiliki didalamnya.

![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture13.png?raw=true)

Grid Layout

Diperkenalkan pada API level 14 (Android 4.o / Ice Cream Sandwich), layout ini akan memberikan kemudahan dengan mengakomodir komponen didalamnya ke dalam bentuk Grid (Kolom dan Baris). Dalam sebuah referensi, GridLayout merupakan komponen layout yang sangat flexibel dan dapat dimanfaatkan untuk menyederhanakan pembuatan Layout UI yang bersifat kompleks dan bersarang yang terdapat di komponen Layout lainnya.

![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture14.png?raw=true)

Kapan sebaiknya saya menggunakan masing-masing jenis Layout tersebut?

Pemahaman yang baik terhadap dasar-dasar pembangunan UI di android, pengalaman, feeling, dan mencari tahu bagaimana best practicenya. Semua tergantung latihan dan seberapa sering kita berhadapan dengan kasus-kasus melakukan transformasi UI dari bentuk mockup ke dalam bentuk kode XML di Android. Dengan membiasakan mengkode sisi UI di XML tanpa drag and drop akan mempercepat pembentukan pola pikir dan feeling kita dalam membangun dan mentransformasi UI ke dalam bentuk yang dibutuhkan.

 

Scroll View

ScrollView adalah sebuah komponen yang akan membuat komponen didalam dapat digeser (scroll) secara vertical dan horizontal. Dengan ScrollView, dimungkinkan ukuran komponen didalamnya melebihi ukuran screen. Komponen didalam scrollview hanya diperbolehkan memiliki 1 parent utama dari layout linear, relatif, frame, atau grid layout.

 

Android Unit

Ekosistem android dikenal dengan fragmentasi spesifikasi device yang sangat bervariasi termasuk perbedaan dimensi layar dan kerapatan pixel dari layar di masing-masing jenis device, terdapat 3 jenis pengukuran di desain layout android:

px (pixel)
dp/dip (density-independent pixel)
sp (scale-independent pixels)
Untuk tampilan yang konsisten di handset Android terdapat satuan untuk dimensi dan ukuran dari teks yaitu : dip/dp (density- independent pixel) dan sp (scale-independent pixels). Satuan dp/dip digunakan untuk satuan dari nilai dimensi misal width (attribut : layout_width) dan height (attribut : layout_height) dari sebuah komponen view. Sementara satuan sp digunakan untuk ukuran teks. Perbedaannya dengan dp/dip,  satuan sp akan menyesuaikan ukuran teks sesuai dengan setting ukuran teks di device (yang biasa dapat di akses melalui menu settings oleh user).

 

* Contoh kasus untuk penggunaan Android unit adalah sebagai berikut:

  * Misalkan terdapat dua tablet yang memiliki ukuran layar diagonal 7-inch. Tablet pertama (A) memiliki resolusi layar 1200 x 1920px 320dpi dan yang lainnya (B) beresolusi 2048 x 1536px 326dpi.Membuat button dengan ukuran 300Ãƒâ€”300 px mungkin akan tampak normal pada  tablet A tapi akan tampak kecil di tablet B.
 
 ![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture15.png?raw=true)
 
 Akan lain cerita, jika kita spesifikasikan ukuran buttonnya dengan ukuran yang bergantung pada density layar alias menggunakan dip misal 300Ãƒâ€”300 dp. Button tersebut akan tampak sama padadevices dengan resolusi berbeda.
 
 ![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture16.png?raw=true)
 
  * Apabila kita menggunakan satuan ukuran 200dp akan dikonversi pada device mdpi (device dengan density 160dpi/dots per inch) menjadi 200px dan menjadi 400px pada device xhdpi (density 420dpi) misal pada Device /Emulator Nexus 4. Sehingga ukuran tersebut tampak sama dan konsisten secara fisik untuk beragam device dengan ukuran layar yang berbeda.
  
  ![](https://github.com/Danboru/Dicoding_Lesson5/blob/master/Picture17.png?raw=true)
  
  Standar/Konsistensi Tampilan

Aplikasi yang baik harus memiliki User Interface dan User Experience yang konsisten antar device. Ini adalah sebuah tantangan yang cukup berat di ekosistem Android yang berjalan pada beragam spesifikasi device yang tersedia di pasaran. Bacaan lebih lanjut :

http://developer.android.com/guide/practices/screens_support.html

http://developer.android.com/training/multiscreen/screendensities.html

http://dpi.lv/

https://pixplicity.com/dp-px-converter/

https://www.youtube.com/watch?v=zhszwkcay2A

https://jampasir.wordpress.com/2015/07/15/android-unit-px-pixel-dpdip-density-independent-pixel-dan-sp-scale-independent-pixels/
