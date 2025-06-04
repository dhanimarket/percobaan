<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DhaniPointque</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100">

  <!-- Login Section -->
  <div id="login-section" class="min-h-screen flex items-center justify-center">
    <div class="bg-white p-8 rounded-xl shadow-md w-full max-w-sm">
      <h2 class="text-2xl font-bold text-center mb-6">Login DhaniPoint</h2>
      <input id="username" type="text" placeholder="Username" class="w-full mb-4 p-2 border rounded" />
      <input id="password" type="password" placeholder="Password" class="w-full mb-4 p-2 border rounded" />
      <button onclick="login()" class="w-full bg-blue-600 text-white p-2 rounded hover:bg-blue-700">Login</button>
    </div>
  </div>

  <!-- Dashboard Section -->
  <div id="dashboard" class="hidden p-6 max-w-2xl mx-auto">
    <div class="bg-white p-6 rounded-xl shadow-md">
      <h2 class="text-xl font-semibold mb-2">Selamat Datang di DhaniPoint 🎉</h2>
      <p class="mb-4">Program loyalti khusus pelanggan setia Dhani Market.</p>

      <div class="bg-blue-100 p-4 rounded mb-4">
        <p><strong>Nama / WA Kamu:</strong> <span id="user-wa">0812-XXXX-XXXX</span></p>
        <p><strong>Total Poin:</strong> <span id="total-point">0</span> DhaniPoint</p>
      </div>

      <h3 class="font-bold mb-2">Riwayat Transaksi</h3>
      <table class="w-full text-left mb-4">
        <thead>
          <tr>
            <th>Tanggal</th><th>Layanan</th><th>Jumlah</th><th>Poin</th>
          </tr>
        </thead>
        <tbody id="transaction-table"></tbody>
      </table>

      <h3 class="font-bold mb-2">Tukar Hadiah</h3>
      <table class="w-full text-left mb-4">
        <thead>
          <tr>
            <th>Hadiah</th><th>Poin Dibutuhkan</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>Diskon R55.000</td><td>20</td></tr>
          <tr><td>Top-up 70 UC</td><td>50</td></tr>
          <tr><td>Voucher Diskon Akun Totap 1K</td><td>100</td></tr>
        </tbody>
      </table>

      <button class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">TUKARKAN POIN</button>
    </div>
    <p class="text-sm text-gray-500 mt-4">🎉 <strong>Promo Aktif:</strong> Double Point setiap Jumat – Janganakan!</p>
  </div>

  <script>
    function login() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;

      // Simulasi login manual (ganti dengan integrasi Sheet nanti)
      if (username === "user1" && password === "1234") {
        document.getElementById("login-section").style.display = "none";
        document.getElementById("dashboard").classList.remove("hidden");

        document.getElementById("user-wa").innerText = "0812-3456-7890";
        document.getElementById("total-point").innerText = "78";

        document.getElementById("transaction-table").innerHTML = `
          <tr><td>21 Mei</td><td>Rental ML</td><td>3 hari</td><td>9</td></tr>
          <tr><td>19 Mei</td><td>Top-up 25K</td><td>5</td><td>5</td></tr>
          <tr><td>15 Mei</td><td>Beli akun FF</td><td>80K</td><td>8</td></tr>
        `;
      } else {
        alert("Username atau password salah!");
      }
    }
  </script>

</body>
</html>
