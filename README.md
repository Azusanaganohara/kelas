
# 📚 Discord Bot Kelas

![Discord Bot](https://your-image-link-here)  


Bot Discord ini dirancang untuk mengelola server kelas dengan fitur-fitur yang meliputi pengelolaan jadwal, tugas, musik, dan integrasi API. Semua perintah bot ini menggunakan **slash commands** (`/`), memudahkan pengguna untuk berinteraksi dengan bot secara langsung.

## 📋 Fitur Utama

### 🔧 Admin
- **/ban [user]**: Mengeluarkan user dari server.
- **/kick [user]**: Mengeluarkan user dari server.
- **/announcement [pesan]**: Mengirim pengumuman ke channel yang ditentukan.

### 🗓️ Config
- **/jadwal**: Menampilkan jadwal kelas harian atau mingguan.
- **/tugas**: Menampilkan daftar tugas yang harus dikerjakan beserta deadline-nya.
- **/tambahjadwal [kelas, hari, waktu]**: Menambahkan jadwal baru ke server.
- **/tambahtugas [nama tugas, deadline]**: Menambahkan tugas baru dengan tenggat waktu.

### 🔍 General
- **/cari-anime [judul]**: Mencari informasi anime melalui API.
- **/wikipedia [topik]**: Mencari artikel dari Wikipedia.
- **/kbbi [kata]**: Mencari arti kata dari Kamus Besar Bahasa Indonesia.
- **/help**: Menampilkan daftar perintah yang tersedia.

### 🎶 Music
- **/play [url]**: Memutar musik dari YouTube atau Spotify.
- **/pause**: Menjeda musik yang sedang diputar.
- **/resume**: Melanjutkan musik yang dijeda.
- **/stop**: Menghentikan musik dan bot keluar dari channel.
- **/volume [angka]**: Mengatur volume musik (1-100).
- **/queue**: Menampilkan daftar antrian lagu.
- **/skip**: Melewati lagu yang sedang diputar.
- **/shuffle**: Mengacak lagu di dalam antrian.

## 🛠️ Instalasi

### Persyaratan
- Node.js 16.6 atau lebih baru.
- Token dari Discord Developer Portal.
- Basis data MongoDB untuk menyimpan jadwal dan tugas.

### Langkah-Langkah Instalasi

1. Clone repo ini ke local machine kamu:
   ```bash
   git clone https://github.com/username/repo-name.git
   ```

2. Masuk ke direktori project:
   ```bash
   cd repo-name
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Sesuaikan file konfigurasi `config.js` dengan informasi bot kamu:

   ```js
   module.exports = {
       client: {
           token: 'your-discord-bot-token',
           id: 'your-discord-bot-id',
           guild: 'your-discord-guild-id',
           database: 'your-mongodb'
       },
       embed: {
           color: 0x8224e3,
       },
       api: {
           lavalink: {
               host: 'your-ip-lavalink',
               port: your-port-lavalink,
               password: 'your-pw-lavalink',
               secure: false
           },
           spotify: {
               id: 'your-id-spotify',
               secret: 'your-secret-spotify'
           }
       },
       youtube: {
           id: '',
           secret: ''
       },
       pixiv: {
           username: '',
           pw: '',
           phpsessid: ''
       },
       anilist: {
           endpoint: 'https://graphql.anilist.co'
       },
       weather: {
           weatherApiKey: ''
       }
   };
   ```

5. Jalankan bot dengan:
   ```bash
   node index.js
   ```

## 📝 Penggunaan

Setelah bot berjalan, kamu bisa menggunakan perintah `/` untuk memanfaatkan fitur-fitur bot. Misalnya:
- **/play [url]**: Memutar musik dari YouTube atau Spotify.
- **/jadwal**: Menampilkan jadwal harian atau mingguan kelas.

## 🚀 Deployment

Untuk deployment, kamu bisa menggunakan platform seperti [Heroku](https://www.heroku.com/) atau [Vercel](https://vercel.com/). 
Pastikan konfigurasi bot di `config.js` sudah benar sebelum melakukan deployment.

## 💻 Contributing

Jika kamu ingin berkontribusi pada project ini, silakan buat pull request atau buka issue.

## 📜 License

Proyek ini dilisensikan di bawah [MIT License](LICENSE).
