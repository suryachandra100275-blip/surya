<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surya Teknisi | Service Handphone Premium & Garansi Resmi</title>
    
    <style>
        /* ===================================================================
           1. CORE & GLOBAL STYLES
        =================================================================== */
        body {font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f4f7f6; color: #343a40; line-height: 1.6; scroll-behavior: smooth;}
        .container {max-width: 1200px; margin: 30px auto; padding: 0 20px;}
        .section {background-color: #ffffff; padding: 40px; margin-bottom: 30px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);}
        .section h2 {color: #0056b3; border-bottom: 3px solid #ffc107; padding-bottom: 15px; margin-bottom: 30px; font-size: 2.2em; font-weight: 700; text-align: center;}
        
        /* NAVIGATION BAR */
        .navbar {background-color: #0056b3; padding: 15px 0; position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);}
        .navbar-content {max-width: 1200px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; padding: 0 20px;}
        .navbar-logo {color: white; font-size: 1.5em; font-weight: 800; text-decoration: none;}
        .nav-links a {color: white; text-decoration: none; margin-left: 25px; font-weight: 500; transition: color 0.3s;}
        .nav-links a:hover {color: #ffc107;}

        /* HEADER & PARALLAX */
        .header-parallax {background: linear-gradient(105deg, rgba(0, 123, 255, 0.8) 0%, rgba(0, 86, 179, 0.8) 100%), url('https://via.placeholder.com/1600x600?text=HP+Service+Background'); color: #ffffff; padding: 100px 0; text-align: center; margin-bottom: 40px; background-attachment: fixed; background-size: cover; background-position: center; box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);}
        .icon-header {font-size: 4em; display: inline-block; margin-bottom: 15px; color: #ffc107; animation: bounce-gear 3s ease-in-out infinite;}
        @keyframes bounce-gear {0%, 100% {transform: translateY(0) rotate(0deg);} 50% {transform: translateY(-10px) rotate(10deg);}}

        /* --- NEW: DELIVERY SECTION --- */
        .delivery-promo {
            background-color: #dc3545; /* Warna Merah Menonjol */
            color: white;
            padding: 30px;
            border-radius: 12px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 4px 15px rgba(220, 53, 69, 0.5);
            animation: pulse-border 2s infinite;
        }
        .delivery-promo h3 {
            font-size: 2em;
            margin: 0 0 10px 0;
            font-weight: 800;
        }
        .delivery-promo p {
            font-size: 1.2em;
            margin-bottom: 20px;
        }
        .delivery-promo a {
            background-color: #ffc107;
            color: #343a40;
            padding: 10px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 700;
            transition: background-color 0.3s;
        }
        @keyframes pulse-border {
            0% { border: 3px solid rgba(255, 255, 255, 0.5); }
            50% { border: 3px solid white; }
            100% { border: 3px solid rgba(255, 255, 255, 0.5); }
        }
        
        /* PROSES KERJA (Revisi Wording) */
        .process-flow {display: flex; justify-content: space-between; align-items: flex-start; text-align: center; margin-top: 20px; flex-wrap: wrap;}
        .step {flex: 1; padding: 15px; position: relative; background-color: #f7f9fc; border-radius: 8px; margin: 10px; box-shadow: 0 2px 5px rgba(0,0,0,0.05);}
        .step-icon {font-size: 2.8em; color: #28a745; margin-bottom: 10px; background-color: #e2f0e2; padding: 15px; border-radius: 50%; display: inline-block; border: 2px solid #28a745;}
        .step h4 {color: #007bff; margin: 5px 0;}
        .step:not(:last-child)::after {content: '➔'; position: absolute; right: -25px; top: 45%; transform: translateY(-50%); font-size: 2em; color: #007bff; animation: pulse-arrow 1.5s infinite;}
        @keyframes pulse-arrow {0%, 100% {opacity: 0.8;} 50% {opacity: 1; transform: scale(1.1) translateY(-50%);}}
        @media (max-width: 768px) {
            .step:not(:last-child)::after {content: '↓'; right: 50%; left: unset; top: 100%; transform: translateX(50%); font-size: 1.8em;}
            .step {margin-bottom: 40px;}
        }
        
        /* ... Gaya komponen lainnya tetap seperti sebelumnya ... */
        .warranty-box {background-color: #28a745; color: white; padding: 25px; border-radius: 10px; text-align: center; margin-top: 30px;}
        .layanan-grid {display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px;}
        .layanan-item {cursor: pointer; border: 1px solid #dee2e6; border-radius: 10px; overflow: hidden; background-color: #f8f9fa; transition: transform 0.3s, box-shadow 0.3s;}
        .testimonial-grid {display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;}
        .testimonial-card {padding: 20px; border-left: 5px solid #28a745; background-color: #e2f0e2; border-radius: 8px;}
        .modal {display: none; position: fixed; z-index: 2000; left: 0; top: 0; width: 100%; height: 100%; overflow: auto; background-color: rgba(0,0,0,0.4);}
        .modal-content {background-color: #fefefe; margin: 10% auto; padding: 30px; border-radius: 10px; width: 80%; max-width: 600px; box-shadow: 0 5px 15px rgba(0,0,0,0.3);}
        .close-button {color: #aaa; float: right; font-size: 28px; font-weight: bold;}
        .price-tab-button {background-color: #f8f9fa; border: 2px solid #007bff; color: #007bff; padding: 10px 20px; margin: 5px; border-radius: 20px; cursor: pointer; font-weight: 600; transition: all 0.3s;}
        .price-tab-button.active {background-color: #007bff; color: white; box-shadow: 0 4px 8px rgba(0, 123, 255, 0.4);}
        .price-content {display: none; padding-top: 20px;}
        .price-content.active {display: block;}
        .price-content table {width: 100%; border-collapse: collapse;}
        .price-content th {background-color: #28a745; color: white; padding: 12px 15px; text-align: left;}
        .price-content td {padding: 10px 15px; border-bottom: 1px solid #e9ecef;}
        .price-highlight {font-weight: 700; color: #dc3545;}
        footer {text-align: center; padding: 25px; margin-top: 40px; border-top: 2px solid #ced4da; color: #6c757d; font-size: 1em;}
        .fab-container {position: fixed; bottom: 25px; right: 25px; z-index: 1000;}
        .fab {width: 60px; height: 60px; border-radius: 50%; background-color: #25d366; color: white; text-align: center; line-height: 60px; font-size: 30px; box-shadow: 0 6px 10px rgba(0, 0, 0, 0.3); cursor: pointer; transition: transform 0.3s; text-decoration: none; display: block;}
    </style>
</head>
<body>

    <div class="navbar">
        <div class="navbar-content">
            <a href="#" class="navbar-logo">SURYA TEKNISI</a>
            <div class="nav-links">
                <a href="#layanan">Layanan</a>
                <a href="#harga">Harga</a>
                <a href="#delivery">Antar Jemput</a>
                <a href="#proses">Proses</a>
                <a href="#testimoni">Testimoni</a>
                <a href="#kontak">Kontak</a>
            </div>
        </div>
    </div>

    <div class="header-parallax">
        <div class="header-content">
            <div class="icon-header">🔧</div>
            <h1>SOLUSI SERVICE HP TERPERCAYA</h1>
            <p>Spesialis Service & Konsultasi Handphone Terbaik dengan Garansi Resmi</p>
            <a href="#delivery" style="display: inline-block; margin-top: 20px; padding: 10px 30px; background-color: #ffc107; color: #343a40; text-decoration: none; border-radius: 5px; font-weight: 700; transition: background-color 0.3s;">ANTAR JEMPUT GRATIS SURABAYA!</a>
        </div>
    </div>

    <div class="container">
        
        <section class="warranty-box">
            <h3>⭐ Jaminan Garansi Resmi Hingga 90 Hari!</h3>
            <p>Kami hanya menggunakan suku cadang berkualitas dan memberikan ketenangan pikiran dengan garansi purna jual.</p>
        </section>

        <section class="section" id="layanan">
            <h2>✨ Layanan Inti Kami</h2>
            <p style="text-align: center; margin-bottom: 40px;">Klik salah satu layanan di bawah untuk melihat detail lebih lanjut.</p>
            <div class="layanan-grid">
                <div class="layanan-item" onclick="openModal('layar')"><img src="https://via.placeholder.com/400x220?text=GANTI+LAYAR+ORIGINAL" alt="Pergantian LCD"><div class="layanan-item-content"><h3>Ganti Layar/LCD Original</h3><p>Layanan penggantian layar retak, pecah, atau *blank*.</p></div></div>
                <div class="layanan-item" onclick="openModal('mainboard')"><img src="https://via.placeholder.com/400x220?text=SERVIS+MAINBOARD+IC" alt="Perbaikan IC CPU"><div class="layanan-item-content"><h3>Servis Mainboard (IC CPU, Power)</h3><p>Perbaikan tingkat lanjut untuk HP mati total atau kerusakan cairan.</p></div></div>
                <div class="layanan-item" onclick="openModal('baterai')"><img src="https://via.placeholder.com/400x220?text=GANTI+BATERAI+TERBAIK" alt="Pergantian Baterai"><div class="layanan-item-content"><h3>Baterai & Pengisian Daya</h3><p>Mengganti baterai kembung/boros, perbaikan jalur IC *charging*.</p></div></div>
            </div>
        </section>

        <section id="delivery" class="delivery-promo">
            <h3>🛵 FREE ANTAR JEMPUT DI SURABAYA!</h3>
            <p>Tidak perlu repot ke *workshop*. Kurir kami akan menjemput dan mengantar kembali HP Anda setelah selesai perbaikan. **Gratis Ongkos Kirim!**</p>
            <a href="https://wa.me/6285198331549" target="_blank">Jadwalkan Penjemputan Sekarang</a>
        </section>

        <section class="section" id="harga">
            <h2>💰 Daftar Harga Service Transparan</h2>
            <p style="text-align: center; color: #555; margin-bottom: 25px;">Pilih kategori perangkat Anda untuk melihat perkiraan harga:</p>
            <div class="price-tabs">
                <button class="price-tab-button active" onclick="showPrice('iphone', this)">Apple iPhone</button>
                <button class="price-tab-button" onclick="showPrice('android', this)">Android Premium</button>
                <button class="price-tab-button" onclick="showPrice('ic', this)">Mikrosoldering (IC)</button>
            </div>
            <div id="iphone" class="price-content active">
                <table><thead><tr><th colspan="2">Apple iPhone (LCD & Baterai)</th></tr></thead>
                    <tbody>
                        <tr><td>Ganti LCD iPhone 11</td><td class="price-highlight">Rp 450.000</td></tr>
                        <tr><td>Ganti Baterai iPhone 12</td><td class="price-highlight">Rp 400.000</td></tr>
                        <tr><td>Perbaikan Face ID (Model X ke atas)</td><td class="price-highlight">Mulai Rp 800.000</td></tr>
                    </tbody>
                </table>
            </div>
            <div id="android" class="price-content">
                 <table><thead><tr><th colspan="2">Android Premium (Samsung, Xiaomi, dll.)</th></tr></thead><tbody><tr><td>Ganti LCD Samsung S21 Ultra</td><td class="price-highlight">Mulai Rp 2.500.000</td></tr><tr><td>Ganti Baterai Xiaomi 12 Pro</td><td class="price-highlight">Mulai Rp 550.000</td></tr><tr><td>Perbaikan Ganti Kaca Belakang</td><td class="price-highlight">Mulai Rp 300.000</td></tr></tbody></table>
            </div>
            <div id="ic" class="price-content">
                 <table><thead><tr><th colspan="2">Mikrosoldering & Mainboard</th></tr></thead><tbody><tr><td>Perbaikan IC Power</td><td class="price-highlight">Mulai Rp 600.000</td></tr><tr><td>Perbaikan Jalur Charging/Port</td><td class="price-highlight">Mulai Rp 350.000</td></tr><tr><td>Perbaikan Kerusakan Cairan (Water Damage)</td><td class="price-highlight">Konsultasi</td></tr></tbody></table>
            </div>
            <p style="text-align: center; font-size: 0.9em; color: #888; margin-top: 20px;">*Harga estimasi dan dapat berubah. Selalu hubungi kami untuk diagnosa dan harga final.</p>
        </section>

        <section class="section" id="proses">
            <h2>🔍 Transparansi Proses Service</h2>
            <p style="text-align: center; color: #555;">Kami menjamin proses kerja yang cepat dan transparan dari awal hingga akhir. Khusus area Surabaya, langkah 1 dan 4 dilakukan oleh kurir profesional kami.</p>
            
            <div class="process-flow">
                <div class="step"><div class="step-icon">📞</div><h4>1. Jadwal & Penjemputan Kurir</h4><p>Jadwalkan, Kurir kami menjemput perangkat di lokasi Anda (Surabaya Free).</p></div>
                <div class="step"><div class="step-icon">🔬</div><h4>2. Diagnosa Mendalam</h4><p>Pengujian komponen (Hardware & Software) untuk menentukan akar masalah di workshop.</p></div>
                <div class="step"><div class="step-icon">🛠️</div><h4>3. Proses Perbaikan</h4><p>Eksekusi perbaikan dengan suku cadang berkualitas dan teknisi berpengalaman.</p></div>
                <div class="step"><div class="step-icon">✅</div><h4>4. Quality Check & Pengantaran</h4><p>Pengujian fungsi menyeluruh, lalu diantar kembali ke lokasi Anda (Surabaya Free).</p></div>
            </div>
        </section>

        <section class="section" id="testimoni">
            <h2>🗣️ Apa Kata Pelanggan Kami?</h2>
            <p style="text-align: center; margin-bottom: 30px; color: #555;">Kumpulan ulasan nyata dari pelanggan yang puas dengan layanan kami.</p>
            <div class="testimonial-grid">
                <div class="testimonial-card"><p>"Service LCD iPhone 11 di sini cepat sekali, hanya 1 jam dan hasilnya mulus! Garansi juga jelas."</p><h4>- Bima S. (Jakarta)</h4></div>
                <div class="testimonial-card"><p>"HP saya mati total kena air, diservis di Surya Teknisi akhirnya nyala lagi. Data-data aman. Rekomen!"</p><h4>- Risa M. (Surabaya)</h4></div>
                <div class="testimonial-card"><p>"Ganti baterai Xiaomi jadi awet lagi. Pelayanan ramah dan harganya transparan sesuai janji."</p><h4>- Agus P. (Bandung)</h4></div>
            </div>
        </section>
        
        <section class="section">
             <h2>🧠 Pengetahuan Wajib Pengguna HP</h2>
            <div style="display: flex; gap: 25px; flex-wrap: wrap;">
                <div style="flex: 1; padding: 25px; border-radius: 8px; background-color: #f7f9fc; border-left: 5px solid #007bff; min-width: 300px;"><h3>Kerusakan Software</h3><p>Melibatkan sistem operasi. Seringkali dapat diselesaikan tanpa mengganti *spare part*.</p><ul><li>Masalah Umum: *Bootloop*, Lupa Sandi/PIN, *Virus*, HP *Hang* total.</li></ul></div>
                <div style="flex: 1; padding: 25px; border-radius: 8px; background-color: #f7f9fc; border-left: 5px solid #007bff; min-width: 300px;"><h3>Kerusakan Hardware</h3><p>Melibatkan komponen fisik. Memerlukan penggantian suku cadang atau perbaikan *motherboard*.</p><ul><li>Masalah Umum: Layar retak, *Water Damage*, IC Power mati, *speaker* pecah.</li></ul></div>
            </div>
        </section>

        <footer id="kontak">
            <p>Surya Teknisi &copy; 2025 | Keahlian, Kejujuran, dan Garansi adalah Prioritas Kami.</p>
            <p>Hubungi Kami: <a href="tel:085198331549" style="color: #007bff; text-decoration: none;">0851 9833 1549</a> | Alamat Workshop: Surabaya</p>
        </footer>

    </div>

    <div id="myModal" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3 id="modal-title" style="color: #007bff;">Detail Layanan</h3>
            <img id="modal-image" src="" alt="Detail Layanan">
            <p id="modal-description"></p>
            <a id="modal-contact" href="https://wa.me/6285198331549" target="_blank">Konsultasi Sekarang (via WhatsApp)</a>
        </div>
    </div>

    <div class="fab-container">
        <a href="https://wa.me/6285198331549" target="_blank" class="fab">💬</a>
    </div>

    <script>
        // --- FUNGSI TAB HARGA ---
        function showPrice(tabId, element) {
            const contents = document.querySelectorAll('.price-content');
            contents.forEach(content => content.classList.remove('active'));
            const buttons = document.querySelectorAll('.price-tab-button');
            buttons.forEach(button => button.classList.remove('active'));

            document.getElementById(tabId).classList.add('active');
            if (element) element.classList.add('active');
        }

        // --- FUNGSI MODAL (Detail Layanan) ---
        const modal = document.getElementById("myModal");
        const closeBtn = document.getElementsByClassName("close-button")[0];
        
        const serviceDetails = {
            layar: {
                title: "Ganti Layar/LCD Original",
                desc: "Kami menggunakan panel LCD/OLED kualitas tertinggi yang menjamin sensitivitas sentuhan dan akurasi warna. Tersedia opsi penggantian *glass only* (kaca luar) untuk menghemat biaya jika panel dalam masih berfungsi normal. Garansi suku cadang 90 hari.",
                img: "https://via.placeholder.com/600x300?text=ILLUSTRASI+GANTI+LAYAR"
            },
            mainboard: {
                title: "Servis Mainboard Mikrosoldering",
                desc: "Layanan ini mencakup perbaikan IC Power, IC CPU, IC Charge, dan penanganan kerusakan akibat cairan (water damage). Diagnosa mendalam menggunakan mikroskop. Perbaikan mainboard sangat dianjurkan untuk menyelamatkan data penting Anda.",
                img: "https://via.placeholder.com/600x300?text=ILLUSTRASI+MIKROSOLDERING"
            },
            baterai: {
                title: "Baterai & Pengisian Daya",
                desc: "Ganti baterai dengan kapasitas tinggi atau original untuk daya tahan optimal. Kami juga memperbaiki masalah pengisian daya lambat, tidak mengisi, atau konektor port yang longgar/berkarat. Cepat dan bergaransi.",
                img: "https://via.placeholder.com/600x300?text=ILLUSTRASI+GANTI+BATERAI"
            }
        };

        function openModal(serviceId) {
            const detail = serviceDetails[serviceId];
            document.getElementById('modal-title').textContent = detail.title;
            document.getElementById('modal-description').textContent = detail.desc;
            document.getElementById('modal-image').src = detail.img;
            modal.style.display = "block";
        }

        closeBtn.onclick = function() {
            modal.style.display = "none";
        }

        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
        
        // Inisialisasi: Aktifkan tab iPhone saat halaman dimuat
        document.addEventListener('DOMContentLoaded', () => {
            const iphoneButton = document.querySelector('.price-tab-button[onclick*="iphone"]');
            if(iphoneButton) showPrice('iphone', iphoneButton);
        });
    </script>
</body>
</html>
