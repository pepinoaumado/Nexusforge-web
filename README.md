# Nexusforge-web
Web de cheats para fornite,r6 etc
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NexusForge</title>
<style>
/* Estilos resumidos */
*{box-sizing:border-box;margin:0;padding:0;font-family:Segoe UI, system-ui, -apple-system, Roboto, Arial;}
body{background:#0f0f0f;color:#fff;scroll-behavior:smooth;}
header{position:fixed;top:0;left:0;right:0;display:flex;justify-content:center;gap:18px;padding:12px;background:rgba(0,0,0,0.85);z-index:50;transition:top .25s}
header a, header button{color:#fff;text-decoration:none;font-weight:600;background:transparent;border:none;cursor:pointer}
header .right{position:absolute;right:14px;top:10px;display:flex;gap:8px;align-items:center}
.hero{height:100vh;display:flex;flex-direction:column;justify-content:center;align-items:center;background:linear-gradient(180deg,#8e2de2 0%,#000 60%);text-align:center;padding:20px}
.hero h1{font-size:3rem;margin-bottom:14px}
.hero button{background:#b77fff;border:none;padding:10px 18px;border-radius:8px;color:#fff;cursor:pointer}
main{padding-top:84px;max-width:1200px;margin:0 auto;padding-bottom:80px}
section{margin:48px 16px}
h2{color:#b77fff;margin-bottom:16px;display:inline-block;border-bottom:2px solid #b77fff;padding-bottom:6px}
.card-container{display:flex;flex-wrap:wrap;gap:18px;justify-content:center}
.card{background:#121212;padding:16px;border-radius:12px;width:320px;box-shadow:0 6px 18px rgba(183,119,255,0.04)}
.card img{width:100%;border-radius:8px;margin-bottom:10px}
.card h3{text-align:center;margin-bottom:8px}
.price-option{display:flex;justify-content:space-between;align-items:center;margin:6px 0}
.price-option button{background:#b77fff;border:none;color:#fff;padding:6px 10px;border-radius:6px;cursor:pointer}
.view-btn{width:100%;margin-top:10px;padding:10px;border-radius:8px;border:none;background:#7f4bd9;color:#fff;cursor:pointer}
.checkout-panel{max-width:600px;margin:18px auto;background:#111;padding:16px;border-radius:10px}
.checkout-row{display:flex;gap:8px;margin:8px 0;align-items:center}
.checkout-row input[type="email"], .checkout-row input[type="text"]{flex:1;padding:8px;border-radius:6px;border:1px solid #222;background:#0b0b0b;color:#fff}
#cart-display{margin-top:18px;text-align:center;color:#ffd567;font-weight:700}
@media(max-width:820px){.card{width:92%}}
</style>
</head>
<body>

<header id="header">
  <a href="#home">Home</a>
  <a id="link-products" href="#products">Products</a>
  <a href="#reviews">Reviews</a>
  <a href="#terms">Terms</a>
  <a id="discord-link" href="https://discord.com" target="_blank">Discord</a>
  <div class="right">
    <select id="language" onchange="changeLanguage()">
      <option value="es">Español</option>
      <option value="en" selected>English</option>
      <option value="de">Deutsch</option>
    </select>
    <a id="download-link" style="display:none;color:#ffdd57;margin-left:8px;cursor:pointer">Download</a>
  </div>
</header>

<div id="home" class="hero">
  <h1>Welcome to NexusForge</h1>
  <button onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">Browse Products</button>
</div>

<main>
  <section id="products">
    <h2>Products</h2>
    <div class="card-container">

      <!-- Fortnite Private -->
      <div class="card">
        <img src="assets/img/fortnite_private.jpg" alt="Fortnite Private">
        <h3>Fortnite Private</h3>
        <div class="price-option">1 day - $10.80 <button onclick="addToCheckout('Fortnite Private','FP','1 day',10.80)">Add to Cart</button></div>
        <div class="price-option">3 days - $21 <button onclick="addToCheckout('Fortnite Private','FP','3 days',21)">Add to Cart</button></div>
        <div class="price-option">1 week - $38 <button onclick="addToCheckout('Fortnite Private','FP','1 week',38)">Add to Cart</button></div>
        <div class="price-option">1 month - $70 <button onclick="addToCheckout('Fortnite Private','FP','1 month',70)">Add to Cart</button></div>
        <div class="price-option">Lifetime - $259.99 <button onclick="addToCheckout('Fortnite Private','FP','Lifetime',259.99)">Add to Cart</button></div>
        <button class="view-btn" onclick="openModal('Fortnite Private','assets/video/demo.mp4')">Ver</button>
      </div>

      <!-- Fortnite Ultimate -->
      <div class="card">
        <img src="assets/img/fortnite_ultimate.jpg" alt="Fortnite Ultimate">
        <h3>Fortnite Ultimate</h3>
        <div class="price-option">1 day - $8.99 <button onclick="addToCheckout('Fortnite Ultimate','FU','1 day',8.99)">Add to Cart</button></div>
        <div class="price-option">3 days - $17 <button onclick="addToCheckout('Fortnite Ultimate','FU','3 days',17)">Add to Cart</button></div>
        <div class="price-option">1 week - $33 <button onclick="addToCheckout('Fortnite Ultimate','FU','1 week',33)">Add to Cart</button></div>
        <div class="price-option">1 month - $60 <button onclick="addToCheckout('Fortnite Ultimate','FU','1 month',60)">Add to Cart</button></div>
        <div class="price-option">Lifetime - $249.99 <button onclick="addToCheckout('Fortnite Ultimate','FU','Lifetime',249.99)">Add to Cart</button></div>
        <button class="view-btn" onclick="openModal('Fortnite Ultimate','assets/video/demo.mp4')">Ver</button>
      </div>

      <!-- R6 Full -->
      <div class="card">
        <img src="assets/img/r6_full.jpg" alt="R6 Full">
        <h3>R6 Full</h3>
        <div class="price-option">1 day - $9.99 <button onclick="addToCheckout('R6 Full','R6','1 day',9.99)">Add to Cart</button></div>
        <div class="price-option">3 days - $20 <button onclick="addToCheckout('R6 Full','R6','3 days',20)">Add to Cart</button></div>
        <div class="price-option">1 week - $37 <button onclick="addToCheckout('R6 Full','R6','1 week',37)">Add to Cart</button></div>
        <div class="price-option">1 month - $65 <button onclick="addToCheckout('R6 Full','R6','1 month',65)">Add to Cart</button></div>
        <div class="price-option">Lifetime - $259.99 <button onclick="addToCheckout('R6 Full','R6','Lifetime',259.99)">Add to Cart</button></div>
        <button class="view-btn" onclick="openModal('R6 Full','assets/video/demo.mp4')">Ver</button>
      </div>

      <!-- Battlefield 6 External -->
      <div class="card">
        <img src="assets/img/battlefield6.jpg" alt="Battlefield 6 External">
        <h3>Battlefield 6 External</h3>
        <div class="price-option">1 day - $12 <button onclick="addToCheckout('Battlefield 6','BF6','1 day',12)">Add to Cart</button></div>
        <div class="price-option">3 days - $25 <button onclick="addToCheckout('Battlefield 6','BF6','3 days',25)">Add to Cart</button></div>
        <div class="price-option">1 week - $42 <button onclick="addToCheckout('Battlefield 6','BF6','1 week',42)">Add to Cart</button></div>
        <div class="price-option">1 month - $75 <button onclick="addToCheckout('Battlefield 6','BF6','1 month',75)">Add to Cart</button></div>
        <div class="price-option">Lifetime - $279.99 <button onclick="addToCheckout('Battlefield 6','BF6','Lifetime',279.99)">Add to Cart</button></div>
        <button class="view-btn" onclick="openModal('Battlefield 6','assets/video/demo.mp4')">Ver</button>
      </div>

    </div>
  </section>

  <section id="reviews"><h2>Reviews</h2><p>Comentarios y opiniones de los usuarios.</p></section>
  <section id="terms"><h2>Terms</h2><p>Términos y condiciones de uso.</p></section>

  <!-- Video de ejemplo -->
  <section id="video-section" style="margin:48px 16px;text-align:center;position:relative">
    <video src="assets/video/demo.mp4" controls style="width:90%;border-radius:12px;"></video>
    <button onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})" style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);padding:14px 20px;background:#b77fff;border:none;color:#fff;border-radius:8px;font-size:1.2rem;cursor:pointer">Browse Products</button>
  </section>
</main>

<script>
let cartItems=[];let discountApplied=null;
function addToCheckout(title,packCode,duration,price){cartItems.push({title,packCode,duration,price});renderCartInfo();}
function renderCartInfo(){let total=cartItems.reduce((s,i)=>s+i.price,0);document.getElementById('checkout-summary').textContent=`${cartItems.length} items — Total: $${total.toFixed(2)}`;document.getElementById('cart-display').textContent=cartItems.map(i=>i.title+' '+i.duration+' — $'+i.price).join(' | ');}
function clearCart(){cartItems=[];discountApplied=null;renderCartInfo();document.getElementById('discount-code').value='';}
function applyDiscount(){const code=document.getElementById('discount-code').value.trim();if(!code){alert('Enter discount code');return;}if(code.toUpperCase()==='SAVE10'){discountApplied={code:'SAVE10',pct:10};alert('Discount applied: 10%');renderCartInfo();}else{alert('Invalid code');}}
function openModal(title,videoSrc){document.getElementById('modal').style.display='flex';document.getElementById('modal-title').textContent=title;const v=document.getElementById('modal-video');v.querySelector('source').src=videoSrc;v.load();document.getElementById('header').style.top='-80px';}
function closeModal(){document.getElementById('modal').style.display='none';document.getElementById('modal-video').pause();document.getElementById('header').style.top='0';}
async function startCheckout(){const email=document.getElementById('checkout-email').value.trim();if(!email){alert('Email required');return;}if(cartItems.length===0){alert('Cart is empty');return;}const body={email,discountCode:discountApplied?discountApplied.code:null,items:cartItems};try{const resp=await fetch('/create-checkout-session',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify(body)});const data=await resp.json();if(data.url){window.location=data.url;}else{alert('Error creating checkout session');console.error(data);}}catch(err){console.error(err);alert('Network error');}}
function checkPurchasesOnLoad(){try{fetch('/me/purchases').then(r=>r.json()).then(j=>{if(j.purchases&&j.purchases.length>0){document.getElementById('download-link').style.display='inline';document.getElementById('download-link').onclick=()=>window.location.href='/downloads';}});}catch(e){}}
window.addEventListener('load',checkPurchasesOnLoad);
function changeLanguage(){alert('Idioma cambiado (demo)');}
</script>
</body>
</html>
