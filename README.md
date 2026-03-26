
<html lang="no">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bryllup</title>
  <style>
    body {font-family: Arial, sans-serif; margin:0; background:#f9f6f2; color:#333; text-align:center;}

    header {
      position: relative;
      background:url('Kjerag.JPG') center/cover no-repeat;
      color:white;
      padding:80px 20px;
      overflow:hidden;
    }

    /* MØRK OVERLAY – juster opacity (0.3–0.7 anbefales) */
    header::before {
      content:"";
      position:absolute;
      top:0; left:0; right:0; bottom:0;
      background:rgba(0,0,0,0.35); /* ← JUSTER HER */
      z-index:0;
    }

    header * {
      position:relative;
      z-index:1;
    }

    header h1 {font-size:36px; margin:0;}

    section {padding:20px 15px; max-width:900px; margin:auto;}

    .box {
      background:white;
      padding:20px;
      margin:15px 0;
      border-radius:15px;
      box-shadow:0 4px 10px rgba(0,0,0,0.05);
      opacity:0;
      transform:translateY(20px);
      transition:all 0.8s ease;
    }

    /* FADE-IN effekt */
    .box.visible {
      opacity:1;
      transform:translateY(0);
    }

    img {max-width:100%; border-radius:10px; margin-top:10px;}
    iframe {width:100%; height:250px; border:0; border-radius:10px; margin-top:10px;}

    /* STØRRE RSVP-SKJEMA */
.rsvp {
  height:900px; /* ← JUSTER HER */
    
    #countdown {font-size:20px; margin-top:10px;}

    .btn {
      display:inline-block;
      margin-top:10px;
      padding:10px 15px;
      background:#d8cfc4;
      color:#333;
      text-decoration:none;
      border-radius:8px;
      font-weight:bold;
    }

    .btn:hover {background:#c5bcb2;}

    footer {padding:20px; font-size:14px; color:#777;}

    @media (min-width: 768px) {
      header h1 {font-size:48px;}
      #countdown {font-size:24px;}
      iframe {height:300px;}
    }

    @media (max-width: 600px) {
      body {
      font-size: 18px; /* ← gjør all tekst større */
    }

      h1 {
      font-size: 32px;
    }

      h2 {
      font-size: 24px;
    }

    p {
      font-size: 18px;
    }

  .btn {
    font-size: 16px;
    padding: 12px 18px;
  }
}
  </style>
</head>
<body>

<header>
  <h1>Åshild & Cedrick</h1>
  <p>Vi gifter oss!</p>
  <p><strong>Dato:</strong> <span id="wedding-date">2026-08-15</span></p>
  <div id="countdown"></div>
</header>

<section>

  <div class="box">
    <h2>Se så fine vi er 💛</h2>
    <img src="Vin.JPG" alt="Bryllupsbilde">
  </div>

  <div class="box">
    <h2>Praktisk informasjon</h2>
    <p><strong>Vielse:</strong> Vestbygda kapell kl. 13:00</p>
    <p><strong>Fest:</strong> Spind grendehus AL kl. 15:00</p>
    <p><strong>Kleskode:</strong> Dress og kjole, men ikke for stivt. (Ta med dansesko)</p>
  </div>

  <div class="box">
    <h2>📍Kart til vielsen</h2>
    <iframe src="https://www.google.com/maps?q=Vestbygda%20kapell&output=embed"></iframe>
    <a class="btn" href="https://www.google.com/maps/dir/?api=1&destination=Vestbygda+kapell" target="_blank">Få veibeskrivelse</a>
  </div>

  <div class="box">
    <h2>📍Kart til festen</h2>
    <iframe src="https://www.google.com/maps?q=Spind%20grendehus%20AL&output=embed"></iframe>
    <a class="btn" href="https://www.google.com/maps/dir/?api=1&destination=Spind+grendehus+AL" target="_blank">Få veibeskrivelse</a>
  </div>

  <div class="box">
    <h2>Program</h2>
    <p>13:00 Vielse i Vestbygda kapell<br>15:00 Fest på Spind grendehus<br>19:00 Festen begynner for de store <br> 05:00 Kvelden</p>
  </div>

  <div class="box">
    <h2>Overnatting</h2>
    <p>Vi anbefaler følgende overnattingssteder:</p>
    <p>
      🏡 <a href="https://www.stayover.no/" target="_blank">Stayover @ Lista</a> <br> 
      👆 Her <br> har vi holdt av 22 soveplasser for billigere overnatting. <br>Dersom dette er ønskelig ta kontakt med oss for å få valgt rom/plassering 💛<br>
      🏨 <a href="https://www.rederiethotell.no/rom" target="_blank">Rederiet Hotell</a><br>
      🌊 <a href="https://farsundfjordhotell.no/" target="_blank">Fjordhotellet</a><br>
      ⛺ <a href="https://lomsesanden.no/" target="_blank">Lomsesanden Camping</a><br>
      
    </p>
  </div>

  <div class="box">
    <h2>RSVP 📝</h2>
    <iframe class="rsvp" src="https://docs.google.com/forms/d/e/1FAIpQLSd2oyFLzM-TEauIwwDhfBARAkKgjZftjDCIMes1-Wi5p2QIhQ/viewform?usp=publish-editor"></iframe>
  </div>

  <div class="box">
    <h2>Kontakt</h2>
    <p>Toastmastere: <br>Thea Seglem Tangen +47xxxxxxx <br>Tore Solberg Engebretsen +47xxxxxx</p>
  </div>

</section>

<footer>
  <p>Vi gleder oss til å feire med dere 💛</p>
</footer>

<script>
  // COUNTDOWN
  const weddingDate = new Date(document.getElementById('wedding-date').innerText).getTime();
  const countdownEl = document.getElementById('countdown');

  setInterval(() => {
    const now = new Date().getTime();
    const diff = weddingDate - now;

    if (diff <= 0) {
      countdownEl.innerHTML = "🎉 Dagen er her!";
      return;
    }

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);

    countdownEl.innerHTML = `⏳ ${days} dager, ${hours} timer, ${minutes} minutter igjen`;
  }, 1000);

  // FADE-IN ON SCROLL
  const boxes = document.querySelectorAll('.box');

  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.2 });

  boxes.forEach(box => {
    observer.observe(box);
  });
</script>

</body>
</html>
