Berikut adalah rangkuman tentang **Fractional Knapsack** dalam bentuk ringkas dan menggunakan tabel untuk memperjelas:

---

## Rangkuman Fractional Knapsack

**Fractional Knapsack** adalah versi dari masalah knapsack di mana item dapat diambil sebagian (tidak harus utuh). Tujuannya adalah memaksimalkan total nilai (value) yang bisa dimasukkan ke dalam knapsack dengan kapasitas terbatas. Masalah ini diselesaikan dengan pendekatan greedy, bukan dynamic programming seperti pada 0/1 Knapsack.

### Langkah Penyelesaian:

1. Hitung nilai per unit berat (value/weight) untuk setiap item.
2. Urutkan item berdasarkan nilai per unit berat tertinggi.
3. Ambil item sebanyak mungkin sesuai kapasitas, mulai dari yang nilai per unit tertinggi.
4. Jika item tidak bisa diambil seluruhnya, ambil sebagian sampai kapasitas habis.

### Contoh Tabel Item:

| Item | Value | Weight | Value/Weight |
| ---- | ----- | ------ | ------------ |
| A    | 60    | 10     | 6.0          |
| B    | 100   | 20     | 5.0          |
| C    | 120   | 30     | 4.0          |

Misalnya kapasitas knapsack = 50. Maka:

* Ambil seluruh item A (10 kg)
* Ambil seluruh item B (20 kg)
* Ambil 2/3 dari item C (20 dari 30 kg)

Total value = 60 (A) + 100 (B) + 80 (2/3 dari 120) = **240**

### Kesimpulan:

Fractional Knapsack lebih efisien karena item bisa diambil sebagian, dan penyelesaiannya optimal dengan algoritma greedy berdasarkan nilai per berat tertinggi.
