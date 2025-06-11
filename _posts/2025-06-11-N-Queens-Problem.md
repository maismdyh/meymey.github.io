## Rangkuman N-Queens Problem

**N-Queens Problem** adalah masalah klasik dalam bidang algoritma dan backtracking. Tujuannya adalah menempatkan **N buah ratu (queen)** di atas papan catur berukuran **N x N** sehingga **tidak ada dua ratu yang saling menyerang**.

### Syarat:

* Setiap ratu hanya boleh berada **satu kali** di setiap baris dan kolom.
* Tidak boleh ada dua ratu yang berada pada **diagonal yang sama**.

### Strategi Penyelesaian:

Menggunakan pendekatan **backtracking**:

1. Tempatkan satu ratu di baris tertentu.
2. Cek apakah posisi tersebut aman (tidak diserang ratu lain).
3. Jika aman, lanjut ke baris berikutnya.
4. Jika tidak ada posisi yang aman, **backtrack** ke baris sebelumnya dan coba posisi lain.

### Contoh (N = 4):

Salah satu solusi:

```
. Q . .
. . . Q
Q . . .
. . Q .
```

Ratu (`Q`) tidak saling menyerang secara horizontal, vertikal, atau diagonal.

### Tabel Ringkas:

| N | Jumlah Solusi Unik |
| - | ------------------ |
| 1 | 1                  |
| 2 | 0                  |
| 3 | 0                  |
| 4 | 2                  |
| 5 | 10                 |
| 8 | 92                 |

### Kesimpulan:

N-Queens Problem adalah masalah penempatan dengan kendala (constraint), yang diselesaikan secara sistematis menggunakan backtracking untuk menjelajahi semua konfigurasi yang memungkinkan.
