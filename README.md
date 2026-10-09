<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#101010">
<meta name="description" content="PUSHGARAGE — katalog stock mobil game. Cek stock, pilih mata uang Rp atau RM, dan order via WhatsApp.">
<title>PUSHGARAGE — Digital Car Garage</title>
<style>
:root{--bg:#0b0b0d;--panel:#151518;--panel2:#1d1d21;--red:#f12b36;--text:#f7f7f8;--muted:#a8a8b0;--line:#2b2b31;--green:#35d07f}
*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:var(--bg);color:var(--text);font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif}
a{color:inherit;text-decoration:none}button,input,select{font:inherit}.wrap{width:min(1120px,92%);margin:auto}
header{position:sticky;top:0;z-index:5;background:rgba(11,11,13,.92);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
.nav{display:flex;align-items:center;justify-content:space-between;gap:16px;padding:15px 0}.brand{font-weight:950;letter-spacing:1.5px;font-size:20px}.brand span{color:var(--red)}.navlinks{display:flex;gap:18px;color:var(--muted);font-size:13px}.navlinks a:hover{color:white}
.hero{padding:48px 0 30px}.heroBox{position:relative;overflow:hidden;border:1px solid #34343b;border-radius:24px;padding:clamp(25px,6vw,64px);background:radial-gradient(ellipse at 85% 30%,#5b1119 0%,#211014 25%,#141416 55%,#111113 100%)}
.kicker{display:inline-flex;align-items:center;gap:8px;color:#ff8b91;font-size:11px;font-weight:800;letter-spacing:2px;text-transform:uppercase}.dot{width:7px;height:7px;background:var(--red);border-radius:50%;box-shadow:0 0 14px var(--red)}
h1{font-size:clamp(40px,8vw,78px);line-height:.95;letter-spacing:-3px;margin:18px 0 14px;max-width:650px}h1 em{font-style:normal;color:var(--red)}.hero p{color:#c0c0c7;max-width:470px;line-height:1.7;font-size:15px}
.actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:24px}.btn{border:0;border-radius:11px;padding:12px 16px;font-weight:800;font-size:13px;display:inline-flex;align-items:center;justify-content:center;cursor:pointer}.primary{background:var(--red);color:white}.secondary{background:#25252b;border:1px solid #3b3b43;color:white}.heroFoot{display:flex;gap:22px;flex-wrap:wrap;margin-top:28px;color:#b7b7bf;font-size:12px}.heroFoot strong{color:white}
.section{padding:24px 0 42px}.sectionHead{display:flex;align-items:end;justify-content:space-between;gap:14px;margin-bottom:18px}.eyebrow{color:var(--red);font-size:10px;letter-spacing:2px;font-weight:900;text-transform:uppercase}.section h2{font-size:clamp(25px,4vw,35px);letter-spacing:-1px;margin:7px 0 0}.muted{color:var(--muted);font-size:13px;line-height:1.6}
.controls{display:flex;gap:9px;flex-wrap:wrap;margin-bottom:18px}.controls input,.controls select{min-width:0;background:var(--panel);color:white;border:1px solid var(--line);border-radius:10px;padding:11px 12px;outline:none}.controls input{flex:1;min-width:160px}.controls select{max-width:100%}
.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px}.car{background:var(--panel);border:1px solid var(--line);border-radius:17px;overflow:hidden;transition:transform .2s,border-color .2s}.car:hover{transform:translateY(-3px);border-color:#5a3035}.carImg{aspect-ratio:16/10;background:linear-gradient(135deg,#26262b,#151518);display:flex;align-items:center;justify-content:center;overflow:hidden;position:relative}.carImg img{width:100%;height:100%;object-fit:cover;display:block}.placeholder{font-size:40px;filter:grayscale(.2)}.tag{position:absolute;top:11px;left:11px;background:rgba(8,8,9,.82);border:1px solid #48484f;border-radius:6px;padding:5px 8px;font-size:10px;font-weight:800;letter-spacing:.5px}.carBody{padding:15px}.carTop{display:flex;justify-content:space-between;align-items:center;gap:8px}.car h3{font-size:16px;margin:0}.stock{font-size:10px;color:var(--green);font-weight:800}.stock.sold{color:#ff777e}.carDesc{font-size:12px;color:var(--muted);margin:8px 0 13px;min-height:18px}.priceRow{display:flex;align-items:baseline;gap:7px;flex-wrap:wrap}.price{font-size:20px;font-weight:900;letter-spacing:-.5px}.otherPrice{font-size:11px;color:var(--muted)}.carButtons{display:flex;gap:8px;margin-top:14px}.carButtons .btn{flex:1;padding:10px 8px;font-size:12px}
.empty{padding:35px 16px;text-align:center;color:var(--muted);border:1px dashed var(--line);border-radius:14px;grid-column:1/-1}
.infoGrid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}.info{background:var(--panel);border:1px solid var(--line);padding:18px;border-radius:15px}.infoIcon{font-size:22px}.info h3{font-size:14px;margin:12px 0 6px}.info p{font-size:12px;color:var(--muted);line-height:1.65;margin:0}
.notice{margin-top:18px;background:#171417;border:1px solid #442329;border-radius:14px;padding:15px;color:#d4c6c8;font-size:12px;line-height:1.7}
footer{border-top:1px solid var(--line);padding:24px 0 34px;color:var(--muted);font-size:12px}.footRow{display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap}.footBrand{color:white;font-weight:900;letter-spacing:1px}
.fab{position:fixed;bottom:18px;right:18px;z-index:4;background:#20c969;color:#07170d;padding:13px 16px;border-radius:50px;font-size:12px;font-weight:900;box-shadow:0 8px 28px #0008}
@media(max-width:760px){.grid{grid-template-columns:repeat(2,minmax(0,1fr))}.infoGrid{grid-template-columns:1fr}.navlinks{gap:10px}.navlinks a{font-size:11px}.hero{padding-top:25px}h1{letter-spacing:-2px}.heroBox{border-radius:18px}}
@media(max-width:440px){.grid{grid-template-columns:1fr}.carImg{aspect-ratio:16/9}.navlinks a:nth-child(2){display:none}.sectionHead{align-items:start;flex-direction:column}.heroFoot{gap:12px}}
</style>
</head>
<body>
<header><div class="wrap nav">
  <a class="brand" href="#"><span> PUSH</span>GARAGE</a>
  <nav class="navlinks"><a href="#stock">Stock Mobil</a><a href="#cara-order">Cara Order</a><a href="#kontak">Kontak</a></nav>
</div></header>
<main>
<section class="hero"><div class="wrap"><div class="heroBox">
  <div class="kicker"><span class="dot"></span> Digital Car Garage</div>
  <h1>YOUR NEXT<br><em>RIDE</em> STARTS HERE.</h1>
  <p>Temukan mobil game incaran lu di PushGarage. Cek stock, pilih harga Rp atau RM, lalu order dengan mudah lewat WhatsApp.</p>
  <div class="actions"><a class="btn primary" href="#stock">LIHAT STOCK ↗</a><a class="btn secondary" id="heroWA" href="#">CHAT ADMIN WHATSAPP</a></div>
  <div class="heroFoot"><span><strong>01.</strong> Pilih mobil</span><span><strong>02.</strong> Chat admin</span><span><strong>03.</strong> Konfirmasi stock</span></div>
</div></div></section>

<section class="section" id="stock"><div class="wrap">
  <div class="sectionHead"><div><div class="eyebrow">Current inventory</div><h2>STOCK MOBIL</h2><div class="muted">Stock dapat berubah. Konfirmasi ketersediaan sebelum pembayaran.</div></div><div class="muted" id="count">Memuat stock…</div></div>
  <div class="controls">
    <input id="search" type="search" placeholder="Cari nama mobil..." aria-label="Cari mobil">
    <select id="currency" aria-label="Mata uang"><option value="IDR">Harga Indonesia · Rp</option><option value="MYR">Harga Malaysia · RM</option></select>
    <select id="filter" aria-label="Filter stock"><option value="all">Semua stock</option><option value="available">Tersedia</option><option value="sold">Habis</option></select>
  </div>
  <div class="grid" id="cars"></div>
</div></section>

<section class="section" id="cara-order"><div class="wrap">
  <div class="eyebrow">Simple & easy</div><h2>CARA ORDER</h2><p class="muted" style="margin-top:8px;margin-bottom:18px">Order simpel, tinggal beberapa langkah.</p>
  <div class="infoGrid">
    <article class="info"><div class="infoIcon">🏎️</div><h3>01 — Pilih mobil</h3><p>Lihat katalog dan pilih mobil yang lu mau. Harga bisa dilihat dalam Rp atau RM.</p></article>
    <article class="info"><div class="infoIcon">💬</div><h3>02 — Chat admin</h3><p>Tekan tombol order. Nama mobil dan harga akan disiapkan di pesan WhatsApp.</p></article>
    <article class="info"><div class="infoIcon">✅</div><h3>03 — Konfirmasi</h3><p>Pastikan stock, harga, dan metode pembayaran sudah dikonfirmasi admin sebelum transfer.</p></article>
  </div>
  <div class="notice"><strong>Catatan pembayaran:</strong> Pembayaran Indonesia dapat menggunakan QRIS jika tersedia dari admin. Pembeli Malaysia, silakan konfirmasi metode pembayaran dan total RM lewat WhatsApp. Jangan melakukan pembayaran sebelum stock dan detail transaksi dikonfirmasi.</div>
</div></section>
<section class="section" id="kontak"><div class="wrap"><div class="sectionHead"><div><div class="eyebrow">Need help?</div><h2>CONTACT PUSHGARAGE</h2><p class="muted">Ada pertanyaan atau mau cek stock? Hubungi admin.</p></div><a class="btn primary" id="contactWA" href="#">CHAT VIA WHATSAPP ↗</a></div></div></section>
</main>
<footer><div class="wrap footRow"><div><div class="footBrand">PUSHGARAGE</div><div style="margin-top:6px">Digital car garage · Game car listings</div></div><div>© <span id="year"></span> PushGarage. All rights reserved.</div></div></footer>
<a class="fab" id="floatWA" href="#" aria-label="Chat WhatsApp">WhatsApp ↗</a>
<script>
/* =========================
   CARA UPDATE STOCK (EDIT DI SINI)
   1) name: nama mobil
   2) idr: harga dalam Rupiah
   3) myr: harga dalam Ringgit Malaysia
   4) status: "available" atau "sold"
   5) image: URL foto mobil (boleh kosong "")
   6) note: keterangan singkat
   ========================= */
const WHATSAPP_NUMBER = "6287857520721"; // nomor admin, format internasional tanpa tanda +
const CARS = [
  {id:1,name:"Lamborghini",note:"Mobil game · cek detail ke admin",idr:10000,myr:10,status:"available",image:""},
  {id:2,name:"BMW",note:"Tanya stock dan varian tersedia",idr:0,myr:0,status:"available",image:""},
  {id:3,name:"Ferrari",note:"Tanya stock dan varian tersedia",idr:0,myr:0,status:"available",image:""}
];
const fmt=(value,currency)=>currency==="MYR"?"RM "+Number(value).toLocaleString("en-MY"):"Rp "+Number(value).toLocaleString("id-ID");
function waLink(message){return "https://wa.me/"+WHATSAPP_NUMBER+"?text="+encodeURIComponent(message)}
function setWhatsAppLinks(){
  const generic="Halo admin PushGarage, saya mau tanya stock mobil yang tersedia.";
  ["heroWA","contactWA","floatWA"].forEach(id=>document.getElementById(id).href=waLink(generic));
}
function render(){
 const q=document.getElementById("search").value.toLowerCase().trim();
 const currency=document.getElementById("currency").value;
 const filter=document.getElementById("filter").value;
 const visible=CARS.filter(c=>c.name.toLowerCase().includes(q)&&(filter==="all"||c.status===filter));
 document.getElementById("count").textContent=visible.length+" mobil";
 const container=document.getElementById("cars");
 if(!visible.length){container.innerHTML='<div class="empty">Stock tidak ditemukan. Coba kata pencarian lain.</div>';return}
 container.innerHTML=visible.map(c=>{
   const price=currency==="MYR"?c.myr:c.idr;
   const other=currency==="MYR"?fmt(c.idr,"IDR"):fmt(c.myr,"MYR");
   const status=c.status==="sold"?"HABIS":"TERSEDIA";
   const image=c.image?'<img src="'+c.image.replace(/"/g,"&quot;")+'" alt="'+c.name.replace(/"/g,"&quot;")+'" loading="lazy" onerror="this.style.display=\'none\';this.nextElementSibling.style.display=\'flex\'">':'';
   const sold=c.status==="sold";
   const message="Halo admin PushGarage! Saya tertarik dengan mobil: "+c.name+". Harga yang terlihat: "+fmt(price,currency)+". Mohon konfirmasi stock dan detail pembayaran.";
   return '<article class="car"><div class="carImg">'+image+'<div class="placeholder" style="'+(c.image?'display:none':'')+'">🏎️</div><span class="tag">'+status+'</span></div><div class="carBody"><div class="carTop"><h3>'+c.name+'</h3><span class="stock '+(sold?'sold':'')+'">'+(sold?'SOLD OUT':'● LIVE STOCK')+'</span></div><div class="carDesc">'+c.note+'</div><div class="priceRow"><span class="price">'+(price>0?fmt(price,currency):"Tanya harga")+'</span><span class="otherPrice">'+(price>0?"· "+other:"")+'</span></div><div class="carButtons"><a class="btn primary" href="'+waLink(message)+'" target="_blank" rel="noopener">'+(sold?"TANYA LAGI":"ORDER VIA WA")+'</a></div></div></article>';
 }).join("");
}
["search","currency","filter"].forEach(id=>document.getElementById(id).addEventListener("input",render));
document.getElementById("year").textContent=new Date().getFullYear();
setWhatsAppLinks();render();
</script>
</body>
</html>
