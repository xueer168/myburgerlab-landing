<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Build Your Burger Personality | MyBurgerLab</title>
  <style>
    :root {
      --orange: #FF6B35;
      --teal: #2EC4B6;
      --white: #FFFFFF;
      --grey: #F5F5F5;
      --text-dark: #333333;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: 'Open Sans', sans-serif; background: var(--white); color: var(--text-dark); }
    a { text-decoration: none; color: inherit; }
    .container { width: 90%; max-width: 1200px; margin: 0 auto; }

    /* Grid utility */
    .grid { display: grid; gap: 20px; }

    /* Hero */
    .hero { display: grid; grid-template-columns: 1fr 1fr; align-items: center; padding: 100px 0; background: var(--grey); position: relative; }
    .hero::after { content: ''; position: absolute; inset: 0; background-image: url('data:image/svg+xml;...'); opacity: 0.1; }
    .hero-left { padding-right: 40px; }
    .hero-left h1 { font-size: 48px; margin-bottom: 20px; }
    .hero-left p { font-size: 24px; margin-bottom: 30px; }
    .hero-left img { width: 80%; }
    .hero-right { position: relative; text-align: center; }
    .builder-ui { width: 100%; max-width: 500px; margin: 0 auto; }
    .progress { width: 100%; height: 20px; background: var(--grey); border-radius: 10px; overflow: hidden; margin: 30px 0; }
    .progress-bar { width: 60%; height: 100%; background: var(--orange); transition: width 1s ease; }
    .progress-label { font-weight: bold; }
    .cta-btn { display: inline-block; background: var(--orange); color: var(--white); padding: 15px 40px; font-size: 20px; font-weight: bold; border-radius: 5px; }

    /* Persona Cards */
    .cards { background: #f8f2e7; padding: 80px 0; }
    .cards .grid { grid-template-columns: repeat(3, 1fr); }
    .card { background: #fff; border-radius: 10px; overflow: hidden; transform-style: preserve-3d; transition: transform 0.6s; position: relative; height: 350px; }
    .card:hover { transform: rotateY(180deg); }
    .card-face { position: absolute; inset: 0; backface-visibility: hidden; padding: 20px; display: flex; flex-direction: column; justify-content: space-between; }
    .card-back { transform: rotateY(180deg); display: flex; align-items: center; justify-content: center; background: var(--teal); color: var(--white); }
    .card img { width: 100%; border-radius: 10px; }
    .tag { background: var(--teal); color: var(--white); padding: 5px 10px; display: inline-block; font-family: 'Bubblegum Sans', cursive; }

    /* Campus Event */
    .campus { background: var(--teal); color: var(--white); padding: 80px 0; }
    .campus .grid { grid-template-columns: 3fr 2fr; align-items: center; }
    .map { position: relative; width: 100%; height: 300px; background: #cceef2; border-radius: 10px; }
    .calendar { background: var(--white); color: var(--text-dark); padding: 20px; border-radius: 10px; }
    .calendar h3 { margin-bottom: 10px; }
    .banner { background: rgba(0,0,0,0.5); color: #fff; text-align: center; padding: 10px; border-radius: 5px; margin-bottom: 20px; font-weight: bold; }

    /* UGC Gallery */
    .ugc { padding: 80px 0; }
    .ugc h2 { font-size: 36px; text-align: center; margin-bottom: 40px; }
    .masonry { column-count: 4; column-gap: 20px; }
    .ugc-item { break-inside: avoid; margin-bottom: 20px; position: relative; }
    .ugc-item img { width: 100%; border-radius: 10px; }
    .overlay { position: absolute; bottom: 10px; left: 10px; background: rgba(0,0,0,0.6); color: #fff; padding: 5px 10px; border-radius: 5px; font-size: 14px; }
    .live-dot { position: absolute; top: -10px; right: -10px; width: 20px; height: 20px; background: red; border-radius: 50%; animation: pulse 1.5s infinite; }
    @keyframes pulse { 0% { transform: scale(1); opacity: 1; } 100% { transform: scale(1.5); opacity: 0; } }

    /* Footer CTA */
    .footer-cta { display: grid; grid-template-columns: 1fr 1fr; align-items: center; padding: 80px 0; background: linear-gradient(45deg, var(--orange), var(--teal)); color: var(--white); }
    .footer-cta img { width: 300px; }
    .footer-cta .text { font-size: 32px; font-weight: bold; }
    .footer-cta .qr { margin-top: 20px; }
    .footer-bar { background: #eee; padding: 20px 0; text-align: center; font-size: 14px; color: #666; }
  </style>
</head>
<body>
  <!-- Hero -->
  <header class="hero">
    <div class="hero-left container">
      <h1>DISCOVER YOUR FLAVOR DNA</h1>
      <p>Which burger personality are you?</p>
      <img src="https://via.placeholder.com/400x400?text=Student+Holding+Card" alt="Student holding card">
    </div>
    <div class="hero-right container">
      <img class="builder-ui" src="https://via.placeholder.com/500x300?text=Isometric+UI" alt="Burger builder UI">
      <div class="progress">
        <div class="progress-bar"></div>
      </div>
      <div class="progress-label">BUILD YOUR BURGER PERSONALITY</div>
      <a href="#" class="cta-btn">Start Quiz Now</a>
    </div>
  </header>

  <!-- Persona Cards -->
  <section class="cards">
    <div class="container grid">
      <!-- Card 1 -->
      <div class="card">
        <div class="card-face card-front">
          <img src="https://via.placeholder.com/300x200?text=Tech+Foodie" alt="Tech Foodie">
          <div><span class="tag">#MyBurgerSelf</span></div>
          <div>Spicy: ★★★★☆<br>Creative: ★★★★☆<br>Social: ★★★☆☆</div>
        </div>
        <div class="card-face card-back">
          <div>Tech Foodie<br><a href="#">Learn More →</a></div>
        </div>
      </div>
      <!-- (Repeat similar blocks for the other 5 personas) -->
    </div>
  </section>

  <!-- Campus Event -->
  <section class="campus">
    <div class="container grid">
      <div class="map">
        <!-- Insert campus map SVG or image here -->
      </div>
      <div class="calendar">
        <div class="banner">FREE TOPPINGS FOR FIRST 50 STUDENTS!</div>
        <h3>Event Dates</h3>
        <!-- Simple calendar grid here -->
      </div>
    </div>
  </section>

  <!-- UGC Gallery -->
  <section class="ugc">
    <div class="container">
      <h2>#MyBurgerSelf in the Wild <span class="live-dot"></span></h2>
      <div class="masonry">
        <div class="ugc-item">
          <img src="https://via.placeholder.com/250?text=Post+1" alt="UGC Post">
          <div class="overlay">👍 120   💬 30</div>
        </div>
        <!-- (Add more UGC items here) -->
      </div>
    </div>
  </section>

  <!-- Footer CTA -->
  <footer>
    <div class="footer-cta container">
      <div>
        <img src="https://via.placeholder.com/300x600?text=Mobile+Mockup" alt="Mobile mockup">
      </div>
      <div class="text">
        Scan → Discover → Eat!
        <div class="qr">
          <img src="https://via.placeholder.com/150?text=QR+Code" alt="QR Code">
        </div>
      </div>
    </div>
    <div class="footer-bar container">
      <a href="#">About</a> | <a href="#">FAQ</a> | <a href="#">Contact</a>
    </div>
  </footer>
</body>
</html>
