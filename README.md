<html lang="no">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bryllup</title>

  <style>
    :root {
      --text: clamp(15px, 2.5vw, 19px);
      --h1: clamp(32px, 6vw, 60px);
      --h2: clamp(22px, 4vw, 34px);
      --radius: 15px;
      --bg: #f9f6f2;
      --btn: #d8cfc4;
      --btn-hover: #c5bcb2;
    }

    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: var(--bg);
      color: #333;
      text-align: center;
      font-size: var(--text);
      line-height: 1.5;
    }

    h1 { font-size: var(--h1); margin: 0; }
    h2 { font-size: var(--h2); margin-top: 0; }

    header {
      position: relative;
      background: url('Kjerag2') center 70% /cover no-repeat;
      padding: clamp(50px, 12vw, 120px) 20px;
      color: white;
      overflow: hidden;
    }

    header::before {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.38);
      z-index: 0;
    }

    header * { position: relative; z-index: 1; }
    #countdown { font-size: clamp(18px, 3vw, 30px); margin-top: 10px; font-weight: bold;}

    section {
      padding: 20px 15px;
      max-width: 900px;
      margin: auto;
    }

    .box {
      background: white;
      padding: clamp(15px, 3vw, 25px);
      margin: 20px 0;
      border-radius: var(--radius);
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
      opacity: 0;
      transform: translateY(20px);
      transition: all 0.8s ease;
    }

    .box.visible {
      opacity: 1;
      transform: translateY(0);
    }

    img { max-width: 100%; border-radius: var(--radius); margin-top: 10px; }

    iframe {
      width: 100%;
      border: 0;
      border-radius: var(--radius);
      margin-top: 10px;
      height: clamp(260px, 35vw, 400px);
    }

    .rsvp {
      height: 140vh;
      min-height: 1200px;
    }

    .btn {
      display: inline-block;
      margin-top: 12px;
      padding: 12px 20px;
      background: var(--btn);
      color: #333;
      text-decoration: none;
      border-radius: var(--radius);
      font-weight: bold;
      font-size: clamp(16px, 3vw, 22px);
      transition: background 0.2s ease;
    }

    .btn:hover { background: var(--btn-hover); }

    footer { padding: 20px; font-size: clamp(12px, 2vw, 16px); color: #777; }

    /* =========================================
          MOBIL — FULL BREDDE, KANT TIL KANT
       ========================================= */
    @media (max-width: 700px) {

      section {
        padding: 0;
        max-width: 100%;
      }

      .box {
        margin: 0 0 20px 0;
        border-radius: 0;
        padding: 20px 15px;
      }
    }

  </style>
</head>

<body>

<header>
  <h1>Åshild &amp; Cedrick</h1>
  <p>Vi gifter oss!</p>
  <p><strong>Dato:</strong> <span id="wedding-date">2026-08-15</span></p>
  <div id="countdown"></div>
</header>

<section>

    <div class="box">
    <h2>Program</h2>
    <p>
      <strong>13:00</strong> Vielse i Vestbygda kapell          <br>
      <strong>15:00</strong> Festen begynner på Spind Grendehus <br>
      <strong>19:00</strong> Festen fortsetter for de store     
    </p>
  </div>

  <div class="box">
    <h2>📍 Kart til vielsen</h2>
    <iframe src="https://www.google.com/maps?q=Vestbygda%20kapell&output=embed"></iframe>
    <a class="btn" href="https://www.google.com/maps/dir/?api=1&destination=Vestbygda+kapell" target="_blank">Få veibeskrivelse</a>
  </div>

  <div class="box">
    <h2>📍 Kart til festen</h2>
    <iframe src="https://www.google.com/maps?q=Spind%20grendehus%20AL&output=embed"></iframe>
    <a class="btn" href="https://www.google.com/maps/dir/?api=1&destination=Spind+grendehus+AL" target="_blank">Få veibeskrivelse</a>
  </div>

  <div class="box">
    <h2>Praktisk info</h2>
    <strong>Kleskode:</strong> Dress og kjole – men ikke for stivt. Ta med dansesko!<br>
    <br>Vi ønsker oss ikke gaver, men heller tjenester og hjelp til dagen. <br>
    <strong>Mat:</strong> Vi ønsker å ha tapas på selve dagen og trenger hjelp til å lage tapasretter<br>
    <strong>Opp- og nedrigging:</strong> Vi trenger hjelp til å pynte, dekke på og rydde av.
  </div>

  <div class="box">
    <h2>Overnatting</h2>
    <p>
      🏡 <a href="https://www.stayover.no/" target="_blank">Stayover @ Lista</a>  
      <br> 👆 22 sengeplasser holdt av <br> ta kontakt for romvalg 💛 <br> 
      🏨 <a href="https://www.rederiethotell.no/rom" target="_blank">Rederiet Hotell</a><br>
      🌊 <a href="https://farsundfjordhotell.no/" target="_blank">Fjordhotellet</a><br>
      ⛺ <a href="https://lomsesanden.no/" target="_blank">Lomsesanden Camping</a><br>
    </p>
  </div>

  <div class="box">
    <h2>Kommer dere? 📝</h2>
    <iframe class="rsvp" src="https://docs.google.com/forms/d/e/1FAIpQLSd2oyFLzM-TEauIwwDhfBARAkKgjZftjDCIMes1-Wi5p2QIhQ/viewform?usp=publish-editor"></iframe>
  </div>

  <div class="box">
    <h2>Kontakt</h2>
    <p>
      <strong>Oss:</strong> <br>
      Åshild - 47329070 <br>
      Cedrick - 41558641 <br><br>
      <strong>Toastmastere:</strong><br>
      Thea Seglem Tangen — 46621279<br>
      Tore Solberg Engebretsen — 90242176
    </p>
  </div>

    <div class="box">
    <h2>Se så fine vi er 💛</h2>
    <img src="Vin.JPG" alt="Bryllupsbilde">
  </div>

</section>

<footer>
  <p>Vi gleder oss til å feire med dere 💛</p>
</footer>

<script>
  const weddingDate = new Date(document.getElementById('wedding-date').innerText).getTime();
  const countdownEl = document.getElementById('countdown');

  setInterval(() => {
    const diff = weddingDate - Date.now();

    if (diff <= 0) {
      countdownEl.innerHTML = "🎉 Dagen er her!";
      return;
    }

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);

    countdownEl.textContent = `⏳ ${days} dager, ${hours} timer, ${minutes} minutter igjen`;
  }, 1000);

  const boxes = document.querySelectorAll('.box');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) entry.target.classList.add('visible');
    });
  }, { threshold: 0.2 });

  boxes.forEach(box => observer.observe(box));
</script>

</body>
</html>
