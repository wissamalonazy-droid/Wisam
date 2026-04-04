<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Suhail Elite | بوابة النخبة</title>
    <style>
        :root {
            --gold: #D4AF37;
            --black: #0a0a0a;
            --glass: rgba(255, 255, 255, 0.05);
        }

        body {
            margin: 0;
            padding: 0;
            background: var(--black);
            color: white;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow-x: hidden;
        }

        /* خلفية متحركة خفيفة */
        .bg-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, #1a1a1a 0%, #000 100%);
            z-index: -1;
        }

        .container {
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .logo {
            font-size: 3rem;
            letter-spacing: 5px;
            font-weight: bold;
            color: var(--gold);
            text-transform: uppercase;
            margin-bottom: 20px;
            text-shadow: 0 0 20px rgba(212, 175, 55, 0.3);
        }

        .tagline {
            font-size: 1.2rem;
            color: #888;
            margin-bottom: 40px;
        }

        /* كروت التجربة الترفيهية */
        .experience-grid {
            display: flex;
            gap: 25px;
            padding: 20px;
        }

        .card {
            background: var(--glass);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 30px;
            width: 250px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            transition: 0.4s;
            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: var(--gold);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.1);
        }

        .card h3 {
            color: var(--gold);
            margin-bottom: 15px;
        }

        .btn-enter {
            margin-top: 40px;
            padding: 15px 40px;
            background: transparent;
            border: 1px solid var(--gold);
            color: var(--gold);
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn-enter:hover {
            background: var(--gold);
            color: var(--black);
        }
    </style>
</head>
<body>
    <div class="bg-overlay"></div>
    
    <div class="container">
        <div class="logo">SUHAIL ELITE</div>
        <div class="tagline">حول هويتك إلى أسطورة رقمية.. ترفيه يتجاوز الواقع</div>

        <div class="experience-grid">
            <div class="card">
                <h3>الفارس الرقمي</h3>
                <p>حول صورتك إلى فيديو سينمائي تاريخي بلمسة ذكاء اصطناعي.</p>
            </div>
            <div class="card">
                <h3>اللحن الخاص</h3>
                <p>أغنية راب أو بوب باسمك تعكس هويتك الفخمة.</p>
            </div>
            <div class="card">
                <h3>بوابة الميتا</h3>
                <p>أفاتار "Elite" خاص بك للمجتمعات الافتراضية.</p>
            </div>
        </div>

        <button class="btn-enter" onclick="alert('مرحباً بك في عصر الترفيه الجديد!')">ابدأ رحلتك الآن</button>
    </div>
</body>
</html>
