# Praktikum8

## Diagram Class
```mermaid
classDiagram
    class Mahasiswa {
        +dict data_mahasiswa
        +lihat_data() void
        +tambah_data() void
        +ubah_data() void
        +hapus_data() void
    }
```

## Flowchart
```mermaid
flowchart TD
    A([Start]) --> B[/User Input/]
    B -->|'T'| C[/Tambah Data/]
    B -->|'U'| D[/Ubah Data/]
    B -->|'H'| E[/Hapus Data/]
    B -->|'L'| F[/Lihat Data/]
    B -->|'K'| G([End])
    
    C --> H{Data Valid?}
    H -->|Yes| I[/Tambahkan ke data_mahasiswa/]
    H -->|No| J[/Tampilkan Pesan: Data Sudah Ada/]
    I --> B
    J --> B
    
    D --> K{Nama Ditemukan?}
    K -->|Yes| L[/Tampilkan Data Lama/]
    K -->|No| M[/Tampilkan 'Nama Tidak Ditemukan'/]
    L --> N[/Input Data Baru/]
    N --> O[/Perbarui Data dan Hitung Nilai Akhir/]
    O --> B
    M --> B
    
    E --> P{Data Kosong?}
    P -->|Yes| Q[/Kembali ke Menu/]
    P -->|No| R{Nama Ditemukan?}
    R -->|Yes| S[/Hapus Data/]
    R -->|No| T[/Tampilkan 'Nama Tidak Ditemukan'/]
    S --> B
    T --> B
    Q --> B
    
    F --> U{Ada Data?}
    U -->|Yes| V[/Tampilkan Tabel Data/]
    U -->|No| W[/Tampilkan 'Tidak Ada Data'/]
    V --> B
    W --> B
    
    G --> X([Selesai])

```

## Deskripsi Program
Aplikasi Python untuk manajemen data mahasiswa yang memungkinkan pengguna melakukan operasi CRUD (Create, Read, Update, Delete) pada data mahasiswa.

## Struktur Program

### Komponen Utama
- `data_mahasiswa`: Dictionary untuk menyimpan data mahasiswa
- Fungsi utama:
  - `lihat_data()`: Menampilkan data mahasiswa
  - `tambah_data()`: Menambah data mahasiswa baru
  - `ubah_data()`: Mengubah data mahasiswa
  - `hapus_data()`: Menghapus data mahasiswa

### Alur Kerja Program
1. Pengguna memilih menu (Tambah/Ubah/Hapus/Lihat/Keluar)
2. Program mengeksekusi fungsi sesuai pilihan
3. Data disimpan dalam dictionary `data_mahasiswa`

## Perhitungan Nilai
- Nilai Akhir = (Tugas * 0.3) + (UTS * 0.35) + (UAS * 0.35)
- Bobot:
  - Tugas: 30%
  - UTS: 35%
  - UAS: 35%

## Fitur Khusus
- Validasi input mencegah duplikasi NIM
- Fleksibilitas update data
- Tampilan data dalam format tabel
- Perhitungan otomatis nilai akhir

## Cara Penggunaan
- Jalankan script
- Pilih opsi menu:
  - `T`: Tambah data
  - `U`: Ubah data
  - `H`: Hapus data
  - `L`: Lihat data
  - `K`: Keluar program

