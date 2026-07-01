<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Community Connect & Earn</title>
<link href="https://fonts.googleapis.com/css?family=Inter:wght@400;700&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
<style>
  :root {
    --primary-color: #007bff;
    --secondary-color: #6c757d;
    --accent-color: #28a745;
    --background-light: #f4f4f4;
    --text-light: #ffffff;
    --text-dark: #343a40;
  }

  * { box-sizing: border-box; }

  body {
    font-family: 'Inter', sans-serif;
    margin: 0;
    padding: 0;
    color: var(--text-dark);
    background-color: var(--background-light);
    line-height: 1.4;
  }

  .container {
    max-width: 1200px;
    margin: auto;
    padding: 0 20px;
  }

  /* Header */
  header {
    background-color: var(--primary-color);
    color: var(--text-light);
    padding: 20px 0;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-family: 'Montserrat', sans-serif;
    font-size: 28px;
    font-weight: 700;
    text-decoration: none;
    color: var(--text-light);
  }

  nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
  }

  nav ul li {
    margin-left: 25px;
  }

  nav ul li a {
    color: var(--text-light);
    text-decoration: none;
    font-weight: 700;
    transition: color 0.3s ease;
  }

  nav ul li a:hover {
    color: var(--accent-color);
  }

  /* Hero Section */
  .hero {
    background: linear-gradient(rgba(0,123,255,0.8), rgba(0,123,255,0.6)),
      url('https://via.placeholder.com/1500x600/007bff/ffffff?text=Community+Connect+%26+Earn') no-repeat center center/cover;
    color: var(--text-light);
    padding: 100px 0;
    text-align: center;
  }

  .hero h1 {
    font-family: 'Montserrat', sans-serif;
    font-size: 48px;
    margin-bottom: 20px;
    line-height: 1.2;
  }

  .hero p {
    font-size: 20px;
    margin-bottom: 40px;
    max-width: 80%;
    margin-left: auto;
    margin-right: auto;
  }

  .cta-button {
    display: inline-block;
    background-color: var(--accent-color);
    color: var(--text-light);
    padding: 15px 30px;
    font-size: 18px;
    font-weight: 700;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease, transform 0.3s ease;
  }

  .cta-button:hover {
    background-color: #218838;
    transform: translateY(-2px);
  }

  /* Features Section */
  .features {
    padding: 80px 0;
    text-align: center;
  }

  .features h2,
  .how-it-works h2,
  .testimonials h2 {
    font-family: 'Montserrat', sans-serif;
    font-size: 36px;
    margin-bottom: 50px;
  }

  .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    text-align: left;
  }

  .feature-item {
    background-color: var(--text-light);
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.08);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .feature-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.12);
  }

  .feature-item i {
    font-size: 48px;
    color: var(--primary-color);
    margin-bottom: 20px;
    display: inline-block;
  }

  .feature-item h3 {
    font-size: 22px;
    margin-bottom: 10px;
    font-family: 'Montserrat', sans-serif;
  }

  .feature-item p {
    font-size: 16px;
    color: var(--secondary-color);
  }

  /* How It Works Section */
  .how-it-works {
    background-color: var(--primary-color);
    color: var(--text-light);
    padding: 80px 0;
    text-align: center;
  }

  .steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
  }

  .step-item {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .step-item .icon {
    font-size: 50px;
    margin-bottom: 20px;
    opacity: 0.9;
  }

  .step-item h3 {
    font-size: 20px;
    margin-bottom: 10px;
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
  }

  .step-item p {
    font-size: 16px;
    opacity: 0.9;
  }

  /* Testimonials Section */
  .testimonials {
    padding: 80px 0;
    text-align: center;
  }

  .testimonial-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 40px;
  }

  .testimonial-item {
    background-color: var(--text-light);
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.08);
    text-align: left;
  }

  .testimonial-item .quote {
    font-style: italic;
    color: var(--secondary-color);
    margin-bottom: 15px;
    font-size: 16px;
    position: relative;
    padding-left: 30px;
  }

  .testimonial-item .quote::before {
    content: '\201C';
    font-size: 48px;
    position: absolute;
    top: -10px;
    left: 0;
    color: var(--primary-color);
    opacity: 0.5;
  }

  .testimonial-item .author {
    font-weight: 700;
    color: var(--text-dark);
    font-size: 16px;
  }

  .testimonial-item .author span {
    font-weight: 400;
    color: var(--secondary-color);
    display: block;
    font-size: 14px;
  }

  /* Footer */
  footer {
    background-color: var(--text-dark);
    color: var(--text-light);
    padding: 50px 0;
    text-align: center;
    font-size: 14px;
  }

  footer .container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .footer-logo {
    font-family: 'Montserrat', sans-serif;
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 20px;
  }

  .footer-links {
    display: flex;
    margin-bottom: 20px;
  }

  .footer-links a {
    color: var(--text-light);
    text-decoration: none;
    margin: 0 15px;
    transition: color 0.3s ease;
  }

  .footer-links a:hover {
    color: var(--accent-color);
  }

  .social-icons a {
    color: var(--text-light);
    margin: 0 10px;
    font-size: 20px;
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .social-icons a:hover {
    color: var(--accent-color);
  }

  .copyright {
    margin-top: 30px;
    opacity: 0.7;
  }

  /* Responsive */
  @media (max-width: 768px) {
    header .container {
      flex-direction: column;
    }

    nav ul {
      margin-top: 15px;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav ul li {
      margin: 5px 15px;
    }

    .hero h1 {
      font-size: 32px;
    }

    .hero p {
      font-size: 18px;
    }

    .features h2,
    .how-it-works h2,
    .testimonials h2 {
      font-size: 28px;
      margin-bottom: 30px;
    }

    .feature-grid,
    .steps,
    .testimonial-grid {
      grid-template-columns: 1fr;
    }

    .feature-item,
    .testimonial-item {
      padding: 20px;
    }

    .footer-links {
      flex-direction: column;
      gap: 10px;
    }
  }
</style>
</head>
<body>

<!-- Header -->
<header>
  <div class="container">
    <a href="#" class="logo">OPay Connect</a>
    <nav>
      <ul>
        <li><a href="#features">Features</a></li>
        <li><a href="#how-it-works">How It Works</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="#join">Join Now</a></li>
      </ul>
    </nav>
  </div>
</header>

<!-- Hero -->
<section class="hero">
  <div class="container">
    <h1>Community Connect & Earn</h1>
    <p>Grow your network, share opportunities, and earn rewards together with OPay's community program.</p>
    <a href="#join" class="cta-button">Get Started Today</a>
  </div>
</section>

<!-- Features -->
<section class="features" id="features">
  <div class="container">
    <h2>Why Join Our Community</h2>
    <div class="feature-grid">
      <div class="feature-item">
        <i class="fa-solid fa-people-group"></i>
        <h3>Connect</h3>
        <p>Meet like-minded people in your area and build a network that helps everyone grow.</p>
      </div>
      <div class="feature-item">
        <i class="fa-solid fa-coins"></i>
        <h3>Earn</h3>
        <p>Get rewarded for every referral, transaction, and milestone you reach in the community.</p>
      </div>
      <div class="feature-item">
        <i class="fa-solid fa-shield-halved"></i>
        <h3>Secure</h3>
        <p>Your earnings and data are protected with industry-leading security standards.</p>
      </div>
    </div>
  </div>
</section>

<!-- How It Works -->
<section class="how-it-works" id="how-it-works">
  <div class="container">
    <h2>How It Works</h2>
    <div class="steps">
      <div class="step-item">
        <i class="fa-solid fa-user-plus icon"></i>
        <h3>1. Sign Up</h3>
        <p>Create your free account in minutes.</p>
      </div>
      <div class="step-item">
        <i class="fa-solid fa-share-nodes icon"></i>
        <h3>2. Share</h3>
        <p>Invite friends and share opportunities with your network.</p>
      </div>
      <div class="step-item">
        <i class="fa-solid fa-wallet icon"></i>
        <h3>3. Earn</h3>
        <p>Watch your rewards grow with every connection.</p>
      </div>
    </div>
  </div>
</section>

<!-- Testimonials -->
<section class="testimonials" id="testimonials">
  <div class="container">
    <h2>What Our Community Says</h2>
    <div class="testimonial-grid">
      <div class="testimonial-item">
        <p class="quote">This program changed how I think about earning online. Simple and rewarding.</p>
        <p class="author">Amaka O.<span>Lagos, Nigeria</span></p>
      </div>
      <div class="testimonial-item">
        <p class="quote">I love how easy it is to invite friends and track my rewards in real time.</p>
        <p class="author">Tunde A.<span>Abuja, Nigeria</span></p>
      </div>
      <div class="testimonial-item">
        <p class="quote">A great way to build community while earning extra income on the side.</p>
        <p class="author">Chidinma E.<span>Port Harcourt, Nigeria</span></p>
      </div>
    </div>
  </div>
</section>

<!-- Footer -->
<footer id="join">
  <div class="container">
    <div class="footer-logo">OPay Connect</div>
    <div class="footer-links">
      <a href="#features">Features</a>
      <a href="#how-it-works">How It Works</a>
      <a href="#testimonials">Testimonials</a>
      <a href="#">Contact</a>
    </div>
    <div class="social-icons">
      <a href="#"><i class="fa-brands fa-facebook"></i></a>
      <a href="#"><i class="fa-brands fa-twitter"></i></a>
      <a href="#"><i class="fa-brands fa-instagram"></i></a>
    </div>
    <p class="copyright">&copy; 2026 OPay Connect. All rights reserved.</p>
  </div>
</footer>

</body>
</html>
