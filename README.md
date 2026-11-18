# Tugas Docker Minggu 9: Kontainerisasi Halaman Profil

Tugas rumah mata kuliah Teknologi Open Source. Halaman profil statis (HTML) dibungkus menjadi image Docker berbasis `nginx:alpine`, lalu dijalankan sebagai container.

- Nama: Richardo Takanyuai
- NIM: 202557201005
- Kelas: A

## Isi Repositori
- `index.html`: halaman profil
- `Dockerfile`: resep pembuatan image
- `README.md`: dokumen proyek
- `screenshot.png`: tampilan halaman profil

## Cara Build

```bash
docker build -t profil-richardo:1.0 .
```

## Cara Run

```bash
docker run -d --name profil-richardo -p 8082:80 profil-richardo:1.0
```

Buka http://localhost:8082 di browser.

## Cara Menghentikan dan Membersihkan

```bash
docker stop profil-richardo
docker rm profil-richardo
docker rmi profil-richardo:1.0
```

## Screenshot

![Halaman profil](screenshot.png)
