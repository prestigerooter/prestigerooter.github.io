<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prestige Rooter - Expert Plumbing Services Brooklyn | 24/7 Emergency</title>
  <meta name="description" content="Prestige Rooter - Brooklyn's trusted plumbing experts since 2005. 20,000+ satisfied customers. Emergency service, drain cleaning, water heaters, bathroom & kitchen plumbing. Licensed & insured.">
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lucide/0.263.1/umd/lucide.js"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
    
    * {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    }
    
    .service-card {
      position: relative;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      overflow: visible;
    }
    
    .service-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
      transition: left 0.5s ease;
      z-index: 1;
    }
    
    .service-card:hover::before {
      left: 100%;
    }
    
    .service-card:hover {
      transform: translateY(-8px) scale(1.02);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
      z-index: 10;
    }
    
    .service-details {
      position: absolute;
      background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%);
      padding: 1.5rem;
      border-radius: 16px;
      box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
      border: 1px solid #e5e7eb;
      opacity: 0;
      visibility: hidden;
      transform: translateY(20px);
      transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      z-index: 1000;
      width: 350px;
      left: 50%;
      margin-left: -175px;
      top: 100%;
      margin-top: 15px;
      pointer-events: none;
    }
    
    .service-card:hover .service-details {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }
    
    .service-details::before {
      content: '';
      position: absolute;
      top: -8px;
      left: 50%;
      transform: translateX(-50%);
      width: 0;
      height: 0;
      border-left: 8px solid transparent;
      border-right: 8px solid transparent;
      border-bottom: 8px solid white;
    }
    
    .floating-animation {
      animation: float 3s ease-in-out infinite;
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }
    
    .pulse-animation {
      animation: pulse 2s infinite;
    }
    
    .gradient-text {
      background: linear-gradient(135deg, #1e40af 0%, #3b82f6 50%, #60a5fa 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    
    .hero-bg {
      background: linear-gradient(135deg, #0f172a 0%, #1e293b 25%, #334155 50%, #475569 75%, #64748b 100%);
      position: relative;
      overflow: hidden;
    }
    
    .hero-bg::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="1"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>') repeat;
      opacity: 0.3;
    }
    
    .portfolio-container {
      display: flex;
      overflow-x: auto;
      scroll-behavior: smooth;
      gap: 1.5rem;
      padding: 1.5rem 0;
      scrollbar-width: thin;
      scrollbar-color: #cbd5e0 #f1f5f9;
    }
    
    .portfolio-container::-webkit-scrollbar {
      height: 10px;
    }
    
    .portfolio-container::-webkit-scrollbar-track {
      background: #f1f5f9;
      border-radius: 6px;
    }
    
    .portfolio-container::-webkit-scrollbar-thumb {
      background: linear-gradient(90deg, #3b82f6, #1e40af);
      border-radius: 6px;
    }
    
    .portfolio-slide {
      min-width: 320px;
      height: 240px;
      object-fit: cover;
      border-radius: 16px;
      transition: all 0.4s ease;
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
      border: 3px solid transparent;
    }
    
    .portfolio-slide:hover {
      transform: scale(1.05) rotate(1deg);
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
      border-color: #3b82f6;
    }
    
    .testimonials-container {
      display: flex;
      overflow-x: auto;
      scroll-behavior: smooth;
      gap: 2rem;
      padding: 1.5rem 0;
      scrollbar-width: thin;
      scrollbar-color: #cbd5e0 #f1f5f9;
    }
    
    .testimonial-card {
      min-width: 350px;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    
    .testimonial-card::before {
      content: '"';
      position: absolute;
      top: -10px;
      left: 20px;
      font-size: 6rem;
      color: rgba(59, 130, 246, 0.1);
      font-family: Georgia, serif;
      z-index: 0;
    }
    
    .testimonial-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
    }
    
    .stats-card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      transition: all 0.3s ease;
    }
    
    .stats-card:hover {
      background: rgba(255, 255, 255, 0.15);
      transform: translateY(-2px);
    }
    
    .mobile-menu {
      transform: translateX(-100%);
      transition: transform 0.3s ease;
    }
    
    .mobile-menu.active {
      transform: translateX(0);
    }
    
    .emergency-banner {
      background: linear-gradient(45deg, #dc2626, #ef4444);
      color: white;
      text-align: center;
      padding: 0.75rem;
      font-weight: 600;
      position: relative;
      overflow: hidden;
    }
    
    .emergency-banner::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
      animation: shine 3s infinite;
    }
    
    @keyframes shine {
      0% { left: -100%; }
      100% { left: 100%; }
    }
    
    .feature-icon {
      width: 3rem;
      height: 3rem;
      background: linear-gradient(135deg, #3b82f6, #1e40af);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 1.5rem;
      margin-bottom: 1rem;
      transition: all 0.3s ease;
    }
    
    .feature-card:hover .feature-icon {
      transform: rotate(10deg) scale(1.1);
      box-shadow: 0 8px 25px rgba(59, 130, 246, 0.3);
    }
    
    @media (max-width: 768px) {
      .service-details {
        position: static;
        opacity: 0;
        visibility: hidden;
        transform: none;
        margin: 1rem 0 0 0;
        width: auto;
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
      }
      
      .service-card.active .service-details {
        opacity: 1;
        visibility: visible;
      }
      
      .service-details::before {
        display: none;
      }
    }
    
    .section-divider {
      height: 1px;
      background: linear-gradient(90deg, transparent, #e5e7eb, transparent);
      margin: 2rem 0;
    }
    
    .cta-button {
      background: linear-gradient(135deg, #dc2626 0%, #ef4444 100%);
      color: white;
      border: none;
      padding: 1rem 2rem;
      border-radius: 12px;
      font-weight: 600;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(220, 38, 38, 0.4);
    }
    
    .cta-button:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 25px rgba(220, 38, 38, 0.6);
      background: linear-gradient(135deg, #b91c1c 0%, #dc2626 100%);
    }
    
    .nav-link {
      position: relative;
      transition: all 0.3s ease;
    }
    
    .nav-link::after {
      content: '';
      position: absolute;
      bottom: -4px;
      left: 0;
      width: 0;
      height: 2px;
      background: #fbbf24;
      transition: width 0.3s ease;
    }
    
    .nav-link:hover::after {
      width: 100%;
    }
  </style>
</head>
<body class="font-sans text-gray-800 bg-gray-50 antialiased" id="body">
  <!-- Emergency Banner -->
  <div class="emergency-banner">
    <div class="container mx-auto px-4">
      <p class="text-sm">🚨 <strong>EMERGENCY PLUMBING?</strong> Call Now: <a href="tel:347-276-3160" class="underline font-bold">347-276-3160</a> - Available 24/7!</p>
    </div>
  </div>

  <!-- Header -->
  <header class="bg-white shadow-lg sticky top-0 z-50 border-b border-gray-100">
    <div class="container mx-auto px-4 lg:px-6 py-4">
      <div class="flex items-center justify-between">
        <!-- Enhanced Logo -->
        <div class="flex items-center">
          <div class="relative">
            <img src="logo-transparent.png" alt="Prestige Rooter Logo" class="h-28 w-28 md:h-32 md:w-32 object-contain mr-4 floating-animation">
          </div>
          <div>
            <h1 class="text-2xl font-bold gradient-text">Prestige Rooter</h1>
            <p class="text-sm text-gray-600 font-medium">Professional Plumbing Since 2005</p>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden lg:flex space-x-8 items-center">
          <a href="#home" class="nav-link text-gray-700 hover:text-blue-600 font-medium transition-colors" data-en="Home" data-ru="Главная">Home</a>
          <a href="#about" class="nav-link text-gray-700 hover:text-blue-600 font-medium transition-colors" data-en="About" data-ru="О нас">About</a>
          <a href="#services" class="nav-link text-gray-700 hover:text-blue-600 font-medium transition-colors" data-en="Services" data-ru="Услуги">Services</a>
          <a href="#testimonials" class="nav-link text-gray-700 hover:text-blue-600 font-medium transition-colors" data-en="Testimonials" data-ru="Отзывы">Testimonials</a>
          <a href="#contact" class="nav-link text-gray-700 hover:text-blue-600 font-medium transition-colors" data-en="Contact" data-ru="Контакты">Contact</a>
          <button class="text-2xl hover:scale-110 transition-transform" onclick="toggleLanguage()">🇺🇸🇷🇺</button>
        </nav>

        <!-- Enhanced CTA Button -->
        <a href="#contact" class="hidden lg:block bg-gradient-to-r from-blue-600 to-blue-700 hover:from-blue-700 hover:to-blue-800 text-white px-6 py-3 rounded-lg transition-all font-semibold shadow-lg hover:shadow-xl hover:-translate-y-0.5" data-en="Get Free Quote" data-ru="Получить Расчет">
          <span class="mr-2">📋</span>Get Free Quote
        </a>

        <!-- Mobile Menu Button -->
        <button class="lg:hidden p-2 rounded-lg hover:bg-gray-100 transition-colors" onclick="toggleMobileMenu()">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </div>

      <!-- Enhanced Mobile Menu -->
      <div class="mobile-menu fixed top-0 left-0 w-full h-full bg-white z-50 lg:hidden">
        <div class="flex justify-between items-center p-4 border-b border-gray-200">
          <div class="flex items-center">
            <img src="logo-transparent.png" alt="Prestige Rooter" class="h-20 w-20 object-contain mr-3">
            <span class="text-xl font-bold gradient-text">Prestige Rooter</span>
          </div>
          <button onclick="closeMobileMenu()" class="p-2 rounded-lg hover:bg-gray-100">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>
        <nav class="flex flex-col p-4 space-y-4">
          <a href="#home" class="text-lg font-medium text-gray-700 hover:text-blue-600 py-2 border-b border-gray-100" onclick="closeMobileMenu()" data-en="Home" data-ru="Главная">🏠 Home</a>
          <a href="#about" class="text-lg font-medium text-gray-700 hover:text-blue-600 py-2 border-b border-gray-100" onclick="closeMobileMenu()" data-en="About" data-ru="О нас">👥 About</a>
          <a href="#services" class="text-lg font-medium text-gray-700 hover:text-blue-600 py-2 border-b border-gray-100" onclick="closeMobileMenu()" data-en="Services" data-ru="Услуги">🔧 Services</a>
          <a href="#testimonials" class="text-lg font-medium text-gray-700 hover:text-blue-600 py-2 border-b border-gray-100" onclick="closeMobileMenu()" data-en="Testimonials" data-ru="Отзывы">⭐ Testimonials</a>
          <a href="#contact" class="text-lg font-medium text-gray-700 hover:text-blue-600 py-2 border-b border-gray-100" onclick="closeMobileMenu()" data-en="Contact" data-ru="Контакты">📞 Contact</a>
          <button class="text-lg font-medium text-gray-700 hover:text-blue-600 py-2 text-left" onclick="toggleLanguage()">🌐 Language / Язык</button>
          <a href="tel:347-276-3160" class="cta-button text-center mt-4" onclick="closeMobileMenu()">
            <span class="mr-2">📞</span>Call Now: 347-276-3160
          </a>
        </nav>
      </div>
    </div>
  </header>

  <!-- Enhanced Hero Section -->
  <section id="home" class="hero-bg text-white py-20 lg:py-32 relative">
    <div class="container mx-auto px-4 text-center relative z-10">
      <div class="max-w-4xl mx-auto">
        <h1 class="text-4xl md:text-5xl lg:text-7xl font-bold mb-6 leading-tight" data-en="Brooklyn's Most Trusted Plumbing Experts" data-ru="Самые Надежные Сантехнические Эксперты Бруклина">
          Brooklyn's Most <span class="text-yellow-400">Trusted</span><br>
          Plumbing Experts
        </h1>
        <p class="text-xl md:text-2xl mb-8 text-gray-200 leading-relaxed" data-en="Family-owned since 2005 • 20,000+ satisfied customers • Emergency service available 24/7" data-ru="Семейный бизнес с 2005 года • 20 000+ довольных клиентов • Экстренные услуги 24/7">
          Family-owned since 2005 • 20,000+ satisfied customers • Emergency service available 24/7
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center mb-16">
          <a href="tel:347-276-3160" class="cta-button text-lg pulse-animation">
            <span class="mr-2">📞</span> Emergency: 347-276-3160
          </a>
          <a href="#contact" class="bg-white text-gray-900 px-8 py-4 rounded-lg font-semibold text-lg hover:bg-gray-100 transition-all shadow-lg hover:shadow-xl hover:-translate-y-0.5 inline-flex items-center">
            <span class="mr-2">📋</span> Get Free Estimate
          </a>
        </div>

        <!-- Enhanced Stats Cards -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-6 max-w-5xl mx-auto">
          <div class="stats-card p-6 rounded-xl text-center">
            <div class="feature-icon mx-auto">🚨</div>
            <h3 class="text-xl font-bold mb-2" data-en="24/7 Emergency" data-ru="Экстренная Служба 24/7">24/7 Emergency</h3>
            <p class="text-gray-200 text-sm" data-en="Always available when you need us" data-ru="Всегда доступны, когда мы нужны">Always available when you need us</p>
          </div>
          <div class="stats-card p-6 rounded-xl text-center">
            <div class="feature-icon mx-auto">👥</div>
            <h3 class="text-xl font-bold mb-2" data-en="20,000+ Customers" data-ru="20 000+ Клиентов">20,000+ Customers</h3>
            <p class="text-gray-200 text-sm" data-en="Trusted by Brooklyn families & businesses" data-ru="Доверяют семьи Бруклина">Trusted by Brooklyn families & businesses</p>
          </div>
          <div class="stats-card p-6 rounded-xl text-center">
            <div class="feature-icon mx-auto">🏆</div>
            <h3 class="text-xl font-bold mb-2" data-en="19+ Years Experience" data-ru="19+ Лет Опыта">19+ Years Experience</h3>
            <p class="text-gray-200 text-sm" data-en="Professional expertise guaranteed" data-ru="Профессиональный опыт гарантирован">Professional expertise guaranteed</p>
          </div>
          <div class="stats-card p-6 rounded-xl text-center">
            <div class="feature-icon mx-auto">✅</div>
            <h3 class="text-xl font-bold mb-2" data-en="Licensed & Insured" data-ru="Лицензированы и Застрахованы">Licensed & Insured</h3>
            <p class="text-gray-200 text-sm" data-en="Complete peace of mind" data-ru="Полное спокойствие">Complete peace of mind</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Enhanced About Section -->
  <section id="about" class="py-20 lg:py-32 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold mb-6 gradient-text" data-en="About Prestige Rooter" data-ru="О Prestige Rooter">About Prestige Rooter</h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto leading-relaxed" data-en="Your trusted plumbing partner in Brooklyn, Staten Island, and New Jersey" data-ru="Ваш надежный сантехнический партнер в Бруклине, Статен-Айленде и Нью-Джерси">Your trusted plumbing partner in Brooklyn, Staten Island, and New Jersey</p>
      </div>
      
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center max-w-7xl mx-auto">
        <div>
          <div class="prose prose-lg">
            <p class="text-lg leading-relaxed mb-6 text-gray-700" data-en="Since 2005, Prestige Rooter Inc. has been Brooklyn's premier family-owned plumbing company, proudly serving over 20,000 residential and commercial clients across Brooklyn, Staten Island, and parts of New Jersey." data-ru="С 2005 года Prestige Rooter Inc. является ведущей семейной сантехнической компанией Бруклина, с гордостью обслуживая более 20 000 жилых и коммерческих клиентов в Бруклине, Статен-Айленде и частях Нью-Джерси.">
              Since 2005, <strong>Prestige Rooter Inc.</strong> has been Brooklyn's premier family-owned plumbing company, proudly serving over <strong>20,000 residential and commercial clients</strong> across Brooklyn, Staten Island, and parts of New Jersey.
            </p>
            
            <p class="text-lg leading-relaxed mb-8 text-gray-700" data-en="Based in Sheepshead Bay, our team of certified technicians specializes in comprehensive plumbing solutions - from emergency repairs to complete system installations. We're committed to delivering honest, reliable service that exceeds expectations." data-ru="Расположенная в Шипсхед-Бей, наша команда сертифицированных технических специалистов специализируется на комплексных сантехнических решениях - от аварийных ремонтов до полных системных установок. Мы стремимся предоставлять честные, надежные услуги, которые превосходят ожидания.">
              Based in <strong>Sheepshead Bay</strong>, our team of certified technicians specializes in comprehensive plumbing solutions - from emergency repairs to complete system installations. We're committed to delivering honest, reliable service that exceeds expectations.
            </p>

            <!-- Enhanced Features Grid -->
            <div class="grid grid-cols-2 gap-6 mb-8">
              <div class="feature-card text-center p-6 bg-gradient-to-br from-blue-50 to-blue-100 rounded-xl">
                <div class="feature-icon mx-auto">📅</div>
                <p class="text-3xl font-bold text-blue-900 mb-1">19+</p>
                <p class="text-sm font-medium text-gray-600" data-en="Years of Excellence" data-ru="Лет Превосходства">Years of Excellence</p>
              </div>
              <div class="feature-card text-center p-6 bg-gradient-to-br from-green-50 to-green-100 rounded-xl">
                <div class="feature-icon mx-auto bg-gradient-to-br from-green-600 to-green-700">👨‍👩‍👧‍👦</div>
                <p class="text-3xl font-bold text-green-900 mb-1">20K+</p>
                <p class="text-sm font-medium text-gray-600" data-en="Happy Customers" data-ru="Довольных Семей">Happy Customers</p>
              </div>
            </div>

            <!-- Key Services Highlights -->
            <div class="bg-gradient-to-r from-gray-50 to-gray-100 p-6 rounded-xl">
              <h4 class="font-bold text-lg mb-4 text-gray-900">✨ Our Specialties:</h4>
              <div class="grid grid-cols-2 gap-2 text-sm">
                <div class="flex items-center"><span class="mr-2">🔧</span>Emergency Repairs</div>
                <div class="flex items-center"><span class="mr-2">🚿</span>Bathroom Renovations</div>
                <div class="flex items-center"><span class="mr-2">🔥</span>Water Heater Service</div>
                <div class="flex items-center"><span class="mr-2">🏢</span>Commercial Plumbing</div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="relative">
          <div class="relative overflow-hidden rounded-2xl shadow-2xl">
            <img src="photo1.jpg" alt="Prestige Rooter Professional Team" class="w-full h-[500px] object-cover">
            <div class="absolute inset-0 bg-gradient-to-t from-blue-900/40 to-transparent"></div>
            
            <!-- Floating Info Card -->
            <div class="absolute bottom-6 left-6 right-6 bg-white/95 backdrop-blur-sm p-6 rounded-xl shadow-lg">
              <div class="flex items-center justify-between">
                <div>
                  <h3 class="text-xl font-bold text-gray-900 mb-2" data-en="Our Promise" data-ru="Наше Обещание">Our Promise</h3>
                  <p class="text-gray-700 font-medium" data-en="Quality work, honest pricing, guaranteed satisfaction" data-ru="Качественная работа, честные цены, гарантированное удовлетворение">Quality work, honest pricing, guaranteed satisfaction</p>
                </div>
                <div class="text-4xl">🏆</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Enhanced Services Section -->
  <section id="services" class="bg-gray-50 py-20 lg:py-32">
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold mb-6 gradient-text" data-en="Complete Plumbing Services" data-ru="Полные Сантехнические Услуги">Complete Plumbing Services</h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto" data-en="Professional solutions for every plumbing need - residential and commercial" data-ru="Профессиональные решения для любых сантехнических потребностей - жилых и коммерческих">Professional solutions for every plumbing need - residential and commercial</p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8 max-w-7xl mx-auto" style="padding-bottom: 250px;">
        <!-- Emergency Plumbing -->
        <div class="service-card bg-gradient-to-br from-red-50 via-red-100 to-red-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-red-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🚨</div>
          <h3 class="text-xl font-bold mb-3 text-red-900" data-en="Emergency Plumbing" data-ru="Аварийная Сантехника">Emergency Plumbing</h3>
          <p class="text-sm text-red-700 font-medium mb-4" data-en="24/7 Emergency Response" data-ru="Экстренное Реагирование 24/7">24/7 Emergency Response</p>
          <div class="inline-flex items-center text-xs text-red-600 bg-red-100 px-3 py-1 rounded-full">
            <span class="w-2 h-2 bg-red-500 rounded-full mr-2 animate-pulse"></span>
            Available Now
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🚨 Emergency Services Include:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>24/7 Emergency Response</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Burst Pipe Repair & Replacement</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Overflowing Toilets & Sewage Backup</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Flood Response & Water Cleanup</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Emergency Leak Detection</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Gas Line Emergency Repairs</li>
            </ul>
            <div class="mt-4 p-3 bg-red-50 rounded-lg">
              <p class="text-xs text-red-700 font-semibold">⚡ Average Response Time: Under 1 Hour</p>
            </div>
          </div>
        </div>

        <!-- Drain & Sewer Services -->
        <div class="service-card bg-gradient-to-br from-blue-50 via-blue-100 to-blue-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-blue-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🚽</div>
          <h3 class="text-xl font-bold mb-3 text-blue-900" data-en="Drain & Sewer Services" data-ru="Услуги по Дренажу и Канализации">Drain & Sewer Services</h3>
          <p class="text-sm text-blue-700 font-medium mb-4" data-en="Complete drain cleaning solutions" data-ru="Комплексные решения для очистки дренажа">Complete drain cleaning solutions</p>
          <div class="inline-flex items-center text-xs text-blue-600 bg-blue-100 px-3 py-1 rounded-full">
            <span class="mr-1">🔧</span>Most Popular
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🚽 Drain & Sewer Solutions:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Professional Drain Cleaning</li>
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Sewer Line Cleaning & Repair</li>
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Complete Sewer Line Replacement</li>
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Hydro Jetting / High-Pressure Cleaning</li>
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Video Camera Pipe Inspections</li>
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Tree Root Intrusion Removal</li>
              <li class="flex items-start"><span class="mr-2 text-blue-500">•</span>Commercial Grease Trap Cleaning</li>
            </ul>
          </div>
        </div>

        <!-- Pipe Services -->
        <div class="service-card bg-gradient-to-br from-green-50 via-green-100 to-green-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-green-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🔧</div>
          <h3 class="text-xl font-bold mb-3 text-green-900" data-en="Pipe Services" data-ru="Услуги по Трубам">Pipe Services</h3>
          <p class="text-sm text-green-700 font-medium mb-4" data-en="Expert pipe repair & installation" data-ru="Экспертный ремонт и установка труб">Expert pipe repair & installation</p>
          <div class="inline-flex items-center text-xs text-green-600 bg-green-100 px-3 py-1 rounded-full">
            <span class="mr-1">⭐</span>Specialists
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🔧 Complete Pipe Solutions:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-green-500">•</span>Professional Pipe Cleaning & Maintenance</li>
              <li class="flex items-start"><span class="mr-2 text-green-500">•</span>Pipe Repair & Complete Repiping</li>
              <li class="flex items-start"><span class="mr-2 text-green-500">•</span>Frozen Pipe Thawing & Prevention</li>
              <li class="flex items-start"><span class="mr-2 text-green-500">•</span>Advanced Leak Detection & Sealing</li>
              <li class="flex items-start"><span class="mr-2 text-green-500">•</span>Trenchless Pipe Repair Technology</li>
              <li class="flex items-start"><span class="mr-2 text-green-500">•</span>Gas Line Installation & Repair</li>
            </ul>
          </div>
        </div>

        <!-- Bathroom Plumbing -->
        <div class="service-card bg-gradient-to-br from-purple-50 via-purple-100 to-purple-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-purple-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🚿</div>
          <h3 class="text-xl font-bold mb-3 text-purple-900" data-en="Bathroom Plumbing" data-ru="Сантехника для Ванной">Bathroom Plumbing</h3>
          <p class="text-sm text-purple-700 font-medium mb-4" data-en="Complete bathroom solutions" data-ru="Комплексные решения для ванной">Complete bathroom solutions</p>
          <div class="inline-flex items-center text-xs text-purple-600 bg-purple-100 px-3 py-1 rounded-full">
            <span class="mr-1">🏠</span>Residential
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🚿 Bathroom Services:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-purple-500">•</span>Toilet Repairs & Replacements</li>
              <li class="flex items-start"><span class="mr-2 text-purple-500">•</span>Faucet & Sink Installation</li>
              <li class="flex items-start"><span class="mr-2 text-purple-500">•</span>Shower & Bathtub Plumbing</li>
              <li class="flex items-start"><span class="mr-2 text-purple-500">•</span>Stubborn Clog Removal</li>
              <li class="flex items-start"><span class="mr-2 text-purple-500">•</span>Water Pressure Optimization</li>
              <li class="flex items-start"><span class="mr-2 text-purple-500">•</span>Complete Bathroom Renovation Plumbing</li>
            </ul>
          </div>
        </div>

        <!-- Kitchen Plumbing -->
        <div class="service-card bg-gradient-to-br from-yellow-50 via-yellow-100 to-yellow-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-yellow-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🍽️</div>
          <h3 class="text-xl font-bold mb-3 text-yellow-900" data-en="Kitchen Plumbing" data-ru="Сантехника для Кухни">Kitchen Plumbing</h3>
          <p class="text-sm text-yellow-700 font-medium mb-4" data-en="Kitchen installation & repair" data-ru="Установка и ремонт кухни">Kitchen installation & repair</p>
          <div class="inline-flex items-center text-xs text-yellow-600 bg-yellow-100 px-3 py-1 rounded-full">
            <span class="mr-1">👨‍🍳</span>Chef Approved
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🍽️ Kitchen Plumbing Services:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-yellow-500">•</span>Kitchen Sink & Faucet Installation</li>
              <li class="flex items-start"><span class="mr-2 text-yellow-500">•</span>Garbage Disposal Repair/Replacement</li>
              <li class="flex items-start"><span class="mr-2 text-yellow-500">•</span>Dishwasher Hookups & Connections</li>
              <li class="flex items-start"><span class="mr-2 text-yellow-500">•</span>Ice Maker Line Installation</li>
              <li class="flex items-start"><span class="mr-2 text-yellow-500">•</span>Instant Hot Water Dispenser Setup</li>
              <li class="flex items-start"><span class="mr-2 text-yellow-500">•</span>Grease Clog Removal & Prevention</li>
            </ul>
          </div>
        </div>

        <!-- Water Heater Services -->
        <div class="service-card bg-gradient-to-br from-orange-50 via-orange-100 to-orange-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-orange-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🌡️</div>
          <h3 class="text-xl font-bold mb-3 text-orange-900" data-en="Water Heater Services" data-ru="Услуги по Водонагревателям">Water Heater Services</h3>
          <p class="text-sm text-orange-700 font-medium mb-4" data-en="Tank & tankless specialists" data-ru="Специалисты по бакам и безбаковым">Tank & tankless specialists</p>
          <div class="inline-flex items-center text-xs text-orange-600 bg-orange-100 px-3 py-1 rounded-full">
            <span class="mr-1">🔥</span>Hot Water Experts
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🌡️ Water Heater Solutions:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-orange-500">•</span>Water Heater Installation (Tank & Tankless)</li>
              <li class="flex items-start"><span class="mr-2 text-orange-500">•</span>Emergency Water Heater Repairs</li>
              <li class="flex items-start"><span class="mr-2 text-orange-500">•</span>Preventive Maintenance Programs</li>
              <li class="flex items-start"><span class="mr-2 text-orange-500">•</span>Expansion Tank Installation</li>
              <li class="flex items-start"><span class="mr-2 text-orange-500">•</span>Hot Water Supply Troubleshooting</li>
            </ul>
            <div class="mt-4 p-3 bg-orange-50 rounded-lg">
              <p class="text-xs text-orange-700 font-semibold">💡 Energy Efficient Options Available</p>
            </div>
          </div>
        </div>

        <!-- Heating & Boiler Services -->
        <div class="service-card bg-gradient-to-br from-red-50 via-orange-100 to-red-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-red-200" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🔥</div>
          <h3 class="text-xl font-bold mb-3 text-red-900" data-en="Heating & Boiler Services" data-ru="Услуги по Отоплению и Котлам">Heating & Boiler Services</h3>
          <p class="text-sm text-red-700 font-medium mb-4" data-en="Heating system specialists" data-ru="Специалисты по отопительным системам">Heating system specialists</p>
          <div class="inline-flex items-center text-xs text-red-600 bg-red-100 px-3 py-1 rounded-full">
            <span class="mr-1">❄️</span>Winter Ready
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🔥 Heating & Boiler Services:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Boiler Installation & Replacement</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Boiler Repair & Annual Maintenance</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Radiant Floor Heating Installation</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Baseboard Heating Systems</li>
              <li class="flex items-start"><span class="mr-2 text-red-500">•</span>Smart Thermostat & Zone Control</li>
            </ul>
          </div>
        </div>

        <!-- Commercial Services -->
        <div class="service-card bg-gradient-to-br from-gray-50 via-gray-100 to-gray-200 p-6 rounded-2xl shadow-lg text-center cursor-pointer border border-gray-300" onclick="toggleServiceDetails(this)">
          <div class="text-4xl mb-4">🏢</div>
          <h3 class="text-xl font-bold mb-3 text-gray-900" data-en="Commercial Plumbing" data-ru="Коммерческая Сантехника">Commercial Plumbing</h3>
          <p class="text-sm text-gray-700 font-medium mb-4" data-en="Business & industrial solutions" data-ru="Решения для бизнеса и промышленности">Business & industrial solutions</p>
          <div class="inline-flex items-center text-xs text-gray-600 bg-gray-200 px-3 py-1 rounded-full">
            <span class="mr-1">💼</span>Business Solutions
          </div>
          <div class="service-details">
            <h4 class="font-bold text-gray-900 mb-3">🏢 Commercial Services:</h4>
            <ul class="text-left text-sm space-y-2 text-gray-700">
              <li class="flex items-start"><span class="mr-2 text-gray-500">•</span>Multi-Unit Building Plumbing</li>
              <li class="flex items-start"><span class="mr-2 text-gray-500">•</span>Restaurant & Retail Plumbing</li>
              <li class="flex items-start"><span class="mr-2 text-gray-500">•</span>Backflow Prevention & Testing</li>
              <li class="flex items-start"><span class="mr-2 text-gray-500">•</span>Water Main Installation & Repair</li>
              <li class="flex items-start"><span class="mr-2 text-gray-500">•</span>Industrial Drainage Systems</li>
              <li class="flex items-start"><span class="mr-2 text-gray-500">•</span>Maintenance Contracts Available</li>
            </ul>
          </div>
        </div>
      </div>


  <!-- Enhanced Portfolio Section -->
  <section id="portfolio" class="py-20 lg:py-32 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold mb-6 gradient-text" data-en="Our Work Gallery" data-ru="Галерея Наших Работ">Our Work Gallery</h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto" data-en="Take a look at some of our recent projects showcasing quality craftsmanship and attention to detail" data-ru="Взгляните на некоторые из наших недавних проектов, демонстрирующих качественное мастерство и внимание к деталям">Take a look at some of our recent projects showcasing quality craftsmanship and attention to detail</p>
      </div>
      
      <div class="portfolio-container">
        <img src="portfolio1.jpg" alt="Bathroom Renovation Project" class="portfolio-slide" title="Modern Bathroom Renovation - Brooklyn">
        <img src="portfolio2.jpg" alt="Kitchen Plumbing Installation" class="portfolio-slide" title="Complete Kitchen Plumbing - Staten Island">
        <img src="portfolio3.jpg" alt="Water Heater Installation" class="portfolio-slide" title="Tankless Water Heater Installation">
        <img src="portfolio4.jpg" alt="Emergency Pipe Repair" class="portfolio-slide" title="Emergency Pipe Repair - 24/7 Service">
        <img src="portfolio5.jpg" alt="Commercial Plumbing Project" class="portfolio-slide" title="Commercial Building Plumbing">
        <img src="portfolio6.jpg" alt="Sewer Line Replacement" class="portfolio-slide" title="Complete Sewer Line Replacement">
        <img src="portfolio7.jpg" alt="Boiler Installation" class="portfolio-slide" title="High-Efficiency Boiler Installation">
        <img src="portfolio8.jpg" alt="Drain Cleaning Service" class="portfolio-slide" title="Professional Drain Cleaning">
        <img src="portfolio9.jpg" alt="Bathroom Fixture Installation" class="portfolio-slide" title="Luxury Bathroom Fixtures">
        <img src="portfolio10.jpg" alt="Kitchen Sink Installation" class="portfolio-slide" title="Modern Kitchen Sink Setup">
        <img src="portfolio11.jpg" alt="Pipe Replacement Project" class="portfolio-slide" title="Whole House Repiping">
        <img src="portfolio12.jpg" alt="Gas Line Installation" class="portfolio-slide" title="Safe Gas Line Installation">
        <img src="portfolio13.jpg" alt="Water Filtration System" class="portfolio-slide" title="Home Water Filtration System">
        <img src="portfolio14.jpg" alt="Heating System Repair" class="portfolio-slide" title="Radiant Heating System">
        <img src="portfolio15.jpg" alt="Commercial Kitchen Plumbing" class="portfolio-slide" title="Restaurant Kitchen Plumbing">
      </div>
      
      <div class="text-center mt-12">
        <div class="inline-flex items-center bg-gradient-to-r from-blue-50 to-blue-100 px-6 py-3 rounded-full">
          <span class="text-2xl mr-3">📸</span>
          <span class="text-blue-800 font-semibold">Swipe to see more projects →</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Enhanced Testimonials Section -->
  <section id="testimonials" class="py-20 lg:py-32 bg-gradient-to-br from-blue-50 to-indigo-100">
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold mb-6 gradient-text" data-en="What Our Customers Say" data-ru="Что Говорят Наши Клиенты">What Our Customers Say</h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto" data-en="Real reviews from real customers who trust Prestige Rooter" data-ru="Настоящие отзывы от настоящих клиентов, которые доверяют Prestige Rooter">Real reviews from real customers who trust Prestige Rooter</p>
        <div class="flex justify-center items-center mt-6">
          <div class="flex text-yellow-500 text-2xl mr-3">⭐⭐⭐⭐⭐</div>
          <span class="text-lg font-semibold text-gray-700">4.9/5 Average Rating</span>
        </div>
      </div>
      
      <div class="testimonials-container">
        <div class="testimonial-card bg-white p-8 rounded-2xl shadow-lg">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-blue-600 to-blue-800 rounded-full flex items-center justify-center mr-4">
              <span class="text-white font-bold text-lg">IP</span>
            </div>
            <div>
              <p class="font-bold text-lg text-gray-900">Ivan Petrov</p>
              <p class="text-gray-600">Sheepshead Bay, Brooklyn</p>
              <div class="flex text-yellow-500 mt-1">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <p class="text-gray-700 leading-relaxed relative z-10">"The team at Prestige Rooter fixed a stubborn kitchen clog that had been bothering us for weeks. They arrived promptly, worked efficiently, and cleaned up perfectly. Saved my dinner party!"</p>
          <div class="mt-4 text-sm text-blue-600 font-medium">✅ Verified Customer • Kitchen Plumbing</div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-2xl shadow-lg">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-green-600 to-green-800 rounded-full flex items-center justify-center mr-4">
              <span class="text-white font-bold text-lg">OI</span>
            </div>
            <div>
              <p class="font-bold text-lg text-gray-900">Olga Ivanova</p>
              <p class="text-gray-600">Bay Ridge, Brooklyn</p>
              <div class="flex text-yellow-500 mt-1">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <p class="text-gray-700 leading-relaxed relative z-10">"A burst pipe flooded my basement at 2 AM. Prestige Rooter's emergency service was incredible - they were there within an hour and handled both the repair and cleanup. True lifesavers!"</p>
          <div class="mt-4 text-sm text-green-600 font-medium">✅ Verified Customer • Emergency Service</div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-2xl shadow-lg">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-purple-600 to-purple-800 rounded-full flex items-center justify-center mr-4">
              <span class="text-white font-bold text-lg">DS</span>
            </div>
            <div>
              <p class="font-bold text-lg text-gray-900">Dmitri Sokolov</p>
              <p class="text-gray-600">Brighton Beach, Brooklyn</p>
              <div class="flex text-yellow-500 mt-1">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <p class="text-gray-700 leading-relaxed relative z-10">"Professional installation of my new tankless water heater. The technician explained everything clearly and the work was completed faster than expected. Hot water back in no time!"</p>
          <div class="mt-4 text-sm text-purple-600 font-medium">✅ Verified Customer • Water Heater Service</div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-2xl shadow-lg">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-pink-600 to-pink-800 rounded-full flex items-center justify-center mr-4">
              <span class="text-white font-bold text-lg">TK</span>
            </div>
            <div>
              <p class="font-bold text-lg text-gray-900">Tatiana Kuznetsova</p>
              <p class="text-gray-600">Coney Island, Brooklyn</p>
              <div class="flex text-yellow-500 mt-1">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <p class="text-gray-700 leading-relaxed relative z-10">"Complete bathroom renovation plumbing was handled with precision and care. Every fixture works perfectly, and they stayed on schedule and budget. Highly recommend!"</p>
          <div class="mt-4 text-sm text-pink-600 font-medium">✅ Verified Customer • Bathroom Renovation</div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-2xl shadow-lg">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-red-600 to-red-800 rounded-full flex items-center justify-center mr-4">
              <span class="text-white font-bold text-lg">MG</span>
            </div>
            <div>
              <p class="font-bold text-lg text-gray-900">Maria Gonzalez</p>
              <p class="text-gray-600">Sunset Park, Brooklyn</p>
              <div class="flex text-yellow-500 mt-1">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <p class="text-gray-700 leading-relaxed relative z-10">"Major sewer backup on Sunday night - Prestige Rooter's 24/7 service cleared it completely by morning. Professional, courteous, and reasonably priced. What a relief!"</p>
          <div class="mt-4 text-sm text-red-600 font-medium">✅ Verified Customer • Sewer Service</div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-2xl shadow-lg">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-indigo-600 to-indigo-800 rounded-full flex items-center justify-center mr-4">
              <span class="text-white font-bold text-lg">JC</span>
            </div>
            <div>
              <p class="font-bold text-lg text-gray-900">John Carter</p>
              <p class="text-gray-600">Jersey City, NJ</p>
              <div class="flex text-yellow-500 mt-1">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <p class="text-gray-700 leading-relaxed relative z-10">"Burst pipe emergency at my business - Prestige Rooter's rapid response prevented major water damage and lost revenue. Professional service that goes above and beyond!"</p>
          <div class="mt-4 text-sm text-indigo-600 font-medium">✅ Verified Customer • Commercial Emergency</div>
        </div>
      </div>
      
      <!-- Team Photo -->
      <div class="mt-16 text-center">
        <div class="relative inline-block">
          <img src="photo2.jpg" alt="Prestige Rooter Team at Work" class="mx-auto w-full max-w-4xl h-80 object-cover rounded-2xl shadow-2xl">
          <div class="absolute inset-0 bg-gradient-to-t from-blue-900/30 to-transparent rounded-2xl"></div>
          <div class="absolute bottom-6 left-6 right-6 bg-white/95 backdrop-blur-sm p-6 rounded-xl shadow-lg">
            <h3 class="text-2xl font-bold text-gray-900 mb-2">🏆 Award-Winning Team</h3>
            <p class="text-gray-700">Our certified technicians bring decades of combined experience to every job</p>
          </div>
        </div>
      </div>
    </div>
  </section>

 <!-- Enhanced Contact Section -->
  <section id="contact" class="bg-gradient-to-br from-slate-800 via-slate-900 to-slate-800 text-white py-20 lg:py-32 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-10">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 25%, #3b82f6 0%, transparent 50%), radial-gradient(circle at 75% 75%, #1e40af 0%, transparent 50%);"></div>
    </div>
    
    <div class="container mx-auto px-4 relative z-10">
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold mb-6 text-white" data-en="Get In Touch Today" data-ru="Свяжитесь с нами Сегодня">Get In Touch Today</h2>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto" data-en="Ready to solve your plumbing problems? Contact Brooklyn's most trusted plumbing experts" data-ru="Готовы решить ваши сантехнические проблемы? Свяжитесь с самыми надежными сантехническими экспертами Бруклина">Ready to solve your plumbing problems? Contact Brooklyn's most trusted plumbing experts</p>
      </div>
      
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 max-w-7xl mx-auto">
        <!-- Contact Information -->
        <div>
          <div class="mb-12">
            <h3 class="text-3xl font-bold mb-8" data-en="Contact Information" data-ru="Контактная Информация">Contact Information</h3>
            
            <div class="space-y-8">
              <!-- Regular Phone -->
              <div class="flex items-start group">
                <div class="w-16 h-16 bg-gradient-to-br from-blue-500 to-blue-600 rounded-2xl flex items-center justify-center mr-6 group-hover:scale-110 transition-transform">
                  <span class="text-white text-2xl">📞</span>
                </div>
                <div>
                  <p class="font-bold text-xl mb-2 text-blue-400">Business Line</p>
                  <a href="tel:347-276-3160" class="text-xl font-bold text-white hover:text-blue-300 transition-colors">347-276-3160</a>
                  <p class="text-gray-400 mt-1">For appointments and general inquiries</p>
                </div>
              </div>

              <!-- Address -->
              <div class="flex items-start group">
                <div class="w-16 h-16 bg-gradient-to-br from-green-500 to-green-600 rounded-2xl flex items-center justify-center mr-6 group-hover:scale-110 transition-transform">
                  <span class="text-white text-2xl">📍</span>
                </div>
                <div>
                  <p class="font-bold text-xl mb-2 text-green-400">Service Address</p>
                  <p class="text-white text-lg" data-en="Brooklyn, NY 11223" data-ru="Бруклин, NY 11223">Brooklyn, NY 11223</p>
                  <p class="text-gray-400 mt-1">Sheepshead Bay area</p>
                </div>
              </div>

              <!-- Email -->
              <div class="flex items-start group">
                <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-purple-600 rounded-2xl flex items-center justify-center mr-6 group-hover:scale-110 transition-transform">
                  <span class="text-white text-2xl">✉️</span>
                </div>
                <div>
                  <p class="font-bold text-xl mb-2 text-purple-400">Email</p>
                  <a href="mailto:Prestigerooter@gmail.com" class="text-lg text-white hover:text-purple-300 transition-colors">Prestigerooter@gmail.com</a>
                  <p class="text-gray-400 mt-1">For quotes and project inquiries</p>
                </div>
              </div>

              <!-- Hours -->
              <div class="flex items-start group">
                <div class="w-16 h-16 bg-gradient-to-br from-yellow-500 to-orange-500 rounded-2xl flex items-center justify-center mr-6 group-hover:scale-110 transition-transform">
                  <span class="text-white text-2xl">🕒</span>
                </div>
                <div>
                  <p class="font-bold text-xl mb-2 text-yellow-400">Business Hours</p>
                  <div class="text-white">
                    <p data-en="Monday - Friday: 7:00 AM - 7:00 PM" data-ru="Понедельник - Пятница: 7:00-19:00">Monday - Friday: 7:00 AM - 7:00 PM</p>
                    <p data-en="Saturday: 8:00 AM - 6:00 PM" data-ru="Суббота: 8:00-18:00">Saturday: 8:00 AM - 6:00 PM</p>
                    <p data-en="Sunday: 8:00 AM - 6:00 PM" data-ru="Воскресенье: 8:00-18:00">Sunday: 8:00 AM - 6:00 PM</p>
                  </div>
                  <p class="text-red-300 font-semibold mt-2" data-en="⚡ Emergency Services Available 24/7" data-ru="⚡ Экстренные услуги доступны 24/7">⚡ Emergency Services Available 24/7</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Enhanced Contact Form -->
        <div>
          <div class="bg-white p-10 rounded-2xl shadow-2xl">
            <div class="text-center mb-8">
              <h3 class="text-3xl font-bold text-gray-900 mb-4" data-en="Request Your Free Quote" data-ru="Запросить Бесплатную Смету">Request Your Free Quote</h3>
              <p class="text-gray-600">Get a detailed estimate for your plumbing needs</p>
            </div>
            
            <form onsubmit="handleFormSubmit(event)" class="space-y-6">
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div>
                  <label for="name" class="block mb-2 font-semibold text-gray-700" data-en="Full Name *" data-ru="Полное Имя *">Full Name *</label>
                  <input type="text" id="name" required class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white" placeholder="John Smith">
                </div>
                <div>
                  <label for="phone" class="block mb-2 font-semibold text-gray-700" data-en="Phone Number *" data-ru="Номер Телефона *">Phone Number *</label>
                  <input type="tel" id="phone" required class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white" placeholder="(555) 123-4567">
                </div>
              </div>

              <div>
                <label for="email" class="block mb-2 font-semibold text-gray-700" data-en="Email Address" data-ru="Адрес Электронной Почты">Email Address</label>
                <input type="email" id="email" class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white" placeholder="john@email.com">
              </div>

              <div>
                <label for="service" class="block mb-2 font-semibold text-gray-700" data-en="Service Type" data-ru="Тип Услуги">Service Type</label>
                <select id="service" class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white">
                  <option value="">Select a service...</option>
                  <option value="emergency">🚨 Emergency Plumbing</option>
                  <option value="drain">🚽 Drain & Sewer Services</option>
                  <option value="water-heater">🌡️ Water Heater Services</option>
                  <option value="bathroom">🚿 Bathroom Plumbing</option>
                  <option value="kitchen">🍽️ Kitchen Plumbing</option>
                  <option value="heating">🔥 Heating & Boiler Services</option>
                  <option value="commercial">🏢 Commercial Services</option>
                  <option value="other">❓ Other / Not Sure</option>
                </select>
              </div>

              <div>
                <label for="urgency" class="block mb-2 font-semibold text-gray-700">Urgency Level</label>
                <select id="urgency" class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white">
                  <option value="">Select urgency...</option>
                  <option value="emergency">🚨 Emergency - Need help now!</option>
                  <option value="urgent">⚡ Urgent - Within 24 hours</option>
                  <option value="soon">📅 Soon - Within a few days</option>
                  <option value="planning">📋 Planning - Just getting quotes</option>
                </select>
              </div>

              <div>
                <label for="address" class="block mb-2 font-semibold text-gray-700">Service Address</label>
                <input type="text" id="address" class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white" placeholder="123 Main Street, Brooklyn, NY">
              </div>

              <div>
                <label for="message" class="block mb-2 font-semibold text-gray-700" data-en="Describe Your Plumbing Issue" data-ru="Опишите Вашу Сантехническую Проблему">Describe Your Plumbing Issue</label>
                <textarea id="message" class="w-full p-4 border border-gray-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all bg-gray-50 focus:bg-white" rows="5" placeholder="Please describe your plumbing issue in detail. Include any symptoms, when it started, and what you've already tried..."></textarea>
              </div>

              <button type="submit" class="w-full bg-gradient-to-r from-blue-600 to-blue-700 hover:from-blue-700 hover:to-blue-800 text-white px-8 py-4 rounded-xl font-bold text-lg transition-all shadow-lg hover:shadow-xl hover:-translate-y-1 flex items-center justify-center">
                <span class="mr-3">📧</span>
                <span data-en="Send My Request" data-ru="Отправить Мой Запрос">Send My Request</span>
              </button>
            </form>

            <!-- Response Time Promise -->
            <div class="mt-8 p-6 bg-gradient-to-r from-green-50 to-green-100 border border-green-200 rounded-xl">
              <div class="flex items-center justify-center mb-3">
                <div class="w-10 h-10 bg-green-500 rounded-full flex items-center justify-center mr-3">
                  <span class="text-white font-bold">✓</span>
                </div>
                <h4 class="font-bold text-green-800 text-lg">Our Response Promise</h4>
              </div>
              <div class="text-center text-green-700 space-y-2">
                <p><strong>Emergency Calls:</strong> Response within 1 hour</p>
                <p><strong>Regular Inquiries:</strong> Response within 2 hours during business hours</p>
                <p><strong>Free Estimates:</strong> Always provided upfront</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Enhanced Footer -->
  <footer class="bg-gray-900 text-white py-16">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-12">
        <!-- Company Info -->
        <div class="md:col-span-2">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-gradient-to-br from-blue-600 to-blue-800 rounded-2xl flex items-center justify-center mr-4">
              <img src="logo-transparent.png" alt="Prestige Rooter" class="w-10 h-10 object-contain">
            </div>
            <div>
              <h3 class="text-2xl font-bold">Prestige Rooter Inc.</h3>
              <p class="text-gray-400">Professional Plumbing Since 2005</p>
            </div>
          </div>
          <p class="text-gray-300 leading-relaxed mb-6">Brooklyn's most trusted family-owned plumbing company, proudly serving over 20,000 satisfied customers across Brooklyn, Staten Island, and New Jersey with reliable, professional plumbing services.</p>
          
          <!-- Certifications -->
          <div class="flex flex-wrap gap-4">
            <div class="bg-gray-800 px-4 py-2 rounded-lg text-sm font-medium">✅ Licensed & Insured</div>
        
            <div class="bg-gray-800 px-4 py-2 rounded-lg text-sm font-medium">⭐ 4.9/5 Rating</div>
          </div>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-xl font-bold mb-6">Quick Links</h4>
          <ul class="space-y-3">
            <li><a href="#home" class="text-gray-300 hover:text-white transition-colors flex items-center"><span class="mr-2">🏠</span>Home</a></li>
            <li><a href="#about" class="text-gray-300 hover:text-white transition-colors flex items-center"><span class="mr-2">👥</span>About Us</a></li>
            <li><a href="#services" class="text-gray-300 hover:text-white transition-colors flex items-center"><span class="mr-2">🔧</span>Services</a></li>
            <li><a href="#testimonials" class="text-gray-300 hover:text-white transition-colors flex items-center"><span class="mr-2">⭐</span>Reviews</a></li>
            <li><a href="#contact" class="text-gray-300 hover:text-white transition-colors flex items-center"><span class="mr-2">📞</span>Contact</a></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h4 class="text-xl font-bold mb-6">Contact Info</h4>
          <div class="space-y-4 text-sm">
            <div class="flex items-start">
              <span class="text-lg mr-3">📍</span>
              <div>
                
                <p class="text-gray-300">Brooklyn, NY 11223</p>
              </div>
            </div>
            <div class="flex items-center">
              <span class="text-lg mr-3">📞</span>
              <a href="tel:347-276-3160" class="text-blue-400 hover:text-blue-300 transition-colors font-bold">347-276-3160</a>
            </div>
            <div class="flex items-center">
              <span class="text-lg mr-3">✉️</span>
              <a href="mailto:Prestigerooter@gmail.com" class="text-blue-400 hover:text-blue-300 transition-colors">Prestigerooter@gmail.com</a>
            </div>
            <div class="flex items-start">
              <span class="text-lg mr-3">🕒</span>
              <div class="text-gray-300">
                <p>Mon-Fri: 7 AM - 7 PM</p>
                <p class="text-red-400 font-semibold">Emergency: 24/7</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="border-t border-gray-700 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <p class="text-gray-400 text-sm mb-4 md:mb-0">&copy; 2025 Prestige Rooter Inc. All rights reserved. Licensed & Insured Plumbing Contractor.</p>
          <div class="flex space-x-6 text-sm">
            <a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">Warranty</a>
            <button onclick="toggleLanguage()" class="text-gray-400 hover:text-white transition-colors">🌐 Language</button>
          </div>
        </div>
      </div>
    </div>
  </footer>

  <!-- Enhanced JavaScript -->
  <script>
    // Mobile menu functionality
    function toggleMobileMenu() {
      const mobileMenu = document.querySelector('.mobile-menu');
      mobileMenu.classList.toggle('active');
      document.body.style.overflow = mobileMenu.classList.contains('active') ? 'hidden' : 'auto';
    }

    function closeMobileMenu() {
      const mobileMenu = document.querySelector('.mobile-menu');
      mobileMenu.classList.remove('active');
      document.body.style.overflow = 'auto';
    }

    // Enhanced service details functionality
    function toggleServiceDetails(element) {
      if (window.innerWidth <= 768) {
        // Close other open service details
        const allServices = document.querySelectorAll('.service-card');
        allServices.forEach(service => {
          if (service !== element) {
            service.classList.remove('active');
          }
        });
        element.classList.toggle('active');
      }
    }

    // Service hover positioning for desktop
    document.querySelectorAll('.service-card').forEach(serviceCard => {
      serviceCard.addEventListener('mouseenter', function() {
        if (window.innerWidth > 768) {
          const serviceDetails = this.querySelector('.service-details');
          if (serviceDetails) {
            const rect = this.getBoundingClientRect();
            const windowWidth = window.innerWidth;
            const detailsWidth = 350;
            
            serviceDetails.style.left = '50%';
            serviceDetails.style.marginLeft = '-175px';
            
            // Adjust if would go off screen
            if (rect.left + detailsWidth/2 > windowWidth - 20) {
              serviceDetails.style.left = 'auto';
              serviceDetails.style.right = '0';
              serviceDetails.style.marginLeft = '0';
            } else if (rect.left - detailsWidth/2 < 20) {
              serviceDetails.style.left = '0';
              serviceDetails.style.marginLeft = '0';
            }
          }
        }
      });
    });

    // Smooth scrolling with header offset
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        const targetElement = document.getElementById(targetId);
        if (targetElement) {
          const headerHeight = document.querySelector('header').offsetHeight + 20;
          const targetPosition = targetElement.offsetTop - headerHeight;
          
          window.scrollTo({
            top: targetPosition,
            behavior: 'smooth'
          });
          
          // Close mobile menu if open
          closeMobileMenu();
        }
      });
    });

    // Enhanced form submission
    function handleFormSubmit(event) {
      event.preventDefault();
      
      const name = document.getElementById('name').value.trim();
      const phone = document.getElementById('phone').value.trim();
      const email = document.getElementById('email').value.trim();
      const service = document.getElementById('service').value;
      const urgency = document.getElementById('urgency').value;
      const address = document.getElementById('address').value.trim();
      const message = document.getElementById('message').value.trim();
      
      // Enhanced validation
      if (!name || !phone) {
        alert('Please fill in your name and phone number - these are required fields.');
        return;
      }
      
      if (phone.length < 10) {
        alert('Please enter a valid phone number.');
        return;
      }
      
      if (email && !email.includes('@')) {
        alert('Please enter a valid email address.');
        return;
      }
      
      // Simulate form submission
      const submitButton = event.target.querySelector('button[type="submit"]');
      const originalText = submitButton.innerHTML;
      submitButton.innerHTML = '<span class="mr-2">⏳</span>Sending Request...';
      submitButton.disabled = true;
      
      // Simulate API call
      setTimeout(() => {
        alert(`Thank you, ${name}! Your request has been submitted successfully. We will contact you at ${phone} within ${urgency === 'emergency' ? '1 hour' : '2 hours during business hours'}. For immediate emergencies, please call 347-276-3160.`);
        
        // Reset form
        event.target.reset();
        submitButton.innerHTML = originalText;
        submitButton.disabled = false;
      }, 2000);
    }

    // Language toggle functionality
    let currentLanguage = 'en';
    function toggleLanguage() {
      if (currentLanguage === 'en') {
        currentLanguage = 'ru';
        document.querySelectorAll('[data-ru]').forEach(element => {
          element.textContent = element.getAttribute('data-ru');
        });
        document.getElementById('body').setAttribute('lang', 'ru');
      } else {
        currentLanguage = 'en';
        document.querySelectorAll('[data-en]').forEach(element => {
          element.textContent = element.getAttribute('data-en');
        });
        document.getElementById('body').setAttribute('lang', 'en');
      }
    }

    // Click outside to close mobile menu
    document.addEventListener('click', function(event) {
      const mobileMenu = document.querySelector('.mobile-menu');
      const menuButton = document.querySelector('.mobile-menu button');
      
      if (mobileMenu.classList.contains('active') && 
          !mobileMenu.contains(event.target) && 
          !event.target.closest('.mobile-menu-button')) {
        closeMobileMenu();
      }
    });

    // Intersection Observer for scroll animations
    if ('IntersectionObserver' in window) {
      const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -50px 0px'
      };

      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
            entry.target.style.transform = 'translateY(0)';
          }
        });
      }, observerOptions);

      // Observe sections for animation
