<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>2026 Pro Greeting</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@400;600&family=Hind:wght@500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* No Scroll Fullscreen */
        html, body {
            height: 100%; margin: 0; padding: 0; overflow: hidden;
            width: 100vw; background-color: #000; touch-action: manipulation;
        }

        body {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://i.ibb.co/qMXn642f/image-search-1767248130136.jpg');
            background-size: cover; background-position: center;
            font-family: 'Poppins', sans-serif; display: flex;
            justify-content: center; align-items: center; color: white; text-align: center;
        }

        /* Flower Layer - Card ke upar */
        .flower-petal {
            position: absolute; top: -10%; z-index: 999;
            pointer-events: none; animation: fall linear forwards;
        }
        @keyframes fall { to { transform: translateY(110vh) rotate(360deg); } }

        /* DHAK DHAK (Fast Heartbeat) Animation */
        @keyframes dhakDhak {
            0% { transform: scale(1); }
            15% { transform: scale(1.15); box-shadow: 0 0 35px rgba(255, 215, 0, 0.7); }
            30% { transform: scale(1); }
            45% { transform: scale(1.15); box-shadow: 0 0 35px rgba(255, 215, 0, 0.7); }
            100% { transform: scale(1); }
        }

        #initialUI { width: 90%; z-index: 10; }
        
        .shayari-box {
            background: rgba(0, 0, 0, 0.6); padding: 20px; border-radius: 20px;
            backdrop-filter: blur(10px); margin-bottom: 30px; border: 1px solid rgba(255,215,0,0.3);
        }

        .unlock-btn {
            padding: 18px 45px; font-size: 1.2rem; font-weight: 700; color: #000;
            background: linear-gradient(45deg, #ffd700, #fff); border: none;
            border-radius: 50px; text-transform: uppercase; cursor: pointer;
            animation: dhakDhak 1.2s infinite; 
        }

        /* Wish Card */
        .wish-container {
            position: fixed; top: 50%; left: 50%;
            transform: translate(-50%, -50%) scale(0.5);
            width: 88%; max-width: 400px; padding: 35px 20px;
            background: rgba(0, 0, 0, 0.9); backdrop-filter: blur(20px);
            border-radius: 30px; border: 2px solid #ffd700; opacity: 0;
            pointer-events: none; transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            z-index: 100;
        }
        .wish-container.active { opacity: 1; transform: translate(-50%, -50%) scale(1); pointer-events: all; }

        h1.year-2026 { font-size: 5rem; color: #ffd700; line-height: 1; margin: 10px 0; font-family: 'Playfair Display', serif; }

        /* Action Buttons */
        .btn-group { display: flex; flex-direction: column; gap: 12px; margin-top: 20px; }

        .retry-btn {
            background: #ffd700; color: #000; padding: 15px; border-radius: 50px;
            border: none; font-weight: 800; font-size: 1.1rem; cursor: pointer;
            animation: dhakDhak 1s infinite; /* Retry pe bhi Dhak Dhak */
        }

        .back-btn {
            background: rgba(255, 255, 255, 0.1); color: #fff; padding: 10px;
            border-radius: 50px; border: 1px solid rgba(255, 255, 255, 0.3);
            font-size: 0.9rem; cursor: pointer; transition: 0.2s;
        }
        .back-btn:active { background: rgba(255, 255, 255, 0.3); transform: scale(0.9); }

        .footer-social { position: fixed; bottom: 25px; display: flex; gap: 10px; z-index: 50; }
        .btn-share { padding: 12px 20px; border-radius: 50px; color: white; text-decoration: none; font-size: 0.8rem; font-weight: 600; display: flex; align-items: center; gap: 8px; }
        .wa { background: #25D366; } .fb { background: #1877F2; }

        .hidden { display: none !important; }
    </style>
</head>
<body>

    <audio id="clickSound" src="https://www.soundjay.com/buttons/sounds/button-37a.mp3"></audio>
    <audio id="bgMusic" src="https://www.chosic.com/wp-content/uploads/2021/04/Magical-Story-Gentle-Piano.mp3" loop></audio>

    <div id="initialUI">
        <div class="shayari-box">
            <p style="font-family: 'Hind', sans-serif; font-size: 1.3rem;">दाल रोटी थाली में, <br> <span style="color:#ffd700; font-weight:600;">जो मुझे हैप्पी न्यू ईयर ना बोले वो गिर पड़े नाली में । 😉</span></p>
        </div>
        <button class="unlock-btn" onclick="startCelebration()">Tap To Open</button><br>
        <img src="https://i.ibb.co/6Q3qNCk/pngtree-2026-illustration-frame-lettering-floral-frame-vintage-png-image-17088693.webp" style="width: 180px; margin-top: 30px; opacity: 0.8;">
    </div>

    <div class="wish-container" id="celebrationCard">
        <p style="letter-spacing: 4px; font-size: 0.7rem; color: #aaa;">GREETINGS FROM</p>
        <h1 style="font-family: 'Playfair Display', serif; font-size: 2.5rem; margin: 0;">Happy New Year</h1>
        <h1 class="year-2026">2026</h1>
        
        <div style="font-size: 0.85rem; color: #ff6b6b; font-style: italic; margin: 15px 0; padding: 10px; border-left: 3px solid #ffd700; text-align: left; background: rgba(255,255,255,0.05);">"When you are leaving for New Year's Eve Holidays and your boss assigns you a task."</div>
        
        <div class="btn-group">
            <button class="retry-btn" onclick="retryMagic()">Retry Magic 🌸</button>
            <button class="back-btn" onclick="goBack()"><i class="fas fa-arrow-left"></i> Back To Start</button>
        </div>
    </div>

    <div class="footer-social">
        <a href="https://wa.me/?text=Check this 2026 Greeting! 🎊" class="btn-share wa"><i class="fab fa-whatsapp"></i> WhatsApp</a>
        <a href="https://www.facebook.com/sharer/sharer.php" class="btn-share fb"><i class="fab fa-facebook-f"></i> Facebook</a>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <script>
        let rainInterval;

        function createFlower() {
            const petals = ['🌸', '🌹', '✨', '💐'];
            const flower = document.createElement('div');
            flower.className = 'flower-petal';
            flower.innerHTML = petals[Math.floor(Math.random() * petals.length)];
            flower.style.left = Math.random() * 100 + 'vw';
            flower.style.fontSize = Math.random() * 20 + 20 + 'px';
            flower.style.animationDuration = Math.random() * 2 + 1.5 + 's';
            document.body.appendChild(flower);
            setTimeout(() => flower.remove(), 4000);
        }

        function startCelebration() {
            document.getElementById('clickSound').play().catch(()=>{});
            document.getElementById('bgMusic').play().catch(()=>{});
            
            document.getElementById('initialUI').classList.add('hidden');
            document.getElementById('celebrationCard').classList.add('active');
            
            // Start Flower Rain
            if(!rainInterval) rainInterval = setInterval(createFlower, 150);
            triggerConfetti();
        }

        function retryMagic() {
            document.getElementById('clickSound').currentTime = 0;
            document.getElementById('clickSound').play().catch(()=>{});
            
            // Super Fast Flower Burst
            for(let i=0; i<40; i++) {
                setTimeout(createFlower, i * 30);
            }
            triggerConfetti();
        }

        function goBack() {
            document.getElementById('clickSound').play().catch(()=>{});
            document.getElementById('initialUI').classList.remove('hidden');
            document.getElementById('celebrationCard').classList.remove('active');
            
            // Clear rain on back to save memory
            clearInterval(rainInterval);
            rainInterval = null;
        }

        function triggerConfetti() {
            confetti({ particleCount: 150, spread: 80, origin: { y: 0.6 }, zIndex: 1000 });
        }
    </script>
</body>
</html>
