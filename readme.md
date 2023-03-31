# Nama : Muhamad Alfito Santosa (tim : FE-8)

# Penjelasan

## Jawaban Nomor 1

### Soal :

1. Kita sudah mengetahui bahwa banyaknya user maksimal adalah 100.
   Buat sebuah program yang menampilkan teks ‘User ke - 1 … User ke - 100’ pada setiap baris di halaman HTML.
   Lakukan FOR LOOP pada Javascript.

### Jawaban :

jawaban tertera pada file [Jawaban Nomor 1.html](https://github.com/alfitosantosa/LoopingBersamaMasTata/nomerSatu.html "Github Alfito")

**Penjelasan ada pada comment pada kode berikut : **

```html
<h2>Jumlah User</h2>
<ul id="list"></ul>

<script>
  // Mengambil elemen ul #list
  const list = document.getElementById("list");

  // input nilai ke variabel user
  let user = 100;

  // Lakukan perulangan berdasarkan jumlah user
  for (let i = 1; i <= 100; i++) {
    list.innerHTML += `<li>user ke :${i}</li>`;
    // console.log(`<li>user ke :${i}<li>`);
  }
</script>
```

## Jawaban Nomor 2

### Soal :

2. Lakukan pengulangan menggunakan FOR LOOP untuk melakukan penambahan nilai sebanyak 10 kali.

- Nilai awal = 0
- Pengulangan = 10 kali
- Nilai awal ditambah 2 setiap pengulangan
- Tampilan hasil penambahan pada setiap pengulangan

### Jawaban :

jawaban tertera pada file [Jawaban Nomor 2.html](https://github.com/alfitosantosa/LoopingBersamaMasTata/nomerDua.html "Github Alfito")

**Penjelasan ada pada comment pada kode berikut : **

```html
<script>
  // input nilai awal ke variabel nilai awal
  let nilaiAwal = 0;

  // lakukan perulangan sebanyak 10
  for (let i = 1; i <= 10; i++) {
    // setiap perulangan nilai awal di tambah 2
    nilaiAwal += 2;
    // menampilkan perulangan dan total nilai awal
    console.log(`perulangan ke ${i} \nnilai awal = ${nilaiAwal}`);
  }
</script>
```

## Jawaban Nomor 3

### Soal :

3.  Lakukan pengulangan dengan FOR LOOP yang melakukan iterasi dari 0..20.

- Setiap iterasi/pengulangan lakukan pengecekan apakah nilai tersebut ganjil atau genap.
- Tampilkan keterangan ganjil dan genap pada sebuah nilai setiap pengulangan

### Jawaban :

jawaban tertera pada file [Jawaban Nomor 3.html](https://github.com/alfitosantosa/LoopingBersamaMasTata/nomerTiga.html "Github Alfito")

**Penjelasan ada pada comment pada kode berikut : **

```html
<script>
  // lakukan perulangan sebanyak 20
  for (let i = 1; i <= 20; i++) {
    // setiap perulangan melakukan pengecekan apakah perulangan ganjil atau genap lalu menampilkan nya
    i % 2 == 0
      ? console.log(`Perulangan Ke ${i} adalah genap`)
      : console.log(`Perulangan Ke ${i} adalah ganjil`);
  }
</script>
```

## Jawaban Nomor 4

### Soal :

4. Tampilkan sebuah Konfirmasi Pop Up kepada user menggunakan confirm();
   -Berikan teks ‘Apakah anda mau mengulang’ pada box confirm
   -Jika user memilih ‘OK’ maka program akan terus menampilan pop up yang sama
   -Jika user memilih ‘Cancel’ maka program akan menampilkan teks ‘Perulangan sudah dilakukan sebanyak …(jumlah klik OK yang dilakukan user)

### Jawaban :

jawaban tertera pada file [Jawaban Nomor 4.html](https://github.com/alfitosantosa/LoopingBersamaMasTata/nomerEmpat.html "Github Alfito")

**Penjelasan ada pada comment pada kode berikut : **

```html
<script>
  // mendeklarasikan variabel jumlah perulangan
  let perulangan = 0;

  // Mendeklarasikan variabel lagi dengan nilai true
  let lagi = true;

  // melakukan perulangan jika nilai lagi adalah true
  while (lagi) {
    perulangan++;
    // menampilkan confirm dan menyimpan hasilnya ke variable mau
    let mau = confirm("Apakah anda mau mengulang");
    // melakukan pengecekan nilai variabel mau
    mau == true ? (lagi = true) : (lagi = false);
  }
  // menampilkan jumlah perulangan
  alert(`perulangan sudah dilakukan sebanyak : ${perulangan}`);
</script>
```

## Jawaban Nomor 5

### Soal :

5. Buat sebuah program kuis.
   Tampilkan prompt() untuk meminta inputan dari user. Tampilan teks ‘Sebutkan kepanjangan dari nama IB (Impact Byte)?’

- Lakukan pengecekan apakah jawaban dari user sudah benar
- Jika benar, tampilkan alert ‘Selamat jawaban kamu benar’
- Jika salah, lakukan pengulangan untuk menampilkan prompt() yg sama hingga jawaban dari user benar

### Jawaban :

jawaban tertera pada file [Jawaban Nomor 5.html](https://github.com/alfitosantosa/LoopingBersamaMasTata/nomerLima.html "Github Alfito")

**Penjelasan ada pada comment pada kode berikut : **

```html
<script>
  // Mendeklarasikan variabel benar dengan nilai true
  let benar = true;

  // melakukan perulangan jika variabel benar bernilai true
  while (benar) {
    // menampilkan prompt
    let jawabanUser = prompt("Apa kepanjangan dari IB? (Impact Byte)");

    //   mengkonversi jawaban user menjadi huruf kecil
    jawabanUser = jawabanUser.toLowerCase();
    //   menlakukan pengkondisian jawaban benar atau salah
    if (jawabanUser == "impact byte") {
      // kalau benar, maka variabel benar akan bernilai false. sehingga akan keluar dari perulangan
      benar = false;
    } else {
      // kalau salah akan menampilkan alert salah
      alert("Jawaban kamu salah");
    }
  }

  // setelah benar dan keluar dari perulangan. maka akan menampilkan alert jawaban benar
  alert("SELAMAT JAWABAN KAMU BENAR");
</script>
```
