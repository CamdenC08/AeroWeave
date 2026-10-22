<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>APEX Carbon | Precision Automotive Carbon Fiber</title>
  <style>
    :root {
      --bg: #0a0a0c;
      --card-bg: #141418;
      --card-border: #24242e;
      --accent: #e50914;
      --accent-hover: #ff2a35;
      --text-main: #f5f5f7;
      --text-muted: #8e8e99;
      --container: 1140px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      background-color: var(--bg);
      color: var(--text-main);
      line-height: 1.6;
      background-image:
        radial-gradient(#181822 15%, transparent 16%),
        radial-gradient(#181822 15%, transparent 16%);
      background-size: 16px 16px;
      background-position: 0 0, 8px 8px;
    }

    .container {
      width: 90%;
      max-width: var(--container);
      margin: 0 auto;
    }

    /* Navigation */
    header {
      border-bottom: 1px solid var(--card-border);
      background: rgba(10, 10, 12, 0.9);
      backdrop-filter: blur(8px);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .nav-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.2rem 0;
    }

    .logo {
      font-size: 1.4rem;
      font-weight: 900;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }

    .logo span {
      color: var(--accent);
    }

    .cart-btn {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      color: var(--text-main);
      padding: 0.6rem 1.2rem;
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .cart-btn span {
      background: var(--accent);
      font-size: 0.75rem;
      padding: 2px 7px;
      border-radius: 10px;
    }

    /* Hero Section */
    .hero {
      padding: 5rem 0 3.5rem;
      text-align: center;
    }

    .tagline {
      display: inline-block;
      text-transform: uppercase;
      font-size: 0.8rem;
      letter-spacing: 2px;
      color: var(--accent);
      background: rgba(229, 9, 20, 0.1);
      border: 1px solid rgba(229, 9, 20, 0.3);
      padding: 0.3rem 0.9rem;
      border-radius: 20px;
      margin-bottom: 1.2rem;
      font-weight: 700;
    }

    .hero h1 {
      font-size: 3rem;
      font-weight: 800;
      line-height: 1.15;
      margin-bottom: 1rem;
      letter-spacing: -0.5px;
    }

    .hero p {
      color: var(--text-muted);
      font-size: 1.15rem;
      max-width: 600px;
      margin: 0 auto 2.5rem;
    }

    /* Specs & Trust */
    .specs-strip {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
      margin-bottom: 4rem;
    }

    .spec-card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      padding: 1.5rem;
      border-radius: 8px;
      text-align: center;
    }

    .spec-card h3 {
      font-size: 1.05rem;
      margin-bottom: 0.3rem;
    }

    .spec-card p {
      font-size: 0.85rem;
      color: var(--text-muted);
    }

    /* Filter Controls */
    .catalog-controls {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 2rem;
      gap: 1rem;
    }

    .filter-buttons {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
    }

    .filter-btn {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      color: var(--text-muted);
      padding: 0.5rem 1rem;
      border-radius: 6px;
      cursor: pointer;
      font-size: 0.9rem;
      transition: all 0.2s ease;
    }

    .filter-btn:hover, .filter-btn.active {
      background: var(--accent);
      color: #fff;
      border-color: var(--accent);
    }

    /* Product Grid */
    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1.5rem;
      margin-bottom: 5rem;
    }

    .product-gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
      margin: 0 0 5rem;
    }

    .gallery-item {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: 12px;
      overflow: hidden;
      transition: transform 0.2s ease, border-color 0.2s ease;
    }

    .gallery-item:hover {
      transform: translateY(-4px);
      border-color: #3b3b4f;
    }

    .gallery-item img {
      width: 100%;
      height: 260px;
      object-fit: cover;
      display: block;
      background: #1a1b20;
    }

    .gallery-item h4 {
      padding: 1rem 1rem 1.1rem;
      font-size: 1rem;
      font-weight: 700;
      color: var(--text-main);
    }

    .product-card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: 10px;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: transform 0.2s, border-color 0.2s;
      cursor: pointer;
    }

    .product-card:hover {
      transform: translateY(-4px);
      border-color: #3b3b4f;
    }

    .product-img {
      height: 180px;
      background: #1b1b22;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #555;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      border-bottom: 1px solid var(--card-border);
      position: relative;
      overflow: hidden;
    }

    .product-image-wrap {
      position: relative;
      height: 180px;
      overflow: hidden;
      border-bottom: 1px solid var(--card-border);
      background: #17171d;
    }

    .product-image {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: transform 0.3s ease;
    }

    .product-card:hover .product-image {
      transform: scale(1.04);
    }

    .product-badge {
      position: absolute;
      top: 10px;
      left: 10px;
      background: rgba(0, 0, 0, 0.8);
      font-size: 0.7rem;
      padding: 3px 8px;
      border-radius: 4px;
      border: 1px solid #333;
      color: #f5f5f7;
      z-index: 1;
    }

    .product-body {
      padding: 1.2rem;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
    }

    .product-title {
      font-size: 1.1rem;
      font-weight: 700;
      margin-bottom: 0.3rem;
    }

    .product-meta {
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-bottom: 1rem;
    }

    .product-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: auto;
      padding-top: 1rem;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
    }

    .product-price {
      font-size: 1.15rem;
      font-weight: 800;
      color: #fff;
    }

    .add-btn {
      background: var(--accent);
      color: #fff;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      transition: background 0.2s;
    }

    .add-btn:hover {
      background: var(--accent-hover);
    }

    .cart-panel {
      position: fixed;
      right: 0;
      top: 0;
      width: min(420px, 92vw);
      height: 100vh;
      background: #101014;
      border-left: 1px solid var(--card-border);
      box-shadow: -20px 0 40px rgba(0,0,0,0.35);
      transform: translateX(110%);
      transition: transform 0.25s ease;
      z-index: 200;
      display: flex;
      flex-direction: column;
    }

    .cart-panel.open {
      transform: translateX(0);
    }

    .cart-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.2rem 1.2rem 1rem;
      border-bottom: 1px solid var(--card-border);
    }

    .cart-header h3 {
      font-size: 1.3rem;
    }

    .close-cart {
      background: transparent;
      border: 1px solid var(--card-border);
      color: var(--text-main);
      width: 36px;
      height: 36px;
      border-radius: 50%;
      cursor: pointer;
    }

    .cart-items {
      flex: 1;
      overflow: auto;
      padding: 1rem 1rem 0;
    }

    .cart-item {
      display: grid;
      grid-template-columns: 80px 1fr auto;
      gap: 0.85rem;
      padding: 0.75rem 0;
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }

    .cart-item img {
      width: 80px;
      height: 80px;
      object-fit: cover;
      border-radius: 8px;
      border: 1px solid var(--card-border);
    }

    .cart-item-name {
      font-weight: 700;
      margin-bottom: 0.15rem;
    }

    .cart-item-meta {
      color: var(--text-muted);
      font-size: 0.75rem;
    }

    .cart-item-price {
      font-weight: 700;
      white-space: nowrap;
    }

    .empty-cart {
      text-align: center;
      color: var(--text-muted);
      padding: 2rem 1rem;
      font-size: 0.95rem;
    }

    .cart-footer {
      border-top: 1px solid var(--card-border);
      padding: 1rem 1.2rem 1.4rem;
      background: rgba(17, 17, 21, 0.9);
    }

    .cart-total-row {
      display: flex;
      justify-content: space-between;
      margin-bottom: 1rem;
      font-weight: 700;
    }

    .checkout-btn {
      width: 100%;
      background: var(--accent);
      color: #fff;
      border: none;
      border-radius: 8px;
      padding: 0.9rem 1rem;
      font-size: 0.95rem;
      font-weight: 700;
      cursor: pointer;
    }

    .checkout-btn:hover {
      background: var(--accent-hover);
    }

    .cart-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.5);
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.2s ease;
      z-index: 150;
    }

    .cart-overlay.open {
      opacity: 1;
      visibility: visible;
    }

    .product-modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.72);
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 2rem;
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.2s ease;
      z-index: 250;
    }

    .product-modal-overlay.open {
      opacity: 1;
      visibility: visible;
    }

    .product-modal {
      width: min(980px, 92vw);
      background: #111215;
      border: 1px solid var(--card-border);
      border-radius: 18px;
      overflow: hidden;
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      box-shadow: 0 30px 80px rgba(0,0,0,0.45);
    }

    .product-modal-image-wrap {
      position: relative;
      min-height: 420px;
      background: #1a1b20;
    }

    .product-modal-image {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .product-modal-content {
      padding: 1.8rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .product-modal-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 1rem;
    }

    .product-modal-content h3 {
      font-size: 2rem;
      line-height: 1.1;
      margin: 0;
    }

    .product-modal-price {
      font-size: 1.8rem;
      font-weight: 800;
      color: #fff;
    }

    .product-modal-description {
      color: var(--text-muted);
      font-size: 0.98rem;
    }

    .product-modal-specs {
      list-style: none;
      display: grid;
      gap: 0.5rem;
      margin-top: 0.25rem;
    }

    .product-modal-specs li {
      display: flex;
      align-items: center;
      gap: 0.55rem;
      color: var(--text-main);
      font-size: 0.9rem;
    }

    .product-modal-specs li::before {
      content: "●";
      color: var(--accent);
      font-size: 0.8rem;
    }

    .product-modal-actions {
      margin-top: auto;
      display: flex;
      gap: 0.75rem;
      flex-wrap: wrap;
    }

    .product-modal-actions button {
      flex: 1;
      min-width: 160px;
    }

    .close-modal {
      background: transparent;
      border: 1px solid var(--card-border);
      color: var(--text-main);
      width: 38px;
      height: 38px;
      border-radius: 50%;
      cursor: pointer;
      font-size: 1.25rem;
    }

    @media (max-width: 760px) {
      .product-modal {
        grid-template-columns: 1fr;
      }

      .product-modal-image-wrap {
        min-height: 260px;
      }
    }

    /* Footer */
    footer {
      border-top: 1px solid var(--card-border);
      padding: 3rem 0;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.85rem;
    }
  </style>
</head>
<body>

  <div class="cart-overlay" id="cart-overlay" onclick="toggleCart(false)"></div>

  <div class="product-modal-overlay" id="product-modal-overlay" onclick="closeProductModal()">
    <div class="product-modal" onclick="event.stopPropagation()">
      <div class="product-modal-image-wrap">
        <img class="product-modal-image" id="product-modal-image" alt="Product image" />
      </div>
      <div class="product-modal-content">
        <div class="product-modal-header">
          <div id="product-modal-title"></div>
          <button class="close-modal" type="button" aria-label="Close product" onclick="closeProductModal()">×</button>
        </div>
        <div class="product-modal-price" id="product-modal-price"></div>
        <p class="product-modal-description" id="product-modal-description"></p>
        <ul class="product-modal-specs" id="product-modal-specs"></ul>
        <div class="product-modal-actions">
          <button class="add-btn" type="button" id="product-modal-add">Add to Cart</button>
        </div>
      </div>
    </div>
  </div>

  <aside class="cart-panel" id="cart-panel" aria-live="polite">
    <div class="cart-header">
      <h3>Your Cart</h3>
      <button class="close-cart" type="button" aria-label="Close cart" onclick="toggleCart(false)">×</button>
    </div>
    <div class="cart-items" id="cart-items"></div>
    <div class="cart-footer">
      <div class="cart-total-row">
        <span>Subtotal</span>
        <span id="cart-total">$0</span>
      </div>
      <button class="checkout-btn" type="button">Checkout</button>
    </div>
  </aside>

  <header>
    <div class="container nav-inner">
      <div class="logo">Apex <span>Carbon</span></div>
      <button class="cart-btn" type="button" onclick="toggleCart(true)">
        Cart <span id="cart-count">0</span>
      </button>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div class="tagline">Aerospace-Grade Pre-Preg Carbon</div>
      <h1>Shed Weight. Command Downforce.</h1>
      <p>Precision-molded 2x2 weave components engineered for exact OEM fitment and maximum aerodynamic efficiency.</p>
    </section>

    <!-- Specs Strip -->
    <section class="specs-strip">
      <div class="spec-card">
        <h3>2x2 Twill Weave</h3>
        <p>Pre-impregnated dry carbon fiber for maximum tensile strength.</p>
      </div>
      <div class="spec-card">
        <h3>UV High-Gloss Clear</h3>
        <p>Resistant to yellowing, heat hazing, and stone chipping.</p>
      </div>
      <div class="spec-card">
        <h3>OEM Cad Fitment</h3>
        <p>3D-scanned direct bolt-on replacement for factory mounting points.</p>
      </div>
    </section>

    <!-- Filter Buttons -->
    <div class="catalog-controls">
      <h2 style="font-size: 1.5rem; font-weight: 800;">Catalog</h2>
      <div class="filter-buttons">
        <button class="filter-btn active" onclick="filterParts('all', this)">All Parts</button>
        <button class="filter-btn" onclick="filterParts('aero', this)">Aero & Spoilers</button>
        <button class="filter-btn" onclick="filterParts('body', this)">Hoods & Fenders</button>
        <button class="filter-btn" onclick="filterParts('interior', this)">Interior Trim</button>
      </div>
    </div>

    <!-- Gallery / Product Section -->
    <section class="product-gallery">
      <div class="gallery-item">
        <img src="images/wheel-top.png" alt="Carbon Fiber Steering Wheel - High-Gloss 2x2 Weave" />
        <h4>2x2 Carbon Weave</h4>
      </div>

      <div class="gallery-item">
        <img src="images/wheel-full.png" alt="Carbon Fiber Steering Wheel - Full View" />
        <h4>Full Wheel Assembly</h4>
      </div>

      <div class="gallery-item">
        <img src="images/wheel-grip.png" alt="Carbon Fiber Steering Wheel - Perforated Leather Grip" />
        <h4>Perforated Grip</h4>
      </div>
    </section>

    <!-- Products Grid -->
    <div class="products-grid" id="product-grid"></div>
  </main>

  <footer>
    <div class="container">
      <p>&copy; 2026 APEX Carbon Dynamics. Built for track days and street performance.</p>
    </div>
  </footer>

  <script>
    const products = [
      {
        id: 1,
        name: "GT Track Rear Wing",
        category: "aero",
        price: 899,
        priceLabel: "$899",
        weave: "2x2 Dry Carbon",
        badge: "Universal",
        image: "https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=900&q=80",
        description: "High-downforce rear wing with a precision-molded carbon shell and adjustable end plates for track-focused stability.",
        specs: ["2x2 twill pre-preg carbon", "Adjustable angle setting", "Direct fit hardware included"]
      },
      {
        id: 2,
        name: "Vented Lightweight Hood",
        category: "body",
        price: 250,
        priceLabel: "$250",
        weave: "Pre-Preg Autoclave",
        badge: "Direct Fit",
        image: "https://images.unsplash.com/photo-1553440569-bcc63803a83d?auto=format&fit=crop&w=900&q=80",
        description: "A lightweight hood with functional vents and OEM-style fitment for improved airflow and reduced mass.",
        specs: ["Autoclave cured carbon shell", "OEM bolt locations", "Vent channels for heat extraction"]
      },
      {
        id: 3,
        name: "Carbon Fiber M Sports Car Steering Wheel for BMW F07 F30 F10 F12 F15 F16 F34 F35 F36 F20 F22 F25 F26 F32 F80 M3 M5 E70 E71 E90",
        category: "interior",
        price: 150,
        priceLabel: "$150",
        weave: "Carbon Fiber M Sport",
        badge: "Interior",
        image: "images/wheel-full.png",
        description: "High-end carbon fiber M Sport steering wheel designed for BMW F-series and M-series models with a premium OEM-inspired feel and aggressive motorsport styling.",
        specs: ["Carbon fiber M Sport trim", "BMW fitment specific design", "Premium steering wheel upgrade"]
      },
      {
        id: 4,
        name: "Front Lip Splitter V2",
        category: "aero",
        price: 640,
        priceLabel: "$640",
        weave: "2x2 Gloss",
        badge: "High Downforce",
        image: "https://images.unsplash.com/photo-1544636331-e26879cd4d9b?auto=format&fit=crop&w=900&q=80",
        description: "Front lip splitter engineered to reduce lift and sharpen front-end grip on road and track setups.",
        specs: ["Aero profile geometry", "Gloss clearcoat finish", "Low-drag mounting system"]
      },
      {
        id: 5,
        name: "Side Mirror Caps (Pair)",
        category: "body",
        price: 310,
        priceLabel: "$310",
        weave: "Full Replacement",
        badge: "Direct Clip",
        image: "https://images.unsplash.com/photo-1511919884226-fd3cad34687c?auto=format&fit=crop&w=900&q=80",
        description: "Clean, aggressive mirror caps that replace the factory units with a lightweight carbon finish.",
        specs: ["Pair set included", "OEM-compatible mount", "High-gloss clear finish"]
      },
      {
        id: 6,
        name: "Paddle Shifter Extensions",
        category: "interior",
        price: 180,
        priceLabel: "$180",
        weave: "Red Tinted Carbon",
        badge: "Interior",
        image: "https://images.unsplash.com/photo-1525609004556-c46c7d6cf023?auto=format&fit=crop&w=900&q=80",
        description: "Carbon paddle shifter extensions that improve grip, style, and tactile feedback behind the wheel.",
        specs: ["Red-tinted weave", "Slip-resistant texture", "Easy install trim pieces"]
      },
      {
        id: 7,
        name: "Carbon Diffuser Kit",
        category: "aero",
        price: 760,
        priceLabel: "$760",
        weave: "Dry Carbon Sides",
        badge: "Track Ready",
        image: "https://images.unsplash.com/photo-1553440569-bcc63803a83d?auto=format&fit=crop&w=900&q=80",
        description: "A performance diffuser kit that reduces rear-end turbulence and sharpens overall vehicle stability.",
        specs: ["Separate diffuser channels", "UV-protected coating", "Track-use design"]
      },
      {
        id: 8,
        name: "Carbon Hood Vent Panel",
        category: "body",
        price: 250,
        priceLabel: "$250",
        weave: "2x2 Matte",
        badge: "Street Aero",
        image: "https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?auto=format&fit=crop&w=900&q=80",
        description: "Carbon hood vent panel with a realistic high-end OEM fit and a clean, aggressive street performance profile.",
        specs: ["Matte carbon finish", "Lightweight trim shell", "Factory-style fit"]
      },
      {
        id: 9,
        name: "Center Console Trim",
        category: "interior",
        price: 260,
        priceLabel: "$260",
        weave: "Gloss Carbon",
        badge: "Luxury",
        image: "https://images.unsplash.com/photo-1489824904134-891ab64532f1?auto=format&fit=crop&w=900&q=80",
        description: "A high-contrast console enhancement that delivers a premium cabin upgrade with minimal installation effort.",
        specs: ["Gloss clearcoat finish", "Interior fitment", "Premium hand-finished look"]
      },
      {
        id: 10,
        name: "Carbon Drift Spoiler",
        category: "aero",
        price: 1180,
        priceLabel: "$1,180",
        weave: "3K Twill",
        badge: "Pro-Level",
        image: "https://images.unsplash.com/photo-1494905998402-395d579af36f?auto=format&fit=crop&w=900&q=80",
        description: "A larger rear spoiler built for elevated downforce and a clear visual statement with aggressive styling.",
        specs: ["3K carbon weave", "Reinforced mount layout", "Track-grade balance"]
      }
    ];

    let cart = [];

    function formatCurrency(value) {
      return new Intl.NumberFormat('en-US', {
        style: 'currency',
        currency: 'USD',
        maximumFractionDigits: 0
      }).format(value);
    }

    function renderProducts(items) {
      const grid = document.getElementById("product-grid");
      grid.innerHTML = items.map((p) => `
        <div class="product-card" data-product-id="${p.id}" tabindex="0" role="button" aria-label="View ${p.name}">
          <div class="product-image-wrap">
            <span class="product-badge">${p.badge}</span>
            <img class="product-image" src="${p.image}" alt="${p.name}" />
          </div>
          <div class="product-body">
            <h3 class="product-title">${p.name}</h3>
            <p class="product-meta">${p.weave}</p>
            <div class="product-footer">
              <span class="product-price">${p.priceLabel}</span>
              <button class="add-btn" type="button" data-product-id="${p.id}">Add to Cart</button>
            </div>
          </div>
        </div>
      `).join("");

      document.querySelectorAll(".product-card").forEach((card) => {
        card.addEventListener("click", (event) => {
          if (event.target.closest(".add-btn")) return;
          openProductModal(Number(card.dataset.productId));
        });

        card.addEventListener("keydown", (event) => {
          if (event.key === "Enter" || event.key === " ") {
            event.preventDefault();
            openProductModal(Number(card.dataset.productId));
          }
        });
      });

      document.querySelectorAll(".add-btn").forEach((button) => {
        button.addEventListener("click", (event) => {
          event.stopPropagation();
          addToCart(Number(button.dataset.productId));
        });
      });
    }

    function filterParts(cat, btn) {
      document.querySelectorAll(".filter-btn").forEach((b) => b.classList.remove("active"));
      btn.classList.add("active");

      if (cat === "all") {
        renderProducts(products);
      } else {
        renderProducts(products.filter((p) => p.category === cat));
      }
    }

    function openProductModal(productId) {
      const product = products.find((item) => item.id === productId);
      if (!product) return;

      document.getElementById("product-modal-image").src = product.image;
      document.getElementById("product-modal-image").alt = product.name;
      document.getElementById("product-modal-title").innerHTML = `<h3>${product.name}</h3>`;
      document.getElementById("product-modal-price").textContent = product.priceLabel;
      document.getElementById("product-modal-description").textContent = product.description;
      document.getElementById("product-modal-specs").innerHTML = product.specs.map((spec) => `<li>${spec}</li>`).join("");

      const modalAddBtn = document.getElementById("product-modal-add");
      modalAddBtn.dataset.productId = product.id;
      modalAddBtn.onclick = () => addToCart(product.id);

      document.getElementById("product-modal-overlay").classList.add("open");
    }

    function closeProductModal() {
      document.getElementById("product-modal-overlay").classList.remove("open");
    }

    function toggleCart(forceOpen) {
      const panel = document.getElementById("cart-panel");
      const overlay = document.getElementById("cart-overlay");
      const shouldOpen = typeof forceOpen === "boolean" ? forceOpen : !panel.classList.contains("open");

      panel.classList.toggle("open", shouldOpen);
      overlay.classList.toggle("open", shouldOpen);
    }

    function updateCart() {
      const count = cart.length;
      const total = cart.reduce((sum, item) => sum + item.price, 0);
      document.getElementById("cart-count").innerText = count;
      document.getElementById("cart-total").innerText = formatCurrency(total);

      const itemsEl = document.getElementById("cart-items");

      if (!count) {
        itemsEl.innerHTML = '<div class="empty-cart">Your cart is empty. Add a few performance parts to get started.</div>';
        return;
      }

      itemsEl.innerHTML = cart.map(item => `
        <div class="cart-item">
          <img src="${item.image}" alt="${item.name}" />
          <div>
            <div class="cart-item-name">${item.name}</div>
            <div class="cart-item-meta">${item.weave}</div>
          </div>
          <div class="cart-item-price">${item.priceLabel}</div>
        </div>
      `).join("");
    }

    function addToCart(productId) {
      const product = products.find((item) => item.id === productId);
      if (!product) return;

      cart.push(product);
      updateCart();
      toggleCart(true);
      closeProductModal();
    }

    renderProducts(products);
    updateCart();
  </script>
</body>
</html>
