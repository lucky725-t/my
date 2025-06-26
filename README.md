<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Special Someone ❤️</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500&display=swap');
        
        body {
            background: linear-gradient(45deg, #ffccd5, #ff9e9e);
            min-height: 100vh;
            font-family: 'Poppins', sans-serif;
            overflow-x: hidden;
        }
        
        .heart {
            position: absolute;
            pointer-events: none;
            animation: float 5s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }
        
        .message-box {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            transition: all 0.3s ease;
        }
        
        .message-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
        }
        
        .title {
            font-family: 'Great Vibes', cursive;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .btn-heart {
            transition: all 0.3s ease;
        }
        
        .btn-heart:hover {
            transform: scale(1.1);
        }

        /* Audio player styling */
        #audioPlayer {
            position: fixed;
            bottom: 20px;
            right: 20px;
            opacity: 0;
            width: 0;
            height: 0;
        }

        /* Song info styling */
        .now-playing {
            position: fixed;
            bottom: 80px;
            right: 20px;
            background: rgba(255,255,255,0.9);
            padding: 8px 12px;
            border-radius: 20px;
            font-size: 14px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            display: flex;
            align-items: center;
        }

        .now-playing::before {
            content: '♫ ';
            margin-right: 5px;
        }

        .browser-alert {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(0,0,0,0.7);
            color: white;
            padding: 10px;
            text-align: center;
            z-index: 1000;
            display: none;
        }
    </style>
