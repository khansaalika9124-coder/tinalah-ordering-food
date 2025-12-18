<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kuliner Desa Wisata Tinalah</title>
  <style>
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      background-color: #f1f8f4;
      color: #2f4f3e;
    }
    header {
      background: linear-gradient(135deg, #2e7d32, #66bb6a);
      color: white;
      padding: 40px 20px;
      text-align: center;
    }
    nav {
      background-color: #e8f5e9;
      padding: 12px;
      text-align: center;
    }
    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: #2e7d32;
      font-weight: 600;
    }
    section {
      padding: 40px 10%;
    }
    h2 {
      color: #1b5e20;
    }
    .card-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 25px;
      margin-top: 20px;
    }
    .card {
      background-color: white;
      border-radius: 16px;
      box-shadow: 0 6px 16px rgba(0,0,0,0.08);
      overflow: hidden;
    }
    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .card-content {
      padding: 20px;
    }
    .card h3 {
      margin-top: 0;
      color: #2e7d32;
    }
    footer {
      background-color: #2e7d32;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
      font-size: 14px;
    }
    .lang {
      font-size: 14px;
      color: #4f6f5f;
      margin-top: 6px;
    }
  button{background:#2e7d32;color:#fff;border:none;padding:8px 14px;border-radius:8px;cursor:pointer}button:hover{background:#1b5e20}.cart{position:fixed;top:20px;right:20px;background:#fff;border-radius:12px;box-shadow:0 6px 16px rgba(0,0,0,.15);padding:15px;width:260px}.cart h3{margin-top:0;color:#1b5e20}.cart ul{list-style:none;padding:0;font-size:14px}.cart li{margin-bottom:6px}.cart-total{font-weight:bold;margin-top:10px}
</style>
</head>
<body>
<div class="cart" id="cart">
  <h3>Keranjang</h3>
  <ul id="cartItems"></ul>
  <div class="cart-total" id="cartTotal">Total: Rp0</div>
  <button onclick="checkout()">Checkout</button>
</div>

<header>
  <h1>Pesan Kuliner Khas Desa Wisata Tinalah</h1>
  <p>Pesan makanan tradisional favoritmu dengan mudah</p>
  <p class="lang">Order your favorite traditional dishes easily</p>
</header>

<nav>
  <a href="#tentang">Tentang | About</a>
  <a href="#menu">Menu | Culinary</a>
  <a href="#pesan">Kunjungi | Visit</a>
</nav>

<section id="tentang">
  <h2>Tentang Layanan Kami</h2>
  <p>
    Kami menyediakan layanan pemesanan kuliner khas Desa Wisata Tinalah yang
    dimasak langsung oleh warga lokal dengan bahan segar dan alami.
  </p>
  <p class="lang">
    We provide an easy ordering service for traditional dishes from Tinalah
    Tourism Village, freshly prepared by local residents.
  </p>
</section>

<section id="menu">
  <h2>Menu Tersedia</h2>
  <p>Pilih menu, masukkan ke keranjang, lalu lakukan pembayaran.</p>
  <p class="lang">Select menu, add to cart, then proceed to payment.</p>

  <div class="card-container">
    <div class="card"><img src="https://source.unsplash.com/600x400/?tiwul"><div class="card-content"><h3>Sego Tiwul</h3><p>Olahan singkong khas desa.</p><p class="lang">Cassava-based traditional rice.</p><p><strong>Rp15.000</strong></p><button onclick="addToCart('Sego Tiwul',15000)">Order Now</button></div></div>
    <div class="card"><img src="https://source.unsplash.com/600x400/?traditional-snack"><div class="card-content"><h3>Geblek</h3><p>Cemilan gurih khas Kulon Progo.</p><p class="lang">Savory local snack.</p><p><strong>Rp10.000</strong></p><button onclick="addToCart('Geblek',10000)">Order Now</button></div></div>
    <div class="card"><img src="https://source.unsplash.com/600x400/?ginger-drink"><div class="card-content"><h3>Wedang Jahe</h3><p>Minuman jahe hangat.</p><p class="lang">Warm ginger drink.</p><p><strong>Rp8.000</strong></p><button onclick="addToCart('Wedang Jahe',8000)">Order Now</button></div></div>
    <div class="card"><img src="https://source.unsplash.com/600x400/?mineral-water"><div class="card-content"><h3>Air Mineral</h3><p>Air mineral botol dingin.</p><p class="lang">Bottled mineral water.</p><p><strong>Rp5.000</strong></p><button onclick="addToCart('Air Mineral',5000)">Order Now</button></div></div>
    <div class="card"><img src="https://source.unsplash.com/600x400/?snack"><div class="card-content"><h3>Cemilan Tradisional</h3><p>Aneka jajanan pasar.</p><p class="lang">Traditional snacks.</p><p><strong>Rp7.000</strong></p><button onclick="addToCart('Cemilan',7000)">Order Now</button></div></div>
    <div class="card"><img src="https://source.unsplash.com/600x400/?instant-noodles"><div class="card-content"><h3>Pop Mie</h3><p>Mie instan siap saji.</p><p class="lang">Instant cup noodles.</p><p><strong>Rp12.000</strong></p><button onclick="addToCart('Pop Mie',12000)">Order Now</button></div></div>
  </div>
</section>

<section id="pesan">
  <h2>Sistem Pemesanan</h2>
  <p>
    Pemesanan dilakukan langsung melalui website ini. Setelah melakukan order,
    pelanggan akan mendapatkan nomor pesanan.
  </p>
  <p class="lang">
    Orders are made directly through this website. After ordering, customers
    will receive an order number.
  </p>

  <p><strong>Sistem Self Service:</strong> Pesanan diambil sendiri sesuai nomor pesanan di area gazebo.</p>
  <p class="lang"><strong>Self-Service System:</strong> Orders are picked up by customers according to the order number near the gazebo.</p>

  <h3>Metode Pembayaran</h3>
  <ul>
    <li>QRIS</li>
    <li>Virtual Account</li>
    <li>GoPay</li>
    <li>ShopeePay</li>
  </ul>
</section>

<footer>
  <p>© 2025 Desa Wisata Tinalah</p>
  <p class="lang">Local Wisdom for Sustainable Tourism</p>
</footer>

<script>
let cart=[];let total=0;
function addToCart(name,price){cart.push({name,price});total+=price;renderCart()}
function renderCart(){const list=document.getElementById('cartItems');list.innerHTML='';cart.forEach(i=>{const li=document.createElement('li');li.textContent=i.name+' - Rp'+i.price;list.appendChild(li)});document.getElementById('cartTotal').textContent='Total: Rp'+total}
function checkout(){if(cart.length===0){alert('Keranjang masih kosong');return;}const orderNumber='TNL-'+Math.floor(Math.random()*9000+1000);alert('Pesanan berhasil! Nomor Pesanan: '+orderNumber+'
Silakan ambil pesanan di gazebo sesuai nomor.');cart=[];total=0;renderCart();}
</script>
</body>
</html>
