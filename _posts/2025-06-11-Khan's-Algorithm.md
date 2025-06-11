## Rangkuman Kahn's Algorithm

**Kahn's Algorithm** adalah algoritma yang digunakan untuk melakukan **Topological Sorting** pada **graf berarah tanpa siklus** (DAG – Directed Acyclic Graph).

### Tujuan:

Menyusun urutan simpul sedemikian rupa sehingga untuk setiap edge `u → v`, simpul `u` muncul sebelum `v` dalam urutan.

### Prinsip Kerja:

Kahn’s Algorithm menggunakan pendekatan **BFS** dan **indegree** (jumlah edge yang masuk ke suatu simpul).

### Langkah-langkah:

1. Hitung **indegree** setiap simpul.
2. Masukkan semua simpul dengan indegree = 0 ke dalam **queue**.
3. Selama queue tidak kosong:

   * Ambil simpul dari queue dan tambahkan ke urutan hasil.
   * Kurangi indegree semua tetangganya.
   * Jika indegree tetangga menjadi 0, masukkan ke queue.
4. Jika semua simpul telah diproses, maka topological sort selesai. Jika tidak, berarti ada **siklus** dalam graf.

### Contoh:

Graf:

```
A → C  
B → C  
C → D
```

Urutan topological bisa: **A, B, C, D** atau **B, A, C, D**

### Tabel Ringkas:

| Komponen       | Deskripsi                       |
| -------------- | ------------------------------- |
| Input          | Graf berarah tanpa siklus (DAG) |
| Output         | Urutan topological              |
| Teknik         | BFS + Indegree                  |
| Deteksi siklus | Jika ada node tak diproses      |

### Kesimpulan:

Kahn’s Algorithm adalah metode efisien untuk topological sorting berbasis queue dan indegree. Cocok untuk mendeteksi siklus dan menyusun urutan dependensi dalam sistem seperti penjadwalan, kompilasi, atau manajemen proyek.
