<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>K2 MART</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Times New Roman', Times, serif, Arial, sans-serif;
        }

        body {
            background-color: #0d0d0d;
            color: #e6e6e6;
        }

        .top-bar {
            background-color: #1a1a1a;
            color: #d4af37;
            text-align: center;
            padding: 9px;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-bottom: 1px solid #2a2a2a;
        }

        header {
            background-color: #0a0a0a;
            border-bottom: 1px solid #1a1a1a;
            padding: 20px 0;
            text-align: center;
        }

        .brand-logo {
            font-size: 32px;
            font-weight: bold;
            letter-spacing: 5px;
            text-transform: uppercase;
            color: #d4af37;
            text-shadow: 0px 2px 4px rgba(212, 175, 55, 0.3);
            text-decoration: none;
            display: block;
            margin-bottom: 15px;
            cursor: pointer;
        }

        .nav-menu {
            display: block;
            text-align: center;
        }

        .nav-link {
            color: #aaaaaa;
            text-decoration: none;
            font-size: 11px;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            font-weight: bold;
            padding: 5px 10px;
            display: inline-block;
            cursor: pointer;
        }

        .nav-link:hover, .nav-link.active {
            color: #d4af37;
        }

        .content-container {
            max-width: 950px;
            margin: 0 auto;
            padding: 45px 15px;
        }

        /* --- BANNER STYLE --- */
        .home-banner {
            width: 100%;
            margin-bottom: 30px;
            border: 1px solid #2a2a2a;
            border-radius: 4px;
            overflow: hidden;
            background-color: #1a1a1a;
            text-align: center;
        }

        .home-banner img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* --- HOME HERO & SHORT DESCRIPTION STYLES --- */
        .home-hero {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(180deg, #111 0%, #070707 100%);
            border: 1px solid #1a1a1a;
            border-radius: 4px;
            margin-bottom: 30px;
        }

        .home-main-title {
            font-size: 36px;
            letter-spacing: 6px;
            color: #ffffff;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        .feature-box {
            background-color: #111111;
            border: 1px solid #222222;
            padding: 20px;
            margin: 15px auto;
            max-width: 500px;
            border-radius: 2px;
            text-align: center;
        }

        .feature-box h2 {
            font-size: 14px;
            color: #d4af37;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 8px;
        }

        .feature-box p {
            font-size: 12px;
            color: #999999;
            line-height: 1.6;
        }

        .home-brand-story {
            margin-top: 35px;
            padding: 25px;
            background-color: #111111;
            border: 1px solid #1e1e1e;
            border-radius: 4px;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.7);
        }

        .story-title {
            font-size: 15px;
            text-transform: uppercase;
            letter-spacing: 3px;
            color: #d4af37;
            margin-bottom: 15px;
            border-bottom: 1px solid #222;
            padding-bottom: 10px;
        }

        .highlight-box {
            background-color: #161616;
            border-left: 3px solid #d4af37;
            padding: 15px;
            font-size: 13px;
            color: #ffffff;
            line-height: 1.6;
            text-align: left;
        }

        .page-title {
            font-size: 22px;
            font-weight: normal;
            letter-spacing: 3px;
            text-transform: uppercase;
            text-align: center;
            margin-bottom: 30px;
            color: #d4af37;
            border-bottom: 1px solid #222;
            padding-bottom: 10px;
        }

        /* --- GRID & CARDS --- */
        .premium-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 25px;
        }

        .product-card {
            background-color: #111111;
            border: 1px solid #222222;
            padding: 12px;
            border-radius: 2px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.5);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .product-image {
            width: 100%;
            height: 160px;
            object-fit: cover;
            background-color: #1a1a1a;
            border: 1px solid #2a2a2a;
            margin-bottom: 10px;
        }

        .product-name {
            font-size: 12px;
            font-weight: bold;
            letter-spacing: 0.5px;
            text-transform: uppercase;
            color: #ffffff;
            margin-bottom: 5px;
        }

        .product-price {
            font-size: 12px;
            color: #d4af37;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .live-rating-container {
            font-size: 12px;
            color: #e5c158;
            margin-bottom: 8px;
            cursor: pointer;
            text-decoration: underline dashed;
            letter-spacing: 0.5px;
            font-weight: bold;
        }
        .live-rating-container:hover {
            color: #ffffff;
        }

        .product-review-link {
            font-size: 10px;
            color: #aaaaaa;
            text-decoration: none;
            cursor: pointer;
            display: inline-block;
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            border: 1px solid #333;
            padding: 5px;
            border-radius: 2px;
            font-weight: bold;
        }

        .product-review-link:hover {
            color: #d4af37;
            border-color: #d4af37;
        }

        .action-btn {
            display: block;
            background-color: #d4af37;
            color: #000000;
            text-decoration: none;
            text-transform: uppercase;
            font-size: 10px;
            font-weight: bold;
            letter-spacing: 1px;
            padding: 8px;
            text-align: center;
            border-radius: 2px;
            margin-top: auto;
            cursor: pointer;
            border: none;
            width: 100%;
        }

        .action-btn:hover {
            background-color: #ffffff;
        }

        /* --- POPUP (REVIEW) --- */
        .reviews-popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 90%;
            max-width: 500px;
            background-color: #111111;
            border: 1px solid #d4af37;
            box-shadow: 0 0 30px rgba(0,0,0,0.9);
            z-index: 1000;
            padding: 25px;
            border-radius: 4px;
        }

        .popup-close {
            float: right;
            color: #999;
            cursor: pointer;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        .popup-close:hover { color: #fff; }

        .popup-backdrop {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 999;
        }

        /* --- ORDER FORM (UPDATED TO MATCH IMAGE) --- */
        .order-form-container {
            max-width: 500px;
            margin: 10px auto;
            background-color: #0d0d0d; /* Matching image bg */
            padding: 20px;
            border-radius: 4px;
        }

        .secure-checkout-title {
            font-size: 20px;
            font-weight: bold;
            letter-spacing: 4px;
            text-transform: uppercase;
            text-align: center;
            margin-bottom: 30px;
            color: #dca743; /* Gold from image */
            border-bottom: 1px solid #222;
            padding-bottom: 20px;
        }

        .back-btn {
            display: inline-block;
            background-color: transparent;
            color: #999999;
            padding: 5px 0;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            border: none;
            cursor: pointer;
            margin-bottom: 15px;
            border-bottom: 1px dashed #444;
        }

        .back-btn:hover {
            color: #dca743;
            border-bottom-color: #dca743;
        }

        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }

        .form-group label {
            display: block;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: #dca743; /* Gold labels */
            margin-bottom: 8px;
            font-weight: bold;
        }

        .form-group input, .form-group textarea, .form-group select {
            width: 100%;
            padding: 14px;
            background-color: #111111; /* Dark input */
            border: 1px solid #2d2d2d;
            color: #ffffff;
            font-size: 13px;
            border-radius: 4px;
            font-family: inherit;
        }

        .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
            border-color: #dca743;
            outline: none;
        }

        .form-group input[readonly] {
            color: #cccccc;
        }

        .submit-order-btn {
            display: block;
            width: 100%;
            background-color: #dca743; /* Gold button */
            color: #000000;
            border: none;
            padding: 16px;
            font-size: 14px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 3px;
            cursor: pointer;
            border-radius: 4px;
            margin-top: 30px;
        }

        .submit-order-btn:hover { background-color: #eebb55; }

        /* --- CONTACT STYLE --- */
        .contact-block {
            background-color: #111111;
            border: 1px solid #222222;
            padding: 30px;
            text-align: center;
            max-width: 450px;
            margin: 0 auto;
            border-radius: 4px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.6);
        }

        .contact-block strong {
            color: #d4af37;
            display: block;
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 12px;
        }

        .whatsapp-btn {
            display: inline-block;
            background-color: #25D366;
            color: #ffffff;
            text-decoration: none;
            font-size: 13px;
            font-weight: bold;
            letter-spacing: 1px;
            padding: 12px 25px;
            border-radius: 3px;
            margin-top: 15px;
            text-transform: uppercase;
            box-shadow: 0 4px 10px rgba(37, 211, 102, 0.3);
            transition: background 0.2s ease;
        }

        .whatsapp-btn:hover {
            background-color: #1ebd58;
            color: #ffffff;
        }

        .page-section { display: none; }
        #home-sec { display: block; }

        footer {
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid #1a1a1a;
            margin-top: 60px;
            background-color: #0a0a0a;
            font-size: 12px;
            color: #666;
        }

        @media (max-width: 768px) {
            .premium-grid { grid-template-columns: repeat(2, 1fr); }
        }
        @media (max-width: 480px) {
            .premium-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <div class="top-bar">Welcome to K2 MART</div>

    <header>
        <div class="brand-logo" onclick="showPage('home-sec')">K2 MART</div>
        <div class="nav-menu">
            <span class="nav-link active" id="link-home" onclick="showPage('home-sec')">Home</span> | 
            <span class="nav-link" id="link-sheets" onclick="showPage('sheets-sec')">Full Sheets</span> | 
            <span class="nav-link" id="link-liquids" onclick="showPage('liquids-sec')">Liquids</span> | 
            <span class="nav-link" id="link-samples" onclick="showPage('samples-sec')">Samples</span> | 
            <span class="nav-link" id="link-contact" onclick="showPage('contact-sec')">Contact</span>
        </div>
    </header>

    <div class="content-container">

        <!-- HOME SECTION -->
        <div id="home-sec" class="page-section">
            
            <div class="home-banner">
                <img src="https://via.placeholder.com/950x300/111111/d4af37?text=K2+MART+MAIN+BANNER" alt="Main Banner">
            </div>

            <div class="home-hero">
                <h1 class="home-main-title">K2 MART</h1>
                <p style="color:#d4af37; font-size:12px; letter-spacing:3px; margin-bottom:25px; font-style: italic;">Premium Quality & Ultimate Perfection</p>
                <div class="feature-box"><h2>100% Trusted Brand</h2><p>Built on flawless trust, providing high-end elite export reliability.</p></div>
                <div class="feature-box"><h2>Wholesale Prices</h2><p>Get top-tier manufacturing materials directly at uncompromised bulk rates.</p></div>
                <div class="feature-box"><h2>Highly Secure Shipping</h2><p>Fast, completely dynamic, and strict confidential safety logistics.</p></div>
            </div>

            <div class="home-brand-story">
                <h2 class="story-title">Confidential Wholesale Operations</h2>
                <div class="highlight-box">
                    <strong style="color: #d4af37; text-transform: uppercase; letter-spacing: 1px; display: block; margin-bottom: 5px;">🔒 Highly Recommended: Secret & Discrete Packaging</strong>
                    We strictly value your absolute privacy and safety. All orders are processed under our premium custom secret packaging system. Bags and parcels are completely non-branded, vacuum-sealed, and double-protected to keep your premium trade materials hidden from unverified eyes during international transit. Flawless security guaranteed.
                </div>
            </div>
        </div>

        <!-- SHEETS SECTION (10 Slots) -->
        <div id="sheets-sec" class="page-section">
            <h2 class="page-title">Full Sheets</h2>
            <div class="premium-grid">
                <!-- Slot 1 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 1</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,000 | Prem: 1,500</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 1')">✍️ leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 1')">Order Now</button>
                </div>
                <!-- Slot 2 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 2</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,200 | Prem: 1,800</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 2')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 2')">Order Now</button>
                </div>
                <!-- Slot 3 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 3</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,400 | Prem: 2,100</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 3')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 3')">Order Now</button>
                </div>
                <!-- Slot 4 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 4</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,500 | Prem: 2,300</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 4')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 4')">Order Now</button>
                </div>
                <!-- Slot 5 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 5</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,600 | Prem: 2,500</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 5')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 5')">Order Now</button>
                </div>
                <!-- Slot 6 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 6</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,700 | Prem: 2,650</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 6')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 6')">Order Now</button>
                </div>
                <!-- Slot 7 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 7</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,800 | Prem: 2,800</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 7')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 7')">Order Now</button>
                </div>
                <!-- Slot 8 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 8</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 1,900 | Prem: 3,000</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 8')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 8')">Order Now</button>
                </div>
                <!-- Slot 9 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 9</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 2,000 | Prem: 3,200</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 9')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 9')">Order Now</button>
                </div>
                <!-- Slot 10 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Full Sheet Slot 10</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 2,200 | Prem: 3,500</p>
                    <span class="product-review-link" onclick="openReviewPage('Full Sheet Slot 10')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Full Sheet Slot 10')">Order Now</button>
                </div>
            </div>
        </div>

        <!-- LIQUIDS SECTION (2 Slots) -->
        <div id="liquids-sec" class="page-section">
            <h2 class="page-title">Liquids Collection</h2>
            <div class="premium-grid">
                <!-- Slot 1 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Liquid Slot 1</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 800 | Prem: 1,200</p>
                    <span class="product-review-link" onclick="openReviewPage('Liquid Slot 1')">✍️ leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Liquid Slot 1')">Order Now</button>
                </div>
                <!-- Slot 2 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Liquid Slot 2</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Std: 900 | Prem: 1,350</p>
                    <span class="product-review-link" onclick="openReviewPage('Liquid Slot 2')">✍️ Leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Liquid Slot 2')">Order Now</button>
                </div>
            </div>
        </div>

        <!-- SAMPLES SECTION (1 Slot) -->
        <div id="samples-sec" class="page-section">
            <h2 class="page-title">Samples Collection</h2>
            <div class="premium-grid">
                <!-- Slot 1 -->
                <div class="product-card">
                    <div class="product-image"></div>
                    <h3 class="product-name">Sample Pack 1</h3>
                    <div class="live-rating-container">★ 5.0 (0 Reviews)</div>
                    <p class="product-price">Price: 500</p>
                    <span class="product-review-link" onclick="openReviewPage('Sample Pack 1')">✍️ leave A Review</span>
                    <button class="action-btn" onclick="selectProduct('Sample Pack 1')">Order Now</button>
                </div>
            </div>
        </div>

        <!-- ORDER FORM SECTION (MATCHING IMAGE "183863.jpg") -->
        <div id="order-sec" class="page-section">
            <button class="back-btn" onclick="goBackToProducts()">← Back</button>
            <div class="order-form-container">
                <h2 class="secure-checkout-title">SECURE CHECKOUT</h2>
                
                <form onsubmit="submitOrder(event)">
                    
                    <div class="form-group">
                        <label>Selected Product</label>
                        <input type="text" id="selected-product-input" readonly>
                    </div>
                    
                    <div class="form-group">
                        <label>Quantity</label>
                        <input type="number" min="1" value="1" required>
                    </div>
                    
                    <div class="form-group">
                        <label>Country / Region</label>
                        <select id="country-select" onchange="toggleOtherCountry()" required>
                            <option value="" disabled selected>Select your country</option>
                            <option value="United States">United States</option>
                            <option value="United Kingdom">United Kingdom</option>
                            <option value="Canada">Canada</option>
                            <option value="Australia">Australia</option>
                            <option value="Germany">Germany</option>
                            <option value="France">France</option>
                            <option value="Pakistan">Pakistan</option>
                            <option value="India">India</option>
                            <option value="United Arab Emirates">United Arab Emirates</option>
                            <option value="Saudi Arabia">Saudi Arabia</option>
                            <option value="Other">Other</option>
                        </select>
                    </div>

                    <!-- Hidden Input for "Other" Country -->
                    <div class="form-group" id="other-country-group" style="display: none;">
                        <label>Enter Your Country</label>
                        <input type="text" id="other-country-input" placeholder="Type your country name">
                    </div>

                    <div class="form-group">
                        <label>Full Name</label>
                        <input type="text" placeholder="Enter Name" required>
                    </div>

                    <div class="form-group">
                        <label>Email Address</label>
                        <input type="email" placeholder="Enter Email" required>
                    </div>

                    <div class="form-group">
                        <label>Phone Number</label>
                        <input type="text" placeholder="Enter Phone" required>
                    </div>
                    
                    <div class="form-group">
                        <label>Shipping Address</label>
                        <textarea rows="3" placeholder="Enter Full Street Address, City, State, Zip Code" required></textarea>
                    </div>

                    <button type="submit" class="submit-order-btn">Confirm Order</button>
                </form>
            </div>
        </div>

        <!-- CONTACT & WHATSAPP SECTION -->
        <div id="contact-sec" class="page-section">
            <h2 class="page-title">Contact Us</h2>
            <div class="contact-block">
                <strong>24/7 Secure Support</strong>
                <p style="font-size: 12px; color: #999; margin-bottom: 15px;">For direct bulk deals, highly confidential queries, or urgent support, reach out directly on WhatsApp.</p>
                <a href="https://wa.me/1234567890" target="_blank" class="whatsapp-btn">💬 Chat on WhatsApp</a>
            </div>
        </div>

    </div>

    <!-- REVIEW POPUP FORM -->
    <div id="popup-backdrop" class="popup-backdrop" onclick="closePopup()"></div>
    <div id="review-popup" class="reviews-popup">
        <span class="popup-close" onclick="closePopup()">X Close</span>
        <h3 style="color:#d4af37; margin-bottom: 15px; border-bottom: 1px solid #333; padding-bottom: 10px;">Leave a Review</h3>
        <p id="review-product-name" style="margin-bottom: 15px; font-weight: bold; color: #fff;"></p>
        
        <form onsubmit="submitReview(event)">
            <div class="form-group">
                <label>Your Name</label>
                <input type="text" placeholder="Enter your name" required>
            </div>
            <div class="form-group">
                <label>Rating</label>
                <select required>
                    <option value="5">★★★★★ (5 Stars)</option>
                    <option value="4">★★★★☆ (4 Stars)</option>
                    <option value="3">★★★☆☆ (3 Stars)</option>
                    <option value="2">★★☆☆☆ (2 Stars)</option>
                    <option value="1">★☆☆☆☆ (1 Star)</option>
                </select>
            </div>
            <div class="form-group">
                <label>Your Review</label>
                <textarea rows="4" placeholder="Write your feedback..." required></textarea>
            </div>
            <button type="submit" class="submit-order-btn" style="margin-top: 15px;">Submit Review</button>
        </form>
    </div>

    <footer>
        &copy; 2026 K2 MART. All Rights Reserved.
    </footer>

    <!-- JAVASCRIPT -->
    <script>
        let lastVisitedCategory = 'home-sec'; 

        function showPage(pageId) {
            let sections = document.querySelectorAll('.page-section');
            sections.forEach(sec => sec.style.display = 'none');
            
            let links = document.querySelectorAll('.nav-link');
            links.forEach(link => link.classList.remove('active'));
            
            document.getElementById(pageId).style.display = 'block';
            let activeLink = document.getElementById('link-' + pageId.replace('-sec', ''));
            if(activeLink) activeLink.classList.add('active');

            if(pageId !== 'order-sec' && pageId !== 'contact-sec') {
                lastVisitedCategory = pageId; 
            }
        }

        function openReviewPage(productName) {
            document.getElementById('review-product-name').innerText = "Product: " + productName;
            document.getElementById('popup-backdrop').style.display = 'block';
            document.getElementById('review-popup').style.display = 'block';
        }

        function closePopup() {
            document.getElementById('popup-backdrop').style.display = 'none';
            document.getElementById('review-popup').style.display = 'none';
        }

        function submitReview(event) {
            event.preventDefault();
            alert("Thank you! Your review has been submitted.");
            closePopup(); 
        }

        // Modified selectProduct function to populate input field
        function selectProduct(productName) {
            document.getElementById('selected-product-input').value = productName;
            showPage('order-sec'); 
            window.scrollTo(0, 0); 
        }

        function goBackToProducts() {
            showPage(lastVisitedCategory); 
        }

        // Toggle "Other Country" input box
        function toggleOtherCountry() {
            let selectBox = document.getElementById("country-select");
            let otherGroup = document.getElementById("other-country-group");
            let otherInput = document.getElementById("other-country-input");
            
            if (selectBox.value === "Other") {
                otherGroup.style.display = "block";
                otherInput.required = true;
            } else {
                otherGroup.style.display = "none";
                otherInput.required = false;
                otherInput.value = "";
            }
        }

        function submitOrder(event) {
            event.preventDefault(); 
            alert("Your order has been placed successfully! We will contact you soon.");
            showPage('home-sec'); 
        }
    </script>
</body>
</html>
