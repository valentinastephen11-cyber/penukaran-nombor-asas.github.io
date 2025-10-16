# penukaran-nombor-asas.github.io
<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Penukar Nombor Asas</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Penukar Nombor Asas</h1>
        <nav>
            <a href="#utama">Utama</a>
            <a href="#penukar">Penukar Nombor</a>
            <a href="#asas">Asas Nombor</a>
            <a href="#penjelasan">Penjelasan Terperinci</a>
        </nav>
    </header>

    <section id="utama">
        <h2>Selamat Datang ke Laman Penukar Nombor Asas!</h2>
        <p>Laman web ini direka untuk membantu anda menukar nombor antara asas yang berbeza dengan mudah dan cepat. Anda juga akan menemui penjelasan terperinci dan contoh untuk memahami konsep ini dengan lebih baik.</p>
    </section>

    <section id="penukar">
        <h2>Penukar Nombor</h2>
        <p>Masukkan nombor, pilih asas asal dan asas sasaran, kemudian klik 'Tukar'.</p>
        <form id="borangPenukar">
            <label for="nombor">Nombor:</label>
            <input type="text" id="nombor" name="nombor" placeholder="Masukkan nombor di sini">

            <label for="asasAsal">Asas Asal:</label>
            <select id="asasAsal" name="asasAsal">
                <option value="2">Perduaan (Asas 2)</option>
                <option value="8">Perlapanan (Asas 8)</option>
                <option value="10">Perpuluhan (Asas 10)</option>
                <option value="16">Perenambelasan (Asas 16)</option>
            </select>

            <label for="asasSasaran">Asas Sasaran:</label>
            <select id="asasSasaran" name="asasSasaran">
                <option value="2">Perduaan (Asas 2)</option>
                <option value="8">Perlapanan (Asas 8)</option>
                <option value="10">Perpuluhan (Asas 10)</option>
                <option value="16">Perenambelasan (Asas 16)</option>
            </select>

            <button type="button" onclick="tukarNombor()">Tukar</button>
        </form>
        <div id="keputusan">
            <p>Hasil: <span id="hasil"></span></p>
        </div>
    </section>

    <section id="asas">
        <h2>Asas Nombor</h2>
        <ul>
            <li><strong>Perduaan (Asas 2):</strong> Menggunakan hanya 0 dan 1. Penting dalam sistem komputer.</li>
            <li><strong>Perlapanan (Asas 8):</strong> Menggunakan digit 0 hingga 7. Kadang-kadang digunakan dalam pengaturcaraan.</li>
            <li><strong>Perpuluhan (Asas 10):</strong> Sistem nombor yang kita gunakan setiap hari.</li>
            <li><strong>Perenambelasan (Asas 16):</strong> Menggunakan digit 0-9 dan huruf A-F. Sering digunakan untuk mewakili alamat memori dan warna dalam komputer.</li>
        </ul>
    </section>

    <section id="penjelasan">
        <h2>Penjelasan Terperinci dan Contoh</h2>
        <h3>Cara Menukar Nombor</h3>
        <p>Berikut adalah beberapa contoh dan cara menukar nombor antara asas yang berbeza:</p>

        <h4>1. Perduaan ke Perpuluhan</h4>
        <p>Untuk menukar nombor perduaan ke perpuluhan, darabkan setiap digit dengan 2<sup>n</sup>, di mana n adalah kedudukan digit bermula dari kanan (0).</p>
        <p>Contoh: 1011<sub>2</sub> = (1 * 2<sup>3</sup>) + (0 * 2<sup>2</sup>) + (1 * 2<sup>1</sup>) + (1 * 2<sup>0</sup>) = 8 + 0 + 2 + 1 = 11<sub>10</sub></p>

        <h4>2. Perpuluhan ke Perduaan</h4>
        <p>Untuk menukar nombor perpuluhan ke perduaan, bahagikan nombor dengan 2 dan catat baki. Ulang sehingga hasil bahagi menjadi 0. Baca baki dari bawah ke atas.</p>
        <p>Contoh: 13<sub>10</sub></p>
        <ol>
            <li>13 / 2 = 6 baki 1</li>
            <li>6 / 2 = 3 baki 0</li>
            <li>3 / 2 = 1 baki 1</li>
            <li>1 / 2 = 0 baki 1</li>
        </ol>
        <p>Jadi, 13<sub>10</sub> = 1101<sub>2</sub></p>

        <h4>3. Perenambelasan ke Perpuluhan</h4>
        <p>Untuk menukar nombor perenambelasan ke perpuluhan, darabkan setiap digit dengan 16<sup>n</sup>, di mana n adalah kedudukan digit bermula dari kanan (0). A=10, B=11, C=12, D=13, E=14, F=15.</p>
        <p>Contoh: 2A<sub>16</sub> = (2 * 16<sup>1</sup>) + (10 * 16<sup>0</sup>) = 32 + 10 = 42<sub>10</sub></p>

        <h4>4. Perpuluhan ke Perenambelasan</h4>
        <p>Untuk menukar nombor perpuluhan ke perenambelasan, bahagikan nombor dengan 16 dan catat baki. Jika baki lebih besar daripada 9, tukarkannya kepada A, B, C, D, E, atau F. Ulang sehingga hasil bahagi menjadi 0. Baca baki dari bawah ke atas.</p>
        <p>Contoh: 45<sub>10</sub></p>
        <ol>
            <li>45 / 16 = 2 baki 13 (D)</li>
            <li>2 / 16 = 0 baki 2</li>
        </ol>
        <p>Jadi, 45<sub>10</sub> = 2D<sub>16</sub></p>
    </section>

    <footer>
        <p>&copy; 2024 Laman Penukar Nombor Asas</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
    line-height: 1.6;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1em 0;
    text-align: center;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 0 1em;
}

section {
    padding: 2em;
    margin: 1em;
    background-color: #fff;
    border-radius: 5px;
}

#penukar form {
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: 0 auto;
}

#penukar label {
    margin-top: 1em;
}

#penukar input[type="text"],
#penukar select {
    padding: 0.5em;
    margin-top: 0.5em;
    border: 1px solid #ccc;
    border-radius: 4px;
}

#penukar button {
    padding: 0.75em;
    margin-top: 1em;
    background-color: #333;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

#keputusan {
    margin-top: 2em;
    text-align: center;
}

#keputusan span {
    font-weight: bold;
}

#asas ul {
    list-style-type: disc;
    margin-left: 2em;
}

#penjelasan h3 {
    margin-top: 1.5em;
}

#penjelasan h4 {
    margin-top: 1em;
}

#penjelasan ol {
    margin-left: 2em;
}

footer {
    text-align: center;
    padding: 1em 0;
    background-color: #333;
    color: #fff;
}
function tukarNombor() {
    let nombor = document.getElementById("nombor").value;
    let asasAsal = document.getElementById("asasAsal").value;
    let asasSasaran = document.getElementById("asasSasaran").value;

    if (!nombor) {
        alert("Sila masukkan nombor.");
        return;
    }

    try {
        let hasil = parseInt(nombor, asasAsal).toString(asasSasaran).toUpperCase();
        document.getElementById("hasil").innerText = hasil;
    } catch (error) {
        alert("Ralat: Sila pastikan nombor dan asas adalah betul.");
        document.getElementById("hasil").innerText = "Ralat";
    }
}
