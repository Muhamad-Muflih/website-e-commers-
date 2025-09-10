<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern E-Commerce Store - GitHub Connected</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.0/font/bootstrap-icons.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        .navbar {
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            backdrop-filter: blur(10px);
            background-color: rgba(255, 255, 255, 0.95);
        }
        .btn-primary:hover {
            transform: scale(1.05);
            transition: transform 0.2s ease;
        }
        .hero-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        .floating-animation {
            animation: float 3s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-10px);
            }
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header/Navbar -->
    <nav class="navbar sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-4">
                <h1 class="text-2xl font-bold text-indigo-600">Shopping Family</h1>
                <div class="hidden md:flex space-x-6">
                    <a href="#home" class="text-gray-700 hover:text-indigo-600 transition">Home</a>
                    <a href="#products" class="text-gray-700 hover:text-indigo-600 transition">Products</a>
                    <a href="#categories" class="text-gray-700 hover:text-indigo-600 transition">Categories</a>
                    <a href="#about" class="text-gray-700 hover:text-indigo-600 transition">About</a>
                    <a href="#contact" class="text-gray-700 hover:text-indigo-600 transition">Contact</a>
                </div>
            </div>
            <div class="flex items-center space-x-4">
                <button class="relative">
                    <i class="bi bi-cart3 text-2xl text-gray-700 hover:text-indigo-600"></i>
                    <span id="cart-count" class="absolute -top-2 -right-2 bg-red-500 text-white text-xs rounded-full h-5 w-5 flex items-center justify-center">0</span>
                </button>
                <button class="md:hidden">
                    <i class="bi bi-list text-2xl text-gray-700"></i>
                </button>
                <a href="https://github.com/yourusername/your-repo" class="text-gray-700 hover:text-black transition">
                    <i class="bi bi-github text-2xl"></i>
                <a>
                <p>© 2025 created Muflih projection
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-bg text-white py-20">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-4xl md:text-6xl font-bold mb-4 floating-animation">Welcome to Shopping family Tembagapura</h2>
            <p class="text-lg md:text-xl mb-8">Discover amazing products at unbeatable prices. Your modern shopping destination.</p>
            <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/29650c74-b33e-4279-8059-d56dcd09f34a.png" alt="Dynamic hero banner featuring happy diverse customers browsing a futuristic online store with neon-lit product displays, holographic interfaces, and seamless user experiences in a clean, modern digital marketplace" class="w-full h-64 md:h-96 object-cover rounded-lg shadow-lg mx-auto mb-8" onload="this.style.filter='brightness(1.1) contrast(1.2)'" onerror="this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/acc1f6af-2d30-4283-af81-15e395dc4998.png'">
            <button class="btn-primary bg-white text-indigo-600 px-8 py-4 rounded-full font-semibold hover:bg-gray-50 transition">Shop Now</button>
            <p class="mt-4 text-sm opacity-80">Proudly hosted on GitHub Pages</p>
        </div>
    </section>

    <!-- Categories Section -->
    <section id="categories" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Shop by Category</h2>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <div class="bg-gray-100 p-6 rounded-lg shadow-md text-center hover:shadow-lg transition cursor-pointer" onclick="filterProducts('electronics')">
                    <i class="bi bi-phone text-4xl text-indigo-600 mb-4"></i>
                    <h3 class="font-semibold text-lg">Electronics</h3>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/21d2dae2-5008-4ff7-9338-81f3780a2c2d.png" alt="Electronics category with latest smartphones, sleek laptops, and cutting-edge gadgets arranged artistically on a minimalist marble countertop in a bright tech showroom ambiance" class="w-full h-32 object-cover rounded mt-4" />
                </div>
                <div class="bg-gray-100 p-6 rounded-lg shadow-md text-center hover:shadow-lg transition cursor-pointer" onclick="filterProducts('home')">
                    <i class="bi bi-house-door text-4xl text-indigo-600 mb-4"></i>
                    <h3 class="font-semibold text-lg">Home & Stationary</h3>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/97766937-82e3-40fe-b869-e05571ce2012.png" alt="Home and Garden section displaying elegant indoor plants, ergonomic furniture, and outdoor decor items in a serene, sunlit living room with large windows and natural greenery" class="w-full h-32 object-cover rounded mt-4" />
                </div>
                <div class="bg-gray-100 p-6 rounded-lg shadow-md text-center hover:shadow-lg transition cursor-pointer" onclick="filterProducts('fashion')">
                    <i class="bi bi-bag text-4xl text-indigo-600 mb-4"></i>
                    <h3 class="font-semibold text-lg">Fashion</h3>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ae703ad1-38a6-4505-980c-52727d82f1c2.png" alt="Fashion category showcasing trendy apparel, stylish accessories, and footwear on professional mannequins in a high-end boutique with warm ambient lighting and full-length mirrors" class="w-full h-32 object-cover rounded mt-4" />
                </div>
                <div class="bg-gray-100 p-6 rounded-lg shadow-md text-center hover:shadow-lg transition cursor-pointer" onclick="filterProducts('sports')">
                    <i class="bi bi-bicycle text-4xl text-indigo-600 mb-4"></i>
                    <h3 class="font-semibold text-lg">Fresh</h3>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/c4524e66-5d72-4c8e-935c-e5681bbc277e.png" alt="Sports and fitness category with professional athletic equipment, colorful sportswear, and motivational posters in a vibrant gym environment with dynamic energy and confidence-boosting vibes" class="w-full h-32 object-cover rounded mt-4" />
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="py-16 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Featured Products</h2>
            <div id="product-grid" class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <!-- Product Cards -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="electronics">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7c727964-7d2a-4c51-a90b-80599651f2fe.png" alt="Premium wireless noise-cancelling headphones in matte black with memory foam ear cushions, ambient light indicators, and a sleek carrying case in a professional audio studio setup" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Wireless Headphones</h3>
                        <p class="text-gray-600 text-sm mb-2">Crystal clear audio with active noise cancellation</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="electronics">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/11f9c60e-0b20-437a-9ff8-a7da6b68cf86.png" alt="Elegant fitness smartwatch with OLED touchscreen, biometric sensors for heart rate and sleep tracking, and a premium silicone band displayed on a minimalist wooden table with morning sunlight" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Smart Watch Pro</h3>
                        <p class="text-gray-600 text-sm mb-2">Health monitoring and smart notifications</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="home">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/531492a9-7948-4e61-87a8-6cf63fbd6372.png" alt="Cozy throw blanket in soft knit fabric with geometric patterns, paired with decorative cushions on a comfortable armchair in a warmly lit living room with bookshelves in the background" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Luxury Throw Blanket</h3>
                        <p class="text-gray-600 text-sm mb-2">Ultra-soft and stylish home essential</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="fashion">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/88dd709e-a47d-4247-9896-ac1ad2cea999.png" alt="Stylish vegan leather jacket with zipper details and minimalist design, hung elegantly on a sleek hanger in a contemporary wardrobe with soft shadow play" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Leather Jacket</h3>
                        <p class="text-gray-600 text-sm mb-2">Timeless style with premium quality</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <!-- More Products -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="sports">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d267eed7-8a37-4497-97e9-686f8ac859a4.png" alt="High-performance running shoes with breathable mesh upper, responsive cushioning sole, and reflective elements, shown on a forest trail with morning mist and natural scenery" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Running Shoes</h3>
                        <p class="text-gray-600 text-sm mb-2">Comfortable and durable for athletes</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="electronics">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d5df9b94-2f26-4ada-904f-ba0e67053a40.png" alt="Compact wireless Bluetooth speaker with 360-degree sound projection, waterproof rating, and rechargeable battery, placed on a picnic blanket near a lake with lush greenery" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Portable Speaker</h3>
                        <p class="text-gray-600 text-sm mb-2">Immersive sound anywhere you go</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="home">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ab671a80-0fd2-43c8-89f0-f0b7bd434984.png" alt="Modern ceramic vase with minimalist lines and metallic gold accents, containing fresh white flowers on a sleek dining table with contemporary chairs and ambient lighting" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Ceramic Vase</h3>
                        <p class="text-gray-600 text-sm mb-2">Elegant home decor piece</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card" data-category="fashion">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/06383f0f-51ff-4522-93a2-e871c0834471.png" alt="Cozy wool scarf in earthy tones with fringe details, draped artistically over a vintage wooden chair in a cozy reading nook with books and warm lamp light" class="w-full h-48 object-cover" />
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-2">Wool Scarf</h3>
                        <p class="text-gray-600 text-sm mb-2">Warm and fashionable accessory</p>
                        <div class="flex items-center justify-between">
                            <span class="text-xl font-bold text-indigo-600">IDR 100.000</span>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition add-to-cart">Add to Cart</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <h2 class="text-3xl font-bold mb-6 text-gray-800">Why Choose Shopping Family?</h2>
                    <ul class="space-y-4">
                        <li class="flex items-center space-x-3">
                            <i class="bi bi-shield-check text-2xl text-green-600"></i>
                            <span class="text-gray-700">100% Secure Payment with SSL encryption</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i class="bi bi-truck text-2xl text-blue-600"></i>
                            <span class="text-gray-700">Free Shipping on Orders Over $100</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i class="bi bi-arrow-counterclockwise text-2xl text-purple-600"></i>
                            <span class="text-gray-700">30-Day Hassle-Free Return Policy</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i class="bi bi-headset text-2xl text-indigo-600"></i>
                            <span class="text-gray-700">24/7 Customer Support via Chat & Email</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i class="bi bi-git text-2xl text-gray-800"></i>
                            <span class="text-gray-700">Open Source on GitHub - Contribute & Customize</span>
                        </li>
                    </ul>
                </div>
                <div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/8aa47016-82f5-44cd-8192-4c56cc1c1b62.png" alt="Illustrative scene of satisfied customers engaging with an e-commerce platform, showing secure checkout processes, fast delivery icons, and continuous customer support chat bubbles in a digitally enhanced, colorful environment" class="w-full h-64 object-cover rounded-lg shadow-lg" />
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-gray-100">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-8 text-gray-800">Get in Touch</h2>
            <p class="text-gray-600 mb-8">Have questions? We're here to help! Reach out on our GitHub repository.</p>
            <a href="https://github.com/yourusername/your-repo" class="bg-gray-800 text-white px-6 py-3 rounded-full font-semibold hover:bg-gray-700 transition inline-flex items-center">
                <i class="bi bi-github mr-2"></i>
                View on GitHub
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-4 gap-8">
                <div>
                    <h3 class="font-semibold mb-4">Shopping Family</h3>
                    <p class="text-gray-300">Your one-stop shop for everything modern and stylish. Proudly open-source on GitHub.</p>
                </div>
                <div>
                    <h4 class="font-semibold mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-gray-300">
                        <li><a href="#" class="hover:text-white transition">About Us</a></li>
                        <li><a href="#" class="hover:text-white transition">Contact</a></li>
                        <li><a href="#" class="hover:text-white transition">Privacy Policy</a></li>
                        <li><a href="#" class="hover:text-white transition">Terms of Service</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-semibold mb-4">Customer Service</h4>
                    <ul class="space-y-2 text-gray-300">
                        <li><a href="#" class="hover:text-white transition">Help Center</a></li>
                        <li><a href="#" class="hover:text-white transition">Returns</a></li>
                        <li><a href="#" class="hover:text-white transition">Size Guide</a></li>
                        <li><a href="#" class="hover:text-white transition">Track Order</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-semibold mb-4">Connect</h4>
                    <div class="flex space-x-4">
                        <a href="#" class="hover:text-white transition"><i class="bi bi-facebook text-xl"></i></a>
                        <a href="#" class="hover:text-white transition"><i class="bi bi-twitter text-xl"></i></a>
                        <a href="#" class="hover:text-white transition"><i class="bi bi-instagram text-xl"></i></a>
                        <a href="#" class="hover:text-white transition"><i class="bi bi-youtube text-xl"></i></a>
                        <a href="https://github.com/yourusername/your-repo" class="hover:text-white transition"><i class="bi bi-github text-xl"></i></a>
                    </div>
                </div>
            </div>
            <div class="text-center mt-8 border-t border-gray-700 pt-8">
                <p>© 2025 created Muflih projection. | Made with <i class="bi bi-heart-fill text-red-500"></i> and hosted on GitHub Pages.</p>
            </div>
        </div>
    </footer>

    <script>
        // Cart functionality
        let cartCount = 0;
        const cartButtons = document.querySelectorAll('.add-to-cart');
        const cartCountElement = document.getElementById('cart-count');

        cartButtons.forEach(button => {
            button.addEventListener('click', () => {
                cartCount++;
                updateCartCount();
                // Animate button
                button.style.transform = 'scale(0.95)';
                setTimeout(() => button.style.transform = 'scale(1)', 150);
            });
        });

        function updateCartCount() {
            cartCountElement.textContent = cartCount;
            cartCountElement.style.animation = 'none';
            cartCountElement.offsetHeight; // Trigger reflow
            cartCountElement.style.animation = 'pulse 0.5s';
        }

        // Filter products (basic implementation)
        function filterProducts(category) {
            const products = document.querySelectorAll('.product-card');
            products.forEach(product => {
                if (category === 'all' || product.dataset.category === category) {
                    product.style.display = 'block';
                } else {
                    product.style.display = 'none';
                }
            });
        }

        // Smooth scrolling for nav links
        document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            });
        });

        // GitHub integration notice
        console.log('ShopHub - Modern E-Commerce Website connected to GitHub Pages!');
        console.log('Visit our repository: https://github.com/yourusername/your-repo');
    </script>
</body>
</html>
</content>
</create_file>

<attempt_completion>
