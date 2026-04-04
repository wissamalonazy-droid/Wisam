<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Suhail Elite | ألعاب النخبة</title>
    <style>
        :root { --gold: #D4AF37; --black: #0a0a0a; }
        body { margin: 0; background: var(--black); color: white; font-family: sans-serif; text-align: center; overflow: hidden; }
        .container { height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; }
        .logo { font-size: 2.5rem; color: var(--gold); letter-spacing: 5px; margin-bottom: 30px; }
        
        /* تصميم عجلة أو صندوق الحظ */
        #display-box {
            width: 300px; height: 200px;
            border: 2px solid var(--gold);
            border-radius: 20px;
            display: flex; align-items: center; justify-content: center;
            font-size: 1.5rem; font-weight: bold;
            background: rgba(255,255,255,0.05);
            margin-bottom: 30px;
            transition: 0.5s;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.2);
        }

        .btn-play {
            padding: 15px 50px;
            background: var(--gold);
            color: var(--black);
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-play:hover { transform: scale(1.1); box-shadow: 0 0 30px var(--gold); }
        
        .result-text { color: var(--gold); animation: fadeIn 1s; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">SUHAIL ELITE</div>
        <p>اكتشف هويتك الأسطورية اليوم..</p>
        
        <div id="display-box">؟ ؟ ؟</div>
        
        <button class="btn-play" onclick="spinWheel()">ابدأ القرعة</button>
        
        <p id="sub-msg" style="margin-top: 20px; color: #666;"></p>
    </div>

    <script>
        const rewards = [
            "الفارس التاريخي (فيديو راب)",
            "زعيم السايبربانك (أفاتار)",
            "شاعر النخبة (قصيدة مخصصة)",
            "المحارب الذهبي (تصوير سينمائي)",
            "عضو VIP (باقة شاملة)"
        ];

        function spinWheel() {
            const box = document.getElementById('display-box');
            const msg = document.getElementById('sub-msg');
            box.style.transform = "rotateX(360deg)";
            box.innerHTML = "جاري الاختيار...";
            
            setTimeout(() => {
                const randomReward = rewards[Math.floor(Math.random() * rewards.length)];
                box.innerHTML = `<span class="result-text">${randomReward}</span>`;
                box.style.transform = "rotateX(0deg)";
                msg.innerHTML = "لقد تم اختيار قدرك الرقمي.. أرسل النتيجة لسهيل لتنفيذها!";
            }, 1500);
        }
    </script>
</body>
</html>
