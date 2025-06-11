## Rangkuman Subset Sum 

**Subset Sum Problem** adalah masalah klasik dalam pemrograman dinamis dan teori himpunan. Tujuannya adalah untuk menentukan apakah dari suatu himpunan bilangan bulat, terdapat **subset (subhimpunan)** yang jumlah elemen-elemennya sama dengan **target tertentu**.

### Tujuan:

Menentukan apakah ada subset dari array `S` yang jumlahnya **sama dengan nilai target `T`**.

---

### Contoh Soal:

**Input**:

* Array = `{3, 34, 4, 12, 5, 2}`
* Target = `9`
  **Output**:
* **True** (karena subset `{4, 5}` atau `{3, 2, 4}` jumlahnya 9)

---

### Metode Penyelesaian:

#### 1. **Brute Force (Backtracking)**

* Mencoba semua kemungkinan subset → kompleksitas eksponensial.

#### 2. **Dynamic Programming (DP)**

* Menggunakan tabel `dp[i][j]` → apakah mungkin membuat jumlah `j` dengan elemen dari indeks `0` sampai `i`.

---

### Tabel DP Contoh:

Misal: `S = {2, 3, 7, 8, 10}`, `T = 11`

| i (elemen ke-i) | 0 | 1 | 2 | 3 | 4  |
| --------------- | - | - | - | - | -- |
| Nilai           | 2 | 3 | 7 | 8 | 10 |

Kita bangun tabel `dp[n+1][sum+1]` (n = banyak elemen, sum = target).
`dp[i][j] = True` jika ada subset dari elemen ke-0 sampai ke-i yang jumlahnya `j`.

---

### Kompleksitas Waktu:

| Teknik        | Kompleksitas Waktu |
| ------------- | ------------------ |
| Backtracking  | O(2ⁿ)              |
| Dynamic Prog. | O(n × sum)         |

---

### Tabel Ringkas:

| Komponen | Deskripsi                                              |
| -------- | ------------------------------------------------------ |
| Input    | Array bilangan bulat dan nilai target                  |
| Output   | `True` atau `False` (apakah subset jumlahnya = target) |
| Teknik   | DP / Rekursi / Backtracking                            |
| Aplikasi | Kriptografi, optimasi, masalah partisi, dll.           |

---

### Kesimpulan:

Subset Sum Problem menguji apakah sebuah jumlah target dapat dibentuk dari elemen-elemen dalam array. Solusi optimal menggunakan **Dynamic Programming**, yang efisien untuk kasus dengan target dan jumlah elemen yang tidak terlalu besar.
