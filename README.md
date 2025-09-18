<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>xevion1 — Nmap Pro</title>
<style>
  /* Page reset */
  :root{
    --bg:#020405;
    --panel:#061117;
    --glass: rgba(255,255,255,0.03);
    --accent: #39ff14;
  }
  *{box-sizing:border-box}
  html,body{height:100%}
  body{
    margin:0;
    font-family: "Courier New", Courier, monospace;
    background: radial-gradient(ellipse at top left,#061018 0%, #020405 40%, #000 100%);
    color:#cfeee9;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    overflow:auto;
  }

  /* Matrix rain */
  .matrix {
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:0;
    opacity:0.15;
    background-image: repeating-linear-gradient(180deg, rgba(0,255,80,0.02) 0 1px, transparent 1px 12px);
    mix-blend-mode:screen;
  }

  .container{
    position:relative;
    z-index:2;
    max-width:980px;
    margin:36px auto;
    padding:28px;
  }

  /* Main card */
  .card{
    background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    border:1px solid rgba(255,255,255,0.04);
    border-radius:14px;
    padding:26px;
    box-shadow: 0 8px 24px rgba(0,0,0,0.7), inset 0 1px 0 rgba(255,255,255,0.02);
    backdrop-filter: blur(6px);
  }

  /* Title area */
  .title-row{
    display:flex;
    align-items:center;
    gap:18px;
    margin-bottom:12px;
  }
  .logo-dot{
    width:64px;height:64px;border-radius:12px;
    display:flex;align-items:center;justify-content:center;
    background: linear-gradient(135deg,#081b17,#0f2a24);
    border:1px solid rgba(255,255,255,0.03);
    box-shadow: 0 6px 20px rgba(0,0,0,0.7), 0 0 18px rgba(57,255,20,0.04) inset;
    font-weight:700;color:var(--accent);
    font-size:20px;
  }
  h1{
    margin:0;font-size:26px;letter-spacing:1px;color:#d8ffee;
  }
  p.lead{margin:4px 0 18px;color:#9fd8c8; font-size:14px}

  /* Neon "hacker" display */
  .neon {
    display:inline-block;
    font-weight:700;
    letter-spacing:2px;
    font-size:28px;
    text-shadow:
      0 0 6px rgba(57,255,20,0.18),
      0 0 20px rgba(57,255,20,0.08);
    padding:6px 10px;
    border-radius:8px;
  }

  /* Color-cycling letters */
  .rainbow-letter{
    display:inline-block;
    animation: hueShift 3.6s linear infinite;
    filter: drop-shadow(0 6px 12px rgba(0,0,0,0.6));
  }
  /* offset each letter by a different animation delay (js sets inline style) */

  @keyframes hueShift {
    0%{color: #39ff14; transform: translateY(0) scale(1)}
    25%{color: #00f2ff; transform: translateY(-4px) scale(1.02)}
    50%{color: #ff3bff; transform: translateY(0) scale(1)}
    75%{color: #ffb84d; transform: translateY(2px) scale(0.99)}
    100%{color: #39ff14; transform: translateY(0) scale(1)}
  }

  /* Blinking cursor effect for subtitle */
  .subtitle{
    font-size:13px;
    color:#98e7c9;
    margin-top:8px;
  }
  .cursor{
    display:inline-block;
    width:10px;
    background:var(--accent);
    margin-left:8px;
    animation: blink 1s steps(2,end) infinite;
    vertical-align:middle;
    height:14px;
    border-radius:2px;
  }
  @keyframes blink{
    0%,50%{opacity:1}
    51%,100%{opacity:0}
  }

  /* Info boxes */
  .info-grid{
    display:flex;
    gap:14px;
    margin-top:20px;
    flex-wrap:wrap;
  }
  .box{
    background:linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));
    border-radius:12px;padding:14px;
    border:1px solid rgba(255,255,255,0.03);
    min-width:220px;flex:1;
  }
  .box h3{margin:0 0 6px 0;font-size:14px}
  .contact a{
    color:inherit;text-decoration:none;
    display:inline-block;margin-top:8px;padding:8px 12px;border-radius:10px;
    background:linear-gradient(90deg, rgba(57,255,20,0.06), rgba(0,242,255,0.03));
    border:1px solid rgba(57,255,20,0.09);
    font-weight:600;
  }

  /* Footer */
  footer{margin-top:18px;color:#79c4b0;font-size:12px}
  @media (max-width:620px){
    .title-row{flex-direction:row;gap:10px}
    .logo-dot{width:48px;height:48px;font-size:18px}
  }
</style>
</head>
<body>
  <div class="matrix" aria-hidden="true"></div>

  <div class="container">
    <div class="card" role="main" aria-labelledby="mainTitle">
      <div class="title-row">
        <div class="logo-dot">Xv</div>
        <div>
          <h1 id="mainTitle">
            <span class="neon" id="app-name">xevion1 nmap pro</span>
          </h1>
          <div class="subtitle">version 1 <span class="cursor" aria-hidden="true"></span></div>
        </div>
      </div>

      <p class="lead">A lightweight decorative "hacker" landing template — neon glow, blinking letters, and contact links ready.</p>

      <div class="info-grid">
        <div class="box">
          <h3>About</h3>
          <p>Ready to start building? Use this template as a homepage or splash screen for your app. Customize text, style, and links below.</p>
        </div>

        <div class="box contact">
          <h3>Contact</h3>
          <p>WhatsApp: <strong>+263 780 667 006</strong></p>
          <p>Email: <strong>xevion1@gmail.com</strong></p>
          <p>
            <!-- WhatsApp link scheme; clicking on mobile will open WhatsApp -->
            <a href="https://wa.me/263780667006" target="_blank" rel="noopener">Message on WhatsApp</a>
          </p>
        </div>

        <div class="box">
          <h3>Quick Actions</h3>
          <p>Use the buttons below to add to home screen or copy contact info.</p>
          <p style="margin-top:10px;">
            <button onclick="copyEmail()" style="padding:8px 10px;border-radius:8px;border:none;cursor:pointer">Copy Email</button>
            <button onclick="copyPhone()" style="padding:8px 10px;border-radius:8px;border:none;cursor:pointer;margin-left:8px">Copy Phone</button>
          </p>
        </div>
      </div>

      <footer>© xevion1 • decorative hacker template</footer>
    </div>
  </div>

<script>
  // Split the main app name into individual span letters and give each a slightly different animation delay.
  (function makeRainbowText(){
    const el = document.getElementById('app-name');
    const text = el.textContent.trim();
    el.textContent = '';
    for (let i=0;i<text.length;i++){
      const ch = text[i];
      const span = document.createElement('span');
      span.className = 'rainbow-letter';
      span.textContent = (ch === ' ') ? '\u00A0' : ch;
      // Stagger animation by small fractions so colors wave across the text
      const delay = (i * 0.06).toFixed(2) + 's';
      span.style.animationDelay = delay;
      // Slight size variance for jitter
      span.style.display = 'inline-block';
      el.appendChild(span);
    }
  })();

  // Copy helpers
  function copyEmail(){
    navigator.clipboard?.writeText('xevion1@gmail.com').then(()=>{
      alert('Email copied to clipboard');
    }).catch(()=>{ alert('Could not copy — select and copy manually: xevion1@gmail.com')})
  }
  function copyPhone(){
    navigator.clipboard?.writeText('+263780667006').then(()=>{
      alert('Phone number copied to clipboard');
    }).catch(()=>{ alert('Could not copy — select and copy manually: +263780667006')})
  }

  // Optional: small console banner (for "hacker" visitors who open devtools)
  console.log('%c Welcome, operator. ', 'background:#000;color:#39ff14;padding:8px;border-radius:4px;font-weight:bold');
  console.log('%c Contact: +263780667006 | xevion1@gmail.com', 'color:#9fd8c8');
</script>
</body>
</html>
