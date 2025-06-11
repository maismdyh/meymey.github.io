## Rangkuman Dijkstra's Algorithm

**Dijkstra's Algorithm** adalah algoritma yang digunakan untuk mencari **jarak terpendek** dari satu **simpul sumber** ke semua simpul lain dalam sebuah **graf berbobot dengan bobot non-negatif**.

### Tujuan:

Menemukan **shortest path** dari sumber ke simpul lain dalam graf berbobot.

### Syarat:

* Graf bisa berbentuk berarah atau tak berarah.
* Semua bobot edge **harus ≥ 0** (tidak boleh negatif).

### Cara Kerja:

1. Inisialisasi jarak semua simpul ke **tak hingga (∞)**, kecuali simpul sumber = 0.
2. Gunakan **priority queue** (atau min-heap) untuk memilih simpul dengan jarak terkecil yang belum diproses.
3. Untuk setiap tetangga dari simpul saat ini:

   * Hitung jarak baru melalui simpul saat ini.
   * Jika jarak baru lebih kecil, perbarui jaraknya.
4. Ulangi hingga semua simpul telah diproses.

### Contoh Graf:

```
     (2)
A -------- B
|          |
(1)       (3)
|          |
C -------- D
     (4)
```

Dijkstra dari A:

| Simpul | Jarak dari A |
| ------ | ------------ |
| A      | 0            |
| B      | 2            |
| C      | 1            |
| D      | 5            |

### Tabel Ringkas:

| Komponen     | Deskripsi                         |
| ------------ | --------------------------------- |
| Input        | Graf berbobot, bobot ≥ 0          |
| Output       | Jarak terpendek dari sumber       |
| Teknik       | Greedy, Priority Queue / Min-Heap |
| Kompleksitas | O((V + E) log V) dengan heap      |

### Kesimpulan:

Dijkstra’s Algorithm adalah metode efisien untuk menemukan jalur terpendek di graf berbobot non-negatif. Sangat berguna dalam pemetaan, jaringan, dan sistem navigasi.
