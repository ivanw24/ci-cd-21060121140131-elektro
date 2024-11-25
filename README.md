# CI/CD dengan GitHub Actions

Ini adalah proyek yang mengimplementasikan **Continuous Integration (CI)** dan **Continuous Deployment (CD)** menggunakan **GitHub Actions** untuk deploy aplikasi Node.js ke **GitHub Pages**.

## Deskripsi Proyek

Proyek ini adalah aplikasi Node.js sederhana yang dijalankan di port 3000 dan mengembalikan pesan "Hello, GitHub Actions!" saat diakses. Proyek ini juga dilengkapi dengan pengujian menggunakan **Jest** dan **Supertest**.

## Proses CI/CD

### **Continuous Integration (CI)**

Proses CI dimulai setiap kali ada perubahan (push atau pull request) di branch `main`. Workflow CI melakukan hal berikut:

1. **Checkout Kode**: Mengambil kode terbaru dari repository.
2. **Setup Node.js**: Mengatur lingkungan Node.js versi 16.
3. **Install Dependensi**: Menginstal dependensi yang diperlukan untuk proyek.
4. **Menjalankan Pengujian**: Menjalankan pengujian otomatis menggunakan Jest untuk memastikan aplikasi berjalan dengan benar.

Workflow CI dijalankan pada sistem operasi **Ubuntu** dengan menggunakan GitHub Actions.

### **Continuous Deployment (CD)**

Setelah pipeline CI berhasil dijalankan, branch `gh-pages` secara otomatis dibuat dan konten aplikasi dideploy ke **GitHub Pages**. GitHub Pages kemudian digunakan untuk menampilkan aplikasi secara langsung di web.

Proses CD dilakukan dengan langkah-langkah berikut:

1. **Checkout Kode**: Mengambil kode dari repository.
2. **Setup Node.js**: Mengatur lingkungan Node.js.
3. **Build Aplikasi**: Membuat file statis yang dibutuhkan untuk GitHub Pages.
4. **Deploy ke GitHub Pages**: File hasil build dipindahkan ke branch `gh-pages` dan diterbitkan ke halaman web.

### **Link Hasil Deployment**

Setelah deployment selesai, aplikasi dapat diakses melalui GitHub Pages pada link berikut:

[**Link ke GitHub Pages**](https://ivanw24.github.io/ci-cd-21060121140131-elektro/)

### **Cara Menjalankan Proyek Secara Lokal**

Untuk menjalankan aplikasi ini di mesin lokal Anda:

1. Clone repository:
   ```bash
   git clone https://github.com/ivanw24/ci-cd-21060121140131-elektro.git
   cd ci-cd-21060121140131-elektro
