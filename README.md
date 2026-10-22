# Masakan Kekinian (msknkkn)

**Live: https://msknkkn.xsrazy.web.id**

Masakan Kekinian adalah website pencarian resep masakan. Pengunjung bisa mencari resep berdasarkan kata kunci, menelusuri resep berdasarkan jenis makanan, melihat daftar makanan populer, lalu membuka detail resep lengkap dengan bahan dan langkah memasaknya. Semua data resep berasal dari Spoonacular API dan ditampilkan dalam Bahasa Inggris sesuai data aslinya, sementara situs ini ditujukan terutama untuk pengguna Indonesia yang mencari ide masakan.

> Repo ini adalah repo dokumentasi (showcase). Source code aplikasi bersifat private dan tidak disertakan di sini.

## Kenapa Web Ini Dibuat

Cari ide masakan itu sering jadi masalah sehari-hari: bahan di dapur ada, tapi idenya mentok. Website resep yang sudah ada umumnya berat, penuh iklan, atau harus daftar dulu sebelum bisa membaca resep sampai habis. Masakan Kekinian dibuat sebagai alternatif yang ringan dan langsung bisa dipakai: buka situsnya, cari atau pilih jenis makanan, dan resep langsung tampil tanpa akun dan tanpa biaya.

Web ini juga jadi sarana praktik membangun aplikasi web modern berbasis React yang mengambil data dari API publik secara langsung, lengkap sampai tahap deployment dan domain sendiri.

## Tujuan

- Membantu pengguna Indonesia menemukan ide masakan sehari-hari maupun untuk acara khusus dengan cepat.
- Menyediakan pencarian resep yang sederhana: cukup kata kunci atau jenis makanan, tanpa perlu registrasi.
- Menampilkan resep populer sebagai inspirasi instan bagi pengunjung yang belum tahu mau masak apa.
- Menjadi bagian dari portofolio web pribadi yang dikelola dan di-deploy secara mandiri.

## Fitur

- **Halaman utama** dengan hero bertuliskan "Your Best Cooking Companion", pemilih jenis makanan "Find Your Type of Meal", dan daftar "Popular Food Recipe".
- **Pencarian resep** berdasarkan kata kunci, hasilnya diambil langsung dari Spoonacular API.
- **Telusur berdasarkan jenis makanan**, misalnya appetizer, beverage, bread, breakfast, brunch, dessert, dinner, drink, salad, sauce, snack, dan soup, masing-masing dengan ikon kategorinya sendiri.
- **Makanan populer**: daftar resep yang sedang populer, tampil otomatis di halaman utama sebagai inspirasi.
- **Detail resep**: bahan-bahan dan langkah memasak untuk setiap resep yang dipilih.
- **Kartu resep (FoodCard)** yang konsisten dipakai di semua daftar, menampilkan gambar dan nama makanan.
- **Navbar dan sidebar** untuk navigasi antarhalaman, plus footer sebagai penutup halaman.
- **Indikator loading** selama data resep diambil dari API, supaya pengunjung tahu halaman sedang bekerja.

## Frontend

- Dibangun sebagai aplikasi satu halaman (SPA) berbasis **React 18** dengan **Create React App** (react-scripts 5).
- Routing antarhalaman memakai **React Router DOM 6**; pengambilan dan penyimpanan cache data dari API dibantu **React Query 3**.
- Styling memakai **Tailwind CSS** ditambah CSS per komponen.
- Komponen utama ada di `src/components/`: NavBar, HeroSection, MealType, PopularFoods, FoodCard, SideBar, dan Footer.
- Logika pengambilan data dipisah ke `src/hooks/`: `useFetchPopularFood` untuk makanan populer, `useFetchRecipe` untuk detail resep, dan `useSearch` untuk pencarian.

## Backend / Cara Kerja

- Aplikasi ini tidak memiliki backend sendiri: tidak ada server, tidak ada serverless function, tidak ada database, dan tidak ada sistem akun pengguna.
- Browser pengunjung memanggil **Spoonacular API** secara langsung dari sisi client setiap kali halaman dibuka, dicari, atau detail resep diminta. Data resep, gambar makanan, dan hasil pencarian semuanya disediakan oleh API eksternal tersebut pada saat itu juga.
- Karena datanya live dari API, koleksi resep yang tampil selalu mengikuti katalog Spoonacular dan tidak disimpan secara lokal di situs ini.
- Situs di-deploy di **Vercel**; setiap perubahan pada source code yang masuk ke branch utama langsung terdeploy ke produksi dan bisa diakses lewat domain msknkkn.xsrazy.web.id.

## Catatan

- Repo ini berisi dokumentasi saja. Source code aplikasi Masakan Kekinian disimpan di repo private terpisah.
- Nama "msknkkn" adalah singkatan santai dari "Masakan Kekinian".

## 🌐 Socials
[![Behance](https://img.shields.io/badge/Behance-1769ff?logo=behance&logoColor=white)](https://behance.net/xsrazy) [![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/xsrazy) [![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://facebook.com/xsrazy) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/xsrazy) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/xsrazy) [![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://medium.com/@xsrazy) [![Pinterest](https://img.shields.io/badge/Pinterest-%23E60023.svg?logo=Pinterest&logoColor=white)](https://pinterest.com/xsrazy) [![Quora](https://img.shields.io/badge/Quora-%23B92B27.svg?logo=Quora&logoColor=white)](https://quora.com/profile/xsrazy) [![Reddit](https://img.shields.io/badge/Reddit-%23FF4500.svg?logo=Reddit&logoColor=white)](https://reddit.com/user/xsrazy) [![Stack Overflow](https://img.shields.io/badge/-Stackoverflow-FE7A16?logo=stack-overflow&logoColor=white)](https://stackoverflow.com/users/31065073) [![Twitch](https://img.shields.io/badge/Twitch-%239146FF.svg?logo=Twitch&logoColor=white)](https://twitch.tv/xsrazy) [![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/xsrazy) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/c/xsrazy)

## 💰 You can help me by Donating
[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=plastic&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/xsrazy) [![PayPal](https://img.shields.io/badge/PayPal-00457C?style=plastic&logo=paypal&logoColor=white)](https://paypal.me/xsrazy) [![Patreon](https://img.shields.io/badge/Patreon-F96854?style=plastic&logo=patreon&logoColor=white)](https://patreon.com/Xsrazy) [![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=plastic&logo=ko-fi&logoColor=white)](https://ko-fi.com/xsrazy)
