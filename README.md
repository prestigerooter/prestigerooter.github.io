<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prestige Rooter - Trusted Plumbing Services in Brooklyn, NY</title>
  <meta name="description" content="Prestige Rooter, a family-owned plumbing company since 2005, offers reliable services to over 20,000 customers in Brooklyn, Staten Island, and New Jersey.">
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lucide/0.263.1/umd/lucide.js"></script>
  <style>
    .service-box {
      position: relative;
      transition: all 0.3s ease;
      z-index: 1;
    }
    .service-box:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
      z-index: 200;
    }
    .service-details {
      display: none;
      position: absolute;
      background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
      padding: 1rem;
      border-radius: 12px;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
      z-index: 1000;
      max-width: 320px;
      width: 320px;
      border: 1px solid #e2e8f0;
      pointer-events: none;
      left: 50%;
      transform: translateX(-50%);
      top: 100%;
      margin-top: 8px;
    }
    
    .service-box:hover .service-details {
      display: block;
      animation: fadeInUp 0.3s ease-out;
    }
    
    /* Check if popup would go off-screen and adjust position */
    .service-details.adjust-left {
      left: 0;
      transform: none;
    }
    
    .service-details.adjust-right {
      left: auto;
      right: 0;
      transform: none;
    }
    
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateX(-50%) translateY(10px);
      }
      to {
        opacity: 1;
        transform: translateX(-50%) translateY(0);
      }
    }
    
    .portfolio-container {
      display: flex;
      overflow-x: auto;
      scroll-behavior: smooth;
      padding: 1rem 0;
      scrollbar-width: thin;
      scrollbar-color: #cbd5e0 #f7fafc;
      gap: 1rem;
    }
    .portfolio-container::-webkit-scrollbar {
      height: 8px;
    }
    .portfolio-container::-webkit-scrollbar-track {
      background: #f7fafc;
      border-radius: 4px;
    }
    .portfolio-container::-webkit-scrollbar-thumb {
      background: #cbd5e0;
      border-radius: 4px;
    }
    .portfolio-container::-webkit-scrollbar-thumb:hover {
      background: #a0aec0;
    }
    .portfolio-slide {
      min-width: 280px;
      height: 200px;
      object-fit: cover;
      border-radius: 12px;
      transition: transform 0.3s ease;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }
    .portfolio-slide:hover {
      transform: scale(1.05);
    }
    .testimonials-container {
      display: flex;
      overflow-x: auto;
      scroll-behavior: smooth;
      gap: 1.5rem;
      padding: 1rem 0;
      scrollbar-width: thin;
      scrollbar-color: #cbd5e0 #f7fafc;
    }
    .testimonials-container::-webkit-scrollbar {
      height: 8px;
    }
    .testimonials-container::-webkit-scrollbar-track {
      background: #f7fafc;
      border-radius: 4px;
    }
    .testimonials-container::-webkit-scrollbar-thumb {
      background: #cbd5e0;
      border-radius: 4px;
    }
    .mobile-menu {
      display: none;
    }
    .mobile-menu.active {
      display: block;
    }
    .gradient-bg {
      background: linear-gradient(135deg, #1e3a8a 0%, #3b82f6 100%);
    }
    .hero-gradient {
      background: linear-gradient(135deg, #1e40af 0%, #3b82f6 50%, #60a5fa 100%);
    }
    @media (max-width: 768px) {
      .service-details {
        position: static;
        display: none;
        margin-top: 0.5rem;
        max-width: none;
        width: auto;
        transform: none;
        left: auto;
      }
      .service-box.active .service-details {
        display: block;
      }
      .desktop-nav {
        display: none;
      }
      .mobile-menu-button {
        display: block;
      }
    }
    @media (min-width: 769px) {
      .mobile-menu-button {
        display: none;
      }
    }
  </style>
</head>
<body class="font-sans text-gray-800 bg-gray-50" id="body">
  <!-- Header -->
  <header class="gradient-bg text-white sticky top-0 z-40 shadow-lg">
    <div class="container mx-auto px-4 lg:px-6 py-4">
      <div class="flex items-center justify-between">
        <!-- Logo -->
        <div class="flex items-center">
          <img src="logo-transparent.png" alt="Prestige Rooter Logo" class="h-16 mr-3">
          <div class="hidden sm:block">
            <h1 class="text-xl font-bold">Prestige Rooter</h1>
            <p class="text-sm opacity-90">Since 2005</p>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <nav class="desktop-nav hidden lg:flex space-x-6 items-center">
          <a href="#home" class="text-lg hover:text-yellow-300 transition-colors" data-en="Home" data-ru="Главная">Home</a>
          <a href="#about" class="text-lg hover:text-yellow-300 transition-colors" data-en="About" data-ru="О нас">About</a>
          <a href="#services" class="text-lg hover:text-yellow-300 transition-colors" data-en="Services" data-ru="Услуги">Services</a>
          <a href="#testimonials" class="text-lg hover:text-yellow-300 transition-colors" data-en="Testimonials" data-ru="Отзывы">Testimonials</a>
          <a href="#contact" class="text-lg hover:text-yellow-300 transition-colors" data-en="Contact" data-ru="Контакты">Contact</a>
          <button class="text-lg hover:text-yellow-300 transition-colors" onclick="toggleLanguage()">🇺🇸/🇷🇺</button>
        </nav>

        <!-- CTA Button (Desktop) -->
        <a href="#contact" class="hidden lg:block bg-yellow-500 text-blue-900 px-6 py-3 rounded-lg hover:bg-yellow-400 transition-colors font-semibold" data-en="Get Free Quote" data-ru="Получить Расчет">Get Free Quote</a>

        <!-- Mobile Menu Button -->
        <button class="mobile-menu-button lg:hidden" onclick="toggleMobileMenu()">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div class="mobile-menu lg:hidden mt-4 pb-4 border-t border-blue-800">
        <nav class="flex flex-col space-y-3 pt-4">
          <a href="#home" class="text-lg hover:text-yellow-300 transition-colors" onclick="closeMobileMenu()" data-en="Home" data-ru="Главная">Home</a>
          <a href="#about" class="text-lg hover:text-yellow-300 transition-colors" onclick="closeMobileMenu()" data-en="About" data-ru="О нас">About</a>
          <a href="#services" class="text-lg hover:text-yellow-300 transition-colors" onclick="closeMobileMenu()" data-en="Services" data-ru="Услуги">Services</a>
          <a href="#testimonials" class="text-lg hover:text-yellow-300 transition-colors" onclick="closeMobileMenu()" data-en="Testimonials" data-ru="Отзывы">Testimonials</a>
          <a href="#contact" class="text-lg hover:text-yellow-300 transition-colors" onclick="closeMobileMenu()" data-en="Contact" data-ru="Контакты">Contact</a>
          <button class="text-lg hover:text-yellow-300 transition-colors text-left" onclick="toggleLanguage()">🇺🇸/🇷🇺 Language</button>
          <a href="#contact" class="bg-yellow-500 text-blue-900 px-6 py-3 rounded-lg hover:bg-yellow-400 transition-colors font-semibold text-center mt-4" onclick="closeMobileMenu()" data-en="Get Free Quote" data-ru="Получить Расчет">Get Free Quote</a>
        </nav>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero-gradient text-white py-16 lg:py-24">
    <div class="container mx-auto px-4 text-center">
      <h1 class="text-3xl md:text-4xl lg:text-6xl font-bold mb-6 leading-tight" data-en="Trusted Plumbing Solutions Since 2005" data-ru="Надежные Сантехнические Решения с 2005">Trusted Plumbing Solutions Since 2005</h1>
      <p class="text-lg md:text-xl lg:text-2xl mb-8 max-w-4xl mx-auto leading-relaxed" data-en="Prestige Rooter, a family-owned and operated plumbing company, delivers reliable, high-quality services to Brooklyn, Staten Island, and New Jersey." data-ru="Prestige Rooter — семейная сантехническая компания, предлагающая надежные и качественные услуги в Бруклине, Статен-Айленде и Нью-Джерси.">Prestige Rooter, a family-owned and operated plumbing company, delivers reliable, high-quality services to Brooklyn, Staten Island, and New Jersey.</p>
      
      <div class="flex flex-col sm:flex-row gap-4 justify-center items-center mb-12">
        <a href="tel:347-276-3160" class="bg-red-600 hover:bg-red-700 text-white px-8 py-4 rounded-lg font-semibold text-lg transition-colors flex items-center">
          <span class="mr-2">📞</span> Call Now: 347-276-3160
        </a>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mx-auto">
        <div class="bg-white/10 backdrop-blur-sm p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-2" data-en="24/7 Emergency Service" data-ru="Экстренная Служба 24/7">24/7 Emergency Service</h3>
          <p data-en="Available when you need us most" data-ru="Доступны, когда мы нужны больше всего">Available when you need us most</p>
        </div>
        <div class="bg-white/10 backdrop-blur-sm p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-2" data-en="20,000+ Happy Customers" data-ru="20 000+ Довольных Клиентов">20,000+ Happy Customers</h3>
          <p data-en="Trusted by families & businesses" data-ru="Нам доверяют семьи и предприятия">Trusted by families & businesses</p>
        </div>
        <div class="bg-white/10 backdrop-blur-sm p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-2" data-en="Licensed & Insured" data-ru="Лицензированы и Застрахованы">Licensed & Insured</h3>
          <p data-en="Professional service guaranteed" data-ru="Профессиональные услуги гарантированы">Professional service guaranteed</p>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-16 lg:py-24">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl lg:text-4xl font-bold text-center mb-12" data-en="About Prestige Rooter" data-ru="О Prestige Rooter">About Prestige Rooter</h2>
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center max-w-6xl mx-auto">
        <div>
          <p class="text-lg leading-relaxed mb-6" data-en="Established in 2005, Prestige Rooter Inc. is a family-owned and operated plumbing company proudly serving Brooklyn, Staten Island, and parts of New Jersey. With over 20,000 satisfied residential and commercial clients, we've built a reputation for being the go-to team for reliable, honest, and top-quality plumbing services." data-ru="Основанная в 2005 году, Prestige Rooter Inc. — семейная сантехническая компания, с гордостью обслуживающая Бруклин, Статен-Айленд и части Нью-Джерси. С более чем 20 000 довольных клиентов, включая жилых и коммерческих, мы завоевали репутацию команды, которой доверяют за надежность, честность и высокое качество услуг.">Established in 2005, Prestige Rooter Inc. is a family-owned and operated plumbing company proudly serving Brooklyn, Staten Island, and parts of New Jersey. With over 20,000 satisfied residential and commercial clients, we've built a reputation for being the go-to team for reliable, honest, and top-quality plumbing services.</p>
          
          <p class="text-lg leading-relaxed mb-6" data-en="Based in Sheepshead Bay, our expert technicians specialize in everything from emergency drain cleaning and sewer line repairs to advanced camera inspections, water heater installations, radiant heating systems, and full-service plumbing solutions." data-ru="Расположенная в Шипсхед-Бей, наша команда опытных техников специализируется на всем: от экстренной очистки канализации и ремонта канализационных линий до передовых камерных осмотров, установки водонагревателей, систем радиаторного отопления и комплексных сантехнических решений.">Based in Sheepshead Bay, our expert technicians specialize in everything from emergency drain cleaning and sewer line repairs to advanced camera inspections, water heater installations, radiant heating systems, and full-service plumbing solutions.</p>

          <div class="grid grid-cols-2 gap-4 mb-6">
            <div class="text-center p-4 bg-blue-50 rounded-lg">
              <p class="text-2xl font-bold text-blue-900">19+</p>
              <p class="text-sm text-gray-600" data-en="Years Experience" data-ru="Лет Опыта">Years Experience</p>
            </div>
            <div class="text-center p-4 bg-blue-50 rounded-lg">
              <p class="text-2xl font-bold text-blue-900">20K+</p>
              <p class="text-sm text-gray-600" data-en="Happy Customers" data-ru="Довольных Клиентов">Happy Customers</p>
            </div>
          </div>
        </div>
        <div class="relative">
          <img src="photo1.jpg" alt="Prestige Rooter Team" class="w-full h-96 object-cover rounded-2xl shadow-lg">
          <div class="absolute inset-0 bg-gradient-to-t from-blue-900/20 to-transparent rounded-2xl"></div>
          <div class="absolute bottom-6 left-6 bg-white/90 backdrop-blur-sm p-4 rounded-lg">
            <h3 class="text-xl font-semibold mb-2" data-en="Our Mission" data-ru="Наша Миссия">Our Mission</h3>
            <p class="text-gray-700 text-sm" data-en="Getting the job done right the first time" data-ru="Выполнение работы правильно с первого раза">Getting the job done right the first time</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="bg-white py-16 lg:py-24 relative overflow-visible">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl lg:text-4xl font-bold text-center mb-12" data-en="Our Services" data-ru="Наши Услуги">Our Services</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 max-w-7xl mx-auto" style="padding-bottom: 200px;">
        <!-- Emergency Plumbing -->
        <div class="service-box bg-gradient-to-br from-red-50 to-red-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🚨</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Emergency Plumbing" data-ru="Аварийная Сантехника">Emergency Plumbing</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="24/7 Emergency Response" data-ru="Экстренное Реагирование 24/7">24/7 Emergency Response</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• 24/7 Emergency Response</li>
              <li>• Burst Pipe Repair</li>
              <li>• Overflowing Toilets</li>
              <li>• Flood Response & Cleanup</li>
              <li>• Emergency Leak Detection</li>
            </ul>
          </div>
        </div>

        <!-- Drain & Sewer Services -->
        <div class="service-box bg-gradient-to-br from-blue-50 to-blue-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🚽</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Drain & Sewer Services" data-ru="Услуги по Дренажу и Канализации">Drain & Sewer Services</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Complete drain solutions" data-ru="Комплексные решения для дренажа">Complete drain solutions</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Drain Cleaning</li>
              <li>• Sewer Line Cleaning</li>
              <li>• Sewer Line Repairs & Replacement</li>
              <li>• Hydro Jetting / High-Pressure Water Jet</li>
              <li>• Video Camera Pipe Inspections</li>
              <li>• Root Intrusion Removal</li>
              <li>• Grease Trap Cleaning (Commercial)</li>
            </ul>
          </div>
        </div>

        <!-- Pipe Services -->
        <div class="service-box bg-gradient-to-br from-green-50 to-green-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🔧</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Pipe Services" data-ru="Услуги по Трубам">Pipe Services</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Expert pipe solutions" data-ru="Экспертные решения для труб">Expert pipe solutions</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Pipe Cleaning & Maintenance</li>
              <li>• Pipe Repair & Repiping</li>
              <li>• Frozen Pipe Thawing</li>
              <li>• Leak Detection & Sealing</li>
              <li>• Trenchless Pipe Repair</li>
              <li>• Gas Line Installation & Repair</li>
            </ul>
          </div>
        </div>

        <!-- Bathroom Plumbing -->
        <div class="service-box bg-gradient-to-br from-purple-50 to-purple-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🚿</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Bathroom Plumbing" data-ru="Сантехника для Ванной">Bathroom Plumbing</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Complete bathroom solutions" data-ru="Комплексные решения для ванной">Complete bathroom solutions</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Toilet Repairs & Replacements</li>
              <li>• Faucet & Sink Installation</li>
              <li>• Shower & Bathtub Plumbing</li>
              <li>• Clog Removal</li>
              <li>• Water Pressure Fixes</li>
              <li>• Bathroom Renovation Plumbing</li>
            </ul>
          </div>
        </div>

        <!-- Kitchen Plumbing -->
        <div class="service-box bg-gradient-to-br from-yellow-50 to-yellow-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🍽️</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Kitchen Plumbing" data-ru="Сантехника для Кухни">Kitchen Plumbing</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Kitchen installation & repair" data-ru="Установка и ремонт кухни">Kitchen installation & repair</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Sink & Faucet Installation</li>
              <li>• Garbage Disposal Repair/Replacement</li>
              <li>• Dishwasher Hookups</li>
              <li>• Ice Maker Line Installation</li>
              <li>• Instant Hot Water Dispenser Installation</li>
              <li>• Grease Clog Removal</li>
            </ul>
          </div>
        </div>

        <!-- Water Heater Services -->
        <div class="service-box bg-gradient-to-br from-orange-50 to-orange-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🌡️</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Water Heater Services" data-ru="Услуги по Водонагревателям">Water Heater Services</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Tank & tankless solutions" data-ru="Решения с баком и без бака">Tank & tankless solutions</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Water Heater Installation (Tank & Tankless)</li>
              <li>• Water Heater Repairs</li>
              <li>• Water Heater Maintenance</li>
              <li>• Expansion Tank Installation</li>
              <li>• Hot Water Supply Troubleshooting</li>
            </ul>
          </div>
        </div>

        <!-- Heating & Boiler Services -->
        <div class="service-box bg-gradient-to-br from-red-50 to-orange-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🔥</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Heating & Boiler Services" data-ru="Услуги по Отоплению и Котлам">Heating & Boiler Services</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Heating system experts" data-ru="Эксперты по отопительным системам">Heating system experts</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Boiler Installation & Replacement</li>
              <li>• Boiler Repair & Maintenance</li>
              <li>• Radiant Floor Heating Installation</li>
              <li>• Baseboard Heating Systems</li>
              <li>• Thermostat & Zone Control Installations</li>
            </ul>
          </div>
        </div>

        <!-- Commercial Plumbing Services -->
        <div class="service-box bg-gradient-to-br from-gray-50 to-gray-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🏢</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Commercial Plumbing Services" data-ru="Коммерческие Сантехнические Услуги">Commercial Plumbing Services</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Business & industrial solutions" data-ru="Решения для бизнеса и промышленности">Business & industrial solutions</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Plumbing for Multi-Unit Buildings</li>
              <li>• Restaurant & Retail Plumbing</li>
              <li>• Backflow Prevention & Testing</li>
              <li>• Water Main Installation</li>
              <li>• Industrial Drainage Systems</li>
              <li>• Maintenance Contracts</li>
            </ul>
          </div>
        </div>

        <!-- Filtration & Water Quality -->
        <div class="service-box bg-gradient-to-br from-cyan-50 to-cyan-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">💧</div>
          <h3 class="text-lg font-semibold mb-2" data-en="Filtration & Water Quality" data-ru="Фильтрация и Качество Воды">Filtration & Water Quality</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Clean water solutions" data-ru="Решения для чистой воды">Clean water solutions</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• Water Filtration Systems</li>
              <li>• Water Softener Installations</li>
              <li>• Lead Pipe Replacement</li>
              <li>• Reverse Osmosis Systems</li>
            </ul>
          </div>
        </div>

        <!-- General Installation & Plumbing Renovations -->
        <div class="service-box bg-gradient-to-br from-teal-50 to-teal-100 p-6 rounded-xl shadow-md text-center relative cursor-pointer" onclick="toggleServiceDetails(this)">
          <div class="text-3xl mb-3">🏠</div>
          <h3 class="text-lg font-semibold mb-2" data-en="General Installation & Plumbing Renovations" data-ru="Общие Установки и Реконструкции Сантехники">General Installation & Plumbing Renovations</h3>
          <p class="text-sm text-gray-600 mb-2" data-en="Complete renovation services" data-ru="Полные услуги реконструкции">Complete renovation services</p>
          <div class="service-details">
            <ul class="text-left text-sm space-y-1">
              <li>• New Construction Plumbing</li>
              <li>• Whole-Home Repiping</li>
              <li>• Plumbing Inspections (Pre-Purchase)</li>
              <li>• Permitting & Code Compliance</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section id="portfolio" class="py-16 lg:py-24 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl lg:text-4xl font-bold text-center mb-8" data-en="Our Portfolio" data-ru="Наш Портфель">Our Portfolio</h2>
      <p class="text-center text-lg mb-12 max-w-3xl mx-auto text-gray-600" data-en="Explore some completed residential/commercial projects showcasing our quality and expertise." data-ru="Изучите подборку наших завершенных проектов, демонстрирующих качество и профессионализм Prestige Rooter. Посмотрите примеры нашей работы, от ремонта в жилых домах до коммерческих установок.">Explore some of our completed residential/commercial projects showcasing Prestige Rooter's quality and expertise.</p>
      <div class="portfolio-container">
        <img src="portfolio1.jpg" alt="Portfolio 1" class="portfolio-slide">
        <img src="portfolio2.jpg" alt="Portfolio 2" class="portfolio-slide">
        <img src="portfolio3.jpg" alt="Portfolio 3" class="portfolio-slide">
        <img src="portfolio4.jpg" alt="Portfolio 4" class="portfolio-slide">
        <img src="portfolio5.jpg" alt="Portfolio 5" class="portfolio-slide">
        <img src="portfolio6.jpg" alt="Portfolio 6" class="portfolio-slide">
        <img src="portfolio7.jpg" alt="Portfolio 7" class="portfolio-slide">
        <img src="portfolio8.jpg" alt="Portfolio 8" class="portfolio-slide">
        <img src="portfolio9.jpg" alt="Portfolio 9" class="portfolio-slide">
        <img src="portfolio10.jpg" alt="Portfolio 10" class="portfolio-slide">
        <img src="portfolio11.jpg" alt="Portfolio 11" class="portfolio-slide">
        <img src="portfolio12.jpg" alt="Portfolio 12" class="portfolio-slide">
        <img src="portfolio13.jpg" alt="Portfolio 13" class="portfolio-slide">
        <img src="portfolio14.jpg" alt="Portfolio 14" class="portfolio-slide">
        <img src="portfolio15.jpg" alt="Portfolio 15" class="portfolio-slide">
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials" class="py-16 lg:py-24 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl lg:text-4xl font-bold text-center mb-12" data-en="What Our Customers Say" data-ru="Что Говорят Наши Клиенты">What Our Customers Say</h2>
      <div class="testimonials-container">
        <div class="bg-gradient-to-br from-blue-50 to-blue-100 p-6 rounded-xl shadow-md min-w-[300px] lg:min-w-[350px]">
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-blue-900 rounded-full flex items-center justify-center mr-3">
              <span class="text-white font-bold">IP</span>
            </div>
            <div>
              <p class="font-semibold">Ivan Petrov</p>
              <p class="text-sm text-gray-600">Brooklyn, NY</p>
            </div>
          </div>
          <div class="flex text-yellow-500 mb-3">
            <span>⭐⭐⭐⭐⭐</span>
          </div>
          <p class="italic text-gray-700">"The team at Prestige Rooter fixed a stubborn kitchen clog in under an hour—saved my dinner party!"</p>
        </div>

        <div class="bg-gradient-to-br from-green-50 to-green-100 p-6 rounded-xl shadow-md min-w-[300px] lg:min-w-[350px]">
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-green-900 rounded-full flex items-center justify-center mr-3">
              <span class="text-white font-bold">OI</span>
            </div>
            <div>
              <p class="font-semibold">Olga Ivanova</p>
              <p class="text-sm text-gray-600">Brooklyn, NY</p>
            </div>
          </div>
          <div class="flex text-yellow-500 mb-3">
            <span>⭐⭐⭐⭐⭐</span>
          </div>
          <p class="italic text-gray-700">"A burst pipe flooded my basement, but Prestige Rooter's quick cleanup and repair were a lifesaver."</p>
        </div>

        <div class="bg-gradient-to-br from-purple-50 to-purple-100 p-6 rounded-xl shadow-md min-w-[300px] lg:min-w-[350px]">
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-purple-900 rounded-full flex items-center justify-center mr-3">
              <span class="text-white font-bold">DS</span>
            </div>
            <div>
              <p class="font-semibold">Dmitri Sokolov</p>
              <p class="text-sm text-gray-600">Brooklyn, NY</p>
            </div>
          </div>
          <div class="flex text-yellow-500 mb-3">
            <span>⭐⭐⭐⭐⭐</span>
          </div>
          <p class="italic text-gray-700">"The installation of my new water heater was seamless—hot water back in no time!"</p>
        </div>

        <div class="bg-gradient-to-br from-pink-50 to-pink-100 p-6 rounded-xl shadow-md min-w-[300px] lg:min-w-[350px]">
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-pink-900 rounded-full flex items-center justify-center mr-3">
              <span class="text-white font-bold">TK</span>
            </div>
            <div>
              <p class="font-semibold">Tatiana Kuznetsova</p>
              <p class="text-sm text-gray-600">Brooklyn, NY</p>
            </div>
          </div>
          <div class="flex text-yellow-500 mb-3">
            <span>⭐⭐⭐⭐⭐</span>
          </div>
          <p class="italic text-gray-700">"My bathroom renovation plumbing was handled with precision—everything works perfectly now."</p>
        </div>

        <div class="bg-gradient-to-br from-red-50 to-red-100 p-6 rounded-xl shadow-md min-w-[300px] lg:min-w-[350px]">
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-red-900 rounded-full flex items-center justify-center mr-3">
              <span class="text-white font-bold">MG</span>
            </div>
            <div>
              <p class="font-semibold">Maria Gonzalez</p>
              <p class="text-sm text-gray-600">Brooklyn, NY</p>
            </div>
          </div>
          <div class="flex text-yellow-500 mb-3">
            <span>⭐⭐⭐⭐⭐</span>
          </div>
          <p class="italic text-gray-700">"The 24/7 emergency service cleared a major sewer backup overnight—relief at last!"</p>
        </div>

        <div class="bg-gradient-to-br from-indigo-50 to-indigo-100 p-6 rounded-xl shadow-md min-w-[300px] lg:min-w-[350px]">
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-indigo-900 rounded-full flex items-center justify-center mr-3">
              <span class="text-white font-bold">JC</span>
            </div>
            <div>
              <p class="font-semibold">John Carter</p>
              <p class="text-sm text-gray-600">New Jersey</p>
            </div>
          </div>
          <div class="flex text-yellow-500 mb-3">
            <span>⭐⭐⭐⭐⭐</span>
          </div>
          <p class="italic text-gray-700">"The rapid response to my burst pipe prevented major water damage—highly impressed!"</p>
        </div>
      </div>
      <div class="mt-12 text-center">
        <img src="photo2.jpg" alt="Prestige Rooter Team at Work" class="mx-auto w-full max-w-2xl h-64 object-cover rounded-2xl shadow-lg">
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="gradient-bg text-white py-16 lg:py-24">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl lg:text-4xl font-bold text-center mb-12" data-en="Contact Us" data-ru="Свяжитесь с нами">Contact Us</h2>
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 max-w-6xl mx-auto">
        <div>
          <h3 class="text-2xl font-bold mb-6" data-en="Get in Touch" data-ru="Свяжитесь с нами">Get in Touch</h3>
          
          <div class="space-y-6">
            <div class="flex items-center">
              <div class="w-12 h-12 bg-yellow-500 rounded-full flex items-center justify-center mr-4">
                <span class="text-blue-900 text-xl">📍</span>
              </div>
              <div>
                <p class="font-semibold">Address</p>
                <p data-en="24 Manhattan Court, Brooklyn, NY 11223" data-ru="24 Манхэттен Корт, Бруклин, NY 11223">24 Manhattan Court, Brooklyn, NY 11223</p>
              </div>
            </div>

            <div class="flex items-center">
              <div class="w-12 h-12 bg-yellow-500 rounded-full flex items-center justify-center mr-4">
                <span class="text-blue-900 text-xl">📞</span>
              </div>
              <div>
                <p class="font-semibold">Phone</p>
                <a href="tel:347-276-3160" class="text-yellow-300 hover:text-yellow-200 text-lg">347-276-3160</a>
              </div>
            </div>

            <div class="flex items-center">
              <div class="w-12 h-12 bg-yellow-500 rounded-full flex items-center justify-center mr-4">
                <span class="text-blue-900 text-xl">✉️</span>
              </div>
              <div>
                <p class="font-semibold">Email</p>
                <a href="mailto:Prestigerooter@gmail.com" class="text-yellow-300 hover:text-yellow-200">Prestigerooter@gmail.com</a>
              </div>
            </div>

            <div class="flex items-center">
              <div class="w-12 h-12 bg-yellow-500 rounded-full flex items-center justify-center mr-4">
                <span class="text-blue-900 text-xl">🕒</span>
              </div>
              <div>
                <p class="font-semibold">Hours</p>
                <p data-en="Mon-Fri: 7 AM - 7 PM" data-ru="Пн-Пт: 7:00-19:00">Mon-Fri: 7 AM - 7 PM</p>
                <p class="text-sm text-yellow-200" data-en="Emergency Services Available 24/7" data-ru="Экстренные услуги доступны 24/7">Emergency Services Available 24/7</p>
              </div>
            </div>
          </div>

          <div class="mt-8 p-6 bg-white/10 backdrop-blur-sm rounded-xl">
            <h4 class="text-xl font-semibold mb-4" data-en="Service Areas" data-ru="Районы Обслуживания">Service Areas</h4>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 text-sm">
              <div>
                <p class="font-semibold mb-2">Brooklyn</p>
                <ul class="space-y-1 text-gray-300">
                  <li>Sheepshead Bay</li>
                  <li>Brighton Beach</li>
                  <li>Coney Island</li>
                  <li>Bay Ridge</li>
                </ul>
              </div>
              <div>
                <p class="font-semibold mb-2">Staten Island</p>
                <ul class="space-y-1 text-gray-300">
                  <li>New Springville</li>
                  <li>Eltingville</li>
                  <li>Tottenville</li>
                  <li>Richmond</li>
                </ul>
              </div>
              <div>
                <p class="font-semibold mb-2">New Jersey</p>
                <ul class="space-y-1 text-gray-300">
                  <li>Bayonne</li>
                  <li>Jersey City</li>
                  <li>Hoboken</li>
                  <li>Union City</li>
                </ul>
              </div>
            </div>
          </div>
        </div>

        <div>
          <div class="bg-white text-gray-800 p-8 rounded-xl shadow-lg">
            <h3 class="text-2xl font-semibold mb-6 text-center" data-en="Request a Quote" data-ru="Запросить Расчет">Request a Quote</h3>
            <form onsubmit="handleFormSubmit(event)" class="space-y-4">
              <div>
                <label for="name" class="block mb-2 font-medium" data-en="Full Name *" data-ru="Полное Имя *">Full Name *</label>
                <input type="text" id="name" required class="w-full p-3 border border-gray-300 rounded-lg focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-colors" placeholder="John Smith">
              </div>

              <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div>
                  <label for="phone" class="block mb-2 font-medium" data-en="Phone *" data-ru="Телефон *">Phone *</label>
                  <input type="tel" id="phone" required class="w-full p-3 border border-gray-300 rounded-lg focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-colors" placeholder="(555) 123-4567">
                </div>
                <div>
                  <label for="email" class="block mb-2 font-medium" data-en="Email" data-ru="Эл. почта">Email</label>
                  <input type="email" id="email" class="w-full p-3 border border-gray-300 rounded-lg focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-colors" placeholder="john@email.com">
                </div>
              </div>

              <div>
                <label for="service" class="block mb-2 font-medium" data-en="Service Needed" data-ru="Необходимая Услуга">Service Needed</label>
                <select id="service" class="w-full p-3 border border-gray-300 rounded-lg focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-colors">
                  <option value="">Select a service...</option>
                  <option value="emergency">Emergency Plumbing</option>
                  <option value="drain">Drain & Sewer Services</option>
                  <option value="water-heater">Water Heater Services</option>
                  <option value="bathroom">Bathroom Plumbing</option>
                  <option value="kitchen">Kitchen Plumbing</option>
                  <option value="heating">Heating & Boiler Services</option>
                  <option value="commercial">Commercial Services</option>
                  <option value="other">Other</option>
                </select>
              </div>

              <div>
                <label for="message" class="block mb-2 font-medium" data-en="Describe Your Issue" data-ru="Опишите Вашу Проблему">Describe Your Issue</label>
                <textarea id="message" class="w-full p-3 border border-gray-300 rounded-lg focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-colors" rows="4" placeholder="Please describe the plumbing issue you're experiencing..."></textarea>
              </div>

              <button type="submit" class="w-full bg-blue-900 hover:bg-blue-800 text-white px-6 py-4 rounded-lg font-semibold text-lg transition-colors flex items-center justify-center">
                <span class="mr-2">📧</span>
                <span data-en="Send Request" data-ru="Отправить Запрос">Send Request</span>
              </button>
            </form>

            <div class="mt-6 p-4 bg-green-50 border border-green-200 rounded-lg">
              <p class="text-green-800 text-sm text-center">
                <span class="font-semibold">🕒 Quick Response:</span> We typically respond within 1 hour during business hours!
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-900 text-white py-12">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
        <div>
          <div class="flex items-center mb-4">
            <div class="w-12 h-12 bg-blue-600 rounded-full flex items-center justify-center mr-3">
              <img src="logo-transparent.png" alt="Prestige Rooter" class="w-8 h-8 object-contain">
            </div>
            <div>
              <h3 class="text-xl font-bold">Prestige Rooter Inc.</h3>
              <p class="text-sm text-gray-400">Since 2005</p>
            </div>
          </div>
          <p class="text-gray-300 text-sm leading-relaxed">Your trusted family-owned plumbing company serving Brooklyn, Staten Island, and New Jersey with reliable, professional services.</p>
        </div>

        <div>
          <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
          <ul class="space-y-2 text-sm">
            <li><a href="#home" class="text-gray-300 hover:text-white transition-colors">Home</a></li>
            <li><a href="#about" class="text-gray-300 hover:text-white transition-colors">About Us</a></li>
            <li><a href="#services" class="text-gray-300 hover:text-white transition-colors">Services</a></li>
            <li><a href="#testimonials" class="text-gray-300 hover:text-white transition-colors">Testimonials</a></li>
            <li><a href="#contact" class="text-gray-300 hover:text-white transition-colors">Contact</a></li>
          </ul>
        </div>

        <div>
          <h4 class="text-lg font-semibold mb-4">Services</h4>
          <ul class="space-y-2 text-sm">
            <li><span class="text-gray-300">Emergency Plumbing</span></li>
            <li><span class="text-gray-300">Drain Cleaning</span></li>
            <li><span class="text-gray-300">Water Heaters</span></li>
            <li><span class="text-gray-300">Bathroom Plumbing</span></li>
            <li><span class="text-gray-300">Commercial Services</span></li>
          </ul>
        </div>

        <div>
          <h4 class="text-lg font-semibold mb-4">Contact Info</h4>
          <div class="space-y-2 text-sm">
            <p class="text-gray-300">📍 24 Manhattan Court<br>Brooklyn, NY 11223</p>
            <p class="text-gray-300">📞 <a href="tel:347-276-3160" class="hover:text-white transition-colors">347-276-3160</a></p>
            <p class="text-gray-300">✉️ <a href="mailto:Prestigerooter@gmail.com" class="hover:text-white transition-colors">Prestigerooter@gmail.com</a></p>
          </div>
        </div>
      </div>

      <div class="border-t border-gray-700 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <p class="text-gray-400 text-sm">&copy; 2025 Prestige Rooter Inc. All rights reserved.</p>
          <div class="flex space-x-6 mt-4 md:mt-0">
            <a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">Licensed & Insured</a>
          </div>
        </div>
      </div>
    </div>
  </footer>

  <script>
    // Mobile menu toggle
    function toggleMobileMenu() {
      const mobileMenu = document.querySelector('.mobile-menu');
      mobileMenu.classList.toggle('active');
    }

    function closeMobileMenu() {
      const mobileMenu = document.querySelector('.mobile-menu');
      mobileMenu.classList.remove('active');
    }

    // Service hover functionality - simplified and fixed
    document.querySelectorAll('.service-box').forEach(serviceBox => {
      serviceBox.addEventListener('mouseenter', function(e) {
        const serviceDetails = this.querySelector('.service-details');
        if (serviceDetails && window.innerWidth > 768) {
          // Check if popup would go off screen and adjust position
          const rect = this.getBoundingClientRect();
          const popupWidth = 320;
          const windowWidth = window.innerWidth;
          
          serviceDetails.classList.remove('adjust-left', 'adjust-right');
          
          // If popup would go off right edge
          if (rect.left + popupWidth/2 > windowWidth - 20) {
            serviceDetails.classList.add('adjust-right');
          }
          // If popup would go off left edge  
          else if (rect.left - popupWidth/2 < 20) {
            serviceDetails.classList.add('adjust-left');
          }
        }
      });
    });

    function toggleServiceDetails(element) {
      if (window.innerWidth <= 768) {
        element.classList.toggle('active');
        // Close other open service details
        const allServices = document.querySelectorAll('.service-box');
        allServices.forEach(service => {
          if (service !== element) {
            service.classList.remove('active');
          }
        });
      }
    }

    // Smooth scrolling for navigation
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        const targetElement = document.getElementById(targetId);
        if (targetElement) {
          const headerHeight = document.querySelector('header').offsetHeight;
          const targetPosition = targetElement.offsetTop - headerHeight - 20;
          
          window.scrollTo({
            top: targetPosition,
            behavior: 'smooth'
          });
        }
      });
    });

    // Form submission
    function handleFormSubmit(event) {
      event.preventDefault();
      
      const name = document.getElementById('name').value;
      const phone = document.getElementById('phone').value;
      const email = document.getElementById('email').value;
      const service = document.getElementById('service').value;
      const message = document.getElementById('message').value;
      
      // Simple validation
      if (!name || !phone) {
        alert('Please fill in all required fields (Name and Phone).');
        return;
      }
      
      // Here you would typically send the data to your server
      alert('Thank you for your request! We will contact you within 1 hour during business hours.');
      
      // Reset form
      event.target.reset();
    }

    // Language toggle function
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

    // Close mobile menu when clicking outside
    document.addEventListener('click', function(event) {
      const mobileMenu = document.querySelector('.mobile-menu');
      const menuButton = document.querySelector('.mobile-menu-button');
      
      if (!mobileMenu.contains(event.target) && !menuButton.contains(event.target)) {
        mobileMenu.classList.remove('active');
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

      // Observe elements for animation
      document.querySelectorAll('section').forEach(section => {
        section.style.opacity = '0';
        section.style.transform = 'translateY(30px)';
        section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
        observer.observe(section);
      });
    }
  </script>
</body>
</html>
