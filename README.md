<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday, Habibah Khoirunnisa Ramadhan ✨</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Canvas Confetti Library -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:ital,wght@0,300;0,400;0,600;0,700;1,400&family=Sacramento&family=Playfair+Display:ital,wght@0,500;0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                        cursive: ['Sacramento', 'cursive'],
                        serif: ['Playfair Display', 'serif'],
                        mono: ['Montserrat', 'sans-serif'],
                    },
                    colors: {
                        roseGold: '#f472b6',
                        roseAccent: '#fb7185',
                        midnight: '#0b0614',
                        midnightLight: '#180a2b',
                        goldGlow: '#fbbf24',
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'pulse-glow': 'pulseGlow 2.5s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'flicker': 'flicker 0.15s ease-in-out infinite alternate',
                        'spin-slow': 'spin 12s linear infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0px) rotate(0deg)' },
                            '50%': { transform: 'translateY(-12px) rotate(1deg)' },
                        },
                        pulseGlow: {
                            '0%, 100%': { opacity: '1', filter: 'drop-shadow(0 0 20px rgba(244,114,182,0.6))' },
                            '50%': { opacity: '0.6', filter: 'drop-shadow(0 0 8px rgba(244,114,182,0.2))' },
                        },
                        flicker: {
                            '0%': { transform: 'scale(1) rotate(-1deg)', opacity: '0.9' },
                            '100%': { transform: 'scale(1.15) rotate(2deg)', opacity: '1' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #0b0614;
            color: #f3f4f6;
            overflow-x: hidden;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        /* Glassmorphism styling */
        .glass-card {
            background: rgba(24, 10, 43, 0.65);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.12);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.6);
        }

        .glass-card-hover {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .glass-card-hover:hover {
            transform: translateY(-8px) scale(1.02);
            border-color: rgba(244, 114, 182, 0.5);
            box-shadow: 0 25px 50px -12px rgba(244, 114, 182, 0.3);
        }

        /* Glowing text gradient */
        .text-glow-gradient {
            background: linear-gradient(135deg, #ffffff 0%, #f472b6 45%, #e879f9 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 35px rgba(244, 114, 182, 0.4);
        }

        /* Polaroid styling & 3D tilt */
        .polaroid-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.15);
            padding: 12px 12px 20px 12px;
            border-radius: 16px;
            transition: all 0.5s cubic-bezier(0.23, 1, 0.32, 1);
            cursor: pointer;
            box-shadow: 0 15px 35px rgba(0,0,0,0.4);
        }

        .polaroid-card:hover {
            transform: translateY(-12px) rotate(1.5deg) scale(1.03);
            border-color: rgba(244, 114, 182, 0.6);
            box-shadow: 0 25px 50px rgba(244, 114, 182, 0.25);
        }

        /* Candle Flame Styling */
        .flame {
            width: 16px;
            height: 26px;
            background: linear-gradient(to top, #ff4500, #ff8c00, #ffd700, #ffffff);
            border-radius: 50% 50% 35% 35%;
            position: absolute;
            top: -24px;
            left: 50%;
            transform: translateX(-50%);
            box-shadow: 0 0 20px #ff8c00, 0 0 40px #ffd700;
            transform-origin: center bottom;
            animation: flicker 0.15s ease-in-out infinite alternate;
        }

        .flame.extinguished {
            display: none;
        }

        .smoke {
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            width: 8px;
            height: 8px;
            background: rgba(200, 200, 200, 0.6);
            border-radius: 50%;
            opacity: 0;
            pointer-events: none;
        }

        @keyframes rise {
            0% { opacity: 0.8; transform: translate(-50%, 0) scale(1); }
            100% { opacity: 0; transform: translate(-50%, -50px) scale(3.5); }
        }

        .smoke.active {
            animation: rise 2s ease-out forwards;
        }

        /* Envelope Styling */
        .envelope-wrapper {
            perspective: 1000px;
        }

        .envelope {
            position: relative;
            width: 100%;
            max-width: 440px;
            height: 270px;
            background: #25103d;
            border-radius: 16px;
            box-shadow: 0 20px 45px rgba(0,0,0,0.6);
            cursor: pointer;
            transition: transform 0.6s ease;
        }

        .envelope-flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 220px solid transparent;
            border-right: 220px solid transparent;
            border-top: 145px solid #361758;
            transform-origin: top;
            transition: transform 0.6s ease, z-index 0.6s ease;
            z-index: 3;
        }

        .envelope.open .envelope-flap {
            transform: rotateX(180deg);
            z-index: 1;
        }

        /* Equalizer Bars */
        .eq-bar {
            width: 3px;
            height: 16px;
            background-color: #f472b6;
            border-radius: 2px;
            transition: height 0.2s ease;
        }

        /* Scrollbar aesthetics */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0b0614;
        }
        ::-webkit-scrollbar-thumb {
            background: #3b1d5c;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #f472b6;
        }
    </style>