</head>
<body class="flex items-center justify-center p-4">
    
       
    </div>
    
    <!-- Multiple audio sources for compatibility -->
    <audio id="audioPlayer" loop>
        <source src="https://audio.jukehost.co.uk/KtoysMbakvwof9eu0sSoUVP80Ywk0WWr" type="audio/mpeg">
        <source src="https://audio.jukehost.co.uk/KtoysMbakvwof9eu0sSoUVP80Ywk0WWr" type="audio/ogg">
        Your browser does not support the audio element.
    </audio>
    
    <!-- Now playing info -->
    <div id="nowPlaying" class="now-playing">
        BACHALO - Akhil
    </div>
    
    <!-- Volume control -->
    <div id="volumeControl" class="fixed bottom-16 right-4 bg-white p-2 rounded-full shadow-lg">
        <input type="range" min="0" max="1" step="0.1" value="0.5" 
               class="w-24" 
               oninput="document.getElementById('audioPlayer').volume = this.value">
    </div>
    
    <div id="hearts-container"></div>
    
    <div class="message-box rounded-xl p-8 max-w-2xl w-full relative overflow-hidden">
        <!-- Watermark hearts -->
        <div class="absolute -top-20 -right-20 text-red-200 opacity-20 text-6xl">❤️❤️</div>
        <div class="absolute -bottom-20 -left-20 text-red-200 opacity-20 text-6xl">❤️❤️</div>
        
        <div class="text-center mb-8">
            <h1 class="title text-5xl md:text-6xl text-pink-600 mb-4">For My Love</h1>
            <div class="h-12">
                <span id="typed" class="text-xl text-gray-700 font-medium"></span>
            </div>
        </div>
        
        <div class="space-y-6 text-gray-700 text-lg mb-8">
            <p>Every moment with you feels like a beautiful dream I never want to wake up from.</p>
            <p>Your smile lights up my world brighter than a thousand suns.</p>
            <p>I fall in love with you more each day, in ways I didn't even know were possible.</p>
        </div>
        
        <div class="flex justify-center">
            <button onclick="createHearts()" class="btn-heart px-6 py-3 bg-gradient-to-r from-pink-500 to-red-500 text-white rounded-full shadow-lg flex items-center">
                <span class="mr-2">Click for Love</span>
                <span class="text-xl">❤️</span>
            </button>
        </div>
        
        <!-- Memory section -->
        <div class="mt-12 border-t border-pink-200 pt-6">
            <h2 class="text-2xl text-center text-pink-600 mb-4">Our Beautiful Memories</h2>
            <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
                <div class="memory-box bg-white p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow">
                    <div class="text-pink-500 text-2xl mb-2">🌟</div>
                    <h3 class="font-medium">Our First Date</h3>
                    <p class="text-sm text-gray-500">The day I knew you were special</p>
                </div>
                <div class="memory-box bg-white p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow">
                    <div class="text-pink-500 text-2xl mb-2">🎂</div>
                    <h3 class="font-medium">Your Birthday</h3>
                    <p class="text-sm text-gray-500">Seeing your happy smile</p>
                </div>
                <div class="memory-box bg-white p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow">
                    <div class="text-pink-500 text-2xl mb-2">🌙</div>
                    <h3 class="font-medium">Late Night Talks</h3>
                    <p class="text-sm text-gray-500">Hours feel like minutes</p>
                </div>
            </div>
        </div>

        <!-- Music control button -->
        <button id="musicToggle" class="fixed bottom-4 right-4 bg-pink-500 text-white p-3 rounded-full shadow-lg">
            ♫ ♫
        </button>
    </div>

    <script>
        // Browser compatibility check
        const isIOS = /iPad|iPhone|iPod/.test(navigator.userAgent);
        const isSafari = /Safari/.test(navigator.userAgent) && /Apple Computer/.test(navigator.vendor);
        
        if (isIOS || isSafari) {
            document.getElementById('browserAlert').style.display = 'block';
            setTimeout(() => {
                document.getElementById('browserAlert').style.display = 'none';
            }, 5000);
        }

        // Typing animation
        var typed = new Typed('#typed', {
            strings: [
                "You make my heart skip a beat",
                "My favorite place is with you",
                "Forever wouldn't be long enough",
                "I love you more every day"
            ],
            typeSpeed: 50,
            backSpeed: 30,
            loop: true,
            showCursor: false
        });
        
        // Audio player logic
        const audioPlayer = document.getElementById('audioPlayer');
        const musicToggle = document.getElementById('musicToggle');
        const volumeControl = document.getElementById('volumeControl');
        const nowPlaying = document.getElementById('nowPlaying');
        let isMusicPlaying = false;

        // Enable audio on any user interaction (required for some browsers)
        function enableAudio() {
            const playPromise = audioPlayer.play();
            
            if (playPromise !== undefined) {
                playPromise.then(_ => {
                    // Audio is playing
                    isMusicPlaying = true;
                    musicToggle.innerHTML = '♫ ♫';
                    nowPlaying.style.display = 'flex';
                    volumeControl.style.display = 'block';
                    audioPlayer.volume = 0.5;
                })
                .catch(error => {
                    // Audio play was prevented
                    console.log("Audio play prevented, waiting for user interaction");
                    document.getElementById('browserAlert').style.display = 'block';
                });
            }
        }

        // Start music after user interaction
        function startMusic() {
            // First try to play (might work on Chrome/Firefox)
            enableAudio();
            
            // Set up user interaction handler
            const interactionEvents = ['click', 'touchstart', 'keydown'];
            
            interactionEvents.forEach(event => {
                window.addEventListener(event, () => {
                    enableAudio();
                    // Remove all interaction listeners after first interaction
                    interactionEvents.forEach(e => {
                        window.removeEventListener(e, enableAudio);
                    });
                }, { once: true });
            });
        }

        // Initialize music
        startMusic();

        // Music toggle button
        musicToggle.addEventListener('click', function() {
            if (isMusicPlaying) {
                audioPlayer.pause();
                musicToggle.innerHTML = '♫';
                volumeControl.style.display = 'none';
                nowPlaying.style.display = 'none';
            } else {
                audioPlayer.play();
                musicToggle.innerHTML = '♫ ♫';
                volumeControl.style.display = 'block';
                nowPlaying.style.display = 'flex';
            }
            isMusicPlaying = !isMusicPlaying;
        });

        // Volume control visibility
        musicToggle.addEventListener('mouseenter', function() {
            if (isMusicPlaying) {
                volumeControl.style.display = 'block';
            }
        });

        volumeControl.addEventListener('mouseleave', function() {
            setTimeout(() => {
                volumeControl.style.display = 'none';
            }, 2000);
        });

        // Create floating hearts
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 2 + 's';
            heart.style.fontSize = Math.random() * 20 + 10 + 'px';
            document.getElementById('hearts-container').appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 5000);
        }
        
        function createHearts() {
            // Ensure music is playing at good volume when button clicked
            if (!isMusicPlaying) {
                audioPlayer.play();
                isMusicPlaying = true;
                musicToggle.innerHTML = '♫ ♫';
                volumeControl.style.display = 'block';
                nowPlaying.style.display = 'flex';
            }
            audioPlayer.volume = 0.7;
            
            // Create hearts animation
            for (let i = 0; i < 15; i++) {
                setTimeout(createHeart, i * 100);
            }
            
            // Show romantic messages
            const messages = [
                "I love you!",
                "You're amazing!",
                "My heart is yours",
                "You're my dream come true",
                "I'm so lucky to have you"
            ];
            const randomMessage = messages[Math.floor(Math.random() * messages.length)];
            
            const alertDiv = document.createElement('div');
            alertDiv.className = 'fixed top-4 left-1/2 transform -translate-x-1/2 bg-white px-6 py-3 rounded-full shadow-lg text-pink-600 font-medium animate-bounce';
            alertDiv.textContent = randomMessage;
            document.body.appendChild(alertDiv);
            
            setTimeout(() => {
                alertDiv.remove();
            }, 2000);
        }
        
        // Create occasional random hearts
        setInterval(createHeart, 3000);

        // Show brief instructions for mobile users
        if (/Mobi|Android/i.test(navigator.userAgent)) {
            const mobileAlert = document.createElement('div');
            mobileAlert.className = 'fixed top-4 left-1/2 transform -translate-x-1/2 bg-white px-6 py-3 rounded-full shadow-lg text-pink-600 font-medium animate-bounce';
            mobileAlert.textContent = 'Tap "Click for Love" for music!';
            document.body.appendChild(mobileAlert);
            
            setTimeout(() => {
                mobileAlert.remove();
            }, 3000);
        }
    </script>
</body>
</html>
