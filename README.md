
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Seaborne Care supports underprivileged communities through essential supplies, kindness and community action.">
  <title>Seaborne Care | Spreading Hope</title>

  <style>
    :root {
      --green: #123d38;
      --mint: #d7f0c1;
      --cream: #f7f5ed;
      --text: #263b35;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: Arial, sans-serif;
      background: var(--cream);
      color: var(--text);
      line-height: 1.6;
    }

    nav {
      background: var(--green);
      color: white;
      padding: 20px 8%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
    }

    .logo {
      font-size: 25px;
      font-weight: bold;
      letter-spacing: 0.5px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
    }

    nav a:hover { color: var(--mint); }

    .hero {
      min-height: 570px;
      padding: 80px 8%;
      background:
        linear-gradient(90deg, rgba(10,43,38,.91),
        rgba(10,43,38,.42)),
        url("https://images.unsplash.com/photo-1469571486292-0ba58a3f068b?auto=format&fit=crop&w=1800&q=85")
        center/cover;
      color: white;
      display: flex;
      align-items: center;
    }

    .hero-content { max-width: 650px; }

    .tag {
      color: var(--mint);
      text-transform: uppercase;
      letter-spacing: 3px;
      font-size: 13px;
      font-weight: bold;
    }

    h1 {
      font-size: clamp(42px, 7vw, 72px);
      line-height: 1.08;
      margin: 20px 0;
    }

    .hero p {
      font-size: 18px;
      margin-bottom: 30px;
      max-width: 540px;
    }

    .btn {
      display: inline-block;
      padding: 14px 24px;
      background: var(--mint);
      color: var(--green);
      text-decoration: none;
      font-weight: bold;
      border-radius: 6px;
      transition: .2s;
    }

    .btn:hover { transform: translateY(-2px); }

    section { padding: 75px 8%; }

    .section-title {
      font-size: clamp(30px, 4vw, 42px);
      color: var(--green);
      margin-bottom: 15px;
    }

    .intro {
      max-width: 720px;
      margin-bottom: 35px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
      margin-top: 35px;
    }

    .card {
      background: white;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 5px 20px #123d3810;
    }

    .card img {
      display: block;
      width: 100%;
      height: 220px;
      object-fit: cover;
    }

    .card-content { padding: 25px; }

    .card h3 {
      color: var(--green);
      margin-bottom: 10px;
      font-size: 22px;
    }

    .mission {
      background: #e6ebdd;
      text-align: center;
    }

    .mission p {
      max-width: 750px;
      margin: 15px auto 25px;
    }

    .contact {
      background: var(--green);
      color: white;
      text-align: center;
    }

    .contact h2 { color: white; }

    .contact p {
      margin: 15px auto 25px;
      max-width: 650px;
    }

    footer {
      background: #0b2d29;
      color: #dce8df;
      text-align: center;
      padding: 24px;
      font-size: 14px;
    }

    @media (max-width: 750px) {
      nav { padding: 18px 5%; }
      nav a { margin: 0 10px 0 0; }
      .hero { padding: 65px 6%; min-height: 500px; }
      section { padding: 55px 6%; }
      .cards { grid-template-columns: 1fr; }
      .card img { height: 240px; }
    }
  </style>
</head>

<body>
  <nav>
    <div class="logo">🌊 Seaborne Care</div>
    <div>
      <a href="#about">About</a>
      <a href="#work">Our Work</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <header class="hero">
    <div class="hero-content">
      <span class="tag">Care • Share • Empower</span>
      <h1>Small Acts.<br>Big Changes.</h1>
      <p>
        We believe everyone deserves dignity, care, and the
        essentials of life. Together, we can make a difference
        in the lives of underprivileged communities.
      </p>
      <a href="#contact" class="btn">Join Our Mission →</a>
    </div>
  </header>

  <section id="about">
    <h2 class="section-title">About Seaborne Care</h2>
    <p class="intro">
      Seaborne Care is a community-focused initiative dedicated
      to helping underprivileged people by distributing essential
      supplies and spreading kindness. Our goal is to turn
      compassion into meaningful action.
    </p>
  </section>

  <section id="work">
    <h2 class="section-title">What We Do</h2>
    <p>Small contributions can create lasting positive change.</p>

    <div class="cards">
      <article class="card">
        <img
          src="https://images.unsplash.com/photo-1593113598332-cd288d649433?auto=format&fit=crop&w=800&q=80"
          alt="Community food donation">
        <div class="card-content">
          <h3>Food & Essentials</h3>
          <p>Helping families access everyday necessities and supplies.</p>
        </div>
      </article>

      <article class="card">
        <img
          src="https://images.unsplash.com/photo-1488521787991-ed7bbaae773c?auto=format&fit=crop&w=800&q=80"
          alt="Community support and volunteering">
        <div class="card-content">
          <h3>Community Support</h3>
          <p>Supporting people through thoughtful acts of service.</p>
        </div>
      </article>

      <article class="card">
        <img
          src="https://images.unsplash.com/photo-1469571486292-0ba58a3f068b?auto=format&fit=crop&w=800&q=80"
          alt="People coming together to help others">
        <div class="card-content">
          <h3>Spread Kindness</h3>
          <p>Inspiring more people to participate in community care.</p>
        </div>
      </article>
    </div>
  </section>

  <section class="mission" id="about-mission">
    <h2 class="section-title">Our Mission</h2>
    <p>
      A kinder world begins with us. We aim to bring people together,
      share essential resources, and help every individual feel
      valued, respected, and supported.
    </p>
    <a href="#contact" class="btn">Be Part of the Change</a>
  </section>

  <section class="contact" id="contact">
    <h2 class="section-title">Let's Make a Difference</h2>
    <p>
      Want to volunteer, collaborate, or learn more about Seaborne Care?
      Reach out and become a part of our journey.
    </p>
    <!-- Replace the example email with your official email. -->
    <a class="btn"
       href="mailto:your-email@example.com?subject=Seaborne%20Care%20Enquiry">
      Contact Us
    </a>
  </section>

  <footer>
    <p>© <span id="year"></span> Seaborne Care. All rights reserved.</p>
    <p>Made with ❤️ to spread care and hope.</p>
  </footer>

  <script>
    document.getElementById("year").textContent =
      new Date().getFullYear();
  </script>
</body>
</html>