</head>
<body class="relative min-h-screen text-slate-100 selection:bg-roseGold selection:text-white">

    <!-- Interactive Background Particle Canvas -->
    <canvas id="starCanvas" class="fixed inset-0 pointer-events-none z-0"></canvas>

    <!-- Floating Top Toolbar (Music & Upload Button) -->
    <div class="fixed top-4 left-4 right-4 z-50 flex items-center justify-between max-w-5xl mx-auto pointer-events-none">
        
        <!-- Local Photo Input Trigger -->
        <label for="localPhotoInput" class="pointer-events-auto cursor-pointer glass-card px-4 py-2 rounded-full flex items-center space-x-2 text-xs font-semibold text-roseGold hover:border-roseGold hover:text-white transition-all duration-300 shadow-xl group">
            <svg class="w-4 h-4 text-roseGold group-hover:scale-110 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
            </svg>
            <span class="hidden sm:inline">📷 Upload / Pilih Foto Habibah</span>
            <span class="sm:hidden">📷 Pilih Foto</span>
            <input type="file" id="localPhotoInput" accept="image/*" multiple class="hidden" onchange="handleUserPhotoUpload(event)">
        </label>

        <!-- Music Controller Button -->
        <button id="musicToggleBtn" onclick="toggleAudio()" class="pointer-events-auto glass-card px-4 py-2 rounded-full flex items-center space-x-3 hover:border-roseGold transition-all duration-300 shadow-xl group">
            <div id="equalizer" class="flex items-end space-x-1 h-4">
                <div class="eq-bar h-2"></div>
                <div class="eq-bar h-4"></div>
                <div class="eq-bar h-3"></div>
                <div class="eq-bar h-1"></div>
            </div>
            <span id="musicStatus" class="text-xs font-semibold tracking-wider uppercase text-slate-300 group-hover:text-white">Putar Musik 🎵</span>
        </button>
    </div>

    <!-- Main Content Layout -->
    <main class="relative z-10 max-w-5xl mx-auto px-4 py-16 md:py-24 flex flex-col items-center space-y-28">

        <!-- Hero Section -->
        <section class="text-center space-y-8 pt-4 w-full max-w-3xl flex flex-col items-center">
            
            <!-- Glowing Profile Picture Frame -->
            <div class="relative group">
                <div class="absolute -inset-1.5 bg-gradient-to-r from-roseGold via-purple-500 to-roseAccent rounded-full blur-xl opacity-75 group-hover:opacity-100 transition duration-1000 group-hover:duration-200 animate-pulse-glow"></div>
                <div class="relative w-36 h-36 sm:w-44 sm:h-44 rounded-full p-1 bg-gradient-to-tr from-roseGold via-purple-600 to-amber-300 shadow-2xl overflow-hidden">
                    <img id="profileHeaderImg" src="foto1.jpg" alt="Habibah Khoirunnisa Ramadhan" onerror="this.src='https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=800&q=80'" class="w-full h-full object-cover rounded-full transform group-hover:scale-105 transition duration-500">
                </div>
                <!-- Floating Heart Badge -->
                <div class="absolute bottom-1 right-1 bg-roseGold text-white p-2 rounded-full shadow-lg animate-bounce">
                    ✨
                </div>
            </div>

            <!-- Greeting Badge -->
            <div class="inline-flex items-center space-x-2 px-4 py-1.5 rounded-full glass-card border border-roseGold/30 text-roseGold text-xs font-medium tracking-widest uppercase">
                <span>✨ A Moment to Celebrate ✨</span>
            </div>

            <!-- Main Heading with Typing Effect -->
            <div class="space-y-3">
                <h1 class="text-3xl sm:text-5xl md:text-6xl font-bold tracking-tight leading-tight">
                    <span class="block text-slate-300 text-xl sm:text-2xl md:text-3xl font-light mb-2">Selamat Ulang Tahun,</span>
                    <span id="typedName" class="text-glow-gradient font-serif"></span>
                </h1>
                <p class="text-slate-300 text-sm sm:text-base max-w-xl mx-auto font-light leading-relaxed pt-2">
                    Hari ini adalah perayaan untuk kepribadian yang selalu memancarkan keanggunan, kehangatan, dan ketulusan. Semoga usiamu yang baru diliputi kebahagiaan sejati.
                </p>
            </div>

            <!-- Dedicated By Tag -->
            <div class="pt-2 text-slate-400 text-xs sm:text-sm font-medium">
                Persembahan tulus & doa terbaik dari <span class="text-roseGold font-semibold underline decoration-roseGold/40 underline-offset-4">Rifqi Bilal Afriza</span>
            </div>

            <!-- Scroll Indicator -->
            <div class="pt-6">
                <a href="#gallery" class="text-slate-400 hover:text-roseGold transition-colors flex flex-col items-center space-y-2 text-xs uppercase tracking-widest">
                    <span>Jelajahi Galeri & Pesona</span>
                    <svg class="w-5 h-5 animate-bounce" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
                </a>
            </div>
        </section>

        <!-- Interactive Gallery & Photo Banner Notice -->
        <section id="gallery" class="w-full space-y-8 scroll-mt-24">
            <div class="text-center space-y-3">
                <span class="text-xs font-semibold tracking-widest text-roseGold uppercase">Galeri Kenangan & Pesona</span>
                <h2 class="text-2xl sm:text-4xl font-bold text-slate-100 font-serif">Sosok Anggun dalam Ingatan 📸</h2>
                <p class="text-slate-400 text-sm max-w-lg mx-auto">Klik pada foto mana saja untuk melihat tampilan penuh, atau gunakan tombol di bawah untuk memuat foto langsung dari galeri HP/Laptopmu!</p>
            </div>

            <!-- Photo Upload Helper Card -->
            <div class="glass-card rounded-2xl p-4 sm:p-6 text-center max-w-xl mx-auto border border-roseGold/30 flex flex-col items-center space-y-3 shadow-2xl">
                <div class="text-xs text-slate-300 font-medium">
                    ✨ <span class="text-roseGold font-semibold">Tips Spesial:</span> Kamu bisa memilih 5 foto Habibah sekaligus dari HP/Laptop agar langsung terpasang cantik di preview ini!
                </div>
                <label for="localPhotoInputBanner" class="cursor-pointer px-6 py-2.5 rounded-full bg-gradient-to-r from-roseGold to-purple-600 text-white font-semibold text-xs shadow-lg hover:scale-105 active:scale-95 transition-all flex items-center space-x-2">
                    <span>📁 Pilih / Ganti 5 Foto dari Perangkat</span>
                    <input type="file" id="localPhotoInputBanner" accept="image/*" multiple class="hidden" onchange="handleUserPhotoUpload(event)">
                </label>
            </div>

            <!-- 5 Photo Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 px-2">
                
                <!-- Photo 1 -->
                <div onclick="openLightbox(0)" class="polaroid-card group">
                    <div class="relative w-full h-72 sm:h-80 rounded-xl overflow-hidden bg-slate-900 mb-3">
                        <img id="cardImg0" src="foto1.jpg" alt="Anggun & Penuh Pesona" onerror="this.src='https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=800&q=80'" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4">
                            <span class="text-xs text-roseGold font-mono">Klik untuk memperbesar 🔍</span>
                        </div>
                    </div>
                    <div class="text-center space-y-1">
                        <h3 class="text-slate-200 font-serif text-base font-semibold">Anggun & Penuh Pesona ✨</h3>
                        <p class="text-xs text-slate-400 font-light">Kehangatan pancaran senyum yang selalu menenangkan.</p>
                    </div>
                </div>

                <!-- Photo 2 -->
                <div onclick="openLightbox(1)" class="polaroid-card group">
                    <div class="relative w-full h-72 sm:h-80 rounded-xl overflow-hidden bg-slate-900 mb-3">
                        <img id="cardImg1" src="foto2.jpg" alt="Senyuman Manis" onerror="this.src='https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=800&q=80'" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4">
                            <span class="text-xs text-roseGold font-mono">Klik untuk memperbesar 🔍</span>
                        </div>
                    </div>
                    <div class="text-center space-y-1">
                        <h3 class="text-slate-200 font-serif text-base font-semibold">Senyuman Manis 🌟</h3>
                        <p class="text-xs text-slate-400 font-light">Sinar kebahagiaan yang senantiasa hadir dalam setiap momen.</p>
                    </div>
                </div>

                <!-- Photo 3 -->
                <div onclick="openLightbox(2)" class="polaroid-card group">
                    <div class="relative w-full h-72 sm:h-80 rounded-xl overflow-hidden bg-slate-900 mb-3">
                        <img id="cardImg2" src="foto3.jpg" alt="Momen Keceriaan" onerror="this.src='https://images.unsplash.com/photo-1524504388940-b1c1722653e1?auto=format&fit=crop&w=800&q=80'" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4">
                            <span class="text-xs text-roseGold font-mono">Klik untuk memperbesar 🔍</span>
                        </div>
                    </div>
                    <div class="text-center space-y-1">
                        <h3 class="text-slate-200 font-serif text-base font-semibold">Momen Keceriaan 🌸</h3>
                        <p class="text-xs text-slate-400 font-light">Canda tawa lepas yang membawa energi positif.</p>
                    </div>
                </div>

                <!-- Photo 4 -->
                <div onclick="openLightbox(3)" class="polaroid-card group sm:col-span-1 lg:col-span-1">
                    <div class="relative w-full h-72 sm:h-80 rounded-xl overflow-hidden bg-slate-900 mb-3">
                        <img id="cardImg3" src="foto4.jpg" alt="Keindahan Sederhana" onerror="this.src='https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&w=800&q=80'" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4">
                            <span class="text-xs text-roseGold font-mono">Klik untuk memperbesar 🔍</span>
                        </div>
                    </div>
                    <div class="text-center space-y-1">
                        <h3 class="text-slate-200 font-serif text-base font-semibold">Keindahan Sederhana 💜</h3>
                        <p class="text-xs text-slate-400 font-light">Keanggunan alami yang memikat dalam ketenangan.</p>
                    </div>
                </div>

                <!-- Photo 5 -->
                <div onclick="openLightbox(4)" class="polaroid-card group sm:col-span-2 lg:col-span-2">
                    <div class="relative w-full h-72 sm:h-80 rounded-xl overflow-hidden bg-slate-900 mb-3">
                        <img id="cardImg4" src="foto5.jpg" alt="Gaya Elegan" onerror="this.src='https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=800&q=80'" class="w-full h-full object-cover group-hover:scale-105 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4">
                            <span class="text-xs text-roseGold font-mono">Klik untuk memperbesar 🔍</span>
                        </div>
                    </div>
                    <div class="text-center space-y-1">
                        <h3 class="text-slate-200 font-serif text-base font-semibold">Gaya Elegan & Menawan 💫</h3>
                        <p class="text-xs text-slate-400 font-light">Pesona istimewa yang senantiasa terpancar dari Habibah.</p>
                    </div>
                </div>

            </div>
        </section>

        <!-- Interactive Birthday Cake Section -->
        <section class="w-full flex flex-col items-center text-center space-y-8">
            <div class="space-y-2">
                <span class="text-xs font-semibold tracking-widest text-roseGold uppercase">Perayaan Ulang Tahun</span>
                <h2 class="text-2xl sm:text-3xl font-bold text-slate-100 font-serif">Kue Ulang Tahun Interaktif 🎂</h2>
                <p class="text-slate-400 text-sm max-w-md">Panjatkan keinginan terbaikmu, lalu tiup lilin ini (bisa dengan tombol atau tiup langsung ke mic HP/Laptop) untuk merayakan momen bahagiamu!</p>
            </div>

            <!-- Cake Container -->
            <div class="relative w-64 h-72 sm:w-72 sm:h-80 flex flex-col items-center justify-end pt-8">
                
                <!-- Candles Glow Aura -->
                <div id="candleAura" class="absolute top-10 w-32 h-32 bg-amber-500/25 rounded-full blur-2xl animate-pulse transition-opacity duration-700"></div>

                <!-- Candles Layer -->
                <div class="flex justify-center space-x-6 z-20 mb-[-10px]">
                    <!-- Candle 1 -->
                    <div class="relative w-4 h-16 bg-gradient-to-t from-pink-500 to-rose-300 rounded-t-sm shadow-md">
                        <div id="flame1" class="flame"></div>
                        <div id="smoke1" class="smoke"></div>
                    </div>
                    <!-- Candle 2 (Center) -->
                    <div class="relative w-4 h-20 bg-gradient-to-t from-purple-500 to-indigo-300 rounded-t-sm shadow-md -translate-y-2">
                        <div id="flame2" class="flame"></div>
                        <div id="smoke2" class="smoke"></div>
                    </div>
                    <!-- Candle 3 -->
                    <div class="relative w-4 h-16 bg-gradient-to-t from-pink-500 to-rose-300 rounded-t-sm shadow-md">
                        <div id="flame3" class="flame"></div>
                        <div id="smoke3" class="smoke"></div>
                    </div>
                </div>

                <!-- Cake Layers -->
                <div class="w-full space-y-1 z-10">
                    <!-- Top Layer -->
                    <div class="w-48 sm:w-56 h-16 mx-auto bg-gradient-to-r from-pink-600 via-rose-400 to-pink-500 rounded-t-2xl relative shadow-lg overflow-hidden border-t border-white/20">
                        <div class="absolute top-0 inset-x-0 h-4 bg-white/80 rounded-b-full shadow-inner flex justify-around">
                            <div class="w-4 h-6 bg-white rounded-b-full"></div>
                            <div class="w-4 h-8 bg-white rounded-b-full"></div>
                            <div class="w-4 h-5 bg-white rounded-b-full"></div>
                            <div class="w-4 h-7 bg-white rounded-b-full"></div>
                        </div>
                    </div>
                    <!-- Middle Layer -->
                    <div class="w-56 sm:w-64 h-16 mx-auto bg-gradient-to-r from-purple-900 via-purple-700 to-purple-900 rounded-t-lg relative shadow-lg border-t border-white/10 flex items-center justify-center">
                        <span class="text-xs tracking-widest text-pink-200 font-serif italic">Habibah Khoirunnisa</span>
                    </div>
                    <!-- Bottom Layer -->
                    <div class="w-64 sm:w-72 h-20 mx-auto bg-gradient-to-r from-slate-900 via-purple-950 to-slate-900 rounded-t-lg relative shadow-2xl border-t border-pink-500/30">
                        <div class="absolute inset-x-0 bottom-2 flex justify-center space-x-3">
                            <span class="text-pink-400 text-xs">✨</span>
                            <span class="text-pink-300 text-xs">🌸</span>
                            <span class="text-pink-400 text-xs">✨</span>
                        </div>
                    </div>
                    <!-- Cake Plate -->
                    <div class="w-72 sm:w-80 h-4 bg-slate-300 rounded-full mx-auto shadow-2xl border-b-2 border-slate-400"></div>
                </div>
            </div>

            <!-- Action Buttons -->
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 pt-2">
                <button id="blowBtn" onclick="blowCandles()" class="px-8 py-3.5 rounded-full bg-gradient-to-r from-roseGold to-roseAccent text-white font-semibold shadow-lg shadow-roseGold/30 hover:shadow-roseGold/50 hover:scale-105 active:scale-95 transition-all duration-300 flex items-center space-x-2">
                    <span>💨 Tiup Lilin Sekarang</span>
                </button>
                <button id="micBtn" onclick="enableMicBlow()" class="px-6 py-3.5 rounded-full glass-card text-slate-300 hover:text-white font-medium hover:border-roseGold/50 transition-all duration-300 flex items-center space-x-2 text-sm">
                    <svg class="w-4 h-4 text-roseGold" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 016 0v6a3 3 0 01-3 3z"></path></svg>
                    <span>Gunakan Mikrofon (Tiup ke Mic HP)</span>
                </button>
            </div>
            
            <p id="blowStatus" class="text-xs text-roseGold/80 font-medium h-4"></p>
        </section>

        <!-- Secret Letter Envelope Section -->
        <section class="w-full max-w-2xl flex flex-col items-center text-center space-y-8">
            <div class="space-y-2">
                <span class="text-xs font-semibold tracking-widest text-roseGold uppercase">Pesan Rahasia Dari Hati</span>
                <h2 class="text-2xl sm:text-3xl font-bold text-slate-100 font-serif">Surat Spesial Untuk Habibah ✉️</h2>
                <p class="text-slate-400 text-sm">Sentuh atau klik amplop di bawah untuk membuka pesan hangat yang ditulis khusus untukmu.</p>
            </div>

            <!-- Animated Envelope -->
            <div class="envelope-wrapper py-2">
                <div id="envelope" onclick="openLetterModal()" class="envelope flex flex-col justify-end p-6 border border-white/10 hover:border-roseGold/40 transition-all">
                    <div class="envelope-flap"></div>
                    
                    <div class="z-10 text-center space-y-3 pb-4">
                        <div class="w-12 h-12 mx-auto rounded-full bg-roseGold/20 flex items-center justify-center border border-roseGold/40 text-roseGold">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>
                        </div>
                        <h3 class="text-slate-200 font-serif text-lg font-medium">Kepada: Habibah Khoirunnisa Ramadhan</h3>
                        <p class="text-xs text-roseGold/80 tracking-wider font-mono">Dari: Rifqi Bilal Afriza • Klik Untuk Membuka</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Make a Wish & Shooting Star Section -->
        <section class="w-full glass-card rounded-3xl p-8 sm:p-12 text-center space-y-8 relative overflow-hidden border border-roseGold/20">
            <div class="absolute -top-10 -right-10 w-40 h-40 bg-roseGold/10 rounded-full blur-3xl pointer-events-none"></div>
            
            <div class="max-w-lg mx-auto space-y-3">
                <span class="text-3xl">💫</span>
                <h2 class="text-2xl sm:text-3xl font-bold text-slate-100 font-serif">Panjatkan Doa & Harapan</h2>
                <p class="text-slate-300 text-sm leading-relaxed">Tuliskan impian atau doa terbesarmu untuk usia barumu, lalu terbangkan ke angkasa bintang-bintang.</p>
            </div>

            <div class="max-w-md mx-auto flex flex-col sm:flex-row gap-3">
                <input type="text" id="userWishInput" placeholder="Ketikkan harapanmu di sini..." class="flex-1 px-5 py-3.5 rounded-full bg-slate-950/80 border border-white/20 text-slate-100 placeholder-slate-500 focus:outline-none focus:border-roseGold text-sm transition-all">
                <button onclick="launchWishToStars()" class="px-7 py-3.5 rounded-full bg-gradient-to-r from-roseGold to-purple-600 text-white font-semibold text-sm hover:shadow-lg hover:shadow-roseGold/30 hover:scale-105 active:scale-95 transition-all">
                    Terbangkan 🚀
                </button>
            </div>

            <!-- Wish List Display -->
            <div id="wishListContainer" class="max-w-xl mx-auto flex flex-wrap justify-center gap-2.5 pt-4">
                <!-- Dynamic Wish Chips will appear here -->
            </div>
        </section>

        <!-- Footer -->
        <footer class="w-full text-center space-y-4 pt-10 border-t border-white/10">
            <p class="text-slate-400 text-sm font-light">
                Dirancang khusus dengan ketulusan & rasa hormat oleh <br class="sm:hidden">
                <span class="text-roseGold font-semibold">Rifqi Bilal Afriza</span> ✨
            </p>
            <p class="text-xs text-slate-600">
                © Habibah Khoirunnisa Ramadhan • Special Birthday Edition
            </p>
        </footer>

    </main>

    <!-- Lightbox Modal for Photo viewing -->
    <div id="lightboxModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/90 backdrop-blur-md opacity-0 pointer-events-none transition-opacity duration-300">
        <button onclick="closeLightbox()" class="absolute top-5 right-5 text-slate-300 hover:text-white bg-white/10 p-2.5 rounded-full z-50">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path></svg>
        </button>

        <button onclick="prevPhoto()" class="absolute left-4 sm:left-8 text-slate-300 hover:text-white bg-white/10 p-3 rounded-full z-50">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path></svg>
        </button>

        <button onclick="nextPhoto()" class="absolute right-4 sm:right-8 text-slate-300 hover:text-white bg-white/10 p-3 rounded-full z-50">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
        </button>

        <div class="max-w-3xl w-full flex flex-col items-center space-y-4">
            <div class="relative max-h-[75vh] rounded-2xl overflow-hidden border border-white/20 shadow-2xl">
                <img id="lightboxImg" src="" alt="Zoom Photo" class="max-h-[75vh] w-auto object-contain">
            </div>
            <div class="text-center space-y-1">
                <h3 id="lightboxTitle" class="text-xl font-bold font-serif text-slate-100"></h3>
                <p id="lightboxDesc" class="text-xs sm:text-sm text-slate-300 font-light"></p>
            </div>
        </div>
    </div>

    <!-- Modal for Secret Letter -->
    <div id="letterModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md opacity-0 pointer-events-none transition-opacity duration-500">
        <div class="relative w-full max-w-xl max-h-[90vh] glass-card bg-slate-950/90 border border-roseGold/30 rounded-3xl p-6 sm:p-10 overflow-y-auto space-y-6 shadow-2xl transform scale-95 transition-transform duration-500" id="letterModalContent">
            
            <button onclick="closeLetterModal()" class="absolute top-5 right-5 text-slate-400 hover:text-white bg-white/10 p-2 rounded-full transition-colors">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path></svg>
            </button>

            <div class="border-b border-roseGold/20 pb-4 text-center space-y-2">
                <span class="text-xs font-mono text-roseGold tracking-widest uppercase">Pesan Tulus Dari Hati</span>
                <h3 class="text-2xl sm:text-3xl font-serif text-slate-100">Habibah Khoirunnisa Ramadhan</h3>
                <p class="text-xs text-slate-400 italic">Sebuah ucapan singkat dan doa tulus</p>
            </div>

            <div class="space-y-4 text-slate-200 text-sm sm:text-base leading-relaxed font-light text-justify">
                <p>
                    <span class="text-2xl font-serif text-roseGold">U</span>ntuk Habibah Khoirunnisa Ramadhan,
                </p>
                <p>
                    Selamat bertambah usia. Di hari yang penuh keindahan ini, izinkan aku menyampaikan ucapan selamat dan doa paling tulus untukmu.
                </p>
                <p>
                    Semoga di langkah usiamu yang baru ini, setiap hari yang kamu jalani diliputi oleh kesehatan, keberkahan, serta kedamaian hati. Semoga seluruh impian, harapan besar, dan cita-cita yang kamu perjuangkan diberikan jalan kemudahan hingga kamu bisa tersenyum bangga atas pencapaianmu.
                </p>
                <p>
                    Terima kasih pernah hadir dan memberikan warna indah dalam perjalanan hidupku. Setiap kebaikan, kehangatan, dan kenangan manis yang pernah ada tetap memiliki tempat yang sangat dihormati di dalam ingatanku. Meskipun takdir dan jalan kita mungkin telah berjalan di lintasannya masing-masing, doa terbaikku untuk keselamatan dan kebahagiaanmu tidak akan pernah berkurang.
                </p>
                <p>
                    Tetaplah menjadi Habibah yang senantiasa memancarkan kebaikan, tangguh dalam melangkah, dan lembut dalam bersikap. Semoga Allah SWT senantiasa melindungimu dan memberikan keberkahan umur yang panjang.
                </p>
                <p class="pt-4 font-serif italic text-right text-roseGold">
                    Selamat ulang tahun sekali lagi, Habibah.
                </p>
            </div>

            <div class="border-t border-roseGold/20 pt-4 flex flex-col items-end space-y-1">
                <span class="text-xs text-slate-400">Salam hangat & doa tulus,</span>
                <span class="text-base font-bold text-slate-100 font-serif">Rifqi Bilal Afriza</span>
            </div>
        </div>
    </div>

    <script>
        // Typing Effect for Name
        const nameText = "Habibah Khoirunnisa Ramadhan ✨";
        let typedIdx = 0;
        function typeWriter() {
            if (typedIdx < nameText.length) {
                document.getElementById("typedName").innerHTML += nameText.charAt(typedIdx);
                typedIdx++;
                setTimeout(typeWriter, 80);
            }
        }
        window.addEventListener('DOMContentLoaded', typeWriter);

        // Star Background Particles Canvas
        const canvas = document.getElementById('starCanvas');
        const ctx = canvas.getContext('2d');
        let particles = [];

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        class Particle {
            constructor() {
                this.reset();
            }
            reset() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 2.5 + 0.5;
                this.speedX = (Math.random() - 0.5) * 0.3;
                this.speedY = -Math.random() * 0.5 - 0.1;
                this.opacity = Math.random() * 0.7 + 0.3;
                this.color = Math.random() > 0.4 ? '#f472b6' : (Math.random() > 0.5 ? '#e879f9' : '#fbbf24');
            }
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                if (this.y < -10 || this.x < -10 || this.x > canvas.width + 10) {
                    this.reset();
                    this.y = canvas.height + 10;
                }
            }
            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.globalAlpha = this.opacity;
                ctx.shadowBlur = 8;
                ctx.shadowColor = this.color;
                ctx.fill();
                ctx.globalAlpha = 1;
            }
        }

        for (let i = 0; i < 90; i++) {
            particles.push(new Particle());
        }

        // Shooting Star Effect
        let shootingStars = [];
        class ShootingStar {
            constructor(startX, startY) {
                this.x = startX;
                this.y = startY;
                this.len = Math.random() * 80 + 120;
                this.speed = Math.random() * 10 + 12;
                this.size = Math.random() * 2 + 1;
                this.color = '#f472b6';
                this.opacity = 1;
            }
            update() {
                this.x += this.speed;
                this.y += this.speed * 0.5;
                this.opacity -= 0.015;
            }
            draw() {
                ctx.save();
                ctx.strokeStyle = this.color;
                ctx.lineWidth = this.size;
                ctx.globalAlpha = Math.max(0, this.opacity);
                ctx.beginPath();
                ctx.moveTo(this.x, this.y);
                ctx.lineTo(this.x - this.len, this.y - this.len * 0.5);
                ctx.stroke();
                ctx.restore();
            }
        }

        function animateCanvas() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => {
                p.update();
                p.draw();
            });

            shootingStars.forEach((s, idx) => {
                s.update();
                s.draw();
                if (s.opacity <= 0) shootingStars.splice(idx, 1);
            });

            requestAnimationFrame(animateCanvas);
        }
        animateCanvas();

        // Photo Data State with Unsplash Aesthetic Fallbacks
        const defaultFallbacks = [
            'https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=800&q=80',
            'https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=800&q=80',
            'https://images.unsplash.com/photo-1524504388940-b1c1722653e1?auto=format&fit=crop&w=800&q=80',
            'https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&w=800&q=80',
            'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=800&q=80'
        ];

        const photosData = [
            { src: 'foto1.jpg', title: 'Anggun & Penuh Pesona ✨', desc: 'Kehangatan pancaran senyum yang selalu menenangkan.' },
            { src: 'foto2.jpg', title: 'Senyuman Manis 🌟', desc: 'Sinar kebahagiaan yang senantiasa hadir dalam setiap momen.' },
            { src: 'foto3.jpg', title: 'Momen Keceriaan 🌸', desc: 'Canda tawa lepas yang membawa energi positif.' },
            { src: 'foto4.jpg', title: 'Keindahan Sederhana 💜', desc: 'Keanggunan alami yang memikat dalam ketenangan.' },
            { src: 'foto5.jpg', title: 'Gaya Elegan & Menawan 💫', desc: 'Pesona istimewa yang senantiasa terpancar dari Habibah.' }
        ];

        // Dynamic File Upload Handler (Interactive Image Selection)
        function handleUserPhotoUpload(event) {
            const files = event.target.files;
            if (!files || files.length === 0) return;

            const fileList = Array.from(files);
            fileList.forEach((file, idx) => {
                if (idx < 5) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        const newSrc = e.target.result;
                        photosData[idx].src = newSrc;
                        
                        // Update card image src
                        const cardImg = document.getElementById(`cardImg${idx}`);
                        if (cardImg) cardImg.src = newSrc;

                        // Update top header profile picture if first photo uploaded
                        if (idx === 0) {
                            const headerImg = document.getElementById('profileHeaderImg');
                            if (headerImg) headerImg.src = newSrc;
                        }
                    };
                    reader.readAsDataURL(file);
                }
            });
        }

        // Web Audio Synthesizer for Romantic Melody
        let audioCtx = null;
        let isPlayingAudio = false;
        let melodyTimeout = null;

        function initAudio() {
            if (!audioCtx) {
                audioCtx = new (window.AudioContext || window.webkitAudioContext)();
            }
        }

        function playSoftNote(freq, duration = 1.6) {
            if (!audioCtx || audioCtx.state === 'suspended') return;
            try {
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                
                osc.type = 'sine';
                osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
                
                gain.gain.setValueAtTime(0.001, audioCtx.currentTime);
                gain.gain.exponentialRampToValueAtTime(0.18, audioCtx.currentTime + 0.12);
                gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + duration);

                osc.connect(gain);
                gain.connect(audioCtx.destination);

                osc.start();
                osc.stop(audioCtx.currentTime + duration);
            } catch (e) {
                console.log(e);
            }
        }

        const melodyNotes = [
            261.63, 261.63, 293.66, 261.63, 349.23, 329.63,
            261.63, 261.63, 293.66, 261.63, 392.00, 349.23,
            261.63, 261.63, 523.25, 440.00, 349.23, 329.63, 293.66,
            466.16, 466.16, 440.00, 349.23, 392.00, 349.23
        ];

        let currentNoteIdx = 0;
        function playMelodyLoop() {
            if (!isPlayingAudio) return;
            playSoftNote(melodyNotes[currentNoteIdx], 1.4);
            currentNoteIdx = (currentNoteIdx + 1) % melodyNotes.length;
            
            // Equalizer animation logic
            const eqBars = document.querySelectorAll('.eq-bar');
            eqBars.forEach(bar => {
                bar.style.height = Math.floor(Math.random() * 14 + 4) + 'px';
            });

            melodyTimeout = setTimeout(playMelodyLoop, 550);
        }

        function toggleAudio() {
            initAudio();
            if (audioCtx.state === 'suspended') {
                audioCtx.resume();
            }

            const status = document.getElementById('musicStatus');

            if (isPlayingAudio) {
                isPlayingAudio = false;
                clearTimeout(melodyTimeout);
                status.innerText = "Putar Musik 🎵";
                document.querySelectorAll('.eq-bar').forEach(b => b.style.height = '4px');
            } else {
                isPlayingAudio = true;
                status.innerText = "Musik Diputar 🎶";
                playMelodyLoop();
            }
        }

        // Photo Gallery Lightbox Modal Logic
        let currentPhotoIdx = 0;

        function openLightbox(index) {
            initAudio();
            playSoftNote(523.25, 0.4);
            currentPhotoIdx = index;
            updateLightbox();
            const modal = document.getElementById('lightboxModal');
            modal.classList.remove('opacity-0', 'pointer-events-none');
        }

        function updateLightbox() {
            const data = photosData[currentPhotoIdx];
            const imgElem = document.getElementById('lightboxImg');
            imgElem.src = data.src;
            imgElem.onerror = function() {
                this.src = defaultFallbacks[currentPhotoIdx];
            };
            document.getElementById('lightboxTitle').innerText = data.title;
            document.getElementById('lightboxDesc').innerText = data.desc;
        }

        function closeLightbox() {
            document.getElementById('lightboxModal').classList.add('opacity-0', 'pointer-events-none');
        }

        function nextPhoto() {
            currentPhotoIdx = (currentPhotoIdx + 1) % photosData.length;
            updateLightbox();
        }

        function prevPhoto() {
            currentPhotoIdx = (currentPhotoIdx - 1 + photosData.length) % photosData.length;
            updateLightbox();
        }

        // Candle Blowing Logic with Confetti
        let candlesBlown = false;

        function blowCandles() {
            if (candlesBlown) return;
            candlesBlown = true;

            document.getElementById('flame1').classList.add('extinguished');
            document.getElementById('flame2').classList.add('extinguished');
            document.getElementById('flame3').classList.add('extinguished');

            document.getElementById('smoke1').classList.add('active');
            document.getElementById('smoke2').classList.add('active');
            document.getElementById('smoke3').classList.add('active');

            document.getElementById('candleAura').style.opacity = '0';

            initAudio();
            if (audioCtx) {
                playSoftNote(523.25, 0.5);
                setTimeout(() => playSoftNote(659.25, 0.8), 200);
                setTimeout(() => playSoftNote(783.99, 1.2), 400);
            }

            // Confetti explosion
            confetti({
                particleCount: 120,
                spread: 80,
                origin: { y: 0.6 }
            });

            document.getElementById('blowStatus').innerText = "✨ Lilin telah ditiup! Semoga semua doa Habibah dikabulkan! ✨";
            document.getElementById('blowBtn').classList.add('opacity-50', 'cursor-default');
            document.getElementById('blowBtn').innerText = "🎉 Selamat Ulang Tahun!";
        }

        function enableMicBlow() {
            initAudio();
            document.getElementById('blowStatus').innerText = "🎙️ Tiup kuat ke mikrofon HP/Laptopmu...";
            
            navigator.mediaDevices.getUserMedia({ audio: true }).then(stream => {
                const micCtx = new (window.AudioContext || window.webkitAudioContext)();
                const micInput = micCtx.createMediaStreamSource(stream);
                const analyser = micCtx.createAnalyser();
                analyser.fftSize = 256;
                micInput.connect(analyser);

                const dataArray = new Uint8Array(analyser.frequencyBinCount);

                function checkVolume() {
                    if (candlesBlown) {
                        stream.getTracks().forEach(track => track.stop());
                        return;
                    }
                    analyser.getByteFrequencyData(dataArray);
                    let sum = 0;
                    for (let i = 0; i < dataArray.length; i++) sum += dataArray[i];
                    let average = sum / dataArray.length;

                    if (average > 45) {
                        blowCandles();
                        stream.getTracks().forEach(track => track.stop());
                    } else {
                        requestAnimationFrame(checkVolume);
                    }
                }
                checkVolume();
            }).catch(err => {
                document.getElementById('blowStatus').innerText = "⚠️ Akses mikrofon ditolak. Silakan gunakan tombol tiup manual.";
            });
        }

        // Secret Letter Modal Logic
        function openLetterModal() {
            initAudio();
            playSoftNote(440, 0.4);
            document.getElementById('envelope').classList.add('open');
            setTimeout(() => {
                const modal = document.getElementById('letterModal');
                const content = document.getElementById('letterModalContent');
                modal.classList.remove('opacity-0', 'pointer-events-none');
                content.classList.remove('scale-95');
                content.classList.add('scale-100');
            }, 400);
        }

        function closeLetterModal() {
            const modal = document.getElementById('letterModal');
            const content = document.getElementById('letterModalContent');
            modal.classList.add('opacity-0', 'pointer-events-none');
            content.classList.remove('scale-100');
            content.classList.add('scale-95');
            document.getElementById('envelope').classList.remove('open');
        }

        // Wish Launcher Logic
        function launchWishToStars() {
            const wishInput = document.getElementById('userWishInput');
            const wishText = wishInput.value.trim();
            if (!wishText) return;

            initAudio();
            playSoftNote(880, 1.5);

            // Launch Shooting Star Animation
            shootingStars.push(new ShootingStar(100, 100));
            shootingStars.push(new ShootingStar(200, 50));

            // Append Wish Chip
            const container = document.getElementById('wishListContainer');
            const chip = document.createElement('span');
            chip.className = 'px-4 py-2 rounded-full glass-card border border-roseGold/40 text-xs text-roseGold font-medium animate-bounce shadow-md';
            chip.innerText = '✨ ' + wishText;
            container.appendChild(chip);

            wishInput.value = '';
        }
    </script>
</body>
</html>
