# elyheronetwork 

# Prepare the second version of the homepage with logo, colors, and services section

html_v2 = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elyhero Network Family</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="topbar">
        <img src="logo.jpg" alt="Elyhero Logo" class="logo">
        <div class="languages">
            <a href="#">EN</a> | <a href="#">RW</a> | <a href="#">FR</a>
        </div>
    </header>
    <section class="hero">
        <h1>WELCOME IN ELYHERO NETWORK FAMILY</h1>
        <p class="motto">Honor in our strength, kindness in our heart.</p>
        <p>Your request is our priority. All is well.</p>
        <button onclick="exploreServices()">Explore Our Services</button>
    </section>
    <section class="services">
        <h2>Our Services</h2>
        <ul>
            <li>💼 RRA Services: TIN, VAT, PAYE</li>
            <li>🛂 Irembo Document Submission</li>
            <li>🚗 RURA: Permits & Transport Docs</li>
            <li>🏢 RDB: Business Registration</li>
            <li>👷 MIFOTRA Account Setup</li>
            <li>📱 Phone Unlock & Bypass</li>
            <li>💻🖨️ Computer & Printer Problem Solving</li>
        </ul>
    </section>
    <footer class="footer">
        <p>&copy; 2025 Dr cie Elyhero Network Family</p>
        <p class="motto">Honor in our strength, kindness in our heart.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
"""

css_v2 = """
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f9fb;
    color: #222;
}

.topbar {
    background: #002244;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
}

.logo {
    height: 40px;
}

.topbar .languages a {
    color: white;
    margin: 0 5px;
    text-decoration: none;
}

.hero {
    padding: 80px 20px;
    text-align: center;
    background-color: #e0f7fa;
}

.hero h1 {
    font-size: 2.5em;
    margin-bottom: 0.5em;
}

.hero .motto {
    font-size: 1.2em;
    color: #00796b;
}

.hero button {
    margin-top: 20px;
    padding: 10px 20px;
    font-size: 1em;
    background-color: #004d40;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.services {
    padding: 40px 20px;
    background-color: #ffffff;
    text-align: center;
}

.services h2 {
    font-size: 2em;
    margin-bottom: 20px;
    color: #004d40;
}

.services ul {
    list-style: none;
    padding: 0;
    font-size: 1.1em;
}

.services li {
    margin-bottom: 10px;
}

.footer {
    background-color: #002244;
    color: white;
    text-align: center;
    padding: 20px;
}
"""

js_v2 = """
function exploreServices() {
    window.scrollTo({
        top: document.querySelector('.services').offsetTop,
        behavior: 'smooth'
    });
}
"""

# Create new directory
sample_v2_dir = "/mnt/data/elyhero_homepage_v2"
os.makedirs(sample_v2_dir, exist_ok=True)

# Save files
with open(os.path.join(sample_v2_dir, "index.html"), "w") as f:
    f.write(html_v2)
with open(os.path.join(sample_v2_dir, "style.css"), "w") as f:
    f.write(css_v2)
with open(os.path.join(sample_v2_dir, "script.js"), "w") as f:
    f.write(js_v2)

# Add placeholder logo image (from previously uploaded logo)
logo_src = "/mnt/data/LOGO 2.jpg"
logo_dest = os.path.join(sample_v2_dir, "logo.jpg")
if os.path.exists(logo_src):
    os.system(f"cp '{logo_src}' '{logo_dest}'")

# Zip it
zip_path_v2 = "/mnt/data/elyhero_homepage_v2.zip"
with ZipFile(zip_path_v2, 'w') as zipf:
    for filename in ["index.html", "style.css", "script.js", "logo.jpg"]:
        file_path = os.path.join(sample_v2_dir, filename)
        if os.path.exists(file_path):
            zipf.write(file_path, arcname=filename)

zip_path_v2
# Prepare a more complete version including:
# - Logo
# - Color scheme
# - Hero section
# - Contact Us section
# - Quick Contact Form
# - Footer

html_v3 = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Elyhero Network Family</title>
    <link rel="stylesheet" href="style.css" />
</head>
<body>
    <header class="topbar">
        <img src="logo.jpg" alt="Elyhero Logo" class="logo"/>
        <div class="languages">
            <a href="#">EN</a> | <a href="#">RW</a> | <a href="#">FR</a>
        </div>
    </header>

    <section class="hero">
        <h1>WELCOME IN ELYHERO NETWORK FAMILY</h1>
        <p class="motto">Honor in our strength, kindness in our heart.</p>
        <p>Your request is our priority. All is well.</p>
        <button onclick="exploreServices()">Explore Our Services</button>
    </section>

    <section class="services">
        <h2>Our Services</h2>
        <ul>
            <li>💼 RRA Services: TIN, VAT, PAYE</li>
            <li>🛂 Irembo Document Submission</li>
            <li>🚗 RURA: Permits & Transport Docs</li>
            <li>🏢 RDB: Business Registration</li>
            <li>👷 MIFOTRA Account Setup</li>
            <li>📱 Phone Unlock & Bypass</li>
            <li>💻🖨️ Computer & Printer Problem Solving</li>
        </ul>
    </section>

    <section class="contact">
        <h2>Contact Us</h2>
        <p>Tel / WhatsApp: +250 795 338 853 / 798 980 718</p>
        <p>Email: iradukelissa@gmail.com</p>
        <p>Location: Kigali, Rwanda</p>
    </section>

    <section class="contact-form">
        <h2>Send Us a Message</h2>
        <form>
            <input type="text" name="name" placeholder="Your Name" required />
            <input type="email" name="email" placeholder="Your Email" required />
            <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
            <button type="submit">Send</button>
        </form>
    </section>

    <footer class="footer">
        <img src="logo.jpg" alt="Elyhero Logo Footer" class="footer-logo"/>
        <p>&copy; 2025 Dr cie Elyhero Network Family</p>
        <p class="motto">Honor in our strength, kindness in our heart.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
"""

