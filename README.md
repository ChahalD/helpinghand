<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seaborne Care - Spreading Joy Across Every Occasion</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            500: '#0284c7',
                            600: '#0369a1',
                            700: '#0369a1',
                            800: '#075985',
                            900: '#0c4a6e',
                        },
                        amberAccent: {
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706',
                        }
                    },
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                        heading: ['Poppins', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        .page-section {
            display: none;
        }
        .page-section.active {
            display: block;
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans flex flex-col min-h-screen">

    <!-- GitHub Hosting Instructions Top Banner -->
    <div id="githubBanner" class="bg-gradient-to-r from-slate-900 via-brand-900 to-slate-900 text-white text-xs sm:text-sm py-2 px-4 relative z-50">
        <div class="max-w-7xl mx-auto flex justify-between items-center gap-2">
            <div class="flex items-center gap-2 overflow-hidden">
                <i class="fa-brands fa-github text-amberAccent-400 text-lg flex-shrink-0"></i>
                <p class="truncate">
                    <span class="font-semibold text-amberAccent-400">GitHub Pages Ready!</span> Save this file as <code class="bg-slate-800 px-1.5 py-0.5 rounded text-sky-300 font-mono">index.html</code> in your repository & enable GitHub Pages under Settings > Pages.
                </p>
            </div>
            <button onclick="document.getElementById('githubBanner').remove()" class="text-slate-400 hover:text-white text-base pl-2">
                <i class="fa-solid fa-xmark"></i>
            </button>
        </div>
    </div>

    <!-- Sticky Navigation Bar -->
    <header class="sticky top-0 z-40 bg-white/95 backdrop-blur-md shadow-sm border-b border-slate-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <a href="#home" onclick="navigateTo('home')" class="flex items-center gap-3 group">
                    <div class="w-11 h-11 rounded-xl bg-gradient-to-br from-brand-500 to-brand-700 flex items-center justify-center text-white shadow-md shadow-brand-500/20 group-hover:scale-105 transition-transform">
                        <i class="fa-solid fa-hand-holding-heart text-xl"></i>
                    </div>
                    <div>
                        <span class="text-2xl font-extrabold tracking-tight text-slate-900 font-heading block leading-none">
                            Seaborne <span class="text-brand-600">Care</span>
                        </span>
                        <span class="text-[10px] tracking-widest text-slate-500 uppercase font-semibold">Spreading Smiles Daily</span>
                    </div>
                </a>

                <!-- Desktop Nav Links -->
                <nav class="hidden lg:flex items-center gap-1 font-medium text-slate-600 text-sm">
                    <button onclick="navigateTo('home')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="home">Home</button>
                    <button onclick="navigateTo('about')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="about">About Us</button>
                    <button onclick="navigateTo('mission')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="mission">Our Mission</button>
                    <button onclick="navigateTo('vision')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="vision">Our Vision</button>
                    <button onclick="navigateTo('occasions')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="occasions">Occasions</button>
                    <button onclick="navigateTo('faq')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="faq">FAQ</button>
                    <button onclick="navigateTo('contact')" class="nav-btn px-3 py-2 rounded-lg hover:text-brand-600 hover:bg-brand-50 transition" data-page="contact">Contact Us</button>
                </nav>

                <!-- Action Button -->
                <div class="hidden sm:flex items-center gap-3">
                    <button onclick="navigateTo('contact')" class="bg-gradient-to-r from-brand-600 to-brand-700 hover:from-brand-700 hover:to-brand-800 text-white px-5 py-2.5 rounded-full font-semibold text-sm shadow-md shadow-brand-600/20 hover:shadow-lg transition flex items-center gap-2">
                        <i class="fa-solid fa-heart text-amberAccent-400"></i>
                        <span>Support Us</span>
                    </button>
                </div>

                <!-- Mobile menu toggle -->
                <div class="flex items-center lg:hidden">
                    <button id="mobileMenuBtn" onclick="toggleMobileMenu()" class="p-2 rounded-lg text-slate-600 hover:text-brand-600 hover:bg-slate-100 focus:outline-none">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Nav Menu -->
        <div id="mobileMenu" class="hidden lg:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-6 space-y-2">
            <button onclick="navigateTo('home')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Home</button>
            <button onclick="navigateTo('about')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">About Us</button>
            <button onclick="navigateTo('mission')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Our Mission</button>
            <button onclick="navigateTo('vision')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Our Vision</button>
            <button onclick="navigateTo('occasions')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Occasions & Gallery</button>
            <button onclick="navigateTo('faq')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">FAQ</button>
            <button onclick="navigateTo('contact')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Contact Us</button>
            <button onclick="navigateTo('privacy')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Privacy Policy</button>
            <button onclick="navigateTo('terms')" class="block w-full text-left px-4 py-2.5 rounded-lg font-medium text-slate-700 hover:bg-brand-50 hover:text-brand-600">Terms & Conditions</button>
            <div class="pt-2">
                <button onclick="navigateTo('contact')" class="w-full bg-brand-600 text-white py-3 rounded-xl font-semibold shadow-md flex justify-center items-center gap-2">
                    <i class="fa-solid fa-heart text-amberAccent-400"></i> Get Involved
                </button>
            </div>
        </div>
    </header>

    <!-- Main Content Container -->
    <main class="flex-grow">

        <!-- PAGE 1: HOME PAGE -->
        <section id="page-home" class="page-section active">
            <!-- Hero Section -->
            <div class="relative bg-slate-900 text-white overflow-hidden py-20 lg:py-28">
                <div class="absolute inset-0 z-0 opacity-25 bg-cover bg-center" style="background-image: url('https://images.unsplash.com/photo-1488521787991-ed7bbaae773c?q=80&w=1600&auto=format&fit=crop');"></div>
                <div class="absolute inset-0 bg-gradient-to-r from-slate-950 via-slate-900/90 to-brand-950/80 z-0"></div>
                
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
                    <div class="grid lg:grid-cols-12 gap-12 items-center">
                        <div class="lg:col-span-7 space-y-6">
                            <span class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-brand-500/20 border border-brand-400/30 text-amberAccent-400 font-semibold text-xs tracking-wide uppercase">
                                <i class="fa-solid fa-sparkles"></i> Seaborne Care Initiative
                            </span>
                            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold font-heading text-white leading-tight">
                                Spreading Joy & Care Across <span class="text-transparent bg-clip-text bg-gradient-to-r from-amberAccent-400 to-amber-300">Every Occasion</span>
                            </h1>
                            <p class="text-slate-300 text-lg leading-relaxed max-w-2xl">
                                We believe celebrations belong to everyone. Seaborne Care distributes clothes, food kits, sweets, warm wear, and joy to underprivileged families on Diwali, Holi, New Year, Birthdays, and major festivals.
                            </p>
                            <div class="flex flex-wrap gap-4 pt-4">
                                <button onclick="navigateTo('occasions')" class="bg-brand-600 hover:bg-brand-500 text-white px-7 py-3.5 rounded-full font-bold shadow-lg shadow-brand-600/30 transition transform hover:-translate-y-0.5 flex items-center gap-2">
                                    <span>Explore Occasions</span>
                                    <i class="fa-solid fa-arrow-right text-xs"></i>
                                </button>
                                <a href="https://wa.me/919650285586" target="_blank" class="bg-emerald-600 hover:bg-emerald-500 text-white px-7 py-3.5 rounded-full font-bold shadow-lg shadow-emerald-600/30 transition transform hover:-translate-y-0.5 flex items-center gap-2">
                                    <i class="fa-brands fa-whatsapp text-lg"></i>
                                    <span>WhatsApp Us</span>
                                </a>
                            </div>
                        </div>

                        <div class="lg:col-span-5">
                            <div class="bg-white/10 backdrop-blur-md border border-white/15 p-6 sm:p-8 rounded-3xl shadow-2xl relative">
                                <h3 class="text-2xl font-bold font-heading text-white mb-2">Join Our Drive</h3>
                                <p class="text-slate-300 text-sm mb-6">Partner with us or sponsor a smile on the next upcoming festival!</p>
                                
                                <div class="space-y-4">
                                    <div class="flex items-center gap-4 p-3.5 rounded-2xl bg-white/5 border border-white/10">
                                        <div class="w-12 h-12 rounded-xl bg-amberAccent-500/20 text-amberAccent-400 flex items-center justify-center text-xl font-bold">
                                            <i class="fa-solid fa-gift"></i>
                                        </div>
                                        <div>
                                            <div class="font-bold text-white">Festival Gift Kits</div>
                                            <div class="text-xs text-slate-300">Sweets, new clothes & festive essentials</div>
                                        </div>
                                    </div>

                                    <div class="flex items-center gap-4 p-3.5 rounded-2xl bg-white/5 border border-white/10">
                                        <div class="w-12 h-12 rounded-xl bg-brand-500/20 text-sky-400 flex items-center justify-center text-xl font-bold">
                                            <i class="fa-solid fa-cake-candles"></i>
                                        </div>
                                        <div>
                                            <div class="font-bold text-white">Birthday Happiness</div>
                                            <div class="text-xs text-slate-300">Stationery, treats & school kits for kids</div>
                                        </div>
                                    </div>

                                    <div class="flex items-center gap-4 p-3.5 rounded-2xl bg-white/5 border border-white/10">
                                        <div class="w-12 h-12 rounded-xl bg-emerald-500/20 text-emerald-400 flex items-center justify-center text-xl font-bold">
                                            <i class="fa-solid fa-hands-holding-child"></i>
                                        </div>
                                        <div>
                                            <div class="font-bold text-white">Seasonal Warmth</div>
                                            <div class="text-xs text-slate-300">Blankets & winterwear during New Year</div>
                                        </div>
                                    </div>
                                </div>

                                <button onclick="navigateTo('contact')" class="w-full mt-6 bg-white text-slate-900 hover:bg-slate-100 font-bold py-3.5 rounded-2xl transition shadow-md">
                                    Connect For Next Drive
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Stats Counter -->
            <div class="bg-white py-12 border-b border-slate-200">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
                        <div class="p-4">
                            <div class="text-3xl sm:text-4xl font-extrabold text-brand-600 font-heading">5,000+</div>
                            <div class="text-slate-500 text-sm font-medium mt-1">Lives Touched</div>
                        </div>
                        <div class="p-4">
                            <div class="text-3xl sm:text-4xl font-extrabold text-brand-600 font-heading">50+</div>
                            <div class="text-slate-500 text-sm font-medium mt-1">Distribution Drives</div>
                        </div>
                        <div class="p-4">
                            <div class="text-3xl sm:text-4xl font-extrabold text-brand-600 font-heading">10+</div>
                            <div class="text-slate-500 text-sm font-medium mt-1">Festivals Celebrated</div>
                        </div>
                        <div class="p-4">
                            <div class="text-3xl sm:text-4xl font-extrabold text-brand-600 font-heading">100%</div>
                            <div class="text-slate-500 text-sm font-medium mt-1">Transparency</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Major Festive Distribution Drives -->
            <div class="py-20 bg-slate-50">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                    <div class="text-center max-w-3xl mx-auto mb-16">
                        <span class="text-brand-600 font-bold text-sm tracking-wider uppercase">Our Care Spectrum</span>
                        <h2 class="text-3xl sm:text-4xl font-extrabold font-heading text-slate-900 mt-2">Celebrations We Elevate</h2>
                        <p class="text-slate-600 mt-4">We organize specialized distribution events corresponding to significant Indian festivals and personal milestones.</p>
                    </div>

                    <div class="grid md:grid-cols-3 gap-8">
                        <!-- Diwali -->
                        <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-xl transition group">
                            <div class="h-48 overflow-hidden relative">
                                <img src="https://images.unsplash.com/photo-1605810230434-7631ac76ec81?q=80&w=800&auto=format&fit=crop" alt="Diwali Distribution" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
                                <div class="absolute top-4 right-4 bg-amber-500 text-white text-xs font-bold px-3 py-1 rounded-full">Diwali Drive</div>
                            </div>
                            <div class="p-6">
                                <h3 class="text-xl font-bold font-heading text-slate-900">Diwali Light & Sweets Kit</h3>
                                <p class="text-slate-600 text-sm mt-2 leading-relaxed">Distributing traditional sweets, diyas, new ethnic wear, and festive meal hampers to bring light into underprivileged homes.</p>
                            </div>
                        </div>

                        <!-- Holi -->
                        <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-xl transition group">
                            <div class="h-48 overflow-hidden relative">
                                <img src="https://images.unsplash.com/photo-1576487248805-cc291bac5b61?q=80&w=800&auto=format&fit=crop" alt="Holi Distribution" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
                                <div class="absolute top-4 right-4 bg-rose-500 text-white text-xs font-bold px-3 py-1 rounded-full">Holi Festival</div>
                            </div>
                            <div class="p-6">
                                <h3 class="text-xl font-bold font-heading text-slate-900">Holi Colors & Joy Spread</h3>
                                <p class="text-slate-600 text-sm mt-2 leading-relaxed">Providing organic skin-safe colors, pitchkaris for children, and special festive snacks so everyone enjoys the festival of colors safely.</p>
                            </div>
                        </div>

                        <!-- New Year & Winter -->
                        <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-xl transition group">
                            <div class="h-48 overflow-hidden relative">
                                <img src="https://images.unsplash.com/photo-1544027993-37dbfe43562a?q=80&w=800&auto=format&fit=crop" alt="Winter Blanket Drive" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
                                <div class="absolute top-4 right-4 bg-sky-600 text-white text-xs font-bold px-3 py-1 rounded-full">New Year Warmth</div>
                            </div>
                            <div class="p-6">
                                <h3 class="text-xl font-bold font-heading text-slate-900">New Year Winter Care</h3>
                                <p class="text-slate-600 text-sm mt-2 leading-relaxed">Starting every year with comfort. Distributing heavy blankets, woolens, jackets, and hot meals to street dwellers in peak winter.</p>
                            </div>
                        </div>
                    </div>

                    <div class="text-center mt-12">
                        <button onclick="navigateTo('occasions')" class="inline-flex items-center gap-2 text-brand-600 hover:text-brand-700 font-bold text-base border-b-2 border-brand-600 pb-1">
                            <span>View All Occasion Distributions (Dussehra, Birthdays & More)</span>
                            <i class="fa-solid fa-arrow-right text-sm"></i>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Callout CTA -->
            <div class="bg-gradient-to-r from-brand-800 to-brand-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-6">
                    <h2 class="text-3xl sm:text-4xl font-extrabold font-heading max-w-2xl mx-auto">Have a Birthday or Special Day Coming Up?</h2>
                    <p class="text-brand-100 max-w-xl mx-auto text-base">Sponsor a distribution drive on your special day. Celebrate your personal milestones by sharing food, stationery, and clothes with underprivileged children.</p>
                    <div class="pt-2">
                        <button onclick="navigateTo('contact')" class="bg-amberAccent-500 hover:bg-amberAccent-600 text-slate-900 px-8 py-4 rounded-full font-bold text-lg shadow-lg transition transform hover:scale-105">
                            Sponsor A Drive
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- PAGE 2: ABOUT US -->
        <section id="page-about" class="page-section">
            <div class="bg-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">About Seaborne Care</h1>
                    <p class="text-slate-400 mt-2 text-lg">Who We Are & Why We Serve</p>
                </div>
            </div>

            <div class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div>
                        <span class="text-brand-600 font-bold text-sm tracking-widest uppercase">Our Story</span>
                        <h2 class="text-3xl font-extrabold font-heading text-slate-900 mt-2 mb-6">Bringing Human Dignity to Every Festive Moment</h2>
                        <p class="text-slate-600 leading-relaxed mb-4">
                            <strong>Seaborne Care</strong> was founded on a simple yet profound realization: while millions celebrate festivals like Diwali, Holi, Dussehra, and New Year with joy, lights, and delicious food, countless underprivileged families sit in darkness and shortage.
                        </p>
                        <p class="text-slate-600 leading-relaxed mb-6">
                            We bridge this gap. Seaborne Care operates as an compassionate initiative dedicated to gathering essential supplies, warm clothes, educational tools, and celebratory kits to hand-deliver them directly to children, daily wage earners, and elderly individuals in need.
                        </p>

                        <div class="grid grid-cols-2 gap-4">
                            <div class="border-l-4 border-brand-600 pl-4 py-2">
                                <div class="font-bold text-slate-900">Direct Delivery</div>
                                <div class="text-slate-500 text-xs mt-1">Zero middlemen, items given directly</div>
                            </div>
                            <div class="border-l-4 border-amberAccent-500 pl-4 py-2">
                                <div class="font-bold text-slate-900">Occasion Driven</div>
                                <div class="text-slate-500 text-xs mt-1">Tailored for every specific festival</div>
                            </div>
                        </div>
                    </div>

                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1593113598332-cd288d649433?q=80&w=800&auto=format&fit=crop" alt="Volunteers distributing food" class="rounded-3xl shadow-xl w-full">
                        <div class="absolute -bottom-6 -left-6 bg-white p-6 rounded-2xl shadow-xl border border-slate-100 hidden sm:block max-w-xs">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-full bg-emerald-100 text-emerald-600 flex items-center justify-center text-lg">
                                    <i class="fa-solid fa-heart"></i>
                                </div>
                                <div>
                                    <div class="font-bold text-slate-900 text-sm">Driven by Passion</div>
                                    <div class="text-xs text-slate-500">100% Volunteer Backed</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Core Values -->
                <div class="mt-20">
                    <div class="text-center mb-12">
                        <h2 class="text-3xl font-bold font-heading text-slate-900">Our Core Principles</h2>
                    </div>

                    <div class="grid md:grid-cols-3 gap-8">
                        <div class="bg-white p-8 rounded-3xl border border-slate-200 shadow-sm text-center">
                            <div class="w-14 h-14 bg-brand-100 text-brand-600 rounded-2xl flex items-center justify-center text-2xl mx-auto mb-4">
                                <i class="fa-solid fa-handshake"></i>
                            </div>
                            <h3 class="text-xl font-bold text-slate-900 mb-2">Empathy First</h3>
                            <p class="text-slate-600 text-sm leading-relaxed">We respect the self-esteem of every beneficiary, ensuring distribution is done with love and dignity.</p>
                        </div>

                        <div class="bg-white p-8 rounded-3xl border border-slate-200 shadow-sm text-center">
                            <div class="w-14 h-14 bg-amber-100 text-amber-600 rounded-2xl flex items-center justify-center text-2xl mx-auto mb-4">
                                <i class="fa-solid fa-eye"></i>
                            </div>
                            <h3 class="text-xl font-bold text-slate-900 mb-2">Complete Transparency</h3>
                            <p class="text-slate-600 text-sm leading-relaxed">Every item, contribution, and drive is documented and shared with our supporters and community.</p>
                        </div>

                        <div class="bg-white p-8 rounded-3xl border border-slate-200 shadow-sm text-center">
                            <div class="w-14 h-14 bg-emerald-100 text-emerald-600 rounded-2xl flex items-center justify-center text-2xl mx-auto mb-4">
                                <i class="fa-solid fa-people-group"></i>
                            </div>
                            <h3 class="text-xl font-bold text-slate-900 mb-2">Community Inclusion</h3>
                            <p class="text-slate-600 text-sm leading-relaxed">No festival or milestone is complete without making our surrounding underprivileged neighbors part of it.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- PAGE 3: OUR MISSION -->
        <section id="page-mission" class="page-section">
            <div class="bg-brand-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Our Mission</h1>
                    <p class="text-brand-200 mt-2 text-lg">Empowering Underprivileged Lives Through Timely Support</p>
                </div>
            </div>

            <div class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="max-w-3xl mx-auto space-y-8">
                    <div class="bg-white p-8 sm:p-10 rounded-3xl border border-slate-200 shadow-sm space-y-4">
                        <div class="inline-block p-3 bg-brand-50 rounded-2xl text-brand-600 text-2xl font-bold">
                            <i class="fa-solid fa-bullseye"></i>
                        </div>
                        <h2 class="text-2xl font-bold font-heading text-slate-900">The Seaborne Care Mission Statement</h2>
                        <p class="text-slate-600 leading-relaxed">
                            Our mission is to eliminate feelings of deprivation among underprivileged children and families during celebratory occasions. We systematically collect, procure, and distribute essential survival items, educational tools, festive clothes, warm gear, and nutrition—ensuring no individual is forgotten during times of nationwide joy.
                        </p>
                    </div>

                    <div class="grid sm:grid-cols-2 gap-6">
                        <div class="bg-white p-6 rounded-2xl border border-slate-200">
                            <i class="fa-solid fa-shirt text-brand-600 text-2xl mb-3"></i>
                            <h3 class="font-bold text-slate-900 text-lg">Clothing & Footwear</h3>
                            <p class="text-slate-500 text-sm mt-1">Providing new and clean festive clothes, footwear, and protective winter gear.</p>
                        </div>

                        <div class="bg-white p-6 rounded-2xl border border-slate-200">
                            <i class="fa-solid fa-utensils text-amber-500 text-2xl mb-3"></i>
                            <h3 class="font-bold text-slate-900 text-lg">Nutrition & Sweets</h3>
                            <p class="text-slate-500 text-sm mt-1">Distributing fresh meals, festive sweets, ration kits, and clean drinking water.</p>
                        </div>

                        <div class="bg-white p-6 rounded-2xl border border-slate-200">
                            <i class="fa-solid fa-graduation-cap text-emerald-600 text-2xl mb-3"></i>
                            <h3 class="font-bold text-slate-900 text-lg">Kids Education Kits</h3>
                            <p class="text-slate-500 text-sm mt-1">Gifting books, stationery kits, bags, and toys on birthdays & children's days.</p>
                        </div>

                        <div class="bg-white p-6 rounded-2xl border border-slate-200">
                            <i class="fa-solid fa-sun text-rose-500 text-2xl mb-3"></i>
                            <h3 class="font-bold text-slate-900 text-lg">Seasonal Relief</h3>
                            <p class="text-slate-500 text-sm mt-1">Warm blankets in winter, cooling refreshments in summer, and rain gear in monsoon.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- PAGE 4: OUR VISION -->
        <section id="page-vision" class="page-section">
            <div class="bg-gradient-to-r from-slate-900 via-brand-900 to-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Our Vision</h1>
                    <p class="text-slate-300 mt-2 text-lg">A World Where Every Heart Celebrates</p>
                </div>
            </div>

            <div class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="max-w-4xl mx-auto bg-white p-8 sm:p-12 rounded-3xl border border-slate-200 shadow-lg text-center space-y-6">
                    <div class="w-20 h-20 bg-amber-100 text-amber-600 rounded-full flex items-center justify-center text-3xl mx-auto mb-4">
                        <i class="fa-solid fa-eye"></i>
                    </div>
                    <h2 class="text-3xl font-extrabold font-heading text-slate-900">Looking Into The Future</h2>
                    <p class="text-slate-600 text-lg leading-relaxed">
                        We envision a society where socio-economic status does not dictate whether a child gets to smile on their birthday or whether a family gets to light up their home on Diwali.
                    </p>
                    <p class="text-slate-600 leading-relaxed">
                        Our ultimate vision is to scale <strong class="text-slate-900">Seaborne Care</strong> into a nationwide network of compassionate volunteers, enabling seamless distribution drives across every city, town, and village during all major occasions.
                    </p>
                    
                    <div class="pt-6 border-t border-slate-100 grid sm:grid-cols-3 gap-6 text-center">
                        <div>
                            <div class="text-2xl font-bold text-brand-600">Zero Exclusion</div>
                            <div class="text-xs text-slate-500 mt-1">Reaching the most neglected pockets</div>
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-brand-600">Active Youth</div>
                            <div class="text-xs text-slate-500 mt-1">Mobilizing young volunteers daily</div>
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-brand-600">Year-Round Care</div>
                            <div class="text-xs text-slate-500 mt-1">Continuous seasonal support</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- PAGE 5: OCCASIONS & GALLERY -->
        <section id="page-occasions" class="page-section">
            <div class="bg-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Occasions We Celebrate</h1>
                    <p class="text-slate-400 mt-2 text-lg">Bringing Sunshine to Every Event & Festival</p>
                </div>
            </div>

            <div class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- New Year -->
                    <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-md transition">
                        <img src="https://images.unsplash.com/photo-1544027993-37dbfe43562a?q=80&w=800&auto=format&fit=crop" class="w-full h-48 object-cover" alt="New Year Drive">
                        <div class="p-6">
                            <span class="text-xs font-bold text-sky-600 uppercase tracking-wider">January Drive</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">New Year & Winter Relief</h3>
                            <p class="text-slate-600 text-sm mt-2">Distributing heavy blankets, warm coats, caps, and hot soups to night-shelter residents and street families.</p>
                        </div>
                    </div>

                    <!-- Holi -->
                    <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-md transition">
                        <img src="https://images.unsplash.com/photo-1576487248805-cc291bac5b61?q=80&w=800&auto=format&fit=crop" class="w-full h-48 object-cover" alt="Holi Drive">
                        <div class="p-6">
                            <span class="text-xs font-bold text-rose-500 uppercase tracking-wider">Spring Festival</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">Holi Colors of Harmony</h3>
                            <p class="text-slate-600 text-sm mt-2">Distributing herbal organic gulal, pichkaris, and festive snacks so slum children experience a joyful Holi.</p>
                        </div>
                    </div>

                    <!-- Birthdays -->
                    <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-md transition">
                        <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?q=80&w=800&auto=format&fit=crop" class="w-full h-48 object-cover" alt="Birthday Drive">
                        <div class="p-6">
                            <span class="text-xs font-bold text-amber-600 uppercase tracking-wider">Year-Round</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">Birthday Joy Kits</h3>
                            <p class="text-slate-600 text-sm mt-2">Custom birthday celebrations for underprivileged children featuring cakes, balloons, school bags, and stationery sets.</p>
                        </div>
                    </div>

                    <!-- Dussehra -->
                    <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-md transition">
                        <img src="https://images.unsplash.com/photo-1605810230434-7631ac76ec81?q=80&w=800&auto=format&fit=crop" class="w-full h-48 object-cover" alt="Dussehra Drive">
                        <div class="p-6">
                            <span class="text-xs font-bold text-purple-600 uppercase tracking-wider">Autumn Festival</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">Dussehra Food & Clothes</h3>
                            <p class="text-slate-600 text-sm mt-2">Celebrating victory of good over evil by sharing wholesome meals, footwear, and new clothes with laborers.</p>
                        </div>
                    </div>

                    <!-- Diwali -->
                    <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-md transition">
                        <img src="https://images.unsplash.com/photo-1514222709107-a180c68d72b4?q=80&w=800&auto=format&fit=crop" class="w-full h-48 object-cover" alt="Diwali Drive">
                        <div class="p-6">
                            <span class="text-xs font-bold text-amber-500 uppercase tracking-wider">Festival of Lights</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">Diwali Sweet Hampers</h3>
                            <p class="text-slate-600 text-sm mt-2">Distributing traditional sweets, brass/earthen diyas, oil, and new traditional clothing to lighten up every home.</p>
                        </div>
                    </div>

                    <!-- Special Occasions -->
                    <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-sm hover:shadow-md transition">
                        <img src="https://images.unsplash.com/photo-1488521787991-ed7bbaae773c?q=80&w=800&auto=format&fit=crop" class="w-full h-48 object-cover" alt="Special Drives">
                        <div class="p-6">
                            <span class="text-xs font-bold text-emerald-600 uppercase tracking-wider">Custom Milestones</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">Anniversaries & Memory Drives</h3>
                            <p class="text-slate-600 text-sm mt-2">Custom distribution drives sponsored by individuals celebrating wedding anniversaries or remembering loved ones.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- PAGE 6: FAQ PAGE -->
        <section id="page-faq" class="page-section">
            <div class="bg-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Frequently Asked Questions</h1>
                    <p class="text-slate-400 mt-2 text-lg">Everything you need to know about Seaborne Care</p>
                </div>
            </div>

            <div class="py-16 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="space-y-4">

                    <!-- FAQ 1 -->
                    <div class="bg-white rounded-2xl border border-slate-200 overflow-hidden">
                        <button onclick="toggleFaq(1)" class="w-full text-left p-6 font-bold text-slate-900 text-lg flex justify-between items-center gap-4">
                            <span>How does Seaborne Care organize distribution drives?</span>
                            <i id="faq-icon-1" class="fa-solid fa-chevron-down text-brand-600 transition-transform"></i>
                        </button>
                        <div id="faq-answer-1" class="hidden px-6 pb-6 text-slate-600 leading-relaxed text-sm border-t border-slate-100 pt-4">
                            Prior to every major occasion (Diwali, Holi, New Year, etc.), our team surveys target locations like shelter homes, slum clusters, and street setups. We identify exact requirements (clothes sizes, blanket counts, ration needs) and assemble customized gift kits for direct distribution.
                        </div>
                    </div>

                    <!-- FAQ 2 -->
                    <div class="bg-white rounded-2xl border border-slate-200 overflow-hidden">
                        <button onclick="toggleFaq(2)" class="w-full text-left p-6 font-bold text-slate-900 text-lg flex justify-between items-center gap-4">
                            <span>Can I sponsor a distribution drive on my Birthday or Anniversary?</span>
                            <i id="faq-icon-2" class="fa-solid fa-chevron-down text-brand-600 transition-transform"></i>
                        </button>
                        <div id="faq-answer-2" class="hidden px-6 pb-6 text-slate-600 leading-relaxed text-sm border-t border-slate-100 pt-4">
                            Yes, absolutely! You can sponsor sweets, food boxes, stationery kits, or clothes on your special day. Contact us directly via WhatsApp at <strong>9650285586</strong> or email <strong>Care@seabornemcs.in</strong> to plan your drive.
                        </div>
                    </div>

                    <!-- FAQ 3 -->
                    <div class="bg-white rounded-2xl border border-slate-200 overflow-hidden">
                        <button onclick="toggleFaq(3)" class="w-full text-left p-6 font-bold text-slate-900 text-lg flex justify-between items-center gap-4">
                            <span>How can I join Seaborne Care as a volunteer?</span>
                            <i id="faq-icon-3" class="fa-solid fa-chevron-down text-brand-600 transition-transform"></i>
                        </button>
                        <div id="faq-answer-3" class="hidden px-6 pb-6 text-slate-600 leading-relaxed text-sm border-t border-slate-100 pt-4">
                            We welcome passionate volunteers! You can assist in packing festive kits, managing logistics on-site, or spreading awareness. Reach out to us through our Contact page or WhatsApp us to get added to our volunteer list.
                        </div>
                    </div>

                    <!-- FAQ 4 -->
                    <div class="bg-white rounded-2xl border border-slate-200 overflow-hidden">
                        <button onclick="toggleFaq(4)" class="w-full text-left p-6 font-bold text-slate-900 text-lg flex justify-between items-center gap-4">
                            <span>Are items distributed brand new or gently used?</span>
                            <i id="faq-icon-4" class="fa-solid fa-chevron-down text-brand-600 transition-transform"></i>
                        </button>
                        <div id="faq-answer-4" class="hidden px-6 pb-6 text-slate-600 leading-relaxed text-sm border-t border-slate-100 pt-4">
                            For festive occasions like Diwali and New Year, we prioritize brand new clothes, sweets, and educational materials. In blanket or coat drives, we ensure all items are either brand new or thoroughly sanitized and in excellent condition.
                        </div>
                    </div>

                    <!-- FAQ 5 -->
                    <div class="bg-white rounded-2xl border border-slate-200 overflow-hidden">
                        <button onclick="toggleFaq(5)" class="w-full text-left p-6 font-bold text-slate-900 text-lg flex justify-between items-center gap-4">
                            <span>Where is Seaborne Care located?</span>
                            <i id="faq-icon-5" class="fa-solid fa-chevron-down text-brand-600 transition-transform"></i>
                        </button>
                        <div id="faq-answer-5" class="hidden px-6 pb-6 text-slate-600 leading-relaxed text-sm border-t border-slate-100 pt-4">
                            We operate across multiple city hubs through local volunteer coordinators. For official inquiries, write to <strong>Care@seabornemcs.in</strong> or call/WhatsApp <strong>9650285586</strong>.
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- PAGE 7: CONTACT US PAGE -->
        <section id="page-contact" class="page-section">
            <div class="bg-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Contact Seaborne Care</h1>
                    <p class="text-slate-400 mt-2 text-lg">Get in touch to support, partner, or volunteer</p>
                </div>
            </div>

            <div class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-12 gap-12">
                    
                    <!-- Direct Contact Details -->
                    <div class="lg:col-span-5 space-y-6">
                        <div class="bg-white p-8 rounded-3xl border border-slate-200 shadow-sm space-y-6">
                            <h2 class="text-2xl font-bold font-heading text-slate-900">Reach Us Directly</h2>
                            <p class="text-slate-600 text-sm">Feel free to message or call us anytime for drive updates or collaboration.</p>

                            <!-- WhatsApp Direct Card -->
                            <a href="https://wa.me/919650285586" target="_blank" class="flex items-center gap-4 p-4 rounded-2xl bg-emerald-50 border border-emerald-200 hover:bg-emerald-100 transition group">
                                <div class="w-12 h-12 rounded-xl bg-emerald-600 text-white flex items-center justify-center text-2xl group-hover:scale-105 transition">
                                    <i class="fa-brands fa-whatsapp"></i>
                                </div>
                                <div>
                                    <div class="text-xs font-bold text-emerald-800 uppercase tracking-wider">WhatsApp Contact</div>
                                    <div class="text-lg font-extrabold text-slate-900">+91 9650285586</div>
                                    <div class="text-xs text-emerald-700 mt-0.5">Click to open chat instantly</div>
                                </div>
                            </a>

                            <!-- Email Direct Card -->
                            <a href="mailto:Care@seabornemcs.in" class="flex items-center gap-4 p-4 rounded-2xl bg-sky-50 border border-sky-200 hover:bg-sky-100 transition group">
                                <div class="w-12 h-12 rounded-xl bg-brand-600 text-white flex items-center justify-center text-xl group-hover:scale-105 transition">
                                    <i class="fa-solid fa-envelope"></i>
                                </div>
                                <div>
                                    <div class="text-xs font-bold text-brand-800 uppercase tracking-wider">Email Address</div>
                                    <div class="text-base font-extrabold text-slate-900 break-all">Care@seabornemcs.in</div>
                                    <div class="text-xs text-brand-700 mt-0.5">Click to send an email</div>
                                </div>
                            </a>

                            <div class="pt-4 border-t border-slate-100">
                                <div class="font-bold text-slate-900 mb-2">Operational Hours</div>
                                <div class="text-sm text-slate-600">Monday – Sunday: 9:00 AM – 8:00 PM IST</div>
                            </div>
                        </div>
                    </div>

                    <!-- Form -->
                    <div class="lg:col-span-7">
                        <div class="bg-white p-8 sm:p-10 rounded-3xl border border-slate-200 shadow-sm">
                            <h2 class="text-2xl font-bold font-heading text-slate-900 mb-6">Send Us A Message</h2>
                            
                            <form id="contactForm" onsubmit="handleFormSubmit(event)" class="space-y-5">
                                <div class="grid sm:grid-cols-2 gap-5">
                                    <div>
                                        <label class="block text-xs font-bold uppercase text-slate-600 mb-2">Your Name *</label>
                                        <input type="text" required placeholder="John Doe" class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-brand-600">
                                    </div>
                                    <div>
                                        <label class="block text-xs font-bold uppercase text-slate-600 mb-2">Phone / WhatsApp *</label>
                                        <input type="tel" required placeholder="9650285586" class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-brand-600">
                                    </div>
                                </div>

                                <div>
                                    <label class="block text-xs font-bold uppercase text-slate-600 mb-2">Email Address *</label>
                                    <input type="email" required placeholder="you@example.com" class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-brand-600">
                                </div>

                                <div>
                                    <label class="block text-xs font-bold uppercase text-slate-600 mb-2">Occasion / Support Type</label>
                                    <select class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-brand-600 text-slate-700">
                                        <option value="Diwali">Diwali Support Drive</option>
                                        <option value="Holi">Holi Colors & Joy</option>
                                        <option value="NewYear">New Year / Winter Blanket</option>
                                        <option value="Birthday">Personal Birthday Sponsorship</option>
                                        <option value="Volunteer">Want to Volunteer</option>
                                        <option value="General">General Inquiry</option>
                                    </select>
                                </div>

                                <div>
                                    <label class="block text-xs font-bold uppercase text-slate-600 mb-2">Message *</label>
                                    <textarea required rows="4" placeholder="How would you like to collaborate or contribute?" class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-brand-600"></textarea>
                                </div>

                                <button type="submit" class="w-full bg-brand-600 hover:bg-brand-700 text-white font-bold py-3.5 rounded-xl transition shadow-md flex items-center justify-center gap-2">
                                    <i class="fa-solid fa-paper-plane"></i>
                                    <span>Send Message</span>
                                </button>
                            </form>

                            <!-- Success message box -->
                            <div id="formSuccess" class="hidden mt-4 p-4 bg-emerald-50 border border-emerald-200 rounded-xl text-emerald-800 text-sm font-semibold text-center">
                                Thank you! Your message has been received. We will connect with you via WhatsApp/Email shortly.
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- PAGE 8: PRIVACY POLICY -->
        <section id="page-privacy" class="page-section">
            <div class="bg-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Privacy Policy</h1>
                    <p class="text-slate-400 mt-2 text-sm">Last Updated: October 2026</p>
                </div>
            </div>

            <div class="py-16 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-slate-700 leading-relaxed space-y-6 bg-white my-8 p-8 sm:p-12 rounded-3xl border border-slate-200 shadow-sm">
                <h2 class="text-2xl font-bold text-slate-900">1. Commitment to Privacy</h2>
                <p>Seaborne Care ("we", "our", "us") values your privacy. This policy details how we collect, use, and protect information when you visit our website or interact with our distribution drives.</p>

                <h2 class="text-2xl font-bold text-slate-900">2. Information Collection</h2>
                <p>We only collect personal information that you voluntarily provide when contacting us through WhatsApp (+91 9650285586), Email (Care@seabornemcs.in), or our contact forms. This may include your Name, Phone Number, Email Address, and event details.</p>

                <h2 class="text-2xl font-bold text-slate-900">3. Use of Information</h2>
                <p>Your details are used solely for coordinating distribution drives, sharing updates regarding sponsored events, and responding to your inquiries. We do NOT sell, rent, or trade your personal data to third parties.</p>

                <h2 class="text-2xl font-bold text-slate-900">4. Photos & Media Privacy</h2>
                <p>Photos taken during public distribution drives are used strictly for transparency and awareness. If you appear in any photo and wish to have it removed, please email us at Care@seabornemcs.in and we will promptly respect your request.</p>

                <h2 class="text-2xl font-bold text-slate-900">5. Contact Us</h2>
                <p>For any privacy queries, please reach us at Email: <strong>Care@seabornemcs.in</strong> or WhatsApp: <strong>9650285586</strong>.</p>
            </div>
        </section>

        <!-- PAGE 9: TERMS & CONDITIONS -->
        <section id="page-terms" class="page-section">
            <div class="bg-slate-900 text-white py-16">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                    <h1 class="text-4xl font-extrabold font-heading">Terms & Conditions</h1>
                    <p class="text-slate-400 mt-2 text-sm">Last Updated: October 2026</p>
                </div>
            </div>

            <div class="py-16 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-slate-700 leading-relaxed space-y-6 bg-white my-8 p-8 sm:p-12 rounded-3xl border border-slate-200 shadow-sm">
                <h2 class="text-2xl font-bold text-slate-900">1. Website Usage Terms</h2>
                <p>By accessing the Seaborne Care website, you agree to comply with these terms. All content provided on this website is for informational and non-profit welfare awareness purposes.</p>

                <h2 class="text-2xl font-bold text-slate-900">2. Donations & In-Kind Contributions</h2>
                <p>All item distributions (sweets, clothes, blankets, stationery) are carried out directly by Seaborne Care team members and volunteers. We maintain 100% transparency. Items contributed for specific occasions (Diwali, Holi, Birthdays) are directed strictly toward designated beneficiaries.</p>

                <h2 class="text-2xl font-bold text-slate-900">3. Volunteer Guidelines</h2>
                <p>Volunteers participating in Seaborne Care drives are expected to maintain respectful and compassionate conduct toward all beneficiaries and community members.</p>

                <h2 class="text-2xl font-bold text-slate-900">4. Modifications</h2>
                <p>Seaborne Care reserves the right to update these terms at any time. Any changes will be reflected directly on this page.</p>

                <h2 class="text-2xl font-bold text-slate-900">5. Contact</h2>
                <p>Questions regarding terms can be sent to <strong>Care@seabornemcs.in</strong> or via phone at <strong>9650285586</strong>.</p>
            </div>
        </section>

    </main>

    <!-- Professional Footer -->
    <footer class="bg-slate-950 text-slate-400 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-12 gap-10">
                
                <!-- Brand Info -->
                <div class="lg:col-span-4 space-y-4">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-xl bg-brand-600 flex items-center justify-center text-white">
                            <i class="fa-solid fa-hand-holding-heart text-xl"></i>
                        </div>
                        <span class="text-2xl font-extrabold text-white font-heading">
                            Seaborne <span class="text-brand-500">Care</span>
                        </span>
                    </div>
                    <p class="text-sm leading-relaxed text-slate-400">
                        Seaborne Care is a dedicated non-profit social initiative distributing smiles, essential supplies, warm clothing, and festive kits to underprivileged communities across every festival and occasion.
                    </p>
                    <div class="flex gap-3 text-slate-400 pt-2">
                        <a href="https://wa.me/919650285586" target="_blank" class="w-9 h-9 rounded-full bg-slate-900 hover:bg-emerald-600 hover:text-white flex items-center justify-center transition border border-slate-800">
                            <i class="fa-brands fa-whatsapp"></i>
                        </a>
                        <a href="mailto:Care@seabornemcs.in" class="w-9 h-9 rounded-full bg-slate-900 hover:bg-brand-600 hover:text-white flex items-center justify-center transition border border-slate-800">
                            <i class="fa-solid fa-envelope"></i>
                        </a>
                    </div>
                </div>

                <!-- Quick Navigation Links -->
                <div class="lg:col-span-2 space-y-3">
                    <div class="text-white font-bold text-sm uppercase tracking-wider">Pages</div>
                    <ul class="space-y-2 text-sm">
                        <li><button onclick="navigateTo('home')" class="hover:text-amberAccent-400 transition">Home</button></li>
                        <li><button onclick="navigateTo('about')" class="hover:text-amberAccent-400 transition">About Us</button></li>
                        <li><button onclick="navigateTo('mission')" class="hover:text-amberAccent-400 transition">Our Mission</button></li>
                        <li><button onclick="navigateTo('vision')" class="hover:text-amberAccent-400 transition">Our Vision</button></li>
                        <li><button onclick="navigateTo('occasions')" class="hover:text-amberAccent-400 transition">Occasions</button></li>
                    </ul>
                </div>

                <!-- Legal & Help -->
                <div class="lg:col-span-3 space-y-3">
                    <div class="text-white font-bold text-sm uppercase tracking-wider">Help & Policy</div>
                    <ul class="space-y-2 text-sm">
                        <li><button onclick="navigateTo('faq')" class="hover:text-amberAccent-400 transition">FAQ</button></li>
                        <li><button onclick="navigateTo('contact')" class="hover:text-amberAccent-400 transition">Contact Us</button></li>
                        <li><button onclick="navigateTo('privacy')" class="hover:text-amberAccent-400 transition">Privacy Policy</button></li>
                        <li><button onclick="navigateTo('terms')" class="hover:text-amberAccent-400 transition">Terms & Conditions</button></li>
                    </ul>
                </div>

                <!-- Direct Contact Info -->
                <div class="lg:col-span-3 space-y-3">
                    <div class="text-white font-bold text-sm uppercase tracking-wider">Contact Seaborne Care</div>
                    <div class="space-y-3 text-sm">
                        <a href="https://wa.me/919650285586" target="_blank" class="flex items-center gap-3 text-slate-300 hover:text-emerald-400 transition">
                            <i class="fa-brands fa-whatsapp text-emerald-500 text-lg"></i>
                            <span>+91 9650285586</span>
                        </a>
                        <a href="mailto:Care@seabornemcs.in" class="flex items-center gap-3 text-slate-300 hover:text-sky-400 transition break-all">
                            <i class="fa-solid fa-envelope text-brand-500 text-lg"></i>
                            <span>Care@seabornemcs.in</span>
                        </a>
                        <div class="flex items-start gap-3 text-slate-400">
                            <i class="fa-solid fa-heart text-amberAccent-500 text-lg mt-1"></i>
                            <span>Distributing Joy on Diwali, Holi, Birthdays, New Year & Dussehra</span>
                        </div>
                    </div>
                </div>

            </div>

            <!-- Bottom Copyright bar -->
            <div class="mt-12 pt-8 border-t border-slate-900 flex flex-col sm:flex-row justify-between items-center text-xs text-slate-500 gap-4">
                <div>&copy; 2026 Seaborne Care. All Rights Reserved.</div>
                <div class="flex gap-4">
                    <button onclick="navigateTo('privacy')" class="hover:underline">Privacy</button>
                    <span>•</span>
                    <button onclick="navigateTo('terms')" class="hover:underline">Terms</button>
                    <span>•</span>
                    <button onclick="navigateTo('contact')" class="hover:underline">Support</button>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript Logic for Navigation, FAQ & Form -->
    <script>
        // Page Navigation Logic
        function navigateTo(pageId) {
            // Hide all pages
            const pages = document.querySelectorAll('.page-section');
            pages.forEach(p => p.classList.remove('active'));

            // Show selected page
            const targetPage = document.getElementById('page-' + pageId);
            if (targetPage) {
                targetPage.classList.add('active');
            } else {
                document.getElementById('page-home').classList.add('active');
            }

            // Highlight Active Nav Button
            const navBtns = document.querySelectorAll('.nav-btn');
            navBtns.forEach(btn => {
                if (btn.getAttribute('data-page') === pageId) {
                    btn.classList.add('text-brand-600', 'bg-brand-50', 'font-bold');
                } else {
                    btn.classList.remove('text-brand-600', 'bg-brand-50', 'font-bold');
                }
            });

            // Close mobile menu if open
            const mobileMenu = document.getElementById('mobileMenu');
            if (mobileMenu) mobileMenu.classList.add('hidden');

            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Toggle Mobile Navigation
        function toggleMobileMenu() {
            const mobileMenu = document.getElementById('mobileMenu');
            mobileMenu.classList.toggle('hidden');
        }

        // Toggle FAQ Accordion
        function toggleFaq(id) {
            const answer = document.getElementById('faq-answer-' + id);
            const icon = document.getElementById('faq-icon-' + id);
            
            if (answer.classList.contains('hidden')) {
                answer.classList.remove('hidden');
                icon.style.transform = 'rotate(180deg)';
            } else {
                answer.classList.add('hidden');
                icon.style.transform = 'rotate(0deg)';
            }
        }

        // Form Submit Handler
        function handleFormSubmit(event) {
            event.preventDefault();
            const successBox = document.getElementById('formSuccess');
            const form = document.getElementById('contactForm');
            
            successBox.classList.remove('hidden');
            form.reset();

            setTimeout(() => {
                successBox.classList.add('hidden');
            }, 6000);
        }

        // Initialize Hash Routing support (e.g. #about)
        window.addEventListener('load', () => {
            const hash = window.location.hash.replace('#', '');
            if (hash) {
                navigateTo(hash);
            }
        });
    </script>
</body>
</html>
