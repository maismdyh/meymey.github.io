## Rangkuman Depth-First Search (DFS)

**Depth-First Search (DFS)** adalah salah satu algoritma pencarian atau penelusuran graf (baik berbentuk pohon atau graph) yang bekerja dengan menjelajahi simpul (node) sedalam mungkin sebelum kembali (*backtrack*).

### Karakteristik:

* Menggunakan **stack**, baik secara eksplisit atau melalui **rekursi**.
* Cocok untuk:

  * Menemukan jalur
  * Menelusuri seluruh node
  * Menyelesaikan masalah seperti komponen terhubung, topological sorting, dll.

### Cara Kerja:

1. Mulai dari simpul awal.
2. Kunjungi simpul tersebut dan tandai sebagai dikunjungi.
3. Lanjut ke simpul tetangga yang belum dikunjungi.
4. Jika semua tetangga sudah dikunjungi, kembali (backtrack) ke simpul sebelumnya.

### Contoh:

Misalkan graf seperti ini:

```
   A
  / \
 B   C
 |
 D
```

Urutan DFS dari A bisa menjadi:
**A → B → D → C**

### Tabel Perbandingan Singkat DFS vs BFS:

| Aspek       | DFS                    | BFS                        |
| ----------- | ---------------------- | -------------------------- |
| Struktur    | Stack / Rekursi        | Queue                      |
| Penelusuran | Sedalam mungkin        | Selebar mungkin            |
| Memori      | Biasanya lebih hemat   | Bisa lebih boros           |
| Aplikasi    | Topological sort, path | Shortest path (unweighted) |

### Kesimpulan:

DFS menjelajah graf dengan prioritas kedalaman, efisien untuk masalah yang membutuhkan pencarian jalur atau semua kemungkinan, dan mudah diimplementasikan secara rekursif.
