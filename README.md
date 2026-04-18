# new-project-1
e-commerse web site
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Shari Lagbe?</title>
    <style>
        :root {
            --bg: #fff8f2;
            --primary: #b1363a;
            --secondary: #f9d4c2;
            --text: #2e1f16;
            --muted: #6a5348;
            --card: #ffffff;
            --border: rgba(176, 54, 58, 0.12);
            --shadow: 0 18px 40px rgba(0, 0, 0, 0.08);
            font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
        }

        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }

        img {
            max-width: 100%;
            display: block;
        }

        .page {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        header {
            padding: 24px 32px;
            position: sticky;
            top: 0;
            z-index: 10;
            background: rgba(255, 248, 242, 0.96);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(176, 54, 58, 0.08);
        }

        .nav-row {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 16px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .brand {
            font-size: 1.4rem;
            font-weight: 700;
            letter-spacing: 0.02em;
        }

        .brand span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 24px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--muted);
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .menu-toggle {
            display: none;
            border: 1px solid var(--border);
            background: #fff;
            padding: 10px 14px;
            border-radius: 999px;
            cursor: pointer;
        }

        .hero {
            overflow: hidden;
            padding: 64px 32px;
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            align-items: center;
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .hero-copy {
            max-width: 520px;
        }

        .eyebrow {
            display: inline-flex;
            padding: 8px 16px;
            border-radius: 999px;
            background: var(--secondary);
            color: var(--primary);
            font-weight: 700;
            margin-bottom: 20px;
            font-size: 0.85rem;
            letter-spacing: 0.06em;
        }

        h1 {
            font-size: clamp(2.8rem, 5vw, 4.4rem);
            margin: 0 0 24px;
            line-height: 0.95;
        }

        p.lead {
            font-size: 1.05rem;
            color: var(--muted);
            margin: 0 0 30px;
            max-width: 520px;
        }

        .hero-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 16px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 16px 24px;
            border-radius: 999px;
            border: none;
            font-weight: 700;
            cursor: pointer;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            text-decoration: none;
        }

        .btn-primary {
            background: var(--primary);
            color: #fff;
            box-shadow: 0 16px 30px rgba(177, 54, 58, 0.18);
        }

        .btn-secondary {
            background: #fff;
            color: var(--primary);
            border: 1px solid var(--border);
        }

        .btn:hover {
            transform: translateY(-1px);
        }

        .hero-image {
            position: relative;
            display: grid;
            place-items: center;
        }

        .hero-card {
            width: 100%;
            min-height: 440px;
            border-radius: 32px;
            background: linear-gradient(180deg, #ffffff 0%, #f7e7df 100%);
            box-shadow: var(--shadow);
            padding: 24px;
            display: grid;
            gap: 18px;
        }

        .hero-card p {
            margin: 0;
            color: var(--muted);
        }

        .hero-card .card-title {
            font-size: 1.25rem;
            font-weight: 700;
            margin: 0;
        }

        .hero-card .price {
            font-size: 1.35rem;
            color: var(--primary);
            font-weight: 700;
        }

        .hero-card .colors {
            display: flex;
            gap: 12px;
        }

        .swatch {
            width: 18px;
            height: 18px;
            border-radius: 50%;
            border: 1px solid rgba(46, 31, 22, 0.15);
        }

        .swatch:nth-child(1) { background: #d8a3a0; }
        .swatch:nth-child(2) { background: #f7e7df; }
        .swatch:nth-child(3) { background: #b1363a; }

        .section {
            padding: 64px 32px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            margin: 0 0 24px;
            font-size: 2rem;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 24px;
        }

        .product-card {
            background: var(--card);
            border-radius: 28px;
            overflow: hidden;
            box-shadow: var(--shadow);
            border: 1px solid rgba(176, 54, 58, 0.08);
        }

        .product-card img {
            width: 100%;
            height: 320px;
            object-fit: cover;
        }

        .product-card-body {
            padding: 22px;
        }

        .product-card h3 {
            margin: 0 0 12px;
            font-size: 1.15rem;
        }

        .product-card p {
            margin: 0;
            color: var(--muted);
            font-size: 0.95rem;
        }

        .product-meta {
            margin-top: 18px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 700;
            color: var(--primary);
        }

        .categories {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 24px;
            margin-top: 28px;
        }

        .category-card {
            display: flex;
            background: var(--secondary);
            border-radius: 24px;
            padding: 24px;
            gap: 18px;
            align-items: center;
        }

        .category-icon {
            width: 60px;
            height: 60px;
            border-radius: 20px;
            background: #fff;
            display: grid;
            place-items: center;
            font-size: 1.4rem;
            color: var(--primary);
        }

        .category-info h4 {
            margin: 0 0 6px;
            font-size: 1.05rem;
        }

        .category-info p {
            margin: 0;
            color: var(--muted);
            font-size: 0.95rem;
        }

        .newsletter {
            background: #fff;
            border-radius: 28px;
            padding: 42px 32px;
            box-shadow: var(--shadow);
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            gap: 24px;
            align-items: center;
        }

        .newsletter h3 {
            margin: 0 0 12px;
            font-size: 1.8rem;
        }

        .newsletter p {
            margin: 0 0 18px;
            color: var(--muted);
        }

        .newsletter-form {
            display: grid;
            gap: 16px;
        }

        .newsletter-form input {
            padding: 16px 18px;
            border-radius: 14px;
            border: 1px solid rgba(176, 54, 58, 0.18);
            font-size: 1rem;
            width: 100%;
        }

        .newsletter-form button {
            padding: 16px 18px;
            border-radius: 14px;
            border: none;
            background: var(--primary);
            color: #fff;
            font-weight: 700;
            cursor: pointer;
        }

        footer {
            padding: 24px 32px;
            color: var(--muted);
            background: #fff;
            border-top: 1px solid rgba(176, 54, 58, 0.08);
        }

        .footer-row {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 16px;
            flex-wrap: wrap;
        }

        @media (max-width: 980px) {
            .hero {
                grid-template-columns: 1fr;
            }

            .products-grid,
            .categories {
                grid-template-columns: 1fr 1fr;
            }

            .newsletter {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 720px) {
            header {
                padding: 18px 20px;
            }

            .nav-row {
                flex-wrap: wrap;
            }

            .nav-links {
                flex-wrap: wrap;
                justify-content: center;
            }

            .menu-toggle {
                display: inline-flex;
            }

            .hero {
                padding: 48px 20px;
            }

            .section {
                padding: 48px 20px;
            }

            .products-grid,
            .categories {
                grid-template-columns: 1fr;
            }

            .product-card img {
                height: 260px;
            }

            .hero-card {
                min-height: 360px;
            }

            .newsletter {
                padding: 28px 20px;
            }
        }
    </style>
</head>
<body>
    <div class="page">
        <header>
            <div class="nav-row">
                <div class="brand">Shari <span>Lagbe?</span></div>
                <nav class="nav-links">
                    <a href="#collections">Collections</a>
                    <a href="#featured">Featured</a>
                    <a href="#categories">Categories</a>
                    <a href="#newsletter">Newsletter</a>
                </nav>
            </div>
        </header>

        <main>
            <section class="hero">
                <div class="hero-copy">
                    <span class="eyebrow">Handpicked Sarees</span>
                    <h1>Discover elegant sarees for every moment</h1>
                    <p class="lead">Shari Lagbe? brings you premium sarees, ready to charm with rich textures, beautiful prints, and comfortable drape for weddings, parties, and daily wear.</p>
                    <div class="hero-actions">
                        <a href="#featured" class="btn btn-primary">Shop Now</a>
                        <a href="#categories" class="btn btn-secondary">Browse Styles</a>
                    </div>
                </div>
                <div class="hero-image">
                    <div class="hero-card">
                        <p class="card-title">Rose Blossom Silk Saree</p>
                        <p>Soft silk, handwoven print, perfect for festive evenings.</p>
                        <p class="price">৳ 2,980</p>
                        <div class="colors">
                            <span class="swatch"></span>
                            <span class="swatch"></span>
                            <span class="swatch"></span>
                        </div>
                        <img src="https://images.unsplash.com/photo-1541099649105-f69ad21f3246?auto=format&fit=crop&w=800&q=80" alt="Silk saree" />
                    </div>
                </div>
            </section>

            <section id="featured" class="section">
                <h2 class="section-title">Featured Saree Picks</h2>
                <div class="products-grid">
                    <article class="product-card">
                        <img src="https://images.unsplash.com/photo-1524253482453-3fed8d2fe12b?auto=format&fit=crop&w=900&q=80" alt="Floral saree" />
                        <div class="product-card-body">
                            <h3>Floral Chiffon</h3>
                            <p>Lightweight saree with floral elegance and graceful fall.</p>
                            <div class="product-meta">
                                <span>৳ 1,750</span>
                                <span>Buy</span>
                            </div>
                        </div>
                    </article>

                    <article class="product-card">
                        <img src="https://images.unsplash.com/photo-1533612608997-212b06408bb9?auto=format&fit=crop&w=900&q=80" alt="Embroidered saree" />
                        <div class="product-card-body">
                            <h3>Embroidered Organza</h3>
                            <p>Elegant organza saree with delicate hand embroidery.</p>
                            <div class="product-meta">
                                <span>৳ 3,250</span>
                                <span>Buy</span>
                            </div>
                        </div>
                    </article>

                    <article class="product-card">
                        <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?auto=format&fit=crop&w=900&q=80" alt="Designer saree" />
                        <div class="product-card-body">
                            <h3>Designer Banarasi</h3>
                            <p>Classic Banarasi weave with rich motifs and shine.</p>
                            <div class="product-meta">
                                <span>৳ 4,100</span>
                                <span>Buy</span>
                            </div>
                        </div>
                    </article>
                </div>
            </section>

            <section id="categories" class="section">
                <h2 class="section-title">Shop by Category</h2>
                <div class="categories">
                    <div class="category-card">
                        <div class="category-icon">✨</div>
                        <div class="category-info">
                            <h4>Wedding Sarees</h4>
                            <p>Rich fabrics and ornate borders.</p>
                        </div>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">🌸</div>
                        <div class="category-info">
                            <h4>Party Wear</h4>
                            <p>Modern prints and bold colors.</p>
                        </div>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">☀️</div>
                        <div class="category-info">
                            <h4>Daily Comfort</h4>
                            <p>Soft cotton and breathable drape.</p>
                        </div>
                    </div>
                </div>
            </section>

            <section id="newsletter" class="section">
                <div class="newsletter">
                    <div>
                        <h3>Stay in touch</h3>
                        <p>Subscribe for new arrivals, exclusive drops, and special offers delivered to your inbox.</p>
                    </div>
                    <form class="newsletter-form">
                        <input type="email" placeholder="Enter your email" />
                        <button type="submit">Subscribe</button>
                    </form>
                </div>
            </section>
        </main>

        <footer>
            <div class="footer-row">
                <p>© 2026 Shari Lagbe?. Crafted for modern saree lovers.</p>
                <p>Made with elegance and ease.</p>
            </div>
        </footer>
    </div>
</body>
</html>
