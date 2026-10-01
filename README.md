<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bride to Be Celebration</title>

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        roseGold: '#B76E79',
                        blushPink: '#FFD1DC',
                        softCream: '#FAF0E6',
                        warmGold: '#D4AF37',
                        champagne: '#F7E7CE',
                        deepRose: '#9E4753'
                    },
                    fontFamily: {
                        playfair: ['"Playfair Display"', 'serif'],
                        greatVibes: ['"Great Vibes"', 'cursive'],
                        poppins: ['Poppins', 'sans-serif']
                    }
                }
            }
        }
    </script>

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:ital,wght@0,400..800;1,400..800&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Canvas Confetti Library -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #FAF0E6;
            color: #4A4A4A;
            overflow-x: hidden;
        }

        /* Glassmorphism Effect */
        .glass-card {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 209, 220, 0.5);
        }

        /* Floating Petals Animation */
        .petal {
            position: absolute;
            background-color: #FFB7C5;
            border-radius: 150% 0 150% 0;
            opacity: 0.7;
            pointer-events: none;
            z-index: 10;
            animation: animatePetal 10s linear infinite;
        }

        @keyframes animatePetal {
            0% {
                opacity: 0.8;
                transform: top 0 left 0 rotate(0deg) scale(0.8);
            }
            100% {
                opacity: 0;
                transform: translateY(100vh) translateX(100px) rotate(720deg) scale(1.2);
            }
        }

        /* Flip Card Effect */
        .perspective-1000 {
            perspective: 1000px;
        }
        .transform-style-3d {
            transform-style: preserve-3d;
        }
        .backface-hidden {
            backface-visibility: hidden;
            -webkit-backface-visibility: hidden;
        }
        .rotate-y-180 {
            transform: rotateY(180deg);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #FAF0E6;
        }
        ::-webkit-scrollbar-thumb {
            background: #B76E79;
            border-radius: 10px;
        }

        /* Gold Gradient Text */
        .gold-gradient-text {
            background: linear-gradient(135deg, #D4AF37 0%, #B76E79 50%, #AA771C 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Printing adjustments */
        @media print {
            .no-print { display: none !important; }
            body { background: white; color: black; }
            .glass-card { border: 1px solid #ccc; box-shadow: none; background: white; }
        }
    </style>
</head>
<body class="relative min-h-screen pb-16">

    <!-- Petals Animation Container -->
    <div id="petals-container" class="fixed inset-0 pointer-events-none overflow-hidden z-20"></div>

    <!-- Navigation Bar -->
    <nav class="sticky top-0 z-40 glass-card shadow-sm transition-all duration-300 no-print">
        <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="font-greatVibes text-3xl text-roseGold font-bold tracking-wide hover:scale-105 transition-transform">
                Bridal Shower
            </a>
            <div class="flex items-center space-x-2 md:space-x-4">
                <button onclick="triggerConfetti()" class="px-3 py-1.5 text-xs md:text-sm bg-blushPink/60 hover:bg-roseGold hover:text-white text-deepRose font-medium rounded-full transition-all flex items-center gap-1.5 shadow-sm">
                    <i class="fa-solid fa-wand-magic-sparkles"></i>
                    <span>Sembur Confetti</span>
                </button>
                <button onclick="openEditModal()" class="px-3 py-1.5 text-xs md:text-sm bg-roseGold text-white font-medium rounded-full hover:bg-deepRose transition-all flex items-center gap-1.5 shadow-md">
                    <i class="fa-solid fa-pen-to-square"></i>
                    <span>Edit Detail</span>
                </button>
                <button onclick="shareOrDownload()" class="px-3 py-1.5 text-xs md:text-sm border border-roseGold text-roseGold hover:bg-roseGold hover:text-white font-medium rounded-full transition-all flex items-center gap-1.5 shadow-sm">
                    <i class="fa-solid fa-share-nodes"></i>
                    <span class="hidden sm:inline">Bagikan</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- Main Container -->
    <main class="max-w-5xl mx-auto px-4 pt-8 md:pt-12 space-y-16">

        <!-- HERO SECTION -->
        <section class="text-center relative py-12 px-6 rounded-3xl glass-card shadow-xl border border-blushPink/40 overflow-hidden">
            <!-- Decorative Flower Ornaments -->
            <div class="absolute -top-10 -left-10 text-blushPink opacity-30 text-8xl pointer-events-none">
                <i class="fa-solid fa-spa"></i>
            </div>
            <div class="absolute -bottom-10 -right-10 text-blushPink opacity-30 text-8xl pointer-events-none">
                <i class="fa-solid fa-spa"></i>
            </div>

            <div class="inline-block px-4 py-1.5 bg-blushPink/50 text-deepRose font-semibold text-xs md:text-sm rounded-full tracking-wider uppercase mb-4 shadow-sm border border-roseGold/20">
                ✨ Special Bridal Shower Celebration ✨
            </div>

            <h2 class="font-greatVibes text-5xl md:text-7xl text-roseGold mb-2 font-bold drop-shadow-sm">
                Bride to Be
            </h2>
            <h1 id="bride-name-display" class="font-playfair text-3xl md:text-6xl font-extrabold gold-gradient-text tracking-wide mb-6">
                Farhatul Kamilah, M.A
            </h1>

            <p id="hero-message-display" class="max-w-2xl mx-auto text-gray-600 text-sm md:text-base leading-relaxed italic mb-8">
                "Selamat memulai kehidupan sebagai istri, Sahabat Tercantikku! Langkah awal menuju fase hidup baru yang penuh cinta, keberkahan, dan kebahagiaan abadi bersama sang tambatan hati."
            </p>

            <!-- Countdown Timer Card -->
            <div class="bg-white/80 backdrop-blur-md p-6 rounded-2xl shadow-inner border border-roseGold/20 max-w-xl mx-auto">
                <h3 class="font-playfair text-xs md:text-sm uppercase tracking-widest text-roseGold font-bold mb-4">
                    <i class="fa-regular fa-clock mr-1.5"></i> Menghitung Hari Menuju Wedding Day
                </h3>
                <div class="grid grid-cols-4 gap-2 md:gap-4 text-center">
                    <div class="bg-gradient-to-b from-blushPink/30 to-roseGold/10 p-2 md:p-3 rounded-xl border border-roseGold/20 shadow-sm">
                        <span id="timer-days" class="block font-playfair text-2xl md:text-4xl font-bold text-deepRose">00</span>
                        <span class="text-[10px] md:text-xs font-medium text-gray-500 uppercase tracking-wider">Hari</span>
                    </div>
                    <div class="bg-gradient-to-b from-blushPink/30 to-roseGold/10 p-2 md:p-3 rounded-xl border border-roseGold/20 shadow-sm">
                        <span id="timer-hours" class="block font-playfair text-2xl md:text-4xl font-bold text-deepRose">00</span>
                        <span class="text-[10px] md:text-xs font-medium text-gray-500 uppercase tracking-wider">Jam</span>
                    </div>
                    <div class="bg-gradient-to-b from-blushPink/30 to-roseGold/10 p-2 md:p-3 rounded-xl border border-roseGold/20 shadow-sm">
                        <span id="timer-minutes" class="block font-playfair text-2xl md:text-4xl font-bold text-deepRose">00</span>
                        <span class="text-[10px] md:text-xs font-medium text-gray-500 uppercase tracking-wider">Menit</span>
                    </div>
                    <div class="bg-gradient-to-b from-blushPink/30 to-roseGold/10 p-2 md:p-3 rounded-xl border border-roseGold/20 shadow-sm">
                        <span id="timer-seconds" class="block font-playfair text-2xl md:text-4xl font-bold text-deepRose">00</span>
                        <span class="text-[10px] md:text-xs font-medium text-gray-500 uppercase tracking-wider">Detik</span>
                    </div>
                </div>
                <div id="wedding-date-display" class="mt-4 text-xs font-medium text-roseGold italic">
                    <i class="fa-solid fa-calendar-heart mr-1"></i> Tanggal Pernikahan: 10 Oktober 2026
                </div>
            </div>
        </section>

        <!-- AUDIO PLAYER SECTION -->
        <section class="glass-card p-6 rounded-2xl shadow-md border border-blushPink/50 max-w-xl mx-auto flex flex-col md:flex-row items-center gap-4 no-print">
            <div class="relative w-14 h-14 rounded-full bg-roseGold/20 flex items-center justify-center flex-shrink-0 border-2 border-roseGold shadow-md overflow-hidden">
                <i id="music-disc-icon" class="fa-solid fa-compact-disc text-3xl text-roseGold transition-transform duration-1000"></i>
            </div>
            <div class="flex-grow text-center md:text-left w-full">
                <h4 class="font-playfair text-sm font-bold text-deepRose">Romantic Background Music</h4>
                <p id="song-title" class="text-xs text-gray-500 truncate">Acoustic Romance - Tulang & Nadi</p>
                <!-- Custom Progress Bar -->
                <div class="w-full bg-gray-200 h-1.5 rounded-full mt-2 cursor-pointer overflow-hidden" id="progress-container" onclick="setAudioProgress(event)">
                    <div id="audio-progress-bar" class="bg-roseGold h-full w-0 transition-all duration-100"></div>
                </div>
            </div>
            <div class="flex items-center gap-3 flex-shrink-0">
                <button id="play-pause-btn" onclick="toggleAudio()" class="w-10 h-10 rounded-full bg-roseGold hover:bg-deepRose text-white flex items-center justify-center shadow-md transition-all">
                    <i class="fa-solid fa-play" id="play-icon"></i>
                </button>
                <button onclick="toggleMute()" class="w-8 h-8 rounded-full bg-blushPink/50 hover:bg-blushPink text-deepRose flex items-center justify-center transition-all">
                    <i class="fa-solid fa-volume-high" id="volume-icon"></i>
                </button>
            </div>
            <!-- Audio Element with generated synthetic audio or safe romantic royalty-free source -->
            <audio id="bg-audio" loop src="C:\Users\Nanda\Desktop\BRIDE AA\Tiara Andini - Tulang dan Nadi (Official Visualizer).mp3"></audio>
        </section>

        <!-- MEMORIES GALLERY SECTION -->
        <section class="space-y-6">
            <div class="text-center space-y-2">
                <h3 class="font-greatVibes text-4xl text-roseGold font-bold">Memories Gallery</h3>
                <h2 class="font-playfair text-2xl font-bold text-gray-800">Momen Indah Kebersamaan</h2>
                <div class="w-16 h-0.5 bg-roseGold mx-auto rounded-full"></div>
            </div>

            <!-- Upload Photo Button -->
            <div class="flex justify-end no-print">
                <label class="cursor-pointer bg-white text-roseGold border border-roseGold/40 hover:bg-blushPink/30 px-4 py-2 rounded-xl text-xs font-semibold shadow-sm flex items-center gap-2 transition-all">
                    <i class="fa-solid fa-cloud-arrow-up"></i>
                    <span>Tambah Foto Kenangan</span>
                    <input type="file" id="upload-photo-input" accept="image/*" class="hidden" onchange="handlePhotoUpload(event)">
                </label>
            </div>

            <!-- Photos Grid -->
            <div id="gallery-grid" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
                <!-- Sample Photo Items -->
                <div class="group relative rounded-2xl overflow-hidden shadow-lg border-2 border-white aspect-square bg-gray-100 hover:-translate-y-1 transition-all duration-300">
                    <img src="C:\Users\Nanda\Desktop\BRIDE AA\Gemini_Generated_Image_7vwz97vwz97vwz97.jfif" alt="Memory 1" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4 text-white">
                        <p class="font-playfair font-semibold text-sm">Laughing Together</p>
                        <p class="text-xs text-gray-200">POKOKNYA MUSTI LIBURAN BARENG LAGI</p>
                    </div>
                </div>

                <div class="group relative rounded-2xl overflow-hidden shadow-lg border-2 border-white aspect-square bg-gray-100 hover:-translate-y-1 transition-all duration-300">
                    <img src="C:\Users\Nanda\Desktop\BRIDE AA\WhatsApp Image 2026-10-01 at 09.51.12.jpeg" alt="Memory 2" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4 text-white">
                        <p class="font-playfair font-semibold text-sm">Best Friends Forever</p>
                        <p class="text-xs text-gray-200">SELALU CERITA KALO ADA APA-APA WALAUPUN RESPON KITA SAMA-SAMA NGESELIN</p>
                    </div>
                </div>

                <div class="group relative rounded-2xl overflow-hidden shadow-lg border-2 border-white aspect-square bg-gray-100 hover:-translate-y-1 transition-all duration-300">
                    <img src="C:\Users\Nanda\Desktop\BRIDE AA\Gemini_Generated_Image_ez3dleez3dleez3d.jfif" alt="Memory 3" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4 text-white">
                        <p class="font-playfair font-semibold text-sm">Bridal Preparation</p>
                        <p class="text-xs text-gray-200">POKOKNYA JADI ORANG PALING CANTIK DI HARI H</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- REASONS WHY CARDS SECTION -->
        <section class="space-y-6">
            <div class="text-center space-y-2">
                <h3 class="font-greatVibes text-4xl text-roseGold font-bold">Why We Love You</h3>
                <h2 class="font-playfair text-2xl font-bold text-gray-800">Reasons Why You'll Be the Best Bride</h2>
                <p class="text-xs text-gray-500">Klik kartu di bawah untuk melihat alasan manisnya! ✨</p>
                <div class="w-16 h-0.5 bg-roseGold mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Card 1 -->
                <div class="h-64 perspective-1000 group cursor-pointer" onclick="toggleCardFlip(this)">
                    <div class="card-inner relative w-full h-full rounded-2xl shadow-lg border border-roseGold/30 transition-transform duration-700 transform-style-3d">
                        <!-- Front -->
                        <div class="absolute inset-0 bg-gradient-to-br from-white to-blushPink/40 rounded-2xl p-6 flex flex-col items-center justify-center text-center backface-hidden">
                            <div class="w-14 h-14 bg-blushPink text-roseGold rounded-full flex items-center justify-center text-2xl mb-4 shadow-sm">
                                <i class="fa-solid fa-heart"></i>
                            </div>
                            <h4 class="font-playfair font-bold text-roseGold text-lg mb-2">PISCES PALING PERASA</h4>
                            <p class="text-xs text-gray-500">Klik untuk membaca alasan #1</p>
                        </div>
                        <!-- Back -->
                        <div class="absolute inset-0 bg-roseGold text-white rounded-2xl p-6 flex flex-col items-center justify-center text-center backface-hidden rotate-y-180">
                            <i class="fa-solid fa-quote-left text-blushPink/50 text-2xl mb-2"></i>
                            <p class="text-sm font-medium leading-relaxed">
                                Farha adalah sahabat gue yang paling perasa, pisces garis keras HAHAHA but, sangking perasanya mungkin ngomong sama dia adalah solusi terbaik ketika mati rasa WKWK
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="h-64 perspective-1000 group cursor-pointer" onclick="toggleCardFlip(this)">
                    <div class="card-inner relative w-full h-full rounded-2xl shadow-lg border border-roseGold/30 transition-transform duration-700 transform-style-3d">
                        <!-- Front -->
                        <div class="absolute inset-0 bg-gradient-to-br from-white to-blushPink/40 rounded-2xl p-6 flex flex-col items-center justify-center text-center backface-hidden">
                            <div class="w-14 h-14 bg-blushPink text-roseGold rounded-full flex items-center justify-center text-2xl mb-4 shadow-sm">
                                <i class="fa-solid fa-crown"></i>
                            </div>
                            <h4 class="font-playfair font-bold text-roseGold text-lg mb-2">Anggun & Bijak</h4>
                            <p class="text-xs text-gray-500">Klik untuk membaca alasan #2</p>
                        </div>
                        <!-- Back -->
                        <div class="absolute inset-0 bg-roseGold text-white rounded-2xl p-6 flex flex-col items-center justify-center text-center backface-hidden rotate-y-180">
                            <i class="fa-solid fa-quote-left text-blushPink/50 text-2xl mb-2"></i>
                            <p class="text-sm font-medium leading-relaxed">
                                Farha selalu tahu cara menyelesaikan masalah dengan tenang dan penuh kedewasaan. Pokoknya fakhri harus merasa paling beruntung mendapatkan lo
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="h-64 perspective-1000 group cursor-pointer" onclick="toggleCardFlip(this)">
                    <div class="card-inner relative w-full h-full rounded-2xl shadow-lg border border-roseGold/30 transition-transform duration-700 transform-style-3d">
                        <!-- Front -->
                        <div class="absolute inset-0 bg-gradient-to-br from-white to-blushPink/40 rounded-2xl p-6 flex flex-col items-center justify-center text-center backface-hidden">
                            <div class="w-14 h-14 bg-blushPink text-roseGold rounded-full flex items-center justify-center text-2xl mb-4 shadow-sm">
                                <i class="fa-solid fa-champagne-glasses"></i>
                            </div>
                            <h4 class="font-playfair font-bold text-roseGold text-lg mb-2">Teman Hidup Terbaik</h4>
                            <p class="text-xs text-gray-500">Klik untuk membaca alasan #3</p>
                        </div>
                        <!-- Back -->
                        <div class="absolute inset-0 bg-roseGold text-white rounded-2xl p-6 flex flex-col items-center justify-center text-center backface-hidden rotate-y-180">
                            <i class="fa-solid fa-quote-left text-blushPink/50 text-2xl mb-2"></i>
                            <p class="text-sm font-medium leading-relaxed">
                                Sangat amat supportif HAHA, walaupun AA ngeselin tapi dia tuh selalu menjadi tempat cerita paling baik tanpa menghakimi siapapun 
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- MESSAGES & WISHES SECTION -->
        <section class="space-y-6">
            <div class="text-center space-y-2">
                <h3 class="font-greatVibes text-4xl text-roseGold font-bold">Heartfelt Wishes</h3>
                <h2 class="font-playfair text-2xl font-bold text-gray-800">Pesan & Doa dari Bridesmaids</h2>
                <div class="w-16 h-0.5 bg-roseGold mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 items-start">
                <!-- Add Wish Form -->
                <div class="glass-card p-6 rounded-2xl shadow-lg border border-roseGold/30 lg:col-span-1 no-print">
                    <h4 class="font-playfair font-bold text-roseGold text-lg mb-4 flex items-center gap-2">
                        <i class="fa-solid fa-pen-nib"></i> Tulis Ucapan / Doa
                    </h4>
                    <form id="wish-form" onsubmit="handleAddWish(event)" class="space-y-4">
                        <div>
                            <label class="block text-xs font-semibold text-gray-600 mb-1">Nama Kamu / Bridesmaid</label>
                            <input type="text" id="sender-name" required placeholder="Contoh: Ananda Novi Prasetya" class="w-full px-3 py-2 text-sm border border-blushPink rounded-xl focus:ring-2 focus:ring-roseGold focus:outline-none bg-white/80">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-gray-600 mb-1">Peran / Hubungan</label>
                            <input type="text" id="sender-role" placeholder="Contoh: Sahabat dari bocah WKWK" class="w-full px-3 py-2 text-sm border border-blushPink rounded-xl focus:ring-2 focus:ring-roseGold focus:outline-none bg-white/80">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-gray-600 mb-1">Pesan Manis & Doa</label>
                            <textarea id="sender-message" required rows="4" placeholder="Tulis doa dan harapan terbaikmu untuk calon pengantin..." class="w-full px-3 py-2 text-sm border border-blushPink rounded-xl focus:ring-2 focus:ring-roseGold focus:outline-none bg-white/80"></textarea>
                        </div>
                        <button type="submit" class="w-full py-2.5 bg-roseGold hover:bg-deepRose text-white font-semibold rounded-xl text-sm shadow-md transition-all flex items-center justify-center gap-2">
                            <i class="fa-solid fa-paper-plane"></i> Kirim Ucapan
                        </button>
                    </form>
                </div>

                <!-- Wishes Wall Scrollable List -->
                <div class="lg:col-span-2 space-y-4 max-h-[500px] overflow-y-auto pr-2" id="wishes-list">
                    <!-- Wish Card 1 -->
                    <div class="glass-card p-5 rounded-2xl shadow-sm border border-blushPink/60 space-y-2 hover:shadow-md transition-shadow">
                        <div class="flex justify-between items-center">
                            <div>
                                <h5 class="font-playfair font-bold text-roseGold text-base">Ananda Novi Prasetya</h5>
                                <span class="text-[11px] bg-blushPink/50 text-deepRose px-2 py-0.5 rounded-full font-medium">Sahabat dari bocah</span>
                            </div>
                            <span class="text-[10px] text-gray-400"><i class="fa-regular fa-clock mr-1"></i> Baru saja</span>
                        </div>
                        <p class="text-xs md:text-sm text-gray-600 italic leading-relaxed">
                            "Bahagia banget akhirnya sampai di titik ini! Masih ingat dulu cerita-cerita crush, sekarang udah mau akad aja. May your marriage be filled with endless love, laughter, and blessings!"
                        </p>
                    </div>

                    <!-- Wish Card 2 -->
                    <div class="glass-card p-5 rounded-2xl shadow-sm border border-blushPink/60 space-y-2 hover:shadow-md transition-shadow">
                        <div class="flex justify-between items-center">
                            <div>
                                <h5 class="font-playfair font-bold text-roseGold text-base">Nanda paling mantep</h5>
                                <span class="text-[11px] bg-blushPink/50 text-deepRose px-2 py-0.5 rounded-full font-medium">Sahabat dari bocah AA</span>
                            </div>
                            <span class="text-[10px] text-gray-400"><i class="fa-regular fa-clock mr-1"></i> 1 jam lalu</span>
                        </div>
                        <p class="text-xs md:text-sm text-gray-600 italic leading-relaxed">
                            "You are going to be the most stunning bride ever! Semoga ibadah terpanjang ini lancar sampai hari H, bahagia dunia akhirat yaaa dear!"
                        </p>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- LIGHTBOX MODAL -->
    <div id="lightbox-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="relative max-w-3xl w-full bg-transparent rounded-2xl overflow-hidden flex flex-col items-center">
            <button onclick="closeLightbox()" class="absolute top-2 right-2 text-white bg-black/50 hover:bg-black w-9 h-9 rounded-full flex items-center justify-center z-10">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            <img id="lightbox-img" src="" alt="Enlarged memory" class="max-h-[80vh] w-auto object-contain rounded-xl shadow-2xl">
            <p id="lightbox-caption" class="text-white font-playfair mt-3 text-center text-sm md:text-base"></p>
        </div>
    </div>

    <!-- EDIT DETAILS MODAL -->
    <div id="edit-modal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden flex items-center justify-center p-4 no-print">
        <div class="bg-white rounded-3xl max-w-lg w-full p-6 shadow-2xl border border-blushPink space-y-5 max-h-[90vh] overflow-y-auto">
            <div class="flex justify-between items-center border-b border-gray-100 pb-3">
                <h3 class="font-playfair font-bold text-xl text-roseGold flex items-center gap-2">
                    <i class="fa-solid fa-sliders"></i> Edit Detail Ucapan
                </h3>
                <button onclick="closeEditModal()" class="text-gray-400 hover:text-gray-600">
                    <i class="fa-solid fa-xmark text-lg"></i>
                </button>
            </div>

            <div class="space-y-4 text-xs md:text-sm">
                <div>
                    <label class="block font-semibold text-gray-700 mb-1">Nama Calon Pengantin (Bride)</label>
                    <input type="text" id="edit-bride-name" class="w-full px-3 py-2 border border-blushPink rounded-xl focus:ring-2 focus:ring-roseGold focus:outline-none">
                </div>
                <div>
                    <label class="block font-semibold text-gray-700 mb-1">Tanggal Pernikahan (Wedding Day)</label>
                    <input type="date" id="edit-wedding-date" class="w-full px-3 py-2 border border-blushPink rounded-xl focus:ring-2 focus:ring-roseGold focus:outline-none">
                </div>
                <div>
                    <label class="block font-semibold text-gray-700 mb-1">Pesan / Ucapan Utama</label>
                    <textarea id="edit-hero-message" rows="3" class="w-full px-3 py-2 border border-blushPink rounded-xl focus:ring-2 focus:ring-roseGold focus:outline-none"></textarea>
                </div>
            </div>

            <div class="flex justify-end gap-3 pt-2">
                <button onclick="closeEditModal()" class="px-4 py-2 border border-gray-300 rounded-xl text-gray-600 hover:bg-gray-50 text-xs font-semibold">
                    Batal
                </button>
                <button onclick="saveEditDetails()" class="px-5 py-2 bg-roseGold hover:bg-deepRose text-white rounded-xl text-xs font-semibold shadow-md">
                    Simpan Perubahan
                </button>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // State variables
        let weddingTargetDate = new Date("2026-12-24T08:00:00").getTime();
        let audioPlaying = false;

        // Initialize Floating Petals
        function createPetals() {
            const container = document.getElementById('petals-container');
            const petalCount = 15;
            for (let i = 0; i < petalCount; i++) {
                const petal = document.createElement('div');
                petal.classList.add('petal');
                petal.style.left = Math.random() * 100 + 'vw';
                petal.style.animationDuration = (Math.random() * 5 + 7) + 's';
                petal.style.animationDelay = Math.random() * 5 + 's';
                petal.style.width = (Math.random() * 10 + 10) + 'px';
                petal.style.height = (Math.random() * 10 + 10) + 'px';
                container.appendChild(petal);
            }
        }

        // Countdown Timer Logic
        function updateCountdown() {
            const now = new Date().getTime();
            const distance = weddingTargetDate - now;

            if (distance < 0) {
                document.getElementById("timer-days").innerText = "00";
                document.getElementById("timer-hours").innerText = "00";
                document.getElementById("timer-minutes").innerText = "00";
                document.getElementById("timer-seconds").innerText = "00";
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById("timer-days").innerText = days < 10 ? '0' + days : days;
            document.getElementById("timer-hours").innerText = hours < 10 ? '0' + hours : hours;
            document.getElementById("timer-minutes").innerText = minutes < 10 ? '0' + minutes : minutes;
            document.getElementById("timer-seconds").innerText = seconds < 10 ? '0' + seconds : seconds;
        }

        // Confetti effect
        function triggerConfetti() {
            if (typeof confetti === 'function') {
                confetti({
                    particleCount: 80,
                    spread: 70,
                    origin: { y: 0.6 },
                    colors: ['#B76E79', '#FFD1DC', '#D4AF37', '#FAF0E6']
                });
            }
        }

        // Audio Player Logic
        const audio = document.getElementById('bg-audio');
        const playIcon = document.getElementById('play-icon');
        const discIcon = document.getElementById('music-disc-icon');
        const progressBar = document.getElementById('audio-progress-bar');

        function toggleAudio() {
            if (audio.paused) {
                audio.play().then(() => {
                    playIcon.classList.remove('fa-play');
                    playIcon.classList.add('fa-pause');
                    discIcon.classList.add('animate-spin');
                }).catch(err => {
                    console.log("Audio playback prevented:", err);
                });
            } else {
                audio.pause();
                playIcon.classList.remove('fa-pause');
                playIcon.classList.add('fa-play');
                discIcon.classList.remove('animate-spin');
            }
        }

        function toggleMute() {
            audio.muted = !audio.muted;
            const volIcon = document.getElementById('volume-icon');
            if (audio.muted) {
                volIcon.classList.remove('fa-volume-high');
                volIcon.classList.add('fa-volume-xmark');
            } else {
                volIcon.classList.remove('fa-volume-xmark');
                volIcon.classList.add('fa-volume-high');
            }
        }

        audio.ontimeupdate = function() {
            if (audio.duration) {
                const percentage = (audio.currentTime / audio.duration) * 100;
                progressBar.style.width = percentage + '%';
            }
        };

        function setAudioProgress(e) {
            const container = document.getElementById('progress-container');
            const clickX = e.offsetX;
            const width = container.clientWidth;
            if (audio.duration) {
                audio.currentTime = (clickX / width) * audio.duration;
            }
        }

        // Flip Card Toggle
        function toggleCardFlip(cardElement) {
            const inner = cardElement.querySelector('.card-inner');
            inner.classList.toggle('rotate-y-180');
        }

        // Lightbox Functions
        function openLightbox(src, caption) {
            document.getElementById('lightbox-img').src = src;
            document.getElementById('lightbox-caption').innerText = caption || '';
            document.getElementById('lightbox-modal').classList.remove('hidden');
        }

        function closeLightbox() {
            document.getElementById('lightbox-modal').classList.add('hidden');
        }

        // Photo Upload Handling
        function handlePhotoUpload(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const newPhotoSrc = e.target.result;
                    const galleryGrid = document.getElementById('gallery-grid');
                    
                    const newItem = document.createElement('div');
                    newItem.className = "group relative rounded-2xl overflow-hidden shadow-lg border-2 border-white aspect-square bg-gray-100 hover:-translate-y-1 transition-all duration-300";
                    newItem.innerHTML = `
                        <img src="${newPhotoSrc}" alt="Uploaded Memory" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4 text-white">
                            <p class="font-playfair font-semibold text-sm">Special Memory</p>
                            <p class="text-xs text-gray-200">Kenangan Manis Baru</p>
                            <button onclick="openLightbox('${newPhotoSrc}', 'Special Memory')" class="mt-2 text-xs text-blushPink hover:underline text-left">Lihat Ukuran Penuh <i class="fa-solid fa-arrow-right ml-1"></i></button>
                        </div>
                    `;
                    galleryGrid.prepend(newItem);
                    triggerConfetti();
                };
                reader.readAsDataURL(file);
            }
        }

        // Wishes Form Submission
        function handleAddWish(event) {
            event.preventDefault();
            const name = document.getElementById('sender-name').value;
            const role = document.getElementById('sender-role').value || 'Bridesmaid';
            const message = document.getElementById('sender-message').value;

            const wishesList = document.getElementById('wishes-list');
            const newWish = document.createElement('div');
            newWish.className = "glass-card p-5 rounded-2xl shadow-sm border border-blushPink/60 space-y-2 hover:shadow-md transition-all animate-fade-in";
            newWish.innerHTML = `
                <div class="flex justify-between items-center">
                    <div>
                        <h5 class="font-playfair font-bold text-roseGold text-base">${escapeHtml(name)}</h5>
                        <span class="text-[11px] bg-blushPink/50 text-deepRose px-2 py-0.5 rounded-full font-medium">${escapeHtml(role)}</span>
                    </div>
                    <span class="text-[10px] text-gray-400"><i class="fa-regular fa-clock mr-1"></i> Baru saja</span>
                </div>
                <p class="text-xs md:text-sm text-gray-600 italic leading-relaxed">
                    "${escapeHtml(message)}"
                </p>
            `;

            wishesList.prepend(newWish);
            document.getElementById('wish-form').reset();
            triggerConfetti();
        }

        function escapeHtml(text) {
            return text.replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;").replace(/"/g, "&quot;").replace(/'/g, "&#039;");
        }

        // Edit Details Modal Functions
        function openEditModal() {
            document.getElementById('edit-bride-name').value = document.getElementById('bride-name-display').innerText;
            document.getElementById('edit-hero-message').value = document.getElementById('hero-message-display').innerText.replace(/^"|"$/g, '');
            document.getElementById('edit-modal').classList.remove('hidden');
        }

        function closeEditModal() {
            document.getElementById('edit-modal').classList.add('hidden');
        }

        function saveEditDetails() {
            const newName = document.getElementById('edit-bride-name').value;
            const newDate = document.getElementById('edit-wedding-date').value;
            const newMessage = document.getElementById('edit-hero-message').value;

            if (newName) document.getElementById('bride-name-display').innerText = newName;
            if (newMessage) document.getElementById('hero-message-display').innerText = `"${newMessage}"`;

            if (newDate) {
                const dateObj = new Date(newDate + "T08:00:00");
                weddingTargetDate = dateObj.getTime();
                
                const options = { year: 'numeric', month: 'long', day: 'numeric' };
                const formattedDate = dateObj.toLocaleDateString('id-ID', options);
                document.getElementById('wedding-date-display').innerHTML = `<i class="fa-solid fa-calendar-heart mr-1"></i> Tanggal Pernikahan: ${formattedDate}`;
            }

            closeEditModal();
            triggerConfetti();
        }

        // Share or Download Options
        function shareOrDownload() {
            if (navigator.share) {
                navigator.share({
                    title: 'Bride to Be Celebration',
                    text: 'Lihat ucapan & kenangan manis Bride to Be ini!',
                    url: window.location.href,
                }).catch(() => {});
            } else {
                // Fallback to copy link
                const dummy = document.createElement('input');
                document.body.appendChild(dummy);
                dummy.value = window.location.href;
                dummy.select();
                document.execCommand('copy');
                document.body.removeChild(dummy);

                // Quick notification
                alert('Link ucapan Bride to Be berhasil disalin ke clipboard!');
            }
        }

        // Window Onload Initialization
        window.onload = function() {
            createPetals();
            setInterval(updateCountdown, 1000);
            updateCountdown();

            // Set default date picker to default wedding date
            const defaultDate = new Date("2026-12-24");
            document.getElementById('edit-wedding-date').value = defaultDate.toISOString().split('T')[0];
        };
    </script>
</body>
</html>
