## Rangkuman Breadth-First Search (BFS)

**Breadth-First Search (BFS)** adalah algoritma pencarian atau traversal dalam **graf** atau **pohon** yang mengeksplorasi semua simpul tetangga terlebih dahulu (level demi level) sebelum melanjutkan ke simpul pada level berikutnya.

---

### Tujuan:

Menelusuri atau mencari elemen dalam struktur data graf atau pohon secara **melebar** (level-order traversal).

---

### Cara Kerja:

1. Mulai dari simpul awal (source node).
2. Kunjungi semua simpul tetangga langsung terlebih dahulu.
3. Gunakan **queue (antrian)** untuk menyimpan simpul yang akan dikunjungi.
4. Tandai simpul yang sudah dikunjungi agar tidak dikunjungi ulang.

---

### Ilustrasi Proses:

Misal graf:

```
    A
   / \
  B   C
 /     \
D       E
```

Urutan BFS dari A: `A → B → C → D → E`

---

### Implementasi Dasar (Pseudocode):

```
BFS(G, start):
  Buat queue Q
  Tambahkan start ke Q
  Tandai start sebagai dikunjungi

  Selama Q tidak kosong:
    node = dequeue(Q)
    Proses node
    Untuk setiap tetangga node:
      Jika belum dikunjungi:
        Tandai dan masukkan ke Q
```

---

### Tabel Ringkas:

| Komponen      | Deskripsi                                        |
| ------------- | ------------------------------------------------ |
| Struktur Data | Queue (antrian)                                  |
| Strategi      | Traversal level-by-level                         |
| Kompleksitas  | O(V + E)  → V: simpul, E: sisi                   |
| Cocok Untuk   | Pencarian jalur terpendek (graf tak berbobot)    |
| Tipe Graf     | BFS bisa digunakan pada graf berarah/tak berarah |

---

### Perbandingan DFS vs BFS:

| Aspek     | BFS                   | DFS                  |
| --------- | --------------------- | -------------------- |
| Struktur  | Queue                 | Stack/Recursion      |
| Jalur     | Pendek (tak berbobot) | Tidak dijamin pendek |
| Traversal | Level-by-level        | Depth-first          |

---

### Kesimpulan:

BFS efektif untuk pencarian jalur terpendek pada graf tak berbobot dan traversal level-order. Dengan pendekatan berbasis queue dan pengecekan kunjungan, BFS menjamin semua simpul pada level yang sama diproses sebelum lanjut ke level berikutnya.
