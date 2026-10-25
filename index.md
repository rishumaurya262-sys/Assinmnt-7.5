# Assignment 7.5 — Flexbox Mini-Project

## Objective

Build a complete responsive landing page using HTML, CSS, and Flexbox.

## Required Sections

1. Navigation Bar
2. Hero Section
3. Three Feature Cards
4. Call-to-Action Section
5. Footer

## Requirements

* Use Flexbox in the navbar and hero layout.
* Arrange three feature cards in a responsive row.
* Use `gap`, `justify-content`, `align-items`, and `flex-wrap`.
* Keep colors, typography, and spacing consistent.
* Prevent content from overflowing on smaller screens.

## Files Required

* `Assignment-7.5.md`
* `index.html`
* `style.css`

## HTML Code (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NovaTech - Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="navbar">
        <a href="#" class="logo">NovaTech</a>
        <nav class="nav-links">
            <a href="#home">Home</a>
            <a href="#features">Features</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>
        <a href="#contact" class="nav-button">Get Started</a>
    </header>

    <main>
        <section class="hero" id="home">
            <div class="hero-content">
                <p class="tagline">WELCOME TO NOVATECH</p>
                <h1>Build Your Future with Smart Technology</h1>
                <p>Discover simple, reliable, and modern solutions that help you work smarter and achieve more.</p>
                <a href="#features" class="primary-button">Explore Features</a>
            </div>
            <div class="hero-image">
                <img src="https://placehold.co/600x400/DBEAFE/1E40AF?text=NovaTech" alt="NovaTech technology illustration">
            </div>
        </section>

        <section class="features" id="features">
            <div class="section-heading">
                <h2>Our Features</h2>
                <p>Everything you need to get started.</p>
            </div>
            <div class="feature-container">
                <article class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3>Fast Performance</h3>
                    <p>Enjoy a smooth and efficient experience every day.</p>
                </article>
                <article class="feature-card">
                    <div class="feature-icon">🔒</div>
                    <h3>Secure Platform</h3>
                    <p>Keep your work organized with security in mind.</p>
                </article>
                <article class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3>Responsive Design</h3>
                    <p>Use the page on phones, tablets, and computers.</p>
                </article>
            </div>
        </section>

        <section class="cta" id="about">
            <h2>Ready to Get Started?</h2>
            <p>Take the next step and explore NovaTech.</p>
            <a href="#contact" class="cta-button">Start Today</a>
        </section>
    </main>

    <footer class="footer" id="contact">
        <p>&copy; 2026 NovaTech. All rights reserved.</p>
        <p>Designed with HTML and CSS Flexbox.</p>
    </footer>
</body>
</html>
```

## CSS Code (`style.css`)

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    color: #1f2937;
    background-color: #ffffff;
    line-height: 1.6;
}

a {
    text-decoration: none;
}

img {
    display: block;
    max-width: 100%;
}

/* Navigation Bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
    padding: 20px 7%;
    background-color: #ffffff;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
}

.logo {
    color: #2563eb;
    font-size: 26px;
    font-weight: bold;
}

.nav-links {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 24px;
    flex-wrap: wrap;
}

.nav-links a {
    color: #374151;
    font-size: 15px;
}

.nav-links a:hover {
    color: #2563eb;
}

.nav-button,
.primary-button,
.cta-button {
    display: inline-block;
    border-radius: 8px;
    padding: 11px 20px;
    font-weight: bold;
    text-align: center;
}

.nav-button,
.primary-button {
    color: #ffffff;
    background-color: #2563eb;
}

.nav-button:hover,
.primary-button:hover {
    background-color: #1d4ed8;
}

/* Hero Section */
.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 40px;
    padding: 70px 7%;
    background-color: #eff6ff;
}

.hero-content {
    flex: 1 1 300px;
    min-width: 0;
}

.tagline {
    color: #2563eb;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 12px;
}

.hero h1 {
    font-size: clamp(32px, 4vw, 48px);
    line-height: 1.2;
    margin-bottom: 20px;
    overflow-wrap: anywhere;
}

.hero-content > p:not(.tagline) {
    color: #4b5563;
    margin-bottom: 25px;
}

.hero-image {
    flex: 1 1 300px;
    min-width: 0;
}

.hero-image img {
    width: 100%;
    height: auto;
    border-radius: 16px;
}

/* Feature Cards */
.features {
    padding: 70px 7%;
}

.section-heading {
    text-align: center;
    margin-bottom: 35px;
}

.section-heading h2,
.cta h2 {
    font-size: 32px;
    margin-bottom: 10px;
}

.section-heading p {
    color: #6b7280;
}

.feature-container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    gap: 24px;
    flex-wrap: wrap;
}

.feature-card {
    flex: 1 1 240px;
    min-width: 0;
    padding: 28px 22px;
    text-align: center;
    background-color: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 14px;
    box-shadow: 0 5px 18px rgba(0, 0, 0, 0.05);
}

.feature-icon {
    font-size: 36px;
    margin-bottom: 12px;
}

.feature-card h3 {
    margin-bottom: 10px;
    color: #1d4ed8;
}

.feature-card p {
    color: #6b7280;
}

/* Call-to-Action */
.cta {
    padding: 55px 7%;
    text-align: center;
    background-color: #1e40af;
    color: #ffffff;
}

.cta p {
    margin-bottom: 24px;
}

.cta-button {
    background-color: #ffffff;
    color: #1e40af;
}

.cta-button:hover {
    background-color: #dbeafe;
}

/* Footer */
.footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    flex-wrap: wrap;
    padding: 24px 7%;
    color: #d1d5db;
    background-color: #111827;
    font-size: 14px;
}

/* Responsive Design */
@media (max-width: 768px) {
    .navbar {
        justify-content: center;
        text-align: center;
    }

    .nav-links {
        width: 100%;
        gap: 14px;
    }

    .hero {
        flex-direction: column;
        text-align: center;
        padding: 50px 6%;
    }

    .hero-content,
    .hero-image {
        width: 100%;
        flex-basis: auto;
    }

    .features {
        padding: 50px 6%;
    }

    .feature-card {
        flex-basis: 100%;
    }

    .footer {
        justify-content: center;
        text-align: center;
    }
}

@media (max-width: 400px) {
    .navbar {
        padding: 18px 5%;
    }

    .nav-links {
        gap: 10px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .hero h1 {
        font-size: 30px;
    }

    .section-heading h2,
    .cta h2 {
        font-size: 27px;
    }

    .cta {
        padding: 45px 5%;
    }
}
```

## Testing

1. Open `index.html` in a browser.
2. Check the page at desktop width.
3. Reduce the browser width to check the responsive layout.
4. Confirm that the navbar, hero, feature cards, CTA, and footer display correctly.
5. Check that horizontal overflow does not occur on smaller screens.

## Result

A complete responsive landing page was created using HTML, CSS, and Flexbox.

## GitHub Repository

Paste your GitHub repository link here after uploading the files.