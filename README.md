<!DOCTYPE html>

<html lang="he" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>אור החגים – פעילויות וקבלת שבת</title>
<link href="https://fonts.googleapis.com/css2?family=Frank+Ruhl+Libre:wght@300;400;700;900&family=Heebo:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #D4AF37;
    --gold-light: #F5E27A;
    --deep-blue: #0A1628;
    --mid-blue: #112244;
    --sky-blue: #1A3A6B;
    --flame-orange: #FF6B1A;
    --flame-yellow: #FFD700;
    --white: #F8F4E8;
    --cream: #FDF6E3;
    --text: #E8DFC8;
  }

- { margin: 0; padding: 0; box-sizing: border-box; }

body {
font-family: ‘Heebo’, sans-serif;
background: var(–deep-blue);
color: var(–text);
min-height: 100vh;
overflow-x: hidden;
}

/* ===== SKY & STARS BACKGROUND ===== */
.bg-sky {
position: fixed;
inset: 0;
background: radial-gradient(ellipse at 50% 0%, #1A3A6B 0%, #0A1628 60%, #050D1A 100%);
z-index: 0;
}

.stars {
position: fixed;
inset: 0;
z-index: 1;
pointer-events: none;
}
.star {
position: absolute;
width: 2px; height: 2px;
background: white;
border-radius: 50%;
animation: twinkle var(–d, 3s) ease-in-out infinite;
opacity: var(–o, 0.7);
}
@keyframes twinkle {
0%, 100% { opacity: var(–o, 0.7); transform: scale(1); }
50% { opacity: 0.2; transform: scale(0.5); }
}

/* ===== CHANUKIAH ===== */
.chanukiah-wrap {
position: fixed;
bottom: 0;
left: 50%;
transform: translateX(-50%);
z-index: 2;
pointer-events: none;
width: 500px;
opacity: 0.18;
}
.chanukiah-svg { width: 100%; }

/* ===== CONTENT ===== */
.content {
position: relative;
z-index: 10;
min-height: 100vh;
}

/* ===== HEADER ===== */
header {
text-align: center;
padding: 50px 20px 30px;
position: relative;
}
.logo-menorah {
font-size: 52px;
margin-bottom: 10px;
animation: glow-pulse 2s ease-in-out infinite;
display: block;
}
@keyframes glow-pulse {
0%, 100% { text-shadow: 0 0 20px #FFD700, 0 0 40px #FF6B1A; }
50% { text-shadow: 0 0 40px #FFD700, 0 0 80px #FF6B1A, 0 0 120px #FF4400; }
}
header h1 {
font-family: ‘Frank Ruhl Libre’, serif;
font-size: clamp(2rem, 6vw, 3.5rem);
font-weight: 900;
background: linear-gradient(135deg, var(–gold-light), var(–gold), var(–flame-orange));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
line-height: 1.1;
margin-bottom: 8px;
}
header p {
color: #8BA0C0;
font-size: 1rem;
font-weight: 300;
letter-spacing: 0.05em;
}

/* ===== NAV ===== */
nav {
display: flex;
justify-content: center;
gap: 12px;
flex-wrap: wrap;
padding: 0 20px 30px;
}
.nav-btn {
background: rgba(212,175,55,0.1);
border: 1px solid rgba(212,175,55,0.3);
color: var(–gold);
padding: 10px 22px;
border-radius: 30px;
cursor: pointer;
font-family: ‘Heebo’, sans-serif;
font-size: 0.9rem;
font-weight: 500;
transition: all 0.3s;
backdrop-filter: blur(10px);
}
.nav-btn:hover, .nav-btn.active {
background: var(–gold);
color: var(–deep-blue);
box-shadow: 0 0 20px rgba(212,175,55,0.4);
}

/* ===== SECTIONS ===== */
.section {
display: none;
max-width: 900px;
margin: 0 auto;
padding: 0 20px 80px;
animation: fadeUp 0.4s ease;
}
.section.active { display: block; }
@keyframes fadeUp {
from { opacity: 0; transform: translateY(20px); }
to { opacity: 1; transform: translateY(0); }
}

/* ===== SECTION TITLE ===== */
.section-title {
font-family: ‘Frank Ruhl Libre’, serif;
font-size: 1.8rem;
font-weight: 700;
color: var(–gold);
text-align: center;
margin-bottom: 30px;
padding-bottom: 15px;
border-bottom: 1px solid rgba(212,175,55,0.2);
}

/* ===== ACTIVITY CARDS ===== */
.cards-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
gap: 20px;
}
.card {
background: rgba(17,34,68,0.7);
border: 1px solid rgba(212,175,55,0.2);
border-radius: 16px;
overflow: hidden;
cursor: pointer;
transition: all 0.3s;
backdrop-filter: blur(12px);
}
.card:hover {
transform: translateY(-6px);
border-color: var(–gold);
box-shadow: 0 10px 40px rgba(212,175,55,0.2);
}
.card-img {
height: 140px;
display: flex;
align-items: center;
justify-content: center;
font-size: 60px;
background: linear-gradient(135deg, rgba(212,175,55,0.1), rgba(255,107,26,0.1));
}
.card-body { padding: 18px; }
.card-title {
font-family: ‘Frank Ruhl Libre’, serif;
font-size: 1.2rem;
font-weight: 700;
color: var(–gold-light);
margin-bottom: 6px;
}
.card-desc { font-size: 0.85rem; color: #8BA0C0; line-height: 1.5; margin-bottom: 12px; }
.card-price {
font-size: 1rem;
font-weight: 700;
color: var(–flame-orange);
}
.card-badge {
display: inline-block;
background: rgba(212,175,55,0.15);
border: 1px solid rgba(212,175,55,0.3);
color: var(–gold);
font-size: 0.75rem;
padding: 3px 10px;
border-radius: 20px;
margin-bottom: 8px;
}

/* ===== SHABBAT CARD ===== */
.shabbat-hero {
background: linear-gradient(135deg, rgba(17,34,68,0.9), rgba(26,58,107,0.7));
border: 1px solid rgba(212,175,55,0.35);
border-radius: 20px;
padding: 40px;
text-align: center;
margin-bottom: 30px;
position: relative;
overflow: hidden;
backdrop-filter: blur(12px);
}
.shabbat-hero::before {
content: ‘’;
position: absolute;
inset: 0;
background: radial-gradient(ellipse at 50% 0%, rgba(212,175,55,0.1) 0%, transparent 70%);
pointer-events: none;
}
.shabbat-hero h2 {
font-family: ‘Frank Ruhl Libre’, serif;
font-size: 2.2rem;
font-weight: 900;
color: var(–gold);
margin-bottom: 12px;
}
.shabbat-hero p { color: #8BA0C0; font-size: 1rem; line-height: 1.6; margin-bottom: 20px; }
.shabbat-time {
display: inline-block;
background: rgba(212,175,55,0.15);
border: 1px solid var(–gold);
padding: 10px 25px;
border-radius: 30px;
color: var(–gold-light);
font-size: 1.1rem;
font-weight: 700;
margin-bottom: 25px;
}
.shabbat-menu {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
gap: 12px;
text-align: right;
margin-bottom: 25px;
}
.menu-item {
background: rgba(255,255,255,0.04);
border: 1px solid rgba(212,175,55,0.15);
border-radius: 10px;
padding: 12px 16px;
font-size: 0.9rem;
color: var(–text);
}
.menu-item span { color: var(–gold); margin-left: 6px; }

/* ===== BUTTONS ===== */
.btn-primary {
background: linear-gradient(135deg, var(–gold), var(–flame-orange));
color: var(–deep-blue);
border: none;
padding: 14px 35px;
border-radius: 30px;
font-family: ‘Heebo’, sans-serif;
font-size: 1rem;
font-weight: 700;
cursor: pointer;
transition: all 0.3s;
box-shadow: 0 4px 20px rgba(212,175,55,0.3);
}
.btn-primary:hover {
transform: translateY(-2px);
box-shadow: 0 8px 30px rgba(212,175,55,0.5);
}
.btn-secondary {
background: transparent;
color: var(–gold);
border: 1px solid var(–gold);
padding: 12px 28px;
border-radius: 30px;
font-family: ‘Heebo’, sans-serif;
font-size: 0.95rem;
font-weight: 500;
cursor: pointer;
transition: all 0.3s;
}
.btn-secondary:hover { background: rgba(212,175,55,0.1); }

/* ===== MODAL ===== */
.modal-overlay {
display: none;
position: fixed;
inset: 0;
background: rgba(5,13,26,0.92);
z-index: 100;
align-items: center;
justify-content: center;
padding: 20px;
backdrop-filter: blur(6px);
animation: fadeIn 0.3s ease;
}
.modal-overlay.open { display: flex; }
@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

.modal {
background: linear-gradient(160deg, #0E1F3D, #0A1628);
border: 1px solid rgba(212,175,55,0.3);
border-radius: 20px;
padding: 35px;
max-width: 520px;
width: 100%;
max-height: 90vh;
overflow-y: auto;
position: relative;
animation: slideUp 0.3s ease;
box-shadow: 0 20px 60px rgba(0,0,0,0.6), 0 0 40px rgba(212,175,55,0.1);
}
@keyframes slideUp {
from { opacity: 0; transform: translateY(30px); }
to { opacity: 1; transform: translateY(0); }
}
.modal::-webkit-scrollbar { width: 4px; }
.modal::-webkit-scrollbar-track { background: transparent; }
.modal::-webkit-scrollbar-thumb { background: rgba(212,175,55,0.3); border-radius: 2px; }

.modal-close {
position: absolute;
top: 15px;
left: 15px;
background: rgba(212,175,55,0.1);
border: 1px solid rgba(212,175,55,0.2);
color: var(–gold);
width: 32px; height: 32px;
border-radius: 50%;
cursor: pointer;
font-size: 1.1rem;
display: flex; align-items: center; justify-content: center;
transition: all 0.2s;
}
.modal-close:hover { background: rgba(212,175,55,0.2); }

.modal-title {
font-family: ‘Frank Ruhl Libre’, serif;
font-size: 1.6rem;
font-weight: 700;
color: var(–gold);
margin-bottom: 6px;
text-align: center;
}
.modal-subtitle { text-align: center; color: #8BA0C0; font-size: 0.9rem; margin-bottom: 25px; }

/* ===== STEPS ===== */
.steps-bar {
display: flex;
justify-content: center;
gap: 8px;
margin-bottom: 28px;
}
.step-dot {
width: 28px; height: 28px;
border-radius: 50%;
border: 2px solid rgba(212,175,55,0.3);
color: #8BA0C0;
font-size: 0.75rem;
font-weight: 700;
display: flex; align-items: center; justify-content: center;
transition: all 0.3s;
}
.step-dot.active { border-color: var(–gold); color: var(–gold); background: rgba(212,175,55,0.15); }
.step-dot.done { border-color: var(–gold); background: var(–gold); color: var(–deep-blue); }

.step-panel { display: none; }
.step-panel.active { display: block; animation: fadeUp 0.3s ease; }

/* ===== FORM ===== */
.form-row { margin-bottom: 16px; }
.form-row label {
display: block;
font-size: 0.85rem;
color: var(–gold);
margin-bottom: 6px;
font-weight: 500;
}
.form-row input, .form-row select {
width: 100%;
background: rgba(255,255,255,0.05);
border: 1px solid rgba(212,175,55,0.25);
border-radius: 10px;
padding: 12px 14px;
color: var(–white);
font-family: ‘Heebo’, sans-serif;
font-size: 0.95rem;
transition: border-color 0.2s;
outline: none;
}
.form-row input:focus, .form-row select:focus {
border-color: var(–gold);
background: rgba(212,175,55,0.06);
}
.form-row input::placeholder { color: #4A6080; }
.form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }

/* ===== ID CAMERA ===== */
.id-section {
background: rgba(255,255,255,0.03);
border: 1px dashed rgba(212,175,55,0.3);
border-radius: 14px;
padding: 20px;
text-align: center;
margin-bottom: 16px;
cursor: pointer;
transition: all 0.3s;
}
.id-section:hover { border-color: var(–gold); background: rgba(212,175,55,0.05); }
.id-section-icon { font-size: 2.5rem; margin-bottom: 10px; }
.id-section h4 { color: var(–gold-light); font-size: 1rem; margin-bottom: 5px; }
.id-section p { color: #8BA0C0; font-size: 0.8rem; }
.id-options { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 16px; }
.id-option-btn {
background: rgba(212,175,55,0.08);
border: 1px solid rgba(212,175,55,0.25);
border-radius: 12px;
padding: 16px 12px;
text-align: center;
cursor: pointer;
transition: all 0.3s;
color: var(–text);
}
.id-option-btn:hover { border-color: var(–gold); background: rgba(212,175,55,0.15); }
.id-option-btn .icon { font-size: 1.8rem; display: block; margin-bottom: 6px; }
.id-option-btn span { font-size: 0.85rem; color: var(–gold-light); }

/* Camera */
#camera-area {
display: none;
text-align: center;
}
#camera-area.active { display: block; }
#camera-video {
width: 100%;
border-radius: 12px;
border: 2px solid var(–gold);
background: #000;
max-height: 220px;
object-fit: cover;
}
#camera-canvas { display: none; }
#captured-img {
width: 100%;
border-radius: 12px;
border: 2px solid #4CAF50;
max-height: 220px;
object-fit: cover;
display: none;
}
.camera-btns { display: flex; gap: 10px; justify-content: center; margin-top: 12px; flex-wrap: wrap; }
.btn-cam {
background: rgba(212,175,55,0.15);
border: 1px solid var(–gold);
color: var(–gold);
padding: 9px 18px;
border-radius: 20px;
cursor: pointer;
font-family: ‘Heebo’, sans-serif;
font-size: 0.85rem;
font-weight: 500;
transition: all 0.2s;
}
.btn-cam:hover { background: rgba(212,175,55,0.25); }

/* ===== CREDIT CARD ===== */
.credit-card-visual {
background: linear-gradient(135deg, #1A2A4A, #2A4A7A);
border: 1px solid rgba(212,175,55,0.4);
border-radius: 16px;
padding: 22px;
margin-bottom: 20px;
position: relative;
overflow: hidden;
box-shadow: 0 8px 30px rgba(0,0,0,0.4);
}
.credit-card-visual::before {
content: ‘’;
position: absolute;
top: -40px; right: -40px;
width: 120px; height: 120px;
background: rgba(212,175,55,0.08);
border-radius: 50%;
}
.credit-card-visual::after {
content: ‘’;
position: absolute;
bottom: -30px; left: -30px;
width: 90px; height: 90px;
background: rgba(255,107,26,0.08);
border-radius: 50%;
}
.card-chip { font-size: 1.8rem; margin-bottom: 14px; display: block; }
.card-number-display {
font-size: 1.2rem;
letter-spacing: 0.15em;
color: var(–gold-light);
font-weight: 700;
margin-bottom: 12px;
font-family: monospace;
}
.card-info-row {
display: flex;
justify-content: space-between;
font-size: 0.78rem;
color: #8BA0C0;
}
.card-info-row span:last-child { font-weight: 600; color: var(–text); }

.notice-box {
background: rgba(255,107,26,0.08);
border: 1px solid rgba(255,107,26,0.25);
border-radius: 10px;
padding: 12px 16px;
font-size: 0.82rem;
color: #FF9966;
margin-bottom: 18px;
line-height: 1.5;
}

/* ===== SUCCESS ===== */
.success-screen {
text-align: center;
padding: 20px;
}
.success-icon {
font-size: 4rem;
margin-bottom: 15px;
animation: bounceIn 0.6s cubic-bezier(0.68,-0.55,0.265,1.55);
}
@keyframes bounceIn {
from { opacity: 0; transform: scale(0.3); }
to { opacity: 1; transform: scale(1); }
}
.success-screen h3 {
font-family: ‘Frank Ruhl Libre’, serif;
font-size: 1.8rem;
color: var(–gold);
margin-bottom: 10px;
}
.success-screen p { color: #8BA0C0; font-size: 0.95rem; line-height: 1.6; }
.success-details {
background: rgba(212,175,55,0.06);
border: 1px solid rgba(212,175,55,0.2);
border-radius: 12px;
padding: 18px;
margin: 20px 0;
text-align: right;
}
.success-details div {
display: flex;
justify-content: space-between;
padding: 6px 0;
border-bottom: 1px solid rgba(212,175,55,0.1);
font-size: 0.9rem;
}
.success-details div:last-child { border-bottom: none; }
.success-details div span:first-child { color: #8BA0C0; }
.success-details div span:last-child { color: var(–gold-light); font-weight: 600; }

.modal-footer { display: flex; gap: 10px; justify-content: flex-end; margin-top: 20px; flex-wrap: wrap; }

/* Scrollbar */
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: var(–deep-blue); }
::-webkit-scrollbar-thumb { background: rgba(212,175,55,0.3); border-radius: 3px; }

@media (max-width: 480px) {
.form-grid { grid-template-columns: 1fr; }
.id-options { grid-template-columns: 1fr 1fr; }
.modal { padding: 25px 18px; }
header h1 { font-size: 1.8rem; }
}
</style>

</head>
<body>

<div class="bg-sky"></div>
<div class="stars" id="stars"></div>

<!-- Chanukiah background decoration -->

<div class="chanukiah-wrap">
  <svg class="chanukiah-svg" viewBox="0 0 500 300" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- Base -->
    <rect x="200" y="270" width="100" height="12" rx="6" fill="#D4AF37" opacity="0.8"/>
    <rect x="230" y="240" width="40" height="32" rx="4" fill="#D4AF37" opacity="0.8"/>
    <!-- Main arm -->
    <rect x="60" y="225" width="380" height="8" rx="4" fill="#D4AF37" opacity="0.8"/>
    <!-- Candle holders - 9 positions -->
    <g opacity="0.9">
      <!-- Shamash (center, raised) -->
      <rect x="246" y="165" width="8" height="62" rx="3" fill="#D4AF37"/>
      <!-- Left candles -->
      <rect x="86" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <rect x="126" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <rect x="166" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <rect x="206" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <!-- Right candles -->
      <rect x="286" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <rect x="326" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <rect x="366" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
      <rect x="406" y="195" width="8" height="32" rx="3" fill="#D4AF37"/>
    </g>
    <!-- Flames -->
    <g opacity="0.95">
      <ellipse cx="250" cy="155" rx="6" ry="12" fill="#FFD700"/>
      <ellipse cx="90" cy="183" rx="5" ry="10" fill="#FF6B1A"/>
      <ellipse cx="130" cy="183" rx="5" ry="10" fill="#FFD700"/>
      <ellipse cx="170" cy="183" rx="5" ry="10" fill="#FF6B1A"/>
      <ellipse cx="210" cy="183" rx="5" ry="10" fill="#FFD700"/>
      <ellipse cx="290" cy="183" rx="5" ry="10" fill="#FF6B1A"/>
      <ellipse cx="330" cy="183" rx="5" ry="10" fill="#FFD700"/>
      <ellipse cx="370" cy="183" rx="5" ry="10" fill="#FF6B1A"/>
      <ellipse cx="410" cy="183" rx="5" ry="10" fill="#FFD700"/>
    </g>
  </svg>
</div>

<!-- ===== MAIN CONTENT ===== -->

<div class="content">
  <header>
    <span class="logo-menorah">🕎</span>
    <h1>אור החגים</h1>
    <p>פעילויות, קבלת שבת ואירועים מיוחדים</p>
  </header>

  <nav>
    <button class="nav-btn active" onclick="showSection('activities')">🎉 פעילויות</button>
    <button class="nav-btn" onclick="showSection('shabbat')">🕯️ קבלת שבת</button>
    <button class="nav-btn" onclick="showSection('about')">✨ אודות</button>
  </nav>

  <!-- ACTIVITIES -->

  <section id="sec-activities" class="section active">
    <h2 class="section-title">🎊 פעילויות קרובות</h2>
    <div class="cards-grid">
      <div class="card" onclick="openRegModal('סדנת סביבונים וניסים', '₪85', '🌀')">
        <div class="card-img">🌀</div>
        <div class="card-body">
          <span class="card-badge">חנוכה</span>
          <div class="card-title">סדנת סביבונים וניסים</div>
          <div class="card-desc">צרו סביבון ייחודי ביד, שמעו סיפורי חנוכה ואכלו סופגניות טריות</div>
          <div class="card-price">₪85 לאדם</div>
        </div>
      </div>
      <div class="card" onclick="openRegModal('ערב לטבילת סופגניות', '₪65', '🍩')">
        <div class="card-img">🍩</div>
        <div class="card-body">
          <span class="card-badge">חנוכה</span>
          <div class="card-title">ערב לטבילת סופגניות</div>
          <div class="card-desc">10 מילויים שונים, תחרות הסופגניה המוצלחת ופעילות לכל המשפחה</div>
          <div class="card-price">₪65 לאדם</div>
        </div>
      </div>
      <div class="card" onclick="openRegModal('הדלקת נרות קהילתית', 'חינם', '🕯️')">
        <div class="card-img">🕯️</div>
        <div class="card-body">
          <span class="card-badge">ציבורי</span>
          <div class="card-title">הדלקת נרות קהילתית</div>
          <div class="card-desc">הדלקה מרכזית ברחבת העיר, שירה, ריקודים ומוזיקה חיה לכל המשפחה</div>
          <div class="card-price" style="color:#4CAF50">כניסה חופשית</div>
        </div>
      </div>
      <div class="card" onclick="openRegModal('סיור מדריך – ירושלים בחנוכה', '₪120', '🏛️')">
        <div class="card-img">🏛️</div>
        <div class="card-body">
          <span class="card-badge">תרבות</span>
          <div class="card-title">סיור מדריך – ירושלים בחנוכה</div>
          <div class="card-desc">סיור לאור נרות ברחובות העיר העתיקה עם מדריך תיירות מוסמך</div>
          <div class="card-price">₪120 לאדם</div>
        </div>
      </div>
      <div class="card" onclick="openRegModal('אומנות ואור – ציור חנוכיות', '₪95', '🎨')">
        <div class="card-img">🎨</div>
        <div class="card-body">
          <span class="card-badge">יצירה</span>
          <div class="card-title">אומנות ואור – ציור חנוכיות</div>
          <div class="card-desc">סדנת ציור אקריליק מונחה, חנוכיה אישית לקחת הביתה</div>
          <div class="card-price">₪95 לאדם</div>
        </div>
      </div>
      <div class="card" onclick="openRegModal('ספייק נרות חנוכה הגדול', '₪55', '🏆')">
        <div class="card-img">🏆</div>
        <div class="card-body">
          <span class="card-badge">תחרות</span>
          <div class="card-title">טורניר הספייק של חנוכה</div>
          <div class="card-desc">טורניר ספייק 3x3 לכבוד החג, פרסים לזוכים וחנוכיה לכל משתתף</div>
          <div class="card-price">₪55 לקבוצה</div>
        </div>
      </div>
    </div>
  </section>

  <!-- SHABBAT -->

  <section id="sec-shabbat" class="section">
    <div class="shabbat-hero">
      <h2>🕯️ קבלת שבת</h2>
      <p>הצטרפו לארוחת שישי חגיגית, ברכות שבת, ניגוני חסידים וסעודה מסורתית מלאה</p>
      <div class="shabbat-time">⏰ כל שישי | כניסה שעה לפני השקיעה</div>

```
  <div class="shabbat-menu">
    <div class="menu-item"><span>🍷</span> קידוש ולחמניות</div>
    <div class="menu-item"><span>🐟</span> דג גפילטע ביתי</div>
    <div class="menu-item"><span>🥣</span> מרק עוף אמיתי</div>
    <div class="menu-item"><span>🥩</span> עוף צלוי / בשר</div>
    <div class="menu-item"><span>🥗</span> סלטים ביתיים</div>
    <div class="menu-item"><span>🍮</span> קינוח מסורתי</div>
  </div>

  <div style="margin-bottom:10px;color:#8BA0C0;font-size:0.85rem">
    נדרשת הרשמה מראש – מקומות מוגבלים
  </div>
  <button class="btn-primary" onclick="openRegModal('קבלת שבת – ארוחת שישי', '₪180 לאדם', '🕯️')">
    הרשמה לקבלת שבת
  </button>
</div>
```

  </section>

  <!-- ABOUT -->

  <section id="sec-about" class="section">
    <div class="shabbat-hero">
      <h2 style="font-size:1.6rem">✨ אודות אור החגים</h2>
      <p>אנחנו מאמינים שהחגים הם לא רק תאריכים בלוח השנה – הם חוויות שמחברות משפחות, קהילות ולבבות. עם מגוון פעילויות לכל הגילאים וקבלות שבת חמות ומסורתיות, אנחנו כאן כדי שתוכלו לחגוג בגדול.</p>
      <br>
      <p style="color:var(--gold-light)">📧 info@orchagim.co.il &nbsp;|&nbsp; 📞 03-1234567</p>
    </div>
  </section>
</div>

<!-- ===== REGISTRATION MODAL ===== -->

<div class="modal-overlay" id="regModal">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-title" id="modal-event-title">הרשמה לאירוע</div>
    <div class="modal-subtitle" id="modal-event-sub">מלאו את הפרטים להשלמת ההרשמה</div>

```
<!-- Steps indicator -->
<div class="steps-bar">
  <div class="step-dot active" id="dot-1">1</div>
  <div class="step-dot" id="dot-2">2</div>
  <div class="step-dot" id="dot-3">3</div>
  <div class="step-dot" id="dot-4">4</div>
</div>

<!-- Step 1: Personal Info -->
<div class="step-panel active" id="step-1">
  <h4 style="color:var(--gold-light);margin-bottom:18px;font-size:1rem">👤 פרטים אישיים</h4>
  <div class="form-grid">
    <div class="form-row">
      <label>שם פרטי *</label>
      <input type="text" id="fname" placeholder="שם פרטי">
    </div>
    <div class="form-row">
      <label>שם משפחה *</label>
      <input type="text" id="lname" placeholder="שם משפחה">
    </div>
  </div>
  <div class="form-row">
    <label>מספר תעודת זהות *</label>
    <input type="text" id="idnum" placeholder="000000000" maxlength="9">
  </div>
  <div class="form-row">
    <label>תאריך לידה *</label>
    <input type="date" id="bdate">
  </div>
  <div class="form-row">
    <label>טלפון נייד *</label>
    <input type="tel" id="phone" placeholder="05X-XXXXXXX">
  </div>
  <div class="form-row">
    <label>כתובת אימייל *</label>
    <input type="email" id="email" placeholder="your@email.com">
  </div>
  <div class="form-row">
    <label>כמות משתתפים</label>
    <select id="guests">
      <option value="1">1 אדם</option>
      <option value="2">2 אנשים</option>
      <option value="3">3 אנשים</option>
      <option value="4">4 אנשים</option>
      <option value="5">5+ אנשים</option>
    </select>
  </div>
  <div class="modal-footer">
    <button class="btn-primary" onclick="goStep(2)">הבא ← זיהוי</button>
  </div>
</div>

<!-- Step 2: ID Verification -->
<div class="step-panel" id="step-2">
  <h4 style="color:var(--gold-light);margin-bottom:18px;font-size:1rem">🪪 אימות זהות</h4>
  <div id="id-choice-area">
    <p style="color:#8BA0C0;font-size:0.85rem;margin-bottom:16px;line-height:1.5">
      לאימות זהות אנא צלמו/העלו תמונה של תעודת הזהות או הדרכון שלכם
    </p>
    <div class="id-options">
      <div class="id-option-btn" onclick="startCamera('id')">
        <span class="icon">📷</span>
        <span>צלם תעודת זהות</span>
      </div>
      <div class="id-option-btn" onclick="startCamera('passport')">
        <span class="icon">📘</span>
        <span>צלם דרכון</span>
      </div>
      <div class="id-option-btn" onclick="uploadFile()">
        <span class="icon">📤</span>
        <span>העלה קובץ</span>
      </div>
      <div class="id-option-btn" onclick="skipId()">
        <span class="icon">⏭️</span>
        <span>דלג לעכשיו</span>
      </div>
    </div>
  </div>

  <div id="camera-area" class="camera-area">
    <p style="color:var(--gold);font-size:0.85rem;margin-bottom:10px;text-align:center" id="cam-title">מצלמת תעודת זהות</p>
    <video id="camera-video" autoplay playsinline></video>
    <canvas id="camera-canvas"></canvas>
    <img id="captured-img" alt="תמונה שצולמה">
    <div class="camera-btns">
      <button class="btn-cam" id="snap-btn" onclick="snapPhoto()">📸 צלם</button>
      <button class="btn-cam" id="retake-btn" onclick="retakePhoto()" style="display:none">🔄 צלם מחדש</button>
      <button class="btn-cam" onclick="stopCamera()" style="color:#FF6666;border-color:#FF6666">✕ סגור</button>
    </div>
    <div id="capture-ok" style="display:none;text-align:center;margin-top:8px;color:#4CAF50;font-size:0.85rem">
      ✅ התמונה נשמרה בהצלחה!
    </div>
  </div>

  <input type="file" id="file-upload" accept="image/*,.pdf" style="display:none" onchange="fileUploaded(this)">

  <div id="id-success-msg" style="display:none;background:rgba(76,175,80,0.1);border:1px solid rgba(76,175,80,0.3);border-radius:10px;padding:12px;text-align:center;margin-top:12px;color:#4CAF50;font-size:0.9rem">
    ✅ מסמך זהות אומת בהצלחה!
  </div>

  <div class="modal-footer" style="margin-top:20px">
    <button class="btn-secondary" onclick="goStep(1)">← חזרה</button>
    <button class="btn-primary" onclick="goStep(3)">הבא ← תשלום</button>
  </div>
</div>

<!-- Step 3: Payment -->
<div class="step-panel" id="step-3">
  <h4 style="color:var(--gold-light);margin-bottom:14px;font-size:1rem">💳 פרטי תשלום</h4>

  <div class="credit-card-visual">
    <span class="card-chip">💳</span>
    <div class="card-number-display" id="card-display">•••• •••• •••• ••••</div>
    <div class="card-info-row">
      <div><div style="font-size:0.7rem;margin-bottom:3px">שם בעל הכרטיס</div><span id="card-name-display">שמך כאן</span></div>
      <div><div style="font-size:0.7rem;margin-bottom:3px">תוקף</div><span id="card-exp-display">MM/YY</span></div>
    </div>
  </div>

  <div class="notice-box">
    ℹ️ פרטי האשראי מועברים בצורה מאובטחת לחברת הסליקה. האתר לא שומר פרטי כרטיס.
  </div>

  <div class="form-row">
    <label>שם בעל הכרטיס</label>
    <input type="text" id="card-name" placeholder="שם מלא כפי שמופיע בכרטיס" oninput="document.getElementById('card-name-display').textContent=this.value||'שמך כאן'">
  </div>
  <div class="form-row">
    <label>מספר כרטיס</label>
    <input type="text" id="card-num" placeholder="0000 0000 0000 0000" maxlength="19" oninput="formatCardNum(this)">
  </div>
  <div class="form-grid">
    <div class="form-row">
      <label>תוקף</label>
      <input type="text" id="card-exp" placeholder="MM/YY" maxlength="5" oninput="formatExp(this)">
    </div>
    <div class="form-row">
      <label>CVV</label>
      <input type="text" id="card-cvv" placeholder="•••" maxlength="4">
    </div>
  </div>
  <div class="form-row">
    <label>מספר תשלומים</label>
    <select id="installments">
      <option value="1">תשלום אחד</option>
      <option value="3">3 תשלומים</option>
      <option value="6">6 תשלומים</option>
      <option value="12">12 תשלומים</option>
    </select>
  </div>

  <div class="modal-footer">
    <button class="btn-secondary" onclick="goStep(2)">← חזרה</button>
    <button class="btn-primary" onclick="submitPayment()">✨ אישור ותשלום</button>
  </div>
</div>

<!-- Step 4: Success -->
<div class="step-panel" id="step-4">
  <div class="success-screen">
    <div class="success-icon">🎉</div>
    <h3>נרשמת בהצלחה!</h3>
    <p>ברכות! ההרשמה לאירוע אושרה. אישור ישלח לאימייל שלך</p>
    <div class="success-details" id="confirm-details">
      <div><span>אירוע</span><span id="conf-event">-</span></div>
      <div><span>שם</span><span id="conf-name">-</span></div>
      <div><span>אימייל</span><span id="conf-email">-</span></div>
      <div><span>מחיר</span><span id="conf-price">-</span></div>
      <div><span>מספר אישור</span><span id="conf-num">-</span></div>
    </div>
    <p style="color:var(--gold);font-size:0.9rem">🕎 נתראה בחגיגה! חג אורים שמח!</p>
    <div style="margin-top:20px">
      <button class="btn-primary" onclick="closeModal()">סגור</button>
    </div>
  </div>
</div>
```

  </div>
</div>

<script>
// ===== STARS =====
const starsEl = document.getElementById('stars');
for (let i = 0; i < 120; i++) {
  const s = document.createElement('div');
  s.className = 'star';
  s.style.cssText = `left:${Math.random()*100}%;top:${Math.random()*80}%;--d:${2+Math.random()*4}s;--o:${0.3+Math.random()*0.7};width:${1+Math.random()*2}px;height:${1+Math.random()*2}px;animation-delay:${Math.random()*5}s`;
  starsEl.appendChild(s);
}

// ===== NAV =====
let currentEvent = '', currentPrice = '', currentIcon = '';

function showSection(name) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('sec-' + name).classList.add('active');
  event.currentTarget.classList.add('active');
}

// ===== MODAL =====
function openRegModal(title, price, icon) {
  currentEvent = title;
  currentPrice = price;
  currentIcon = icon;
  document.getElementById('modal-event-title').textContent = icon + ' ' + title;
  document.getElementById('modal-event-sub').textContent = 'מחיר: ' + price + ' | מלאו את הפרטים להשלמת ההרשמה';
  document.getElementById('regModal').classList.add('open');
  goStep(1, true);
}

function closeModal() {
  document.getElementById('regModal').classList.remove('open');
  stopCamera();
}

document.getElementById('regModal').addEventListener('click', function(e) {
  if (e.target === this) closeModal();
});

// ===== STEPS =====
let currentStep = 1;
function goStep(n, reset) {
  document.querySelectorAll('.step-panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.step-dot').forEach((d, i) => {
    d.classList.remove('active', 'done');
    if (i + 1 < n) d.classList.add('done');
    else if (i + 1 === n) d.classList.add('active');
  });
  document.getElementById('step-' + n).classList.add('active');
  currentStep = n;
  if (reset) {
    document.getElementById('id-success-msg').style.display = 'none';
    document.getElementById('id-choice-area').style.display = '';
    stopCamera();
  }
}

// ===== CAMERA =====
let stream = null, capturedData = null;

async function startCamera(type) {
  document.getElementById('id-choice-area').style.display = 'none';
  const area = document.getElementById('camera-area');
  area.classList.add('active');
  document.getElementById('cam-title').textContent = type === 'id' ? '📷 מצלמת תעודת זהות' : '📘 מצלמת דרכון';
  document.getElementById('snap-btn').style.display = '';
  document.getElementById('retake-btn').style.display = 'none';
  document.getElementById('captured-img').style.display = 'none';
  document.getElementById('capture-ok').style.display = 'none';
  document.getElementById('camera-video').style.display = '';

  try {
    stream = await navigator.mediaDevices.getUserMedia({
      video: { facingMode: { ideal: 'environment' }, width: { ideal: 1280 }, height: { ideal: 720 } }
    });
    document.getElementById('camera-video').srcObject = stream;
  } catch (err) {
    alert('לא ניתן לגשת למצלמה. אנא בדקו הרשאות בדפדפן.');
    stopCamera();
    document.getElementById('id-choice-area').style.display = '';
  }
}

function snapPhoto() {
  const video = document.getElementById('camera-video');
  const canvas = document.getElementById('camera-canvas');
  canvas.width = video.videoWidth || 640;
  canvas.height = video.videoHeight || 480;
  canvas.getContext('2d').drawImage(video, 0, 0);
  capturedData = canvas.toDataURL('image/jpeg', 0.8);

  const img = document.getElementById('captured-img');
  img.src = capturedData;
  img.style.display = 'block';
  video.style.display = 'none';
  document.getElementById('snap-btn').style.display = 'none';
  document.getElementById('retake-btn').style.display = '';
  document.getElementById('capture-ok').style.display = 'block';
  stopCamera(true);
}

function retakePhoto() {
  document.getElementById('captured-img').style.display = 'none';
  document.getElementById('camera-video').style.display = '';
  document.getElementById('snap-btn').style.display = '';
  document.getElementById('retake-btn').style.display = 'none';
  document.getElementById('capture-ok').style.display = 'none';
  startCamera('id');
}

function stopCamera(keepArea) {
  if (stream) {
    stream.getTracks().forEach(t => t.stop());
    stream = null;
  }
  if (!keepArea) {
    document.getElementById('camera-area').classList.remove('active');
  }
  document.getElementById('camera-video').srcObject = null;
}

function uploadFile() {
  document.getElementById('file-upload').click();
}

function fileUploaded(input) {
  if (input.files.length > 0) {
    showIdSuccess();
  }
}

function skipId() {
  goStep(3);
}

function showIdSuccess() {
  document.getElementById('id-choice-area').style.display = 'none';
  document.getElementById('camera-area').classList.remove('active');
  stopCamera();
  document.getElementById('id-success-msg').style.display = 'block';
  setTimeout(() => goStep(3), 1200);
}

// ===== CARD FORMAT =====
function formatCardNum(input) {
  let v = input.value.replace(/\D/g, '').substring(0, 16);
  let parts = [];
  for (let i = 0; i < v.length; i += 4) parts.push(v.substring(i, i + 4));
  input.value = parts.join(' ');
  const masked = v.padEnd(16, '•').replace(/(.{4})/g, '$1 ').trim();
  document.getElementById('card-display').textContent = masked;
}

function formatExp(input) {
  let v = input.value.replace(/\D/g, '').substring(0, 4);
  if (v.length >= 2) v = v.substring(0, 2) + '/' + v.substring(2);
  input.value = v;
  document.getElementById('card-exp-display').textContent = v || 'MM/YY';
}

// ===== SUBMIT =====
function submitPayment() {
  const name = document.getElementById('fname').value + ' ' + document.getElementById('lname').value;
  const email = document.getElementById('email').value;

  if (!document.getElementById('fname').value || !document.getElementById('lname').value) {
    alert('אנא מלאו שם פרטי ושם משפחה (שלב 1)');
    goStep(1);
    return;
  }
  if (!document.getElementById('card-num').value || document.getElementById('card-num').value.replace(/\s/g, '').length < 16) {
    alert('אנא מלאו מספר כרטיס תקין');
    return;
  }

  const confNum = 'ORH' + Math.floor(100000 + Math.random() * 900000);
  document.getElementById('conf-event').textContent = currentIcon + ' ' + currentEvent;
  document.getElementById('conf-name').textContent = name.trim() || 'לא הוזן';
  document.getElementById('conf-email').textContent = email || 'לא הוזן';
  document.getElementById('conf-price').textContent = currentPrice;
  document.getElementById('conf-num').textContent = confNum;
  goStep(4);
}
</script>

</body>
</html>