css_v3 = """
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f9fb;
    color: #222;
}

.topbar {
    background: #002244;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
}

.logo {
    height: 45px;
}

.languages a {
    color: white;
    margin: 0 6px;
    text-decoration: none;
    font-weight: bold;
}

.hero {
    padding: 60px 20px;
    text-align: center;
    background-color: #e0f7fa;
}

.hero h1 {
    font-size: 2.5em;
    color: #004d40;
    margin-bottom: 10px;
}

.hero .motto {
    font-size: 1.2em;
    color: #00796b;
}

.hero button {
    margin-top: 20px;
    padding: 12px 24px;
    font-size: 1em;
    background-color: #004d40;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
}

.services {
    padding: 40px 20px;
    background-color: #ffffff;
    text-align: center;
}

.services h2 {
    font-size: 2em;
    margin-bottom: 15px;
    color: #004d40;
}

.services ul {
    list-style: none;
    padding: 0;
    font-size: 1.1em;
}

.services li {
    margin-bottom: 10px;
}

.contact {
    background: #f1f1f1;
    padding: 30px 20px;
    text-align: center;
}

.contact h2 {
    color: #002244;
}

.contact-form {
    padding: 30px 20px;
    background-color: #ffffff;
    text-align: center;
}

.contact-form form {
    max-width: 500px;
    margin: auto;
    display: flex;
    flex-direction: column;
}

.contact-form input,
.contact-form textarea {
    margin-bottom: 15px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 1em;
}

.contact-form button {
    padding: 10px 20px;
    font-size: 1em;
    background-color: #004d40;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
}

.footer {
    background-color: #002244;
    color: white;
    text-align: center;
    padding: 20px;
}

.footer-logo {
    height: 40px;
    margin-bottom: 10px;
}
"""

js_v3 = """
function exploreServices() {
    const services = document.querySelector('.services');
    if (services) {
        window.scrollTo({
            top: services.offsetTop,
            behavior: 'smooth'
        });
    }
}
"""

# Create directory and save files
sample_v3_dir = "/mnt/data/elyhero_homepage_v3"
os.makedirs(sample_v3_dir, exist_ok=True)

with open(os.path.join(sample_v3_dir, "index.html"), "w") as f:
    f.write(html_v3)
with open(os.path.join(sample_v3_dir, "style.css"), "w") as f:
    f.write(css_v3)
with open(os.path.join(sample_v3_dir, "script.js"), "w") as f:
    f.write(js_v3)

# Copy logo again
logo_path = "/mnt/data/LOGO 2.jpg"
logo_dest_v3 = os.path.join(sample_v3_dir, "logo.jpg")
if os.path.exists(logo_path):
    os.system(f"cp '{logo_path}' '{logo_dest_v3}'")

# Zip this version
zip_path_v3 = "/mnt/data/elyhero_homepage_v3.zip"
with ZipFile(zip_path_v3, 'w') as zipf:
    for filename in ["index.html", "style.css", "script.js", "logo.jpg"]:
        file_path = os.path.join(sample_v3_dir, filename)
        if os.path.exists(file_path):
            zipf.write(file_path, arcname=filename)

zip_path_v3

visual code
elyhero-website/
│
├── index.html
├── style.css
├── logo.jpg             ← shyiramo ya logo wampaye (uyihindurire izina)
└── rainbow.png          ← shyiramo iriya background image ya rainbow
code
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dr CIE Elyhero Network Family</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="hero">
    <img src="logo.jpg" alt="Elyhero Logo" class="logo"/>
    <h1>WELCOME IN ELYHERO NETWORK FAMILY</h1>
    <p class="motto">Honor in our strength. Kindness in our heart.</p>
  </header>

  <section class="contact">
    <h2>Contact Us</h2>
    <p>Tel/WhatsApp: +(250) 795338853 / 798980718</p>
    <p>Email: iradukelissa@gmail.com</p>
    <p>Location: Kigali, Rwanda</p>
  </section>

  <section class="form-section">
    <h2>Quick Contact Form</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <footer>
    <p>© 2025 Dr CIE Elyhero Network Family. All rights reserved.</p>
  </footer>
</body>
</html>
Style
body {
  font-family: sans-serif;
  margin: 0;
  padding: 0;
  background-image: url('rainbow.png');
  background-size: cover;
  background-repeat: no-repeat;
  color: #fff;
}

header.hero {
  background-color: rgba(0, 0, 0, 0.6);
  text-align: center;
  padding: 2rem;
}

.logo {
  width: 120px;
  margin-bottom: 1rem;
}

.motto {
  font-size: 1.2rem;
  font-style: italic;
}

.contact, .form-section {
  background-color: rgba(0, 128, 0, 0.6);
  padding: 1.5rem;
  margin: 1rem;
  border-radius: 10px;
}

form {
  display: flex;
  flex-direction: column;
}

input, textarea {
  margin: 0.5rem 0;
  padding: 0.5rem;
  border-radius: 5px;
  border: none;
}

button {
  padding: 0.7rem;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

footer {
  text-align: center;
  background-color: rgba(0, 0, 128, 0.6);
  padding: 1rem;
}
Whatsapp chat bubble
<!-- WhatsApp Chat Bubble -->
<a href="https://wa.me/250795338853" class="whatsapp-float" target="_blank" title="Chat with us on WhatsApp">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" class="whatsapp-icon" alt="WhatsApp" />
</a>

<style>
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
</style>
