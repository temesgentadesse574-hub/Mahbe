<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ማሕቤ ቢዝነስ ማዕከል | Mahbe Business Center</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { 
            --blue: #004e92; 
            --yellow: #f7e017; 
            --gradient-body: linear-gradient(135deg, #f5f7fa 0%, #d6e4f0 100%);
            --gradient-footer: linear-gradient(90deg, #e3f2fd 0%, #fffde7 100%);
        }
        
        body { font-family: 'Segoe UI', sans-serif; margin: 0; background: var(--gradient-body); color: #333; overflow-x: hidden; min-height: 100vh; }
        
        header { background: linear-gradient(90deg, var(--blue), var(--yellow)); padding: 10px 5%; display: flex; justify-content: space-between; align-items: center; position: fixed; width: 90%; top: 0; z-index: 1000; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        .logo-area { display: flex; align-items: center; gap: 8px; }
        .logo-img-small { height: 40px; border-radius: 50%; border: 2px solid white; }
        .eth-flag { width: 22px; height: 13px; border-radius: 2px; border: 1px solid #fff; }
        nav a { color: black; text-decoration: none; font-weight: bold; margin-left: 12px; font-size: 0.8rem; cursor: pointer; }

        .content-section { display: none; padding: 110px 5% 60px; animation: fadeIn 0.8s ease; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

        /* Gallery Style */
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 20px; }
        .gallery-item { background: white; padding: 10px; border-radius: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); transition: 0.4s; animation: slideUp 0.6s ease forwards; opacity: 0; }
        @keyframes slideUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
        .gallery-item img { width: 100%; height: auto; border-radius: 10px; display: block; }

        /* Buttons & Boxes */
        .action-box { background: white; padding: 20px; border-radius: 15px; margin-top: 20px; border-left: 6px solid var(--blue); box-shadow: 0 4px 10px rgba(0,0,0,0.05); text-align: left; }
        .action-box h4 { margin-top: 0; color: var(--blue); }
        .btn-link { display: block; padding: 12px; margin: 10px 0; border-radius: 8px; text-decoration: none; font-weight: bold; text-align: center; transition: 0.3s; }
        
        .yt-btn { background: #ff0000; color: white; border: 1px solid white; }
        .tg-btn { background: #0088cc; color: white; }
        .tk-btn { background: #000; color: white; }
        .order-btn { background: var(--yellow); color: black; }

        .welcome-box { background: var(--blue); color: white; padding: 15px; border-radius: 10px; margin-bottom: 25px; text-align: center; border-bottom: 4px solid var(--yellow); }

        .home-hero { text-align: center; }
        .large-logo { width: 130px; height: 130px; border-radius: 50%; border: 4px solid var(--yellow); margin-bottom: 15px; }
        .welcome-title { font-size: 2rem; color: var(--blue); font-weight: bold; }
        
        .social-footer { display: flex; justify-content: center; gap: 15px; margin: 30px 0; }
        .social-icon { width: 35px; height: 35px; border-radius: 50%; color: white; display: flex; align-items: center; justify-content: center; text-decoration: none; font-size: 18px; }
        .tg { background: #0088cc; } .yt { background: #ff0000; } .tk { background: #000; }
        
        footer { background: var(--gradient-footer); padding: 25px; text-align: center; border-top: 1px solid #ddd; font-size: 0.8rem; }
    </style>
</head>
<body>

    <header>
        <div class="logo-area">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="logo-img-small">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Flag_of_Ethiopia.svg" class="eth-flag" alt="Eth">
            <span style="font-weight:bold; font-size: 0.9rem;">ማሕቤ</span>
        </div>
        <nav>
            <a onclick="showSection('home')">Home</a>
            <a onclick="showSection('about')">About</a>
            <a onclick="showSection('services')">Service</a>
            <a onclick="showSection('gallery')">Gallery</a>
        </nav>
    </header>

    <div id="home" class="content-section home-hero" style="display: block;">
        <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="large-logo">
        <div class="welcome-title">እንኳን ደህና መጡ!</div>
        <p>ማሕቤ የቢዝነስ አቅራቢዎች ነን</p>
        
        <div class="action-box" style="text-align: center;">
            <h4>እኛን ላግኘት እና የትዕዛዝ ስራዎች ለመስጠት</h4>
            <div style="display: flex; gap: 10px; justify-content: center;">
                <a href="https://t.me/temu_amen" class="btn-link order-btn" style="flex:1;"><i class="fab fa-telegram-plane"></i> @temu_amen</a>
                <a href="https://t.me/mahbe_3" class="btn-link order-btn" style="flex:1;"><i class="fab fa-telegram-plane"></i> @mahbe_3</a>
            </div>
        </div>

        <div class="action-box">
            <h4>በየቀኑ የሚለቀቁ ስራዎችን ለማየት ቴሌግራማችንን ይጎብኙ</h4>
            <a href="https://t.me/mahitsene_betechirstiyan" class="btn-link tg-btn" target="_blank">ማሕፀነ ቤተክርስቲያን</a>
            <a href="https://t.me/mahbe_business_centere" class="btn-link tg-btn" target="_blank">ማሕቤ ቢዝነስ ማዕከል</a>
        </div>
    </div>

    <div id="about" class="content-section">
        <h2>ስለ እኛ (About)</h2>
        <p>እኛ ማሕቤ ቢዝነስ ማዕከል ነን። መንፈሳዊና ዓለማዊ ለስጋችንም ለነፍሳችንም የሚጠቅሙን ነገሮች የምንገለገልበት ትልቅ ካምፓኒ ነው።</p>
        
        <div class="action-box">
            <h4>መንፈሳዊ እና የስርዓተ ቅዳሴ ትምህርቶች ለመከታተል</h4>
            <a href="https://www.tiktok.com/@mahbe_4?_r=1&_t=ZM-91wveqksd12" class="btn-link tk-btn" target="_blank"><i class="fab fa-tiktok"></i> Follow us on TikTok</a>
        </div>

        <p style="font-size: 0.75rem; color: #777; margin-top: 30px; font-style: italic;">Created by Temesgen Tadesse @temu_amen</p>
    </div>

    <div id="gallery" class="content-section" style="text-align: center;">
        <div class="welcome-box">
            <h3 style="margin:0;">እንኳን ወደ እኛ ስራዎች በደህና መጡ! 🙏</h3>
        </div>
        
        <div class="gallery-grid">
            <div class="gallery-item" style="animation-delay: 0.1s;"><img src="https://i.ibb.co/zhjkJXpm/20251219-224720.png"></div>
            <div class="gallery-item" style="animation-delay: 0.2s;"><img src="https://i.ibb.co/1fwpFk6H/20251216-002122.png"></div>
            <div class="gallery-item" style="animation-delay: 0.3s;"><img src="https://i.ibb.co/QF7PbLyj/20251215-155642.png"></div>
            <div class="gallery-item" style="animation-delay: 0.4s;"><img src="https://i.ibb.co/XN9qjfN/20251210-224030.jpg"></div>
            <div class="gallery-item" style="animation-delay: 0.5s;"><img src="https://i.ibb.co/pj0G79js/20251210-225324.png"></div>
            <div class="gallery-item" style="animation-delay: 0.6s;"><img src="https://i.ibb.co/PZBYcCN3/20251209-234129.jpg"></div>
            <div class="gallery-item" style="animation-delay: 0.7s;"><img src="https://i.ibb.co/PsqD4xFT/20251202-120100.jpg"></div>
            <div class="gallery-item" style="animation-delay: 0.8s;"><img src="https://i.ibb.co/LLrvHzJ/20251205-104728.jpg"></div>
            <div class="gallery-item" style="animation-delay: 0.9s;"><img src="https://i.ibb.co/fYH5CVpV/20251128-093307.png"></div>
            <div class="gallery-item" style="animation-delay: 1.0s;"><img src="https://i.ibb.co/fzPz8G2s/20251127-100038.png"></div>
            <div class="gallery-item" style="animation-delay: 1.1s;"><img src="https://i.ibb.co/zTn3fYKp/20260102-164217.png"></div>
            <div class="gallery-item" style="animation-delay: 1.2s;"><img src="https://i.ibb.co/qMk0cqCf/20251230-112306.png"></div>
            <div class="gallery-item" style="animation-delay: 1.3s;"><img src="https://i.ibb.co/qLhqKJWR/20251230-073553.png"></div>
            <div class="gallery-item" style="animation-delay: 1.4s;"><img src="https://i.ibb.co/8nwp8rkQ/20251219-132621.png"></div>
            <div class="gallery-item" style="animation-delay: 1.5s;"><img src="https://i.ibb.co/LzZCXn0y/20251205-122512.png"></div>
            <div class="gallery-item" style="animation-delay: 1.6s;"><img src="https://i.ibb.co/5XVVtK0q/20251122-144552.png"></div>
            <div class="gallery-item" style="animation-delay: 1.7s;"><img src="https://i.ibb.co/LhnMBPNF/20251120-202649.jpg"></div>
            <div class="gallery-item" style="animation-delay: 1.8s;"><img src="https://i.ibb.co/YB2q959t/20251120-200348.jpg"></div>
            <div class="gallery-item" style="animation-delay: 1.9s;"><img src="https://i.ibb.co/HTs32qzY/20251119-140559.png"></div>
            <div class="gallery-item" style="animation-delay: 2.0s;"><img src="https://i.ibb.co/v7RQtHD/20251118-215305.png"></div>
            <div class="gallery-item" style="animation-delay: 2.1s;"><img src="https://i.ibb.co/WNFRQj2H/20251118-200618.png"></div>
            <div class="gallery-item" style="animation-delay: 2.2s;"><img src="https://i.ibb.co/d0KmLtSN/20251114-122726.jpg"></div>
            <div class="gallery-item" style="animation-delay: 2.3s;"><img src="https://i.ibb.co/FLLpDNv5/20251108-122343.png"></div>
            <div class="gallery-item" style="animation-delay: 2.4s;"><img src="https://i.ibb.co/d46N12Ms/20251109-184251.png"></div>
            <div class="gallery-item" style="animation-delay: 2.5s;"><img src="https://i.ibb.co/3yv4bm2Z/20251023-182429.png"></div>
            <div class="gallery-item" style="animation-delay: 2.6s;"><img src="https://i.ibb.co/vgz9sgX/20251005-123849.png"></div>
            <div class="gallery-item" style="animation-delay: 2.7s;"><img src="https://i.ibb.co/r2JxTnM2/20251003-164027.jpg"></div>
            <div class="gallery-item" style="animation-delay: 2.8s;"><img src="https://i.ibb.co/21dLh2P5/20251106-082659.jpg"></div>
        </div>

        <div class="action-box">
            <h4>ተጨማሪ ስራዎች በቪዲዮ ለማየት</h4>
            <a href="https://youtube.com/@mahbe_4" target="_blank" class="btn-link yt-btn"><i class="fab fa-youtube"></i> Visit YouTube Channel</a>
        </div>
    </div>

    <div id="services" class="content-section">
        <h2>አገልግሎቶቻችን (Service)</h2>
        <div class="action-box"><h4>📹 ቪዲዮ ኢዲቲንግ</h4><p>ከፍተኛ ጥራት ያለው ኤዲቲንግ</p></div>
        <div class="action-box"><h4>🎨 ግራፊክስ ዲዛይን</h4><p>የፈጠራ ስራዎች</p></div>
    </div>

    <div class="social-footer">
        <a href="https://t.me/mahbe_business_centere" target="_blank" class="social-icon tg"><i class="fab fa-telegram-plane"></i></a>
        <a href="https://youtube.com/@mahbe_4" target="_blank" class="social-icon yt"><i class="fab fa-youtube"></i></a>
        <a href="https://www.tiktok.com/@mahbe_4" target="_blank" class="social-icon tk"><i class="fab fa-tiktok"></i></a>
    </div>

    <footer>
        <p>© 2026 ማሕቤ ቢዝነስ ማዕከል | 📞 0928525029 / 0971825151</p>
    </footer>

    <script>
        function showSection(id) {
            const sections = document.getElementsByClassName('content-section');
            for (let s of sections) { s.style.display = 'none'; }
            document.getElementById(id).style.display = 'block';
            window.scrollTo({top: 0, behavior: 'smooth'});
        }
    </script>
</body>
</html>
