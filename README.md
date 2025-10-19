# saharagrillrousehill.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sahara Grill - Authentic Middle Eastern Cuisine</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #8B4513 0%, #D2691E 100%);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0;
            background: rgba(255, 255, 255, 0.15);
            padding: 10px 25px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .logo img {
            height: 80px;
            width: auto;
        }

        nav {
            position: relative;
        }

        .menu-toggle {
            background: rgba(255, 255, 255, 0.95);
            border: 2px solid #8B4513;
            border-radius: 10px;
            padding: 12px 20px;
            font-size: 1.1em;
            font-weight: bold;
            color: #8B4513;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 15px;
            transition: all 0.3s;
        }

        .menu-toggle:hover {
            background: rgba(255, 255, 255, 1);
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .hamburger {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .hamburger span {
            display: block;
            width: 25px;
            height: 3px;
            background: #8B4513;
            border-radius: 2px;
        }

        .nav-dropdown {
            display: none;
            position: absolute;
            top: 60px;
            right: 0;
            background: rgba(255, 255, 255, 0.98);
            border: 2px solid #8B4513;
            border-radius: 10px;
            min-width: 200px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            overflow: hidden;
        }

        .nav-dropdown.active {
            display: block;
        }

        .nav-dropdown a {
            display: block;
            padding: 15px 25px;
            color: #8B4513;
            text-decoration: none;
            font-weight: bold;
            transition: background 0.3s;
            border-bottom: 1px solid rgba(139, 69, 19, 0.1);
        }

        .nav-dropdown a:last-child {
            border-bottom: none;
        }

        .nav-dropdown a:hover {
            background: rgba(255, 140, 0, 0.1);
        }

        nav ul {
            display: none;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(255, 140, 0, 0.85), rgba(255, 140, 0, 0.85)),
                        url('data:image/svg+xml,%3Csvg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"%3E%3Cdefs%3E%3Cpattern id="kebab" width="300" height="300" patternUnits="userSpaceOnUse"%3E%3Cellipse cx="150" cy="80" rx="60" ry="40" fill="%23A0522D" opacity="0.3"/%3E%3Cellipse cx="150" cy="130" rx="50" ry="35" fill="%238B4513" opacity="0.3"/%3E%3Cellipse cx="150" cy="180" rx="55" ry="38" fill="%23CD853F" opacity="0.3"/%3E%3Crect x="140" y="60" width="20" height="150" fill="%23D2691E" opacity="0.2"/%3E%3C/pattern%3E%3C/defs%3E%3Crect fill="%23FF8C00" width="1200" height="600"/%3E%3Crect fill="url(%23kebab)" width="1200" height="600"/%3E%3C/svg%3E');
            background-size: cover;
            background-position: center;
            padding: 100px 0;
            text-align: center;
            color: white;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(139, 69, 19, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(210, 105, 30, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 50% 50%, rgba(160, 82, 45, 0.1) 0%, transparent 60%);
            pointer-events: none;
        }

        .hero h2 {
            font-size: 3.5em;
            margin-bottom: 20px;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.5em;
            margin-bottom: 30px;
        }

        .cta-button {
            display: inline-block;
            background: #8B4513;
            color: white;
            padding: 15px 40px;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.2em;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
        }

        /* Specials Section */
        .specials {
            padding: 80px 0;
            background: #fff;
        }

        .section-title {
            text-align: center;
            font-size: 2.5em;
            color: #8B4513;
            margin-bottom: 50px;
        }

        .specials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 40px;
            margin-top: 40px;
        }

        .special-card {
            background: linear-gradient(135deg, #FF8C00 0%, #FFA500 100%);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }

        .special-card:hover {
            transform: translateY(-10px);
        }

        .special-content {
            padding: 40px;
            color: white;
        }

        .special-card h3 {
            font-size: 2.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .special-card .price {
            font-size: 2em;
            font-weight: bold;
            color: #8B0000;
            background: #FFD700;
            display: inline-block;
            padding: 10px 20px;
            border-radius: 10px;
            margin: 20px 0;
        }

        .special-card .offer {
            font-size: 1.2em;
            margin: 15px 0;
            padding: 15px;
            background: rgba(255,255,255,0.2);
            border-radius: 10px;
        }

        .special-card .details {
            font-size: 0.9em;
            margin-top: 20px;
            opacity: 0.9;
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background: #F5DEB3;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .about-content p {
            font-size: 1.2em;
            line-height: 1.8;
            margin-bottom: 20px;
            color: #555;
        }

        /* Menu Gallery */
        .menu-gallery {
            padding: 80px 0;
            background: #fff;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .gallery-item {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .gallery-item-content {
            padding: 20px;
            background: #f9f9f9;
        }

        .gallery-item h4 {
            color: #8B4513;
            font-size: 1.3em;
            margin-bottom: 10px;
        }

        /* Catering Section */
        .catering {
            padding: 80px 0;
            background: linear-gradient(135deg, #8B4513 0%, #D2691E 100%);
            color: white;
            text-align: center;
        }

        .catering h2 {
            color: #FFD700;
        }

        .catering-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .catering-content p {
            font-size: 1.2em;
            margin: 20px 0;
        }

        .catering-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .catering-feature {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
        }

        .catering-feature h4 {
            font-size: 1.5em;
            margin-bottom: 15px;
            color: #FFD700;
        }

        /* Social Media Section */
        .social {
            padding: 60px 0;
            background: #fff;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 30px;
        }

        .social-link {
            display: inline-block;
            width: 60px;
            height: 60px;
            background: #FF8C00;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
            text-decoration: none;
            transition: transform 0.3s, background 0.3s;
        }

        .social-link:hover {
            transform: scale(1.1);
            background: #8B4513;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        footer p {
            margin: 10px 0;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }

            .nav-dropdown {
                width: 100%;
            }

            .hero h2 {
                font-size: 2em;
            }

            .specials-grid {
                grid-template-columns: 1fr;
            }

            .logo img {
                height: 60px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 120'%3E%3Cdefs%3E%3CradialGradient id='spiral1'%3E%3Cstop offset='0%25' style='stop-color:%238B4513'/%3E%3Cstop offset='50%25' style='stop-color:%23A0522D'/%3E%3Cstop offset='100%25' style='stop-color:%236B3410'/%3E%3C/radialGradient%3E%3CradialGradient id='spiral2'%3E%3Cstop offset='0%25' style='stop-color:%23D2691E'/%3E%3Cstop offset='100%25' style='stop-color:%23CD853F'/%3E%3C/radialGradient%3E%3C/defs%3E%3Ccircle cx='55' cy='60' r='45' fill='url(%23spiral1)'/%3E%3Cpath d='M 55,60 Q 75,40 85,60 T 75,80 T 55,75 T 45,60 T 55,50' fill='none' stroke='%23CD853F' stroke-width='3'/%3E%3Ccircle cx='55' cy='60' r='30' fill='url(%23spiral2)'/%3E%3Cpath d='M 55,60 Q 65,50 70,60 T 65,70 T 55,68 T 50,60 T 55,55' fill='none' stroke='%238B4513' stroke-width='2'/%3E%3Ctext x='120' y='65' font-family='Georgia,serif' font-size='52' fill='%23D2B48C' letter-spacing='2'%3ESahara%3C/text%3E%3Ctext x='120' y='95' font-family='Georgia,serif' font-size='20' fill='%23D2B48C' font-style='italic' letter-spacing='8'%3EGRILL%3C/text%3E%3C/svg%3E" alt="Sahara Grill Logo">
                </div>
                <nav>
                    <button class="menu-toggle" onclick="document.querySelector('.nav-dropdown').classList.toggle('active')">
                        <div class="hamburger">
                            <span></span>
                            <span></span>
                            <span></span>
                        </div>
                        <span>Menu</span>
                    </button>
                    <div class="nav-dropdown">
                        <a href="#about" onclick="document.querySelector('.nav-dropdown').classList.remove('active')">About</a>
                        <a href="#specials" onclick="document.querySelector('.nav-dropdown').classList.remove('active')">Specials</a>
                        <a href="#menu" onclick="document.querySelector('.nav-dropdown').classList.remove('active')">Menu</a>
                        <a href="#catering" onclick="document.querySelector('.nav-dropdown').classList.remove('active')">Catering</a>
                        <a href="#social" onclick="document.querySelector('.nav-dropdown').classList.remove('active')">Connect</a>
                    </div>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h2>Authentic Middle Eastern Cuisine</h2>
            <p>Experience the rich flavors of the Sahara</p>
            <a href="#specials" class="cta-button">View Our Specials</a>
        </div>
    </section>

    <section id="specials" class="specials">
        <div class="container">
            <h2 class="section-title">Daily Specials</h2>
            <div class="specials-grid">
                <div class="special-card">
                    <div class="special-content">
                        <h3>TRADIES SPECIAL</h3>
                        <div class="price">FROM $15</div>
                        <div class="offer">🎁 1 FREE CAN OF DRINK WITH ANY GOZLEME OR KEBAB PURCHASE</div>
                        <p style="font-size: 1.3em; margin: 20px 0;">✅ Gluten Free Kebabs Available</p>
                        <div class="details">
                            <p>⏰ MONDAY TO SATURDAY 10:30 AM - 2:30 PM</p>
                            <p>⚠️ *CONSTRUCTION WORKERS IN PPE ONLY</p>
                        </div>
                    </div>
                </div>

                <div class="special-card">
                    <div class="special-content">
                        <h3>SCHOOL KIDS SPECIAL</h3>
                        <div class="price">FROM $15</div>
                        <div class="offer">🎁 1 FREE CAN OF DRINK WITH ANY SNACKPACK PURCHASE</div>
                        <p style="font-size: 1.3em; margin: 20px 0;">🍟 Loaded Snack Packs with All Your Favorite Toppings</p>
                        <div class="details">
                            <p>⏰ MONDAY TO FRIDAY 3:00 PM - 5:30 PM</p>
                            <p>⚠️ *SPECIAL APPLIES FOR SCHOOL KIDS IN UNIFORM ONLY</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="catering" class="catering">
        <div class="container">
            <h2 class="section-title">Catering Services</h2>
            <div class="catering-content">
                <p>Make your next event unforgettable with Sahara Grill catering!</p>
                <p>Whether it's a corporate lunch, wedding, birthday party, or any special occasion, we bring the authentic taste of the Middle East to your event.</p>
                
                <div class="catering-features">
                    <div class="catering-feature">
                        <h4>🎉 Events</h4>
                        <p>Weddings, parties, corporate functions</p>
                    </div>
                    <div class="catering-feature">
                        <h4>📦 Custom Packages</h4>
                        <p>Tailored menus for any group size</p>
                    </div>
                    <div class="catering-feature">
                        <h4>🚚 Delivery</h4>
                        <p>Fresh food delivered on time</p>
                    </div>
                    <div class="catering-feature">
                        <h4>👨‍🍳 Professional</h4>
                        <p>Experienced catering team</p>
                    </div>
                </div>
                
                <a href="#social" class="cta-button" style="margin-top: 30px;">Contact Us for Catering</a>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Sahara Grill</h2>
            <div class="about-content">
                <p>Welcome to Sahara Grill, where tradition meets taste. We bring you the authentic flavors of Middle Eastern cuisine, prepared fresh daily with the finest ingredients and traditional recipes passed down through generations.</p>
                <p>Our skilled chefs craft each dish with passion and precision, from our signature kebabs and gozleme to our delicious snack packs. Whether you're grabbing a quick lunch or catering a special event, we're committed to delivering an unforgettable dining experience.</p>
                <p>We pride ourselves on offering quality food at great prices, with special offers for tradies and school kids. Come taste the difference at Sahara Grill!</p>
            </div>
        </div>
    </section>

    <section id="menu" class="menu-gallery">
        <div class="container">
            <h2 class="section-title">Our Delicious Menu</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'%3E%3Crect fill='%23D2691E' width='400' height='300'/%3E%3Ctext x='50%25' y='50%25' fill='white' font-size='24' text-anchor='middle' dy='.3em'%3EGrilled Kebabs%3C/text%3E%3C/svg%3E" alt="Kebabs">
                    <div class="gallery-item-content">
                        <h4>Premium Kebabs</h4>
                        <p>Tender, marinated meats grilled to perfection with fresh vegetables and our signature sauces.</p>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'%3E%3Crect fill='%23FF8C00' width='400' height='300'/%3E%3Ctext x='50%25' y='50%25' fill='white' font-size='24' text-anchor='middle' dy='.3em'%3EFresh Gozleme%3C/text%3E%3C/svg%3E" alt="Gozleme">
                    <div class="gallery-item-content">
                        <h4>Traditional Gozleme</h4>
                        <p>Hand-rolled flatbreads filled with savory ingredients and cooked on our traditional griddle.</p>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'%3E%3Crect fill='%238B4513' width='400' height='300'/%3E%3Ctext x='50%25' y='50%25' fill='white' font-size='24' text-anchor='middle' dy='.3em'%3ESnack Packs%3C/text%3E%3C/svg%3E" alt="Snack Packs">
                    <div class="gallery-item-content">
                        <h4>Loaded Snack Packs</h4>
                        <p>Crispy chips topped with your choice of meat, cheese, and our special sauces.</p>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'%3E%3Crect fill='%23CD853F' width='400' height='300'/%3E%3Ctext x='50%25' y='50%25' fill='white' font-size='24' text-anchor='middle' dy='.3em'%3EFresh Salads%3C/text%3E%3C/svg%3E" alt="Salads">
                    <div class="gallery-item-content">
                        <h4>Fresh Salads</h4>
                        <p>Crisp, colorful salads with authentic Middle Eastern flavors and dressings.</p>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'%3E%3Crect fill='%23A0522D' width='400' height='300'/%3E%3Ctext x='50%25' y='50%25' fill='white' font-size='24' text-anchor='middle' dy='.3em'%3EFalafel Wraps%3C/text%3E%3C/svg%3E" alt="Falafel">
                    <div class="gallery-item-content">
                        <h4>Falafel Wraps</h4>
                        <p>Crispy, golden falafel with fresh vegetables and tahini sauce wrapped in warm pita.</p>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'%3E%3Crect fill='%23B8860B' width='400' height='300'/%3E%3Ctext x='50%25' y='50%25' fill='white' font-size='24' text-anchor='middle' dy='.3em'%3EHummus %26 Dips%3C/text%3E%3C/svg%3E" alt="Dips">
                    <div class="gallery-item-content">
                        <h4>Authentic Dips</h4>
                        <p>Creamy hummus, baba ganoush, and tzatziki served with fresh pita bread.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="social" class="social">
        <div class="container">
            <h2 class="section-title">Connect With Us</h2>
            <p style="font-size: 1.2em; margin: 20px 0;">Follow us on social media for daily specials, updates, and mouthwatering photos!</p>
            <div class="social-links">
                <a href="#" class="social-link" title="Facebook">f</a>
                <a href="#" class="social-link" title="Instagram">📷</a>
                <a href="#" class="social-link" title="Twitter">🐦</a>
                <a href="#" class="social-link" title="TikTok">🎵</a>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Sahara Grill. All rights reserved.</p>
            <p>📍 Sydney, NSW | 📞 Contact us for catering inquiries</p>
            <p>🕐 Open Monday to Saturday | Check our specials for specific times</p>
        </div>
    </footer>
</body>
</html>
