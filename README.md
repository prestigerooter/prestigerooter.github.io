<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prestige Rooter - Trusted Plumbing Services in Brooklyn, NY</title>
  <meta name="description" content="Prestige Rooter, a family-owned plumbing company since 2005, offers reliable services to over 20,000 customers in Brooklyn, Staten Island, and New Jersey.">
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .service-box:hover {
      background-color: #e5e7eb;
      transform: scale(1.05);
      transition: all 0.3s ease;
      z-index: 20;
    }
    .service-box:hover .service-details {
      display: block;
    }
    .service-details {
      display: none;
      position: absolute;
      background-color: #f9fafb;
      padding: 6px;
      border-radius: 5px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      z-index: 30;
      max-width: 350px;
      top: 100%;
      left: 50%;
      transform: translateX(-50%);
      min-height: 200px;
    }
    .service-box {
      position: relative;
      overflow: visible;
    }
    .portfolio-slide {
      min-width: 300px;
      height: 200px;
      object-fit: cover;
      margin-right: 10px;
      border-radius: 8px;
    }
    .portfolio-container {
      display: flex;
      overflow-x: auto;
      scroll-behavior: smooth;
      padding: 10px 0;
      scrollbar-width: none; /* Firefox */
    }
    .portfolio-container::-webkit-scrollbar {
      display: none; /* Chrome, Safari, Edge */
    }
  </style>
