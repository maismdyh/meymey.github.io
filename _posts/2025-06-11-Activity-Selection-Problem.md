## Rangkuman Activity Selection Problem

**Activity Selection Problem** adalah masalah penjadwalan klasik yang bertujuan untuk **memilih sebanyak mungkin aktivitas** yang **tidak saling tumpang tindih**, dari sekumpulan aktivitas yang masing-masing memiliki waktu mulai dan waktu selesai.

### Tujuan:

Memaksimalkan jumlah aktivitas yang dapat dilakukan **tanpa konflik waktu**.

### Syarat:

* Setiap aktivitas memiliki waktu mulai (`start`) dan selesai (`finish`).
* Hanya satu aktivitas yang bisa dilakukan dalam satu waktu.

### Strategi Penyelesaian:

Menggunakan **Greedy Algorithm**:

1. **Urutkan aktivitas berdasarkan waktu selesai (finish time)** secara menaik.
2. Pilih aktivitas pertama (dengan waktu selesai paling awal).
3. Untuk aktivitas berikutnya, pilih hanya jika waktu mulainya **≥ waktu selesai aktivitas terakhir yang dipilih**.
4. Ulangi hingga semua aktivitas dipertimbangkan.

### Contoh:

| Aktivitas | Mulai | Selesai |
| --------- | ----- | ------- |
| A1        | 1     | 4       |
| A2        | 3     | 5       |
| A3        | 0     | 6       |
| A4        | 5     | 7       |
| A5        | 8     | 9       |
| A6        | 5     | 9       |

Urut berdasarkan selesai → A1, A2, A4, A5

Aktivitas terpilih (tanpa tumpang tindih): **A1, A4, A5**

### Tabel Ringkas:

| Komponen     | Deskripsi                                 |
| ------------ | ----------------------------------------- |
| Input        | Daftar aktivitas (start & finish)         |
| Output       | Subset aktivitas maksimum tanpa konflik   |
| Teknik       | Greedy (berdasarkan waktu selesai)        |
| Kompleksitas | O(n log n) untuk pengurutan, O(n) seleksi |

### Kesimpulan:

Activity Selection Problem diselesaikan optimal dengan pendekatan greedy, yaitu selalu memilih aktivitas dengan waktu selesai paling awal yang tidak konflik. Efisien untuk penjadwalan, perencanaan tugas, dan manajemen sumber daya.
