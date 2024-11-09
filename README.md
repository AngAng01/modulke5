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
   Program di atas adalah program rekursif yang mencetak urutan angka dari n sampai 1, kemudian kembali mencetak angka dari 1 sampai n. Program ini menggunakan dua cetakan untuk membentuk pola simetris dalam keluaran.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi rekursif yang mencetak angka dari n hingga 1, lalu kembali ke n untuk membentuk pola simetris maju-mundur.
      - Meminta input n, lalu memanggil buatUrutan untuk mencetak pola sesuai nilai n.
      
      
   ## Code Explanation
   ```go
	func buatUrutan(n, current int) {
		fmt.Print(current, " ")
	
		if current == 1 {
			return
		}
	
		buatUrutan(n, current-1)
	
		fmt.Print(current, " ")
	}
   ```
   Kode di atas adalah fungsi rekursif dalam bahasa Go yang mencetak urutan angka dari nilai current hingga 1, lalu kembali mencetak dari 1 hingga current.
   
   ```go
     var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
      fmt.Print("Masukkan nilai N : ")
      fmt.Scan(&n)
   ```
   Kode di atas adalah kode yang digunakan untuk meminta input dari pengguna dan menyimpannya dalam variabel n. 
   
   ```go
      fmt.Println(n)
   ```
   Kode fmt.Println(n) digunakan untuk mencetak nilai variabel n ke layar, diikuti dengan pemindahan baris (newline).

   ```go
      buatUrutan(n, n)
      fmt.Println() 
   ```
   Kode di atas adalah kode yang memanggil fungsi buatUrutan dan mencetak urutan angka berdasarkan nilai n yang dimasukkan pengguna, diikuti dengan baris kosong.

   
   ## SOAL 5
   Program di atas adalah program yang mencetak deret angka ganjil dari 1 hingga nilai n yang dimasukkan oleh pengguna. Program ini menggunakan fungsi rekursif untuk menghasilkan deret angka ganjil dalam rentang yang ditentukan.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi buatDeretGanjil, Fungsi rekursif yang mencetak deret angka ganjil dari 1 hingga nilai n. Fungsi ini memeriksa apakah angka saat ini (current) ganjil, dan jika ya, mencetaknya. Rekursi berlanjut dengan menambah current hingga mencapai n.
      - Fungsi utama yang menginisialisasi program. Program meminta input n dari pengguna, kemudian memanggil fungsi buatDeretGanjil untuk mencetak deret angka ganjil hingga n.
      
      
   ## Code Explanation
   ```go
	func buatDeretGanjil(n, current int) {
		if current > n {
			return
		}
	
		if current % 2 != 0 {
			fmt.Print(current, " ")
		}
	
		buatDeretGanjil(n, current+1)
	}
   ```
   Kode di atas adalah fungsi rekursif yang mencetak deret angka ganjil dari 1 hingga nilai n. Fungsi ini bekerja dengan menambah nilai current secara bertahap dan mencetak angka tersebut hanya jika ganjil.
   
   ```go
     var n int
   ```
   Kode var n int digunakan untuk mendeklarasikan sebuah variabel bernama n dengan tipe data integer (int).

   ```go
      fmt.Print("Masukkan nilai N : ")
      fmt.Scan(&n)
   ```
   Kode di atas adalah kode yang digunakan untuk meminta input dari pengguna dan menyimpannya dalam variabel n. 
   
   ```go
      fmt.Println(n)
   ```
   Kode fmt.Println(n) digunakan untuk mencetak nilai variabel n ke layar, diikuti dengan pemindahan baris (newline).

   ```go
      buatDeretGanjil(n, 1)
      fmt.Println() 
   ```
   Kode di atas adalah kode yang memanggil fungsi rekursif buatDeretGanjil dan mencetak deret angka ganjil dari 1 hingga n. 


   ## SOAL 6
   Program di atas adalah program yang menghitung hasil perpangkatan (pangkat) menggunakan pendekatan rekursi. Fungsi Pangkat menerima dua parameter, yaitu n1 sebagai basis dan n2 sebagai pangkat, lalu menghitung hasil dari n1^n2.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Fungsi Pangkat, Fungsi rekursif untuk menghitung hasil perpangkatan (n1^n2). Jika n2 == 0, mengembalikan 1. Jika tidak, memanggil dirinya sendiri dengan n2-1.
      - Mengambil input dua angka (n1 dan n2) dari pengguna, kemudian memanggil fungsi Pangkat dan mencetak hasilnya.
      
      
   ## Code Explanation
   ```go
	func Pangkat(n1, n2 int) int {
		if n2 == 0 {
			return 1 
		}
		return n1 * Pangkat(n1, n2-1) 
	}
   ```
   Kode di atas adalah fungsi rekursif yang menghitung hasil perpangkatan (pangkat) dari dua bilangan, yaitu n1 (basis) dan n2 (pangkat). Fungsi ini menghitung n1^n2 (basis dipangkatkan ke pangkat) menggunakan pendekatan rekursi.
   
   ```go
     var n1, n2 int
   ```
   Kode di atas adalah deklarasi variabel yang mendeklarasikan dua variabel bertipe int, yaitu n1 dan n2. Variabel ini nantinya digunakan untuk menyimpan nilai yang diberikan oleh pengguna.

   
   ```go
      fmt.Scan(&n1, &n2)
   ```
Kode di atas adalah kode yang digunakan untuk membaca input dari pengguna dan menyimpannya ke dalam variabel n1 dan n2. 


   ```go
      fmt.Println("Hasil :", Pangkat(n1, n2))
   ```
   Kode di atas adalah kode yang digunakan untuk mencetak hasil dari fungsi Pangkat(n1, n2) ke layar, bersama dengan teks "Hasil :". 
