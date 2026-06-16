# Sistem Pemungutan Suara Digital (E-Voting) — Go CLI

![go](https://img.shields.io/badge/go-%3E%3D1.18-00ADD8) ![License](https://img.shields.io/badge/License-MIT-yellow)

Aplikasi CLI untuk sistem pemungutan suara digital berbasis Go dengan fitur lengkap untuk mengelola data kandidat, data pemilih, proses voting, hingga statistik hasil pemilihan.

## 🚀 Fitur Utama

### 📋 Modul Kelola Kandidat

- CRUD data kandidat (nomor urut, nama, visi-misi, jumlah suara)
- Validasi duplikasi nomor urut
- Hapus dengan penggeseran array
- Tampilan tabel rapi

### 🗳️ Modul Kelola Pemilih

- CRUD data pemilih (ID, nama, status memilih)
- Validasi duplikasi ID pemilih
- Status sudah/belum memilih
- Pencegahan pemilihan ganda

### ✅ Modul Voting & Statistik

- Proses voting dengan validasi berlapis
- Pencatatan waktu voting otomatis
- Persentase suara tiap kandidat
- Penentuan kandidat dengan suara terbanyak

### 🔍 Modul Sorting & Searching

- Sorting kandidat by jumlah suara (Selection Sort)
- Sorting kandidat by nomor urut (Insertion Sort)
- Pencarian by nomor urut (Sequential Search)
- Pencarian cepat by nomor urut (Binary Search)

## 🛠️ Teknologi

- **Bahasa**: Go 1.18+
- **Struktur Data**: Array statis + struct
- **Algoritma**:
  - Selection Sort (berdasarkan jumlah suara)
  - Insertion Sort (berdasarkan nomor urut)
  - Sequential Search (nomor urut)
  - Binary Search (nomor urut, data terurut)

## 📥 Instalasi

1. Pastikan Go terinstall:

```
go version
```

2. Clone repo:

```
git clone https://github.com/username/e-voting.git
```

3. Jalankan program:

```
cd e-voting
go run .
```

> Catatan: gunakan `go run .` (bukan `go run main.go`) karena program terdiri dari banyak file dalam satu package.

## 💻 Penggunaan

```
Menu Utama:
1. Kelola Kandidat
2. Kelola Pemilih
3. Voting
4. Statistik Hasil Voting
5. Sorting Data Kandidat
6. Searching Kandidat
0. Keluar
```

## 📂 Struktur File

```
├── main.go                 # Titik masuk program
├── model.go                # Definisi struct & variabel global
├── menu.go                 # Semua tampilan menu & navigasi
├── helper.go               # Fungsi utilitas (input, validasi, tampilan)
├── crud_kandidat.go        # CRUD data kandidat
├── crud_pemilih.go         # CRUD data pemilih
├── voting.go               # Proses voting
├── statistik.go            # Statistik hasil voting
├── sorting_searching.go    # Algoritma sorting & searching
├── dummy.go                # Data awal (dummy)
├── go.mod                  # Konfigurasi modul Go
└── README.md               # Dokumentasi
```

## 🧪 Testing

Program sudah dilengkapi data dummy:

- 4 data kandidat
- 6 data pemilih
- 3 suara awal sudah tercatat

## 🤝 Kontribusi

Pull request dipersilakan. Untuk perubahan besar, buka issue terlebih dahulu.

## 📜 Lisensi

MIT © 2025 Dawuh