</head>
<body class="font-sans text-gray-800 bg-gray-100" id="body">
  <!-- Header -->
  <header class="bg-blue-900 text-white sticky top-0 z-10">
    <div class="container mx-auto px-6 py-4 flex items-center justify-between">
      <div class="flex items-center">
        <img src="logo-transparent.png" alt="Prestige Rooter Logo" class="h-20 mr-4">
      </div>
      <nav class="flex space-x-6 items-center">
        <a href="#home" class="text-2xl px-4 hover:text-yellow-300" data-en="Home" data-ru="Главная">Home</a>|<a href="#about" class="text-2xl px-4 hover:text-yellow-300" data-en="About" data-ru="О нас">About</a>|<a href="#services" class="text-2xl px-4 hover:text-yellow-300" data-en="Services" data-ru="Услуги">Services</a>|<a href="#testimonials" class="text-2xl px-4 hover:text-yellow-300" data-en="Testimonials" data-ru="Отзывы">Testimonials</a>|<a href="#contact" class="text-2xl px-4 hover:text-yellow-300" data-en="Contact" data-ru="Контакты">Contact</a>
        <button class="text-2xl px-4 hover:text-yellow-300" onclick="toggleLanguage()">🇺🇸/🇷🇺</button>
      </nav>
      <a href="#contact" class="bg-yellow-500 text-blue-900 px-4 py-3 rounded hover:bg-yellow-400 text-base" data-en="Request a Quote" data-ru="Связаться">Request a Quote</a>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="home" class="bg-blue-800 text-white py-20">
    <div class="container mx-auto px-4 text-center">
      <h1 class="text-4xl md:text-5xl font-bold mb-4" data-en="Trusted Plumbing Solutions Since 2005" data-ru="Надежные Сантехнические Решения с 2005">Trusted Plumbing Solutions Since 2005</h1>
      <p class="text-lg md:text-xl mb-6" data-en="Prestige Rooter, a family-owned and operated plumbing company, delivers reliable, high-quality services to Brooklyn, Staten Island, and New Jersey." data-ru="Prestige Rooter — семейная сантехническая компания, предлагающая надежные и качественные услуги в Бруклине, Статен-Айленде и Нью-Джерси.">Prestige Rooter, a family-owned and operated plumbing company, delivers reliable, high-quality services to Brooklyn, Staten Island, and New Jersey.</p>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-16">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8" data-en="About Prestige Rooter" data-ru="О Prestige Rooter">About Prestige Rooter</h2>
      <p class="text-lg text-center max-w-3xl mx-auto mb-4" data-en="Established in 2005, Prestige Rooter Inc. is a family-owned and operated plumbing company proudly serving Brooklyn, Staten Island, and parts of New Jersey. With over 20,000 satisfied residential and commercial clients, we’ve built a reputation for being the go-to team for reliable, honest, and top-quality plumbing services. Based in Sheepshead Bay, our expert technicians specialize in everything from emergency drain cleaning and sewer line repairs to advanced camera inspections, water heater installations, radiant heating systems, and full-service plumbing solutions. At Prestige Rooter, we believe in getting the job done right the first time—backed by decades of craftsmanship, integrity, and a commitment to treating your home or business like our own. Whether you're dealing with a leak, a clog, or planning a full renovation, we're here to deliver fast, clean, and lasting results you can trust." data-ru="Основанная в 2005 году, Prestige Rooter Inc. — семейная сантехническая компания, с гордостью обслуживающая Бруклин, Статен-Айленд и части Нью-Джерси. С более чем 20 000 довольных клиентов, включая жилых и коммерческих, мы завоевали репутацию команды, которой доверяют за надежность, честность и высокое качество услуг. Расположенная в Шипсхед-Бей, наша команда опытных техников специализируется на всем: от экстренной очистки канализации и ремонта канализационных линий до передовых камерных осмотров, установки водонагревателей, систем радиаторного отопления и комплексных сантехнических решений. В Prestige Rooter мы верим в выполнение работы правильно с первого раза — это поддерживается десятилетиями мастерства, честности и стремления относиться к вашему дому или бизнесу как к своему. Независимо от того, сталкиваетесь ли вы с протечкой, засором или планируете полную реконструкцию, мы здесь, чтобы обеспечить быстрые, чистые и долговечные результаты, которым можно доверять.">Established in 2005, Prestige Rooter Inc. is a family-owned and operated plumbing company proudly serving Brooklyn, Staten Island, and parts of New Jersey. With over 20,000 satisfied residential and commercial clients, we’ve built a reputation for being the go-to team for reliable, honest, and top-quality plumbing services. Based in Sheepshead Bay, our expert technicians specialize in everything from emergency drain cleaning and sewer line repairs to advanced camera inspections, water heater installations, radiant heating systems, and full-service plumbing solutions. At Prestige Rooter, we believe in getting the job done right the first time—backed by decades of craftsmanship, integrity, and a commitment to treating your home or business like our own. Whether you're dealing with a leak, a clog, or planning a full renovation, we're here to deliver fast, clean, and lasting results you can trust.</p>
      <img src="photo1.jpg" alt="Prestige Rooter Team" class="mx-auto mt-4 w-full max-w-[50%] h-auto object-cover rounded-lg shadow-md">
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="bg-white py-16">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8" data-en="Our Services" data-ru="Наши Услуги">Our Services</h2>
      <div class="grid grid-cols-4 gap-4 justify-center">
        <!-- Emergency Plumbing -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🚨 Emergency Plumbing" data-ru="🚨 Аварийная Сантехника">🚨 Emergency Plumbing</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>24/7 Emergency Response</li>
              <li>Burst Pipe Repair</li>
              <li>Overflowing Toilets</li>
              <li>Flood Response & Cleanup</li>
              <li>Emergency Leak Detection</li>
            </ul>
          </div>
        </div>
        <!-- Drain & Sewer Services -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🚽 Drain & Sewer Services" data-ru="🚽 Услуги по Дренажу и Канализации">🚽 Drain & Sewer Services</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Drain Cleaning</li>
              <li>Sewer Line Cleaning</li>
              <li>Sewer Line Repairs & Replacement</li>
              <li>Sewer Backup & Overflow Solutions</li>
              <li>Hydro Jetting / High-Pressure Water Jet</li>
              <li>Video Camera Pipe Inspections</li>
              <li>Root Intrusion Removal</li>
              <li>Grease Trap Cleaning (Commercial)</li>
            </ul>
          </div>
        </div>
        <!-- Pipe Services -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🔧 Pipe Services" data-ru="🔧 Услуги по Трубам">🔧 Pipe Services</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Pipe Cleaning & Maintenance</li>
              <li>Pipe Repair & Repiping</li>
              <li>Frozen Pipe Thawing</li>
              <li>Leak Detection & Sealing</li>
              <li>Trenchless Pipe Repair</li>
              <li>Gas Line Installation & Repair</li>
            </ul>
          </div>
        </div>
        <!-- Bathroom Plumbing -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🚿 Bathroom Plumbing" data-ru="🚿 Сантехника для Ванной">🚿 Bathroom Plumbing</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Toilet Repairs & Replacements</li>
              <li>Faucet & Sink Installation</li>
              <li>Shower & Bathtub Plumbing</li>
              <li>Clog Removal</li>
              <li>Water Pressure Fixes</li>
              <li>Bathroom Renovation Plumbing</li>
            </ul>
          </div>
        </div>
        <!-- Kitchen Plumbing -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🍽️ Kitchen Plumbing" data-ru="🍽️ Сантехника для Кухни">🍽️ Kitchen Plumbing</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Sink & Faucet Installation</li>
              <li>Garbage Disposal Repair/Replacement</li>
              <li>Dishwasher Hookups</li>
              <li>Ice Maker Line Installation</li>
              <li>Instant Hot Water Dispenser Installation</li>
              <li>Grease Clog Removal</li>
            </ul>
          </div>
        </div>
        <!-- Water Heater Services -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🌡️ Water Heater Services" data-ru="🌡️ Услуги по Водонагревателям">🌡️ Water Heater Services</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Water Heater Installation (Tank & Tankless)</li>
              <li>Water Heater Repairs</li>
              <li>Water Heater Maintenance</li>
              <li>Expansion Tank Installation</li>
              <li>Hot Water Supply Troubleshooting</li>
            </ul>
          </div>
        </div>
        <!-- Heating & Boiler Services -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🔥 Heating & Boiler Services" data-ru="🔥 Услуги по Отоплению и Котлам">🔥 Heating & Boiler Services</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Boiler Installation & Replacement</li>
              <li>Boiler Repair & Maintenance</li>
              <li>Radiant Floor Heating Installation</li>
              <li>Baseboard Heating Systems</li>
              <li>Thermostat & Zone Control Installations</li>
            </ul>
          </div>
        </div>
        <!-- Commercial Plumbing Services -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🏢 Commercial Plumbing Services" data-ru="🏢 Коммерческие Сантехнические Услуги">🏢 Commercial Plumbing Services</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Plumbing for Multi-Unit Buildings</li>
              <li>Restaurant & Retail Plumbing</li>
              <li>Backflow Prevention & Testing</li>
              <li>Water Main Installation</li>
              <li>Industrial Drainage Systems</li>
              <li>Maintenance Contracts</li>
            </ul>
          </div>
        </div>
        <!-- Filtration & Water Quality -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="💧 Filtration & Water Quality" data-ru="💧 Фильтрация и Качество Воды">💧 Filtration & Water Quality</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>Water Filtration Systems</li>
              <li>Water Softener Installations</li>
              <li>Lead Pipe Replacement</li>
              <li>Reverse Osmosis Systems</li>
            </ul>
          </div>
        </div>
        <!-- General Installation & Plumbing Renovations -->
        <div class="service-box bg-gray-200 p-4 rounded-lg shadow-md text-center relative">
          <h3 class="text-lg font-semibold" data-en="🏠 General Installation & Plumbing Renovations" data-ru="🏠 Общие Установки и Реконструкции Сантехники">🏠 General Installation & Plumbing Renovations</h3>
          <div class="service-details text-base p-6">
            <ul class="list-disc pl-4">
              <li>New Construction Plumbing</li>
              <li>Whole-Home Repiping</li>
              <li>Plumbing Inspections (Pre-Purchase)</li>
              <li>Permitting & Code Compliance</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section id="portfolio" class="py-16 bg-gray-100">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8" data-en="Our Portfolio" data-ru="Наш Портфель">Our Portfolio</h2>
      <p class="text-center text-lg mb-6 max-w-2xl mx-auto" data-en="Explore a selection of our completed projects showcasing the quality and expertise of Prestige Rooter. Swipe or scroll horizontally to view all 15 examples of our work, from residential repairs to commercial installations." data-ru="Изучите подборку наших завершенных проектов, демонстрирующих качество и профессионализм Prestige Rooter. Прокрутите или проведите пальцем влево, чтобы увидеть все 15 примеров нашей работы, от ремонта в жилых домах до коммерческих установок.">Explore a selection of our completed projects showcasing the quality and expertise of Prestige Rooter. Swipe or scroll horizontally to view all 15 examples of our work, from residential repairs to commercial installations.</p>
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
  <section id="testimonials" class="py-16">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8" data-en="What Our Customers Say" data-ru="Что Говорят Наши Клиенты">What Our Customers Say</h2>
      <div class="flex overflow-x-auto space-x-6 pb-4 scrollbar-hide">
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"The team at Prestige Rooter fixed a stubborn kitchen clog in under an hour—saved my dinner party!"</p>
          <p class="mt-4 font-semibold">- Ivan Petrov, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"A burst pipe flooded my basement, but Prestige Rooter’s quick cleanup and repair were a lifesaver."</p>
          <p class="mt-4 font-semibold">- Olga Ivanova, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"The installation of my new water heater was seamless—hot water back in no time!"</p>
          <p class="mt-4 font-semibold">- Dmitri Sokolov, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"My bathroom renovation plumbing was handled with precision—everything works perfectly now."</p>
          <p class="mt-4 font-semibold">- Tatiana Kuznetsova, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"The 24/7 emergency service cleared a major sewer backup overnight—relief at last!"</p>
          <p class="mt-4 font-semibold">- Maria Gonzalez, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"A thorough drain cleaning restored my old pipes—impressive attention to detail."</p>
          <p class="mt-4 font-semibold">- Alexei Romanov, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"The weekend sewer line repair was a game-changer for my flooded basement."</p>
          <p class="mt-4 font-semibold">- Sergei Volkov, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"My water filtration system now delivers crystal-clear water—excellent work!"</p>
          <p class="mt-4 font-semibold">- Elena Smirnova, Brooklyn</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md min-w-[300px]">
          <p class="italic">"The rapid response to my burst pipe prevented major water damage—highly impressed!"</p>
          <p class="mt-4 font-semibold">- John Carter, New Jersey</p>
        </div>
      </div>
      <img src="photo2.jpg" alt="Prestige Rooter Team" class="mx-auto mt-4 w-full max-w-[50%] h-auto object-cover rounded-lg shadow-md">
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="bg-blue-900 text-white py-16">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8" data-en="Contact Us" data-ru="Свяжитесь с нами">Contact Us</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div>
          <p class="text-lg mb-4" data-en="Prestige Rooter" data-ru="Prestige Rooter">Prestige Rooter</p>
          <p class="mb-4" data-en="24 Manhattan Court, Brooklyn, NY 11223" data-ru="24 Манхэттен Корт, Бруклин, NY 11223">24 Manhattan Court, Brooklyn, NY 11223</p>
          <p class="mb-4" data-en="Phone: 347-276-3160" data-ru="Телефон: 347-276-3160">Phone: 347-276-3160</p>
          <p class="mb-4" data-en="Email: Prestigerooter@gmail.com" data-ru="Эл. почта: Prestigerooter@gmail.com">Email: Prestigerooter@gmail.com</p>
          <p data-en="Hours: Mon-Fri 7 AM-7 PM, Emergency Services Available for Upcharge" data-ru="Часы работы: Пн-Пт 7:00-19:00, Экстренные услуги доступны за доплату">Hours: Mon-Fri 7 AM-7 PM, Emergency Services Available for Upcharge</p>
        </div>
        <div>
          <div class="bg-white text-gray-800 p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-semibold mb-4" data-en="Get in Touch" data-ru="Свяжитесь с нами">Get in Touch</h3>
            <div>
              <label for="name" class="block mb-2" data-en="Name" data-ru="Имя">Name</label>
              <input type="text" id="name" class="w-full p-2 border rounded mb-4" placeholder="Your Name">
              <label for="email" class="block mb-2" data-en="Email" data-ru="Эл. почта">Email</label>
              <input type="email" id="email" class="w-full p-2 border rounded mb-4" placeholder="Your Email">
              <label for="message" class="block mb-2" data-en="Message" data-ru="Сообщение">Message</label>
              <textarea id="message" class="w-full p-2 border rounded mb-4" rows="4" placeholder="How can we help you?"></textarea>
              <button onclick="alert('Form submitted! We will contact you soon.')" class="bg-yellow-500 text-blue-900 px-4 py-2 rounded hover:bg-yellow-400" data-en="Send Message" data-ru="Отправить сообщение">Send Message</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white py-6">
    <div class="container mx-auto px-4 text-center">
      <p>&copy; 2025 Prestige Rooter. All rights reserved.</p>
      <p class="mt-2">Serving Brooklyn, Staten Island, and New Jersey</p>
      <div class="mt-4 space-x-4">
        <a href="#" class="hover:text-blue-300">Facebook</a>
        <a href="#" class="hover:text-blue-300">Twitter</a>
        <a href="#" class="hover:text-blue-300">Instagram</a>
      </div>
    </div>
  </footer>

  <script>
    // Smooth scrolling for navigation
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
          behavior: 'smooth'
        });
      });
    });

    // Language toggle function
    let lang = 'en';
    function toggleLanguage() {
      if (lang === 'en') {
        lang = 'ru';
        document.querySelectorAll('[data-ru]').forEach(element => {
          element.textContent = element.getAttribute('data-ru');
        });
        document.getElementById('body').setAttribute('lang', 'ru');
      } else {
        lang = 'en';
        document.querySelectorAll('[data-en]').forEach(element => {
          element.textContent = element.getAttribute('data-en');
        });
        document.getElementById('body').setAttribute('lang', 'en');
      }
    }
  </script>
</body>
</html>
