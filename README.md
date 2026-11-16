# RuangPotong
Website Barbershop RuangPotong
<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RuangPotong - Barbershop & Hair Styling</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary-gold: #D4AF37;
            --dark-bg: #0F172A;
            --card-bg: #1E293B;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--dark-bg);
            color: #F8FAFC;
        }

        h1, h2, h3, h4, .serif-font {
            font-family: 'Playfair Display', serif;
        }

        .text-gold { color: var(--primary-gold); }
        .bg-gold { background-color: var(--primary-gold); }
        .border-gold { border-color: var(--primary-gold); }

        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--dark-bg); }
        ::-webkit-scrollbar-thumb { background: #334155; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: var(--primary-gold); }

        .fade-in-up {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }
        .fade-in-up.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .service-card:hover .service-img { transform: scale(1.05); }
        .gallery-item:hover .gallery-overlay { opacity: 1; }
    </style>
</head>
<body class="antialiased selection:bg-yellow-600 selection:text-white">

    <!-- Navigation -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-300 bg-slate-900/90 backdrop-blur-md border-b border-white/10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <div class="flex-shrink-0 cursor-pointer" onclick="window.scrollTo(0,0)">
                    <a href="#beranda" class="text-2xl font-bold serif-font tracking-wide text-white">
                        RUANG<span class="text-gold">POTONG</span>
                    </a>
                </div>
                
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <a href="#beranda" class="hover:text-gold transition-colors px-3 py-2 rounded-md text-sm font-medium">Beranda</a>
                        <a href="#tentang" class="hover:text-gold transition-colors px-3 py-2 rounded-md text-sm font-medium">Tentang Kami</a>
                        <a href="#layanan" class="hover:text-gold transition-colors px-3 py-2 rounded-md text-sm font-medium">Layanan</a>
                        <a href="#keunggulan" class="hover:text-gold transition-colors px-3 py-2 rounded-md text-sm font-medium">Keunggulan</a>
                        <a href="#galeri" class="hover:text-gold transition-colors px-3 py-2 rounded-md text-sm font-medium">Galeri</a>
                        <a href="#kontak" class="bg-gold text-slate-900 hover:bg-yellow-500 px-4 py-2 rounded-full text-sm font-bold transition-all transform hover:scale-105">Kontak</a>
                    </div>
                </div>

                <div class="-mr-2 flex md:hidden">
                    <button type="button" onclick="toggleMobileMenu()" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <div id="mobile-menu" class="hidden md:hidden bg-slate-900 border-t border-white/10">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#beranda" onclick="toggleMobileMenu()" class="text-gray-300 hover:text-gold block px-3 py-2 rounded-md text-base font-medium">Beranda</a>
                <a href="#tentang" onclick="toggleMobileMenu()" class="text-gray-300 hover:text-gold block px-3 py-2 rounded-md text-base font-medium">Tentang Kami</a>
                <a href="#layanan" onclick="toggleMobileMenu()" class="text-gray-300 hover:text-gold block px-3 py-2 rounded-md text-base font-medium">Layanan</a>
                <a href="#keunggulan" onclick="toggleMobileMenu()" class="text-gray-300 hover:text-gold block px-3 py-2 rounded-md text-base font-medium">Keunggulan</a>
                <a href="#galeri" onclick="toggleMobileMenu()" class="text-gray-300 hover:text-gold block px-3 py-2 rounded-md text-base font-medium">Galeri</a>
                <a href="#kontak" onclick="toggleMobileMenu()" class="text-gold font-bold block px-3 py-2 rounded-md text-base">Kontak Kami</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="beranda" class="relative h-screen flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?q=80&w=2074&auto=format&fit=crop" alt="Barbershop Interior" class="w-full h-full object-cover opacity-40">
            <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-slate-900/80 to-transparent"></div>
        </div>

        <div class="relative z-10 text-center px-4 max-w-4xl mx-auto fade-in-up">
            <p class="text-gold font-medium tracking-[0.2em] uppercase mb-4 text-sm md:text-base">Barbershop & Hair Styling</p>
            <h1 class="text-5xl md:text-7xl font-bold text-white mb-6 leading-tight">
                Your Style.<br>Your <span class="text-gold italic">Identity.</span>
            </h1>
            <p class="text-gray-300 text-lg md:text-xl mb-10 max-w-2xl mx-auto font-light">
                RuangPotong adalah barbershop yang mengutamakan keterampilan, kebersihan, dan kenyamanan. Lebih dari sekadar potongan rambut, kami membantu setiap pelanggan tampil percaya diri dengan gaya yang sesuai karakternya.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#layanan" class="px-8 py-4 bg-gold text-slate-900 font-bold rounded-full hover:bg-yellow-500 transition-all transform hover:-translate-y-1 shadow-lg shadow-yellow-900/20">
                    Lihat Layanan
                </a>
                <a href="#tentang" class="px-8 py-4 border border-white/30 text-white font-medium rounded-full hover:bg-white/10 transition-all backdrop-blur-sm">
                    Profil Perusahaan
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="tentang" class="py-20 bg-slate-900 relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                <div class="relative fade-in-up">
                    <div class="grid grid-cols-2 gap-4">
                        <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?q=80&w=1000&auto=format&fit=crop" alt="Barber Working" class="rounded-2xl shadow-2xl w-full h-64 object-cover transform translate-y-8">
                        <img src="https://images.unsplash.com/photo-1503951914875-452162b0f3f1?q=80&w=1000&auto=format&fit=crop" alt="Haircut Detail" class="rounded-2xl shadow-2xl w-full h-64 object-cover">
                    </div>
                    <div class="absolute -z-10 top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-[120%] h-[120%] bg-gold/5 rounded-full blur-3xl"></div>
                </div>

                <div class="fade-in-up delay-100">
                    <h2 class="text-gold text-sm font-bold tracking-widest uppercase mb-2">Mengenal RuangPotong</h2>
                    <h3 class="text-4xl font-bold text-white mb-6 serif-font">Ruang untuk tampil terbaik</h3>
                    <p class="text-gray-400 mb-6 leading-relaxed">
                        RuangPotong hadir sebagai tempat bagi siapa saja yang ingin merawat penampilan rambut dengan tenang dan nyaman. Setiap potongan dikerjakan dengan teliti, mulai dari konsultasi model sampai sentuhan akhir.
                    </p>
                    <p class="text-gray-400 mb-8 leading-relaxed">
                        Kami percaya rambut yang tertata rapi menambah rasa percaya diri. Karena itu, layanan kami dirancang mengikuti kebutuhan dan gaya masing-masing pelanggan.
                    </p>

                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-10 w-10 rounded-full bg-slate-800 flex items-center justify-center text-gold border border-slate-700">
                                <i class="fas fa-user-tie"></i>
                            </div>
                            <div class="ml-4">
                                <h4 class="text-lg font-medium text-white">Profesional</h4>
                                <p class="text-gray-500 text-sm">Dikerjakan dengan keterampilan dan ketelitian tinggi.</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-10 w-10 rounded-full bg-slate-800 flex items-center justify-center text-gold border border-slate-700">
                                <i class="fas fa-pump-soap"></i>
                            </div>
                            <div class="ml-4">
                                <h4 class="text-lg font-medium text-white">Bersih</h4>
                                <p class="text-gray-500 text-sm">Alat dan tempat dijaga kebersihannya demi keamanan Anda.</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-10 w-10 rounded-full bg-slate-800 flex items-center justify-center text-gold border border-slate-700">
                                <i class="fas fa-couch"></i>
                            </div>
                            <div class="ml-4">
                                <h4 class="text-lg font-medium text-white">Nyaman</h4>
                                <p class="text-gray-500 text-sm">Suasana santai dan pelayanan yang ramah.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="layanan" class="py-20 bg-slate-800/50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in-up">
                <h2 class="text-gold text-sm font-bold tracking-widest uppercase mb-2">Our Services</h2>
                <h3 class="text-4xl font-bold text-white serif-font">Layanan Kami</h3>
                <p class="mt-4 text-gray-400 max-w-2xl mx-auto">Pilih layanan sesuai kebutuhanmu. Ketuk Rincian pada setiap kartu untuk melihat daftar harganya.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Haircut -->
                <div class="service-card group bg-slate-900 rounded-2xl overflow-hidden border border-slate-800 hover:border-gold/50 transition-all duration-300 fade-in-up">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://images.unsplash.com/photo-1599351431202-1e0f0137899a?q=80&w=1000&auto=format&fit=crop" alt="Haircut" class="service-img w-full h-full object-cover transition-transform duration-500">
                        <div class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-all"></div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h4 class="text-xl font-bold text-white">Haircut</h4>
                            <span class="text-gold font-bold">Rp20k+</span>
                        </div>
                        <p class="text-gray-400 text-sm mb-6 h-12">Potong rambut dengan berbagai model, dari klasik yang rapi sampai tren terkini.</p>
                        <button onclick="toggleDetails('details-haircut')" class="w-full py-2 mb-3 border border-slate-700 text-gray-300 rounded-lg hover:bg-slate-800 transition-colors text-sm flex items-center justify-center gap-2">
                            <i class="fas fa-list-ul"></i> Lihat Rincian Harga
                        </button>
                        <div id="details-haircut" class="hidden bg-slate-800/50 rounded-lg p-3 mb-4 text-sm border border-slate-700/50">
                            <div class="flex justify-between py-1 border-b border-slate-700/50"><span>Regular Haircut</span> <span class="text-gold">Rp20.000</span></div>
                            <div class="flex justify-between py-1"><span>Premium Haircut</span> <span class="text-gold">Rp25.000</span></div>
                        </div>
                        <a href="https://wa.me/6282335713178?text=Halo%20RuangPotong%2C%20saya%20ingin%20pesan%20Haircut." target="_blank" class="block w-full py-3 bg-green-600 hover:bg-green-500 text-white text-center rounded-lg font-medium transition-colors flex items-center justify-center gap-2">
                            <i class="fab fa-whatsapp"></i> Pesan Sekarang
                        </a>
                    </div>
                </div>

                <!-- Styling -->
                <div class="service-card group bg-slate-900 rounded-2xl overflow-hidden border border-slate-800 hover:border-gold/50 transition-all duration-300 fade-in-up delay-100">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://images.unsplash.com/photo-1622286342621-4bd786c2447c?q=80&w=1000&auto=format&fit=crop" alt="Styling" class="service-img w-full h-full object-cover transition-transform duration-500">
                        <div class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-all"></div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h4 class="text-xl font-bold text-white">Hair Styling</h4>
                            <span class="text-gold font-bold">Rp10k+</span>
                        </div>
                        <p class="text-gray-400 text-sm mb-6 h-12">Penataan rambut sesuai karakter dan kebutuhan acara, supaya penampilanmu tetap terjaga.</p>
                        <button onclick="toggleDetails('details-styling')" class="w-full py-2 mb-3 border border-slate-700 text-gray-300 rounded-lg hover:bg-slate-800 transition-colors text-sm flex items-center justify-center gap-2">
                            <i class="fas fa-list-ul"></i> Lihat Rincian Harga
                        </button>
                        <div id="details-styling" class="hidden bg-slate-800/50 rounded-lg p-3 mb-4 text-sm border border-slate-700/50">
                            <div class="flex justify-between py-1 border-b border-slate-700/50"><span>Basic Styling</span> <span class="text-gold">Rp10.000</span></div>
                            <div class="flex justify-between py-1"><span>Premium Styling</span> <span class="text-gold">Rp15.000</span></div>
                        </div>
                        <a href="https://wa.me/6282335713178?text=Halo%20RuangPotong%2C%20saya%20ingin%20pesan%20Hair%20Styling." target="_blank" class="block w-full py-3 bg-green-600 hover:bg-green-500 text-white text-center rounded-lg font-medium transition-colors flex items-center justify-center gap-2">
                            <i class="fab fa-whatsapp"></i> Pesan Sekarang
                        </a>
                    </div>
                </div>

                <!-- Wash -->
                <div class="service-card group bg-slate-900 rounded-2xl overflow-hidden border border-slate-800 hover:border-gold/50 transition-all duration-300 fade-in-up delay-200">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://images.unsplash.com/photo-1517832606299-7ae9b720a186?q=80&w=1000&auto=format&fit=crop" alt="Hair Wash" class="service-img w-full h-full object-cover transition-transform duration-500">
                        <div class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-all"></div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h4 class="text-xl font-bold text-white">Hair Wash</h4>
                            <span class="text-gold font-bold">Rp10k+</span>
                        </div>
                        <p class="text-gray-400 text-sm mb-6 h-12">Pencucian rambut yang bersih dan menyegarkan, cocok sebagai pelengkap potong rambut.</p>
                        <button onclick="toggleDetails('details-wash')" class="w-full py-2 mb-3 border border-slate-700 text-gray-300 rounded-lg hover:bg-slate-800 transition-colors text-sm flex items-center justify-center gap-2">
                            <i class="fas fa-list-ul"></i> Lihat Rincian Harga
                        </button>
                        <div id="details-wash" class="hidden bg-slate-800/50 rounded-lg p-3 mb-4 text-sm border border-slate-700/50">
                            <div class="flex justify-between py-1 border-b border-slate-700/50"><span>Regular Hair Wash</span> <span class="text-gold">Rp10.000</span></div>
                            <div class="flex justify-between py-1"><span>Premium Hair Wash</span> <span class="text-gold">Rp15.000</span></div>
                        </div>
                        <a href="https://wa.me/6282335713178?text=Halo%20RuangPotong%2C%20saya%20ingin%20pesan%20Hair%20Wash." target="_blank" class="block w-full py-3 bg-green-600 hover:bg-green-500 text-white text-center rounded-lg font-medium transition-colors flex items-center justify-center gap-2">
                            <i class="fab fa-whatsapp"></i> Pesan Sekarang
                        </a>
                    </div>
                </div>

                <!-- Treatment -->
                <div class="service-card group bg-slate-900 rounded-2xl overflow-hidden border border-slate-800 hover:border-gold/50 transition-all duration-300 fade-in-up">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://images.unsplash.com/photo-1560066984-138dadb4c035?q=80&w=1000&auto=format&fit=crop" alt="Treatment" class="service-img w-full h-full object-cover transition-transform duration-500">
                        <div class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-all"></div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h4 class="text-xl font-bold text-white">Hair Treatment</h4>
                            <span class="text-gold font-bold">Rp15k+</span>
                        </div>
                        <p class="text-gray-400 text-sm mb-6 h-12">Perawatan untuk menjaga rambut dan kulit kepala tetap sehat, kuat, dan mudah diatur.</p>
                        <button onclick="toggleDetails('details-treatment')" class="w-full py-2 mb-3 border border-slate-700 text-gray-300 rounded-lg hover:bg-slate-800 transition-colors text-sm flex items-center justify-center gap-2">
                            <i class="fas fa-list-ul"></i> Lihat Rincian Harga
                        </button>
                        <div id="details-treatment" class="hidden bg-slate-800/50 rounded-lg p-3 mb-4 text-sm border border-slate-700/50">
                            <div class="flex justify-between py-1 border-b border-slate-700/50"><span>Hair Mask</span> <span class="text-gold">Rp20.000</span></div>
                            <div class="flex justify-between py-1"><span>Hair Tonic Treatment</span> <span class="text-gold">Rp15.000</span></div>
                        </div>
                        <a href="https://wa.me/6282335713178?text=Halo%20RuangPotong%2C%20saya%20ingin%20pesan%20Hair%20Treatment." target="_blank" class="block w-full py-3 bg-green-600 hover:bg-green-500 text-white text-center rounded-lg font-medium transition-colors flex items-center justify-center gap-2">
                            <i class="fab fa-whatsapp"></i> Pesan Sekarang
                        </a>
                    </div>
                </div>

                <!-- Grooming -->
                <div class="service-card group bg-slate-900 rounded-2xl overflow-hidden border border-slate-800 hover:border-gold/50 transition-all duration-300 fade-in-up delay-100">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?q=80&w=1000&auto=format&fit=crop" alt="Grooming" class="service-img w-full h-full object-cover transition-transform duration-500">
                        <div class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-all"></div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h4 class="text-xl font-bold text-white">Grooming</h4>
                            <span class="text-gold font-bold">Rp10k+</span>
                        </div>
                        <p class="text-gray-400 text-sm mb-6 h-12">Perawatan penampilan pria, mulai dari merapikan rambut sampai detail kecil.</p>
                        <button onclick="toggleDetails('details-grooming')" class="w-full py-2 mb-3 border border-slate-700 text-gray-300 rounded-lg hover:bg-slate-800 transition-colors text-sm flex items-center justify-center gap-2">
                            <i class="fas fa-list-ul"></i> Lihat Rincian Harga
                        </button>
                        <div id="details-grooming" class="hidden bg-slate-800/50 rounded-lg p-3 mb-4 text-sm border border-slate-700/50">
                            <div class="flex justify-between py-1 border-b border-slate-700/50"><span>Beard Trimming</span> <span class="text-gold">Rp15.000</span></div>
                            <div class="flex justify-between py-1"><span>Mustache Trimming</span> <span class="text-gold">Rp10.000</span></div>
                        </div>
                        <a href="https://wa.me/6282335713178?text=Halo%20RuangPotong%2C%20saya%20ingin%20pesan%20Grooming." target="_blank" class="block w-full py-3 bg-green-600 hover:bg-green-500 text-white text-center rounded-lg font-medium transition-colors flex items-center justify-center gap-2">
                            <i class="fab fa-whatsapp"></i> Pesan Sekarang
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us -->
    <section id="keunggulan" class="py-20 bg-slate-900 relative">
        <div class="absolute top-0 left-0 w-full h-full overflow-hidden pointer-events-none">
             <div class="absolute top-1/4 right-0 w-96 h-96 bg-gold/5 rounded-full blur-3xl"></div>
        </div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 fade-in-up">
                <h2 class="text-gold text-sm font-bold tracking-widest uppercase mb-2">Why Choose Us</h2>
                <h3 class="text-4xl font-bold text-white serif-font">Keunggulan Kami</h3>
                <p class="mt-4 text-gray-400">Lima hal yang kami jaga di setiap kunjungan.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5 gap-6">
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-gold transition-colors text-center fade-in-up">
                    <div class="w-14 h-14 mx-auto bg-slate-900 rounded-full flex items-center justify-center text-gold text-2xl mb-4 border border-slate-700">
                        <i class="fas fa-user-check"></i>
                    </div>
                    <h4 class="text-white font-bold mb-2">Profesional & Ramah</h4>
                    <p class="text-gray-400 text-xs">Barber berpengalaman yang melayani dengan sopan dan mau mendengarkan keinginanmu.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-gold transition-colors text-center fade-in-up delay-100">
                    <div class="w-14 h-14 mx-auto bg-slate-900 rounded-full flex items-center justify-center text-gold text-2xl mb-4 border border-slate-700">
                        <i class="fas fa-cut"></i>
                    </div>
                    <h4 class="text-white font-bold mb-2">Kualitas Potongan</h4>
                    <p class="text-gray-400 text-xs">Hasil potongan rapi dan presisi menjadi prioritas utama kami.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-gold transition-colors text-center fade-in-up delay-200">
                    <div class="w-14 h-14 mx-auto bg-slate-900 rounded-full flex items-center justify-center text-gold text-2xl mb-4 border border-slate-700">
                        <i class="fas fa-shield-virus"></i>
                    </div>
                    <h4 class="text-white font-bold mb-2">Bersih & Higienis</h4>
                    <p class="text-gray-400 text-xs">Alat dan area kerja selalu dijaga kebersihannya demi keamanan pelanggan.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-gold transition-colors text-center fade-in-up delay-300">
                    <div class="w-14 h-14 mx-auto bg-slate-900 rounded-full flex items-center justify-center text-gold text-2xl mb-4 border border-slate-700">
                        <i class="fas fa-coffee"></i>
                    </div>
                    <h4 class="text-white font-bold mb-2">Nyaman</h4>
                    <p class="text-gray-400 text-xs">Suasana tenang dan bersahabat, supaya waktu perawatanmu terasa menyenangkan.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 hover:border-gold transition-colors text-center fade-in-up delay-400">
                    <div class="w-14 h-14 mx-auto bg-slate-900 rounded-full flex items-center justify-center text-gold text-2xl mb-4 border border-slate-700">
                        <i class="fas fa-fingerprint"></i>
                    </div>
                    <h4 class="text-white font-bold mb-2">Sesuai Gayamu</h4>
                    <p class="text-gray-400 text-xs">Layanan disesuaikan dengan kebutuhan, karakter, dan gaya masing-masing pelanggan.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section class="py-20 bg-slate-800/30">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="fade-in-up">
                    <img src="https://images.unsplash.com/photo-1521590832167-7bcbfaa6381f?q=80&w=1000&auto=format&fit=crop" alt="Tim RuangPotong" class="rounded-2xl shadow-2xl w-full h-96 object-cover">
                </div>
                <div class="fade-in-up delay-100">
                    <h2 class="text-gold text-sm font-bold tracking-widest uppercase mb-2">About Us</h2>
                    <h3 class="text-4xl font-bold text-white mb-6 serif-font">Tentang Kami</h3>
                    <p class="text-gray-400 mb-4 leading-relaxed">
                        RuangPotong berawal dari keinginan sederhana: menyediakan tempat potong rambut yang rapi, bersih, dan membuat orang merasa nyaman. Dari situ lahir sebuah barbershop yang menempatkan pelanggan sebagai pusat setiap layanan.
                    </p>
                    <p class="text-gray-400 mb-4 leading-relaxed">
                        Kami bergerak di bidang jasa potong rambut, hair styling, dan perawatan rambut. Filosofi kami jelas: setiap orang punya identitas, dan rambut adalah salah satu cara menunjukkannya.
                    </p>
                    <p class="text-gray-400 mb-6 leading-relaxed">
                        Komitmen kami adalah menjaga kualitas pada setiap potongan dan memastikan pelanggan pulang dengan puas.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Vision & Mission -->
    <section class="py-20 bg-slate-900 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <div class="fade-in-up">
                    <h3 class="text-2xl font-bold text-white serif-font mb-4 border-l-4 border-gold pl-4">Visi</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Memberikan pelayanan dan kualitas rambut terbaik melalui keterampilan profesional, pelayanan berkualitas, serta pengalaman yang nyaman bagi setiap pelanggan.
                    </p>
                </div>
                <div class="fade-in-up delay-100">
                    <h3 class="text-2xl font-bold text-white serif-font mb-4 border-l-4 border-gold pl-4">Misi</h3>
                    <ul class="space-y-3 text-gray-400">
                        <li class="flex items-start"><i class="fas fa-check text-gold mt-1 mr-3"></i> Menghadirkan hasil potongan yang rapi dan berkualitas.</li>
                        <li class="flex items-start"><i class="fas fa-check text-gold mt-1 mr-3"></i> Melayani dengan ramah, sopan, dan profesional.</li>
                        <li class="flex items-start"><i class="fas fa-check text-gold mt-1 mr-3"></i> Menjaga kebersihan alat dan tempat usaha.</li>
                        <li class="flex items-start"><i class="fas fa-check text-gold mt-1 mr-3"></i> Menciptakan suasana yang nyaman bagi setiap pelanggan.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="galeri" class="py-20 bg-slate-800/30">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12 fade-in-up">
                <h2 class="text-gold text-sm font-bold tracking-widest uppercase mb-2">Our Gallery</h2>
                <h3 class="text-4xl font-bold text-white serif-font">Galeri</h3>
                <p class="mt-4 text-gray-400">Hasil potongan, model rambut, aktivitas barber, dan suasana tempat usaha.</p>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 auto-rows-[200px]">
                <div class="col-span-2 row-span-2 relative group overflow-hidden rounded-xl cursor-pointer fade-in-up">
                    <img src="https://images.unsplash.com/photo-1503951914875-452162b0f3f1?q=80&w=1000&auto=format&fit=crop" alt="Gallery 1" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="gallery-overlay absolute inset-0 bg-black/60 opacity-0 transition-opacity duration-300 flex items-center justify-center">
                        <span class="text-white font-bold text-lg border-b-2 border-gold pb-1">Interior</span>
                    </div>
                </div>
                <div class="col-span-1 row-span-1 relative group overflow-hidden rounded-xl cursor-pointer fade-in-up">
                    <img src="https://images.unsplash.com/photo-1599351431613-18ef1fdd27e1?q=80&w=1000&auto=format&fit=crop" alt="Gallery 2" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="gallery-overlay absolute inset-0 bg-black/60 opacity-0 transition-opacity duration-300 flex items-center justify-center">
                        <span class="text-white font-bold text-sm border-b-2 border-gold pb-1">Styling</span>
                    </div>
                </div>
                <div class="col-span-1 row-span-1 relative group overflow-hidden rounded-xl cursor-pointer fade-in-up">
                    <img src="https://images.unsplash.com/photo-1622286342621-4bd786c2447c?q=80&w=1000&auto=format&fit=crop" alt="Gallery 3" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="gallery-overlay absolute inset-0 bg-black/60 opacity-0 transition-opacity duration-300 flex items-center justify-center">
                        <span class="text-white font-bold text-sm border-b-2 border-gold pb-1">Detail</span>
                    </div>
                </div>
                <div class="col-span-1 row-span-1 relative group overflow-hidden rounded-xl cursor-pointer fade-in-up">
                    <img src="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?q=80&w=1000&auto=format&fit=crop" alt="Gallery 4" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="gallery-overlay absolute inset-0 bg-black/60 opacity-0 transition-opacity duration-300 flex items-center justify-center">
                        <span class="text-white font-bold text-sm border-b-2 border-gold pb-1">Alat</span>
                    </div>
                </div>
                <div class="col-span-1 row-span-1 relative group overflow-hidden rounded-xl cursor-pointer fade-in-up">
                    <img src="https://images.unsplash.com/photo-1521590832167-7bcbfaa6381f?q=80&w=1000&auto=format&fit=crop" alt="Gallery 5" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="gallery-overlay absolute inset-0 bg-black/60 opacity-0 transition-opacity duration-300 flex items-center justify-center">
                        <span class="text-white font-bold text-sm border-b-2 border-gold pb-1">Suasana</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="kontak" class="py-20 bg-slate-800 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in-up">
                <h2 class="text-gold text-sm font-bold tracking-widest uppercase mb-2">Contact Us</h2>
                <h3 class="text-4xl font-bold text-white serif-font">Kontak Kami</h3>
                <p class="mt-4 text-gray-400">Hubungi RuangPotong untuk tanya layanan, harga, atau jadwal kunjungan.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-slate-900 p-8 rounded-2xl border border-slate-700 text-center hover:border-gold transition-all fade-in-up">
                    <div class="w-16 h-16 bg-green-900/30 rounded-full flex items-center justify-center mx-auto mb-6 text-green-500 text-3xl">
                        <i class="fab fa-whatsapp"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">WhatsApp 1</h4>
                    <p class="text-gray-400 mb-6">+62 823-3571-3178</p>
                    <div class="flex gap-2 justify-center">
                        <a href="https://wa.me/6282335713178?text=Halo%20RuangPotong%2C%20saya%20ingin%20bertanya%20layanan." target="_blank" class="flex-1 bg-green-600 hover:bg-green-500 text-white py-2 rounded-lg font-medium transition-colors">
                            Chat
                        </a>
                        <button onclick="copyToClipboard('+6282335713178')" class="px-4 bg-slate-700 hover:bg-slate-600 text-white rounded-lg transition-colors" title="Salin Nomor">
                            <i class="fas fa-copy"></i>
                        </button>
                    </div>
                </div>

                <div class="bg-slate-900 p-8 rounded-2xl border border-slate-700 text-center hover:border-gold transition-all fade-in-up delay-100">
                    <div class="w-16 h-16 bg-green-900/30 rounded-full flex items-center justify-center mx-auto mb-6 text-green-500 text-3xl">
                        <i class="fab fa-whatsapp"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">WhatsApp 2</h4>
                    <p class="text-gray-400 mb-6">+62 812-1623-7159</p>
                    <div class="flex gap-2 justify-center">
                        <a href="https://wa.me/6281216237159?text=Halo%20RuangPotong%2C%20saya%20ingin%20bertanya%20layanan." target="_blank" class="flex-1 bg-green-600 hover:bg-green-500 text-white py-2 rounded-lg font-medium transition-colors">
                            Chat
                        </a>
                        <button onclick="copyToClipboard('+6281216237159')" class="px-4 bg-slate-700 hover:bg-slate-600 text-white rounded-lg transition-colors" title="Salin Nomor">
                            <i class="fas fa-copy"></i>
                        </button>
                    </div>
                </div>

                <div class="bg-slate-900 p-8 rounded-2xl border border-slate-700 text-center hover:border-gold transition-all fade-in-up delay-200">
                    <div class="w-16 h-16 bg-yellow-900/30 rounded-full flex items-center justify-center mx-auto mb-6 text-gold text-3xl">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">Lokasi & Jam</h4>
                    <p class="text-gray-400 mb-2">Buka Setiap Hari</p>
                    <p class="text-white font-bold mb-6">10:00 - 21:00 WIB</p>
                    <a href="#" class="block w-full bg-slate-700 hover:bg-slate-600 text-white py-2 rounded-lg font-medium transition-colors">
                        Lihat di Maps
                    </a>
                </div>
            </div>
            
            <div class="mt-12 text-center fade-in-up">
                <a href="#" class="inline-flex items-center gap-3 text-gray-400 hover:text-pink-500 transition-colors text-lg">
                    <i class="fab fa-instagram text-2xl"></i>
                    <span>Follow kami di Instagram @RuangPotong</span>
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-950 py-12 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div class="col-span-1 md:col-span-2">
                    <a href="#beranda" class="text-2xl font-bold serif-font tracking-wide text-white block mb-4">
                        RUANG<span class="text-gold">POTONG</span>
                    </a>
                    <p class="text-gray-500 max-w-sm mb-6">
                        Your Style. Your Identity. <br>
                        Barbershop modern dengan pendekatan personal untuk setiap pelanggan.
                    </p>
                </div>
                <div>
                    <h4 class="text-white font-bold mb-4">Navigasi</h4>
                    <ul class="space-y-2 text-gray-500">
                        <li><a href="#beranda" class="hover:text-gold transition-colors">Beranda</a></li>
                        <li><a href="#tentang" class="hover:text-gold transition-colors">Tentang Kami</a></li>
                        <li><a href="#layanan" class="hover:text-gold transition-colors">Layanan</a></li>
                        <li><a href="#keunggulan" class="hover:text-gold transition-colors">Keunggulan</a></li>
                        <li><a href="#galeri" class="hover:text-gold transition-colors">Galeri</a></li>
                        <li><a href="#kontak" class="hover:text-gold transition-colors">Kontak</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-white font-bold mb-4">Hubungi Kami</h4>
                    <ul class="space-y-2 text-gray-500">
                        <li><a href="https://wa.me/6282335713178" class="hover:text-gold transition-colors">WA: +62 823-3571-3178</a></li>
                        <li><a href="https://wa.me/6281216237159" class="hover:text-gold transition-colors">WA: +62 812-1623-7159</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-slate-800 pt-8 text-center text-gray-600 text-sm">
                &copy; 2026 RuangPotong. All Rights Reserved.
            </div>
        </div>
    </footer>

    <div id="toast" class="fixed bottom-5 right-5 bg-green-600 text-white px-6 py-3 rounded-lg shadow-lg transform translate-y-20 opacity-0 transition-all duration-300 z-50 flex items-center gap-2">
        <i class="fas fa-check-circle"></i>
        <span>Nomor berhasil disalin!</span>
    </div>

    <script>
        function toggleMobileMenu() {
            document.getElementById('mobile-menu').classList.toggle('hidden');
        }

        function toggleDetails(id) {
            document.getElementById(id).classList.toggle('hidden');
        }

        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                const toast = document.getElementById('toast');
                toast.classList.remove('translate-y-20', 'opacity-0');
                setTimeout(() => toast.classList.add('translate-y-20', 'opacity-0'), 3000);
            });
        }

        document.addEventListener('DOMContentLoaded', () => {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            document.querySelectorAll('.fade-in-up').forEach(el => observer.observe(el));
        });

        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('shadow-lg');
                navbar.classList.replace('bg-slate-900/90', 'bg-slate-900');
            } else {
                navbar.classList.remove('shadow-lg');
                navbar.classList.replace('bg-slate-900', 'bg-slate-900/90');
            }
        });
    </script>
</body>
</html>

