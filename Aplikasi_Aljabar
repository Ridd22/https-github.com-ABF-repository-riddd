<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Aplikasi Aljabar</title>
  <style>
    body {
      font-family: "Segoe UI", sans-serif;
      background-color: #eef2f7;
      padding: 20px;
      max-width: 800px;
      margin: auto;
    }
    h1 {
      color: #333;
      text-align: center;
    }
    .section {
      background: #fff;
      padding: 20px;
      margin: 20px 0;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    }
    .section h2 {
      margin-top: 0;
      font-size: 1.3rem;
      color: #00509e;
    }
    .form-group {
      margin-bottom: 10px;
    }
    input[type="number"], input[type="text"] {
      padding: 8px;
      margin: 5px 0;
      width: calc(33% - 10px);
      font-size: 1rem;
    }
    button {
      padding: 8px 16px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1rem;
    }
    button:hover {
      background: #0056b3;
    }
    .output {
      margin-top: 10px;
      padding: 10px;
      background: #e0f7fa;
      border-radius: 6px;
      font-weight: bold;
    }
    @media screen and (max-width: 600px) {
      input[type="number"], input[type="text"] {
        width: 100%;
      }
    }
  </style>
</head>
<body>

  <h1>📘 Aplikasi Aljabar Interaktif</h1>

  <!-- Persamaan Linear -->
  <div class="section">
    <h2>1. Persamaan Linear (ax + b = 0)</h2>
    <div class="form-group">
      a: <input type="number" id="a1" placeholder="a"> 
      b: <input type="number" id="b1" placeholder="b">
    </div>
    <button onclick="linear()">Hitung</button>
    <div class="output" id="hasil1"></div>
  </div>

  <!-- Persamaan Kuadrat -->
  <div class="section">
    <h2>2. Persamaan Kuadrat (ax² + bx + c = 0)</h2>
    <div class="form-group">
      a: <input type="number" id="a2" placeholder="a"> 
      b: <input type="number" id="b2" placeholder="b"> 
      c: <input type="number" id="c2" placeholder="c">
    </div>
    <button onclick="kuadrat()">Hitung</button>
    <div class="output" id="hasil2"></div>
  </div>

  <!-- Penyederhanaan Aljabar -->
  <div class="section">
    <h2>3. Penyederhanaan Bentuk Aljabar</h2>
    <p><small>Contoh: <code>3x + 2x - 4 + x - 5</code></small></p>
    <input type="text" id="aljabarInput" placeholder="Masukkan ekspresi">
    <button onclick="sederhanakan()">Sederhanakan</button>
    <div class="output" id="hasil3"></div>
  </div>

  <!-- Pemfaktoran Kuadrat -->
  <div class="section">
    <h2>4. Pemfaktoran Kuadrat Sederhana</h2>
    <div class="form-group">
      a: <input type="number" id="a4" placeholder="a"> 
      b: <input type="number" id="b4" placeholder="b"> 
      c: <input type="number" id="c4" placeholder="c">
    </div>
    <button onclick="faktorkan()">Faktorkan</button>
    <div class="output" id="hasil4"></div>
  </div>

  <script>
    function linear() {
      let a = parseFloat(document.getElementById('a1').value);
      let b = parseFloat(document.getElementById('b1').value);
      let out = document.getElementById('hasil1');

      if (isNaN(a) || isNaN(b)) return out.innerText = "Masukkan nilai a dan b.";

      if (a === 0) {
        out.innerText = (b === 0) ? "Tak hingga solusi." : "Tidak ada solusi.";
      } else {
        out.innerText = x = ${(-b / a).toFixed(4)};
      }
    }

    function kuadrat() {
      let a = parseFloat(document.getElementById('a2').value);
      let b = parseFloat(document.getElementById('b2').value);
      let c = parseFloat(document.getElementById('c2').value);
      let out = document.getElementById('hasil2');

      if (isNaN(a) || isNaN(b) || isNaN(c)) return out.innerText = "Masukkan semua nilai.";

      let D = b * b - 4 * a * c;
      if (a === 0) {
        out.innerText = "Bukan persamaan kuadrat (a ≠ 0).";
      } else if (D < 0) {
        out.innerText = "Tidak ada akar real (akar kompleks).";
      } else if (D === 0) {
        let x = -b / (2 * a);
        out.innerText = Akar kembar: x = ${x.toFixed(4)};
      } else {
        let x1 = (-b + Math.sqrt(D)) / (2 * a);
        let x2 = (-b - Math.sqrt(D)) / (2 * a);
        out.innerText = x₁ = ${x1.toFixed(4)}, x₂ = ${x2.toFixed(4)};
      }
    }

    function sederhanakan() {
      let ekspresi = document.getElementById('aljabarInput').value;
      let out = document.getElementById('hasil3');
      if (!ekspresi) return out.innerText = "Masukkan ekspresi aljabar.";

      try {
        let terms = ekspresi.replace(/\s/g, '').match(/[+-]?[^+-]+/g);
        let koef = 0, konst = 0;

        terms.forEach(term => {
          if (term.includes('x')) {
            let nilai = term.replace('x', '');
            if (nilai === '' || nilai === '+') nilai = 1;
            else if (nilai === '-') nilai = -1;
            koef += parseFloat(nilai);
          } else {
            konst += parseFloat(term);
          }
        });

        let hasil = ${koef !== 0 ? koef + 'x' : ''}${konst > 0 ? '+' + konst : konst < 0 ? konst : ''};
        out.innerText = hasil || '0';
      } catch {
        out.innerText = "Ekspresi tidak valid.";
      }
    }

    function faktorkan() {
      let a = parseInt(document.getElementById('a4').value);
      let b = parseInt(document.getElementById('b4').value);
      let c = parseInt(document.getElementById('c4').value);
      let out = document.getElementById('hasil4');

      if (isNaN(a) || isNaN(b) || isNaN(c)) return out.innerText = "Masukkan semua koefisien.";

      let ac = a * c;
      let found = false;

      for (let m = -100; m <= 100; m++) {
        for (let n = -100; n <= 100; n++) {
          if (m * n === ac && m + n === b) {
            found = true;
            let faktor1 = (${a}x + ${m});
            let faktor2 = (x + ${n});
            out.innerText = Faktorisasi: ${faktor1}${faktor2};
            return;
          }
        }
      }

      if (!found) out.innerText = "Tidak dapat difaktorkan secara sederhana.";
    }
  </script>

</body>
</html>
