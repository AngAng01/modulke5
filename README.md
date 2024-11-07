# MODUL LIMA
 ## SOAL 1
   Program di atas adalah program recursive yang digunakan untuk menghitung deret Fibonacci. Fungsi fibonacci menggunakan rekursi untuk menghitung nilai Fibonacci dari suatu bilangan n, yaitu jumlah dari dua angka sebelumnya dalam deret Fibonacci.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi fibonacci(n int) int, Menghitung nilai Fibonacci untuk n secara rekursif.
      - Paket fmt, Digunakan untuk mencetak hasil ke layar menggunakan fmt.Printf.
      
   ## Code Explanation
   ```go
   func fibonacci(n int) int {
		`if n <= 1 {
		 	return n
		 }
		 return fibonacci(n-1) + fibonacci(n-2)
	}
   ```
   Kode di atas adalah fungsi rekursif untuk menghitung nilai Fibonacci dari bilangan n. Fungsi fibonacci menerima satu parameter integer n dan mengembalikan nilai Fibonacci yang sesuai. 
   
   ```go
      for i := 0; i <= 10; i++ {
	        fmt.Printf("Fibonacci(%d) = %d\n", i, fibonacci(i))
	    }
   ```
   Kode di atas adalah Fungsi permutasi yang digunakan untuk menghitung permutasi dari n elemen yang diambil sebanyak r. Fungsi ini pertama-tama menghitung faktorial dari n (disimpan dalam variabel pembilang) dan faktorial dari n - r (disimpan dalam variabel penyebut) dengan memanfaatkan fungsi factorial. 
   

  ## SOAL 2
   Program di atas adalah program rekursif yang digunakan untuk mencetak pola segitiga bintang dengan jumlah baris yang ditentukan oleh pengguna. Program ini memiliki dua fungsi rekursif utama, cetakBintang dan cetakPola.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi cetakBintang(n int), Fungsi rekursif yang mencetak n bintang dalam satu baris. Jika n bernilai 0, fungsi berhenti.
      - Fungsi cetakPola(n, current int), Fungsi rekursif yang mencetak pola segitiga dengan n baris, di mana setiap baris memiliki jumlah bintang yang sesuai dengan nilai current. Fungsi ini memanggil cetakBintang untuk mencetak bintang pada tiap baris dan kemudian memanggil dirinya sendiri untuk baris berikutnya.
      
   ## Code Explanation
   ```go
   func cetakBintang(n int) {
	    if n == 0 {
	        return
	    }
	    fmt.Print("*")
	    cetakBintang(n - 1)
}
   ```
   Kode di atas adalah fungsi rekursif untuk mencetak sejumlah karakter bintang (*) dalam satu baris.
   
   ```go
      func cetakPola(n, current int) {
	    if current > n {
	        return
	    }
	    cetakBintang(current)
	    fmt.Println()
	    cetakPola(n, current + 1)
}
   ```
   Kode di atas adalah fungsi rekursif bernama cetakPola yang digunakan untuk mencetak pola segitiga bintang dengan jumlah baris n. Fungsi ini memanfaatkan fungsi cetakBintang untuk mencetak bintang pada setiap baris dengan jumlah yang meningkat secara bertahap.

   ```go
       var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
      fmt.Scan(&n)
   ```
   Kode fmt.Scan(&n) digunakan untuk membaca input dari pengguna dan menyimpannya ke dalam variabel n.
   
   ```go
      cetakPola(n, 1)
   ```
   Kode di atas adalah kode untuk memanggil fungsi cetakPola, yang mencetak pola segitiga bintang dengan jumlah baris sesuai nilai n. Pemanggilan cetakPola(n, 1) menginisiasi proses rekursif untuk mencetak baris-baris bintang bertingkat.


   ## SOAL 3
   Program di atas adalah program yang digunakan untuk mencetak faktor-faktor dari sebuah bilangan bulat positif secara rekursif.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi Factors(n, i int): Fungsi rekursif yang mencari dan mencetak faktor-faktor dari bilangan n mulai dari i. Jika n % i == 0, maka i adalah faktor dari n, dan fungsi memanggil dirinya sendiri untuk memeriksa angka berikutnya.
      - Fungsi utama yang meminta input bilangan bulat positif dari pengguna, kemudian memanggil fungsi Factors(n, 1) untuk memulai pencarian faktor-faktor dari bilangan tersebut.
      
   ## Code Explanation
   ```go
   func Factors(n, i int) {
	    if i > n {
	        return
	    }
	    if n%i == 0 {
	        fmt.Print(i, " ")
	    }
	    Factors(n, i+1)
}
   ```
   Kode di atas adalah kode untuk mendeklarasikan fungsi Factors yang digunakan untuk mencari dan mencetak faktor-faktor dari suatu bilangan n secara rekursif. Fungsi ini memeriksa apakah setiap angka mulai dari i hingga n adalah faktor dari n, dan jika ya, mencetak angka tersebut.
   
   ```go
     var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
       var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
      fmt.Print("Masukkan bilangan bulat positif : ")
      fmt.Scan(&n)
   ```
   Kode di atas adalah kode yang digunakan untuk meminta input dari pengguna dan menyimpannya dalam variabel n. 
   
   ```go
      fmt.Println(n)
   ```
   Kode fmt.Println(n) digunakan untuk mencetak nilai variabel n ke layar, diikuti dengan pemindahan baris (newline).

   ```go
      Factors(n, 1)
      fmt.Println()
   ```
   Kode di atas adalah pemanggilan fungsi Factors(n, 1) dan kemudian mencetak baris baru menggunakan fmt.Println().


   ## SOAL 4
   rogram di atas adalah program dalam yang mencetak urutan angka dari n hingga 1 secara rekursif, dan kemudian mencetak urutan angka dari 1 hingga n setelahnya. Program ini menggunakan fungsi rekursif untuk membangun urutan tersebut.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi Factors(n, i int): Fungsi rekursif yang mencari dan mencetak faktor-faktor dari bilangan n mulai dari i. Jika n % i == 0, maka i adalah faktor dari n, dan fungsi memanggil dirinya sendiri untuk memeriksa angka berikutnya.
      - Fungsi utama yang meminta input bilangan bulat positif dari pengguna, kemudian memanggil fungsi Factors(n, 1) untuk memulai pencarian faktor-faktor dari bilangan tersebut.
      
   ## Code Explanation
   ```go
   func Factors(n, i int) {
	    if i > n {
	        return
	    }
	    if n%i == 0 {
	        fmt.Print(i, " ")
	    }
	    Factors(n, i+1)
}
   ```
   Kode di atas adalah kode untuk mendeklarasikan fungsi Factors yang digunakan untuk mencari dan mencetak faktor-faktor dari suatu bilangan n secara rekursif. Fungsi ini memeriksa apakah setiap angka mulai dari i hingga n adalah faktor dari n, dan jika ya, mencetak angka tersebut.
   
   ```go
     var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
       var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
      fmt.Print("Masukkan bilangan bulat positif : ")
      fmt.Scan(&n)
   ```
   Kode di atas adalah kode yang digunakan untuk meminta input dari pengguna dan menyimpannya dalam variabel n. 
   
   ```go
      fmt.Println(n)
   ```
   Kode fmt.Println(n) digunakan untuk mencetak nilai variabel n ke layar, diikuti dengan pemindahan baris (newline).

   ```go
      Factors(n, 1)
      fmt.Println()
   ```
   Kode di atas adalah pemanggilan fungsi Factors(n, 1) dan kemudian mencetak baris baru menggunakan fmt.Println().

   
