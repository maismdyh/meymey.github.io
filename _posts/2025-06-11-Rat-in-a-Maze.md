## Rangkuman Rat in a Maze 

**Rat in a Maze** adalah masalah klasik dalam algoritma **backtracking**, di mana seekor tikus harus menemukan **semua jalur** dari titik awal (biasanya kiri atas) ke tujuan (biasanya kanan bawah) dalam sebuah **papan/grid** yang berisi rintangan.

### Tujuan:

Menemukan **semua kemungkinan jalur** dari start ke end, hanya bergerak ke **arah yang diperbolehkan** (biasanya: atas, bawah, kiri, kanan), dan hanya melalui **sel yang bisa dilewati**.

### Syarat:

* Grid biasanya berupa matriks 2D berisi 0 (tidak bisa dilewati) dan 1 (bisa dilewati).
* Tikus hanya bisa bergerak ke sel yang belum dikunjungi dan nilainya 1.
* Jalur valid harus berakhir di sel tujuan (biasanya kanan bawah).

### Strategi Penyelesaian:

Menggunakan **backtracking**:

1. Mulai dari sel awal (biasanya `(0, 0)`).
2. Rekursif telusuri ke arah yang memungkinkan (kanan, bawah, kiri, atas).
3. Tandai sel yang sedang dikunjungi.
4. Jika mencapai tujuan, simpan jalur tersebut.
5. Backtrack untuk mencoba jalur alternatif.

### Contoh Matriks:

```
1 0 0 0  
1 1 0 1  
0 1 0 0  
1 1 1 1  
```

Salah satu jalur:
→ → ↓ ↓ → → (atau representasi path dalam string: `DDRDRR`)

### Tabel Ringkas:

| Komponen     | Deskripsi                                      |
| ------------ | ---------------------------------------------- |
| Input        | Matriks NxN berisi 1 (jalan) dan 0 (rintangan) |
| Output       | Semua jalur dari start ke tujuan               |
| Teknik       | Backtracking                                   |
| Kompleksitas | O(4^(N×N)) di kasus terburuk (semua 1)         |

### Kesimpulan:

Rat in a Maze adalah masalah eksplorasi semua jalur yang diselesaikan secara rekursif dengan backtracking. Cocok untuk belajar dasar pencarian jalur dan pemecahan masalah dengan constraint.
