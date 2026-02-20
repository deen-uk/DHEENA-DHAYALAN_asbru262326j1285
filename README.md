<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouAndMe Gifts - Handmade Photo Frames & Bouquets</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Poppins', sans-serif; line-height: 1.6; color: #333; overflow-x: hidden;
        }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

        /* === HEADER === */
        header {
            background: linear-gradient(135deg, #ff6b9d, #c44569); color: white;
            position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }
        .nav-bar {
            display: flex; justify-content: space-between; align-items: center; padding: 15px 0;
        }
        .logo {
            font-family: 'Dancing Script', cursive; font-size: 32px; font-weight: 700;
        }
        .nav-links {
            display: flex; list-style: none; gap: 30px;
        }
        .nav-links a {
            color: white; text-decoration: none; font-weight: 500; transition: all 0.3s;
        }
        .nav-links a:hover { color: #ffeaa7; transform: translateY(-2px); }
        .cta-btn {
            background: #ffeaa7; color: #c44569; padding: 12px 30px; border-radius: 50px;
            font-weight: 600; text-decoration: none; transition: all 0.3s;
        }
        .cta-btn:hover { background: #fdcb6e; transform: scale(1.05); }

        /* === HERO SECTION === */
        .hero {
            background: linear-gradient(rgba(255,107,157,0.9), rgba(196,69,105,0.9)),
                        url('https://images.unsplash.com/photo-1574169208507-84376144848b?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover; background-position: center; height: 100vh;
            display: flex; align-items: center; text-align: center; color: white;
        }
        .hero-content h1 {
            font-family: 'Dancing Script', cursive; font-size: 64px; margin-bottom: 20px;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.3);
        }
        .hero-content p {
            font-size: 20px; margin-bottom: 30px; max-width: 600px; margin-left: auto; margin-right: auto;
        }
        .hero-buttons { display: flex; gap: 20px; justify-content: center; flex-wrap: wrap; }

        /* === SECTIONS === */
        section { padding: 80px 0; }
        .section-title {
            font-family: 'Dancing Script', cursive; font-size: 48px; text-align: center;
            margin-bottom: 50px; color: #c44569;
        }

        /* === ABOUT === */
        .about {
            background: #f8f9fa; text-align: center;
        }
        .about-content {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px; align-items: center;
        }
        .about-text h2 { font-size: 36px; margin-bottom: 20px; color: #c44569; }
        .about-features {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px; margin-top: 40px;
        }
        .feature {
            text-align: center; padding: 30px; background: white;
            border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        .feature i { font-size: 48px; color: #ff6b9d; margin-bottom: 20px; }

        /* === PRODUCTS === */
        .products { background: white; }
        .products-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }
        .product-card {
            background: white; border-radius: 20px; overflow: hidden;
            box-shadow: 0 15px 40px rgba(0,0,0,0.1); transition: all 0.4s;
            cursor: pointer; position: relative;
        }
        .product-card:hover {
            transform: translateY(-15px); box-shadow: 0 30px 60px rgba(0,0,0,0.2);
        }
        .product-img {
            width: 100%; height: 280px; object-fit: cover;
        }
        .product-info {
            padding: 25px; text-align: center;
        }
        .product-name {
            font-size: 22px; font-weight: 600; margin-bottom: 10px; color: #2d3436;
        }
        .product-price {
            font-size: 28px; font-weight: 700; color: #00b894; margin-bottom: 15px;
        }
        .customize-btn {
            width: 100%; padding: 15px; background: linear-gradient(45deg, #ff6b9d, #c44569);
            color: white; border: none; border-radius: 50px; font-size: 18px; font-weight: 600;
            cursor: pointer; transition: all 0.3s;
        }
        .customize-btn:hover {
            transform: scale(1.05); box-shadow: 0 10px 30px rgba(255,107,157,0.4);
        }

        /* === INSTAGRAM SECTION === */
        .instagram {
            background: #000; color: white; text-align: center;
        }
        .insta-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px; margin-top: 40px;
        }
        .insta-post {
            position: relative; height: 300px; background-size: cover; background-position: center;
            border-radius: 15px; cursor: pointer; transition: all 0.3s;
        }
        .insta-post:hover { transform: scale(1.05); }
        .insta-overlay {
            position: absolute; bottom: 20px; left: 20px; right: 20px;
            background: rgba(255,255,255,0.9); padding: 15px; border-radius: 10px;
        }

        /* === CONTACT === */
        .contact {
            background: linear-gradient(135deg, #ff6b9d, #c44569); color: white;
            text-align: center;
        }
        .contact-info {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px; margin-top: 40px;
        }
        .contact-item i { font-size: 48px; margin-bottom: 20px; color: #ffeaa7; }
        .contact-form {
            max-width: 600px; margin: 40px auto 0; background: rgba(255,255,255,0.1);
            padding: 40px; border-radius: 20px; backdrop-filter: blur(10px);
        }
        .form-group {
            margin-bottom: 25px; text-align: left;
        }
        .form-group input, .form-group textarea {
            width: 100%; padding: 15px; border: none; border-radius: 10px;
            font-size: 16px; background: rgba(255,255,255,0.9);
        }
        .form-group textarea { height: 120px; resize: vertical; }

        /* === FOOTER === */
        footer {
            background: #2d3436; color: white; text-align: center; padding: 40px 0 20px;
        }
        .social-links {
            display: flex; justify-content: center; gap: 25px; margin: 30px 0; flex-wrap: wrap;
        }

        /* === 🔥 BLINKING ANIMATED SOCIAL ICONS 🔥 === */
        .social-link {
            position: relative; display: inline-flex; align-items: center; gap: 12px;
            color: white; text-decoration: none; font-size: 20px; font-weight: 600;
            padding: 18px 28px; background: linear-gradient(45deg, #ff6b9d, #fd79a8);
            border-radius: 50px; transition: all 0.4s ease; overflow: hidden;
            box-shadow: 0 8px 25px rgba(255,107,157,0.4);
        }

        /* ✨ BLINKING GLOW EFFECT */
        @keyframes blink-glow {
            0%, 100% { 
                box-shadow: 0 8px 25px rgba(255,107,157,0.4), 0 0 20px rgba(255,107,157,0.2);
            }
            50% { 
                box-shadow: 0 8px 40px rgba(255,107,157,0.8), 0 0 40px rgba(255,107,157,0.6);
            }
        }

        /* ✨ PULSE ANIMATION */
        @keyframes pulse-icon {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* ✨ BOUNCING ARROW */
        @keyframes bounce-arrow {
            0%, 20%, 50%, 80%, 100% { transform: translateX(0); }
            40% { transform: translateX(8px); }
            60% { transform: translateX(4px); }
        }

        /* APPLY ANIMATIONS */
        .social-link {
            animation: blink-glow 2s ease-in-out infinite;
        }
        .social-link i {
            animation: pulse-icon 2s ease-in-out infinite;
        }
        .social-link::after {
            content: '→'; font-size: 18px; margin-left: 8px;
            animation: bounce-arrow 1.5s ease-in-out infinite;
        }

        /* HOVER EFFECTS */
        .social-link:hover {
            transform: translateY(-8px) scale(1.08);
            box-shadow: 0 20px 50px rgba(255,107,157,0.7);
            animation-play-state: paused;
        }
        .social-link:hover i {
            transform: scale(1.3) rotate(360deg);
        }
        .social-link:hover::after {
            transform: translateX(12px);
            animation-play-state: paused;
        }

        /* === RESPONSIVE === */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero-content h1 { font-size: 42px; }
            .hero-buttons { flex-direction: column; align-items: center; }
            .products-grid { grid-template-columns: 1fr; }
            .social-links { flex-direction: column; gap: 20px; align-items: center; }
            .social-link { width: 280px; justify-content: center; }
        }

        /* === ANIMATIONS === */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .fade-in { animation: fadeInUp 0.8s ease forwards; }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">You & Me <span style="color:#ffeaa7;">Gifts</span></div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul><br>
            <a href="#contact" class="cta-btn">Order Now <i class="fas fa-gift"></i></a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content container fade-in">
            <h1>Handmade Gifts with ❤️</h1>
            <p>Custom Photo Frames & handmade gifts with love for your special moments</p>
            <div class="hero-buttons">
                <a href="#products" class="cta-btn" style="background:#ffeaa7;color:#c44569;">Shop Now</a>
                
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title fade-in">Why Choose You & Me Gifts?</h2>
            <div class="about-content">
                <div>
                    <h2>Handcrafted with Love</h2>
                    <p>Make your memories into timeless art.</p>
                    <p>Every piece is made by skilled artisans who pour their heart into creating personalized gifts that tell your unique love story.</p>
                </div>
                <img src="https://pin.it/1SvEj5AQF=600" alt="" style="width:100%;border-radius:20px;">
            </div>
            <div class="about-features">
                <div class="feature fade-in">
                    <i class="fas fa-heart"></i>
                    <h3>100% Handmade</h3>
                    <p>No mass production, pure handmade perfection</p>
                </div>
                <div class="feature fade-in">
                    <i class="fas fa-rocket"></i>
                    <h3>Fast Delivery</h3>
                    <p>Ready in 3-7 days across Tamilnadu</p>
                </div>
                <div class="feature fade-in">
                    <i class="fas fa-shipping-fast"></i>
                    <h3>Free Shipping</h3>
                    <p>Free delivery on all orders above ₹999</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section - FIXED HTML STRUCTURE -->
    <section id="products" class="products">
        <div class="container">
            <h2 class="section-title fade-in">Our products</h2>
            <div class="products-grid">
                <div class="product-card fade-in">
                    <img src="https://m.media-amazon.com/images/I/715i0y9-T9L._SL1200_.jpg" class="product-img" alt="Photo Frame">
                    <div class="product-info">
                        <h3>Custom Photo Frame</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6> ₹200<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div>
                </div>
                <div class="product-card fade-in">
                    <img src="https://i.etsystatic.com/26760439/r/il/37975b/3762288938/il_fullxfull.3762288938_g2s8.jpg" class="product-img" alt="Chocolate Bouquet">
                    <div class="product-info">
                        <h3>Gift Hamper</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹150 <span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div>
                </div>
                <div class="product-card fade-in">
                    <img src="https://i.pinimg.com/originals/6e/c3/3d/6ec33d23645e624eafa7c509c07de82e.jpg" class="product-img" alt="Flower Bouquet">
                    <div class="product-info">
                        <h3>Bouquet</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹150<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div>
                </div>
                <div class="product-card fade-in">
                    <img src="https://tse2.mm.bing.net/th/id/OIP.fUYDwg1LGA_L_X8JQTnpwgHaHr?pid=Api&P=0&h=180" class="product-img" alt="LED Frame">
                    <div class="product-info">
                        <h3>LED Photo Frame</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹500 <span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div>  
        </div>
        <div class="product-card fade-in">
                    <img src="https://tse2.mm.bing.net/th/id/OIP.PJJQ7kJ_t2D2XhmrZxTuswHaEK?pid=Api&P=0&h=180" class="product-img" alt="Flower Bouquet">
                    <div class="product-info">
                        <h3>Wish Cards</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹150<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div></div>
                     <div class="product-card fade-in">
                    <img src="https://5.imimg.com/data5/SELLER/Default/2022/5/PC/KG/UL/151800931/polaroid-photos-500x500.jpg" class="product-img" alt="Flower Bouquet">
                    <div class="product-info">
                        <h3>Polorid photo</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹150<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div></div>
                    <div class="product-card fade-in">
                    <img src="https://memoriascriativas.com.br/wp-content/uploads/2023/03/WhatsApp-Image-2023-03-18-at-12.02.29.jpeg" class="product-img" alt="Flower Bouquet">
                    <div class="product-info">
                        <h3>Spotify photo cards</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹150<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div></div>
                    <div class="product-card fade-in">
                    <img src="https://www.wewishes.com/uploads/images/202311/image_870x_6557730c90a0d.webp" class="product-img" alt="Flower Bouquet">
                    <div class="product-info">
                        <h3>Photo album</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹1000<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div></div>
                    <div class="product-card fade-in">
                    <img src="https://i.pinimg.com/736x/7a/37/58/7a37586faa4da9c9a77fa41167b8c271.jpg" class="product-img" alt="Flower Bouquet">
                    <div class="product-info">
                        <h3>Plate deceration</h3>
                        <div class="product-price"><h6 style="font-size:10px;color:#090000;">From :</h6>₹500<span style="font-size:18px;color:#666;text-decoration:line-through;"></span></div>
                        <button class="customize-btn">Customize Now</button>
                    </div></div>
    </section>

    <!-- Instagram Section -->
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title" style="color:white;">Ready to Create Magic?</h2>
            <p style="font-size:20px;margin-bottom:20px;">Send us your photos & message - We'll create something amazing!</p>
            
            <div class="contact-info">
                <div>
                    <i class="fas fa-phone"></i>
                    <h3>Call Us</h3>
                    <p>+91 9976555877</p>
                </div>
                <div>
                    <i class="fas fa-envelope"></i>
                    <h3>Email</h3>
                    <p>youandmegifts26@gmail.com</p>
                </div>
                <div>
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Visit Us</h3>
                    <p>Coimbatore, Tamilnadu</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer with ANIMATED SOCIAL LINKS -->
    <footer>
        <div class="container">
            <div class="logo" style="font-size:28px;margin-bottom:20px;">You & Me Gifts</div>
            <p>&copy; 2026 YouAndMe_Gift.in. Made with ❤️ Coimbatore</p>
            <div class="social-links">
                <a href="https://instagram.com/youandme_gift.in" target="_blank" class="social-link">
                    <i class="fab fa-instagram"></i> Instagram
                </a>
                <a href="https://wa.me/919976555877" target="_blank" class="social-link">
                    <i class="fab fa-whatsapp"></i> WhatsApp
                </a>
                <a href="mailto:youandmegifts26@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i> Email
                </a>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Customize buttons - Updated WhatsApp number
        document.querySelectorAll('.customize-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const productName = this.closest('.product-card').querySelector('h3').textContent;
                window.open(`https://wa.me/919976555877?text=Hi! I want to customize: ${productName}`);
            });
        });

        // Scroll animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationPlayState = 'running';
                }
            });
        });
        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
    </script>
</body>
</html>
