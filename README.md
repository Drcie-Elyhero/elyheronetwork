html <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dr CIE Elyhero Network Family</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- 🌈 Background -->
  <div class="rainbow-bg"></div>

  <!-- 🖼️ Logo & Hero -->
  <header class="hero">
    <img src="logo.png" alt="Elyhero Logo" class="logo" />
    <h1>WELCOME IN ELYHERO NETWORK FAMILY</h1>
    <p class="motto">Honor in our strength • Kindness in our heart</p>
  </header>

  <!-- ✅ Services -->
  <section class="services">
    <h2>Serivisi Dutanga</h2>
    <ul>
      <li>✔️ Gufasha abantu na RRA: TIN, VAT, PAYE</li>
      <li>✔️ Gukora no kohereza inyandiko kuri Irembo</li>
      <li>✔️ Ibyangombwa bya RURA (Permis, Imodoka, Moto...)</li>
      <li>✔️ Kwiyandikisha no gukora ubucuruzi muri RDB</li>
      <li>✔️ Serivisi zose za Leta zikorwa online</li>
      <li>✔️ Gufungura Mifotra</li>
      <li>✔️ Phone unlocking / bypass</li>
      <li>✔️ Computer and printer services</li>
    </ul>
  </section>

  <!-- 📞 Contact Section -->
  <section class="contact">
    <h2>Contact Us</h2>
    <p>📞 Tel/WhatsApp: +250 795338853 / 798980718</p>
    <p>✉️ Email: iradukelissa@gmail.com</p>
    <p>📍 Kigali, Rwanda</p>
  </section>

  <!-- 📩 Quick Contact Form -->
  <section class="form-section">
    <h2>Quick Contact</h2>
    <form action="#" method="post">
      <input type="text" placeholder="Names" required />
      <input type="email" placeholder="Email" required />
      <textarea placeholder="Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <!-- ✅ Footer -->
  <footer>
    <p>&copy; 2025 Dr CIE Elyhero Network Family. All rights reserved.</p>
    <p>Languages: English | Kinyarwanda | Français | Español | Kiswahili</p>
  </footer>

  <!-- 💬 WhatsApp Chat Bubble -->
  <a href="https://wa.me/250795338853" class="whatsapp-float" target="_blank" title="Chat on WhatsApp">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp" class="whatsapp-icon" />
  </a>

  <!-- 📞 Call Now Button -->
  <a href="tel:+250795338853" class="call-now-float" title="Call us now">📞</a>

</body>
</html>
css body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: white;
  color: #222;
}

.rainbow-bg {
  background: linear-gradient(to right, #00f, #0f0, #fff);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  opacity: 0.1;
}

.logo {
  width: 120px;
  margin-top: 20px;
}

.hero {
  text-align: center;
  background: #0077cc;
  color: white;
  padding: 50px 20px;
}

.motto {
  font-style: italic;
  margin-top: 10px;
}

.services, .contact, .form-section {
  padding: 30px 20px;
  background: #f4f4f4;
  margin: 20px;
  border-radius: 10px;
}

footer {
  background: #003366;
  color: white;
  text-align: center;
  padding: 20px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

form input, form textarea {
  padding: 10px;
  font-size: 16px;
  border-radius: 6px;
  border: 1px solid #ccc;
}

form button {
  background: #0077cc;
  color: white;
  border: none;
  padding: 10px;
  font-size: 16px;
  border-radius: 6px;
  cursor: pointer;
}

/* 💬 WhatsApp */
.whatsapp-float {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 100;
}
.whatsapp-icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
}

/* 📞 Call Now */
.call-now-float {
  position: fixed;
  bottom: 90px;
  right: 20px;
  font-size: 32px;
  text-decoration: none;
  background-color: green;
  color: white;
  padding: 10px 14px;
  border-radius: 50%;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
  z-index: 100;
}
