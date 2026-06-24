# TUGAS-MODUL-2
Tugas Praktikum 2-Pengenalan CSS
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktikum CSS</title>
    <style>
        /* Box-sizing universal agar padding & border tidak merusak ukuran elemen */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        /* ===== TAMPILAN UMUM ===== */
        body {
            background-color: #add8e6;
            font-family: Arial, sans-serif;
            padding: 30px 20px;
        }

        h1 {
            color: #ffffff;
            font-size: 40px;
            text-align: center;
            margin-bottom: 20px;
        }

        /* Paragraf di bawah judul */
        .deskripsi {
            background-color: #d3d3d3;
            color: #000000;
            padding: 20px;
            border-radius: 12px;
            max-width: 800px;
            margin: 0 auto 30px auto;
            text-align: center;
            line-height: 1.6;
        }

        /* ===== LAYOUT KOTAK (BOX) DENGAN CSS GRID ===== */
        .container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            max-width: 800px;
            margin: 0 auto;
        }

        .box1,
        .box2,
        .box3 {
            border: 2px solid #000000;
            padding: 10px;
            height: 150px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #2c3e50;
        }

        .box1 {
            background-color: #ff9999; /* merah muda */
        }

        .box2 {
            background-color: #99ff99; /* hijau muda */
        }

        .box3 {
            background-color: #9999ff; /* biru muda */
        }

        /* ===== RESPONSIVE DESIGN ===== */

        /* Tablet: lebar layar <= 768px -> container jadi 2 kolom */
        @media only screen and (max-width: 768px) {
            .container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* Smartphone: lebar layar <= 480px -> container jadi 1 kolom */
        @media only screen and (max-width: 480px) {
            .container {
                grid-template-columns: 1fr;
            }

            h1 {
                font-size: 28px;
            }

            .box1,
            .box2,
            .box3 {
                height: 120px;
            }

            .deskripsi {
                padding: 12px;
            }
        }
    </style>
</head>
<body>

    <!-- Judul Utama -->
    <h1>Praktikum CSS</h1>

    <!-- Paragraf Deskripsi -->
    <p class="deskripsi">
        Ini adalah halaman latihan tugas praktikum CSS yang menerapkan layout kotak
        menggunakan CSS Grid serta desain responsif agar tampilan menyesuaikan
        ukuran layar perangkat, baik desktop, tablet, maupun smartphone.
    </p>

    <!-- Container Kotak (Box) -->
    <div class="container">
        <div class="box1">Box 1</div>
        <div class="box2">Box 2</div>
        <div class="box3">Box 3</div>
    </div>

</body>
</html>
