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
        
        body { 
            font-family: 'Segoe UI', sans-serif; 
            margin: 0; 
            background: var(--gradient-body); 
            color: #333; 
            overflow-x: hidden; 
            min-height: 100vh;
        }
        
        /* Header */
        header { 
            background: linear-gradient(90deg, var(--blue), var(--yellow)); 
            padding: 10px 5%; display: flex; justify-content: space-between; 
            align-items: center; position: fixed; width: 90%; top: 0; z-index: 1000; 
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        .logo-area { display: flex; align-items: center; gap: 8px; }
        .logo-img-small { height: 40px; border-radius: 50%; border: 2px solid white; }
        .eth-flag { width: 22px; height: 13px; border-radius: 2px; border: 1px solid #fff; }
        nav a { color: black; text-decoration: none; font-weight: bold; margin-left: 12px; font-size: 0.8rem; cursor: pointer; }

        /* Login Overlay */
        #login-overlay { 
            position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
            background: linear-gradient(135deg, var(--blue), #002a4d); 
            display: flex; justify-content: center; align-items: center; z-index: 3000; color: white; 
        }
        .login-box { 
            background: rgba(255, 255, 255, 0.1); backdrop-filter: blur(10px); 
            padding: 35px; border-radius: 20px; width: 300px; text-align: center; 
            border: 1px solid rgba(255,255,255,0.2); 
        }
        .login-box input { width: 90%; padding: 12px; margin: 10px 0; border-radius: 8px; border: none; outline: none; }
        .login-btn { background: var(--yellow); color: black; border: none; padding: 12px; width: 100%; border-radius: 8px; font-weight: bold; cursor: pointer; }
        .forget-pass { font-size: 0.75rem; color: #fff; text-decoration: underline; margin-top: 15px; display: block; cursor: pointer; }

        /* Content Sections */
        .content-section { display: none; padding: 110px 8% 60px; animation: fadeIn 0.6s ease-in-out; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        /* Home Style */
        .home-hero { text-align: center; }
        .large-logo { 
            width: 140px; height: 140px; border-radius: 50%; 
            border: 5px solid var(--yellow); box-shadow: 0 10px 25px rgba(0,0,0,0.15); 
            margin-bottom: 20px; 
        }
        .welcome-title { font-size: 2.2rem; color: var(--blue); font-weight: bold; margin-bottom: 10px; }

        h2 { color: var(--blue); border-bottom: 3px solid var(--yellow); display: inline-block; margin-bottom: 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 20px; margin-top: 25px; }
        .card { 
            background: rgba(255, 255, 255, 0.7); padding: 25px; border-radius: 15px; 
            border-left: 6px solid var(--blue); backdrop-filter: blur(5px); 
            text-align: left; box-shadow: 0 4px 10px rgba(0,0,0,0.03);
        }

        /* Creator Style in About */
        .creator-text { font-size: 0.75rem; color: #666; margin-top: 40px; border-top: 1px solid #ddd; padding-top: 10px; font-style: italic; }

        /* Social */
        .social-footer { display: flex; justify-content: center; gap: 18px; margin: 30px 0; }
        .social-icon { width: 40px; height: 40px; border-radius: 50%; color: white; display: flex; align-items: center; justify-content: center; text-decoration: none; font-size: 20px; transition: 0.3s; }
        .tg { background: #0088cc; } .yt { background: #ff0000; } .tk { background: #000; }
        .social-icon:hover { transform: scale(1.1); }

        /* Gradient Footer */
        footer { 
            background: var(--gradient-footer); 
            padding: 25px; text-align: center; 
            border-top: 1px solid #ddd; font-size: 0.8rem; 
        }
    </style>
</head>
<body>

    <div id="login-overlay">
        <div class="login-box">
            <h2 id="login-msg">እንኳን ደህና መጡ!</h2>
            <input type="text" id="username" placeholder="Username">
            <input type="password" id="password" placeholder="Password">
            <button class="login-btn" onclick="checkLogin()">Login / ግባ</button>
            <a href="https://t.me/temu_amen" target="_blank" class="forget-pass">Password ረሱ? (Forget Password)</a>
            <p id="error-msg" style="color: #ff4d4d; display: none; margin-top: 10px; font-weight: bold;">የተሳሳተ መረጃ!</p>
        </div>
    </div>

    <div id="main-site" style="display: none;">
        <header>
            <div class="logo-area">
                <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="logo-img-small">
                <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Flag_of_Ethiopia.svg" class="eth-flag" alt="Ethiopia">
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
            <p style="font-size: 1.25rem; color: #444;">ማሕቤ የቢዝነስ አቅራቢዎች ነን</p>
            <p style="color: #d9534f; font-weight: bold; font-size: 1.5rem; margin-top: 10px;">ምን ይፈልጋሉ?</p>
            <p style="color: #666;">Graphics Design, Video Editing or What you want NOW!</p>
            
            <div class="grid">
                <div class="card"><h4>🚩 ባነር</h4><p>ከ100 በላይ ስራዎች</p></div>
                <div class="card"><h4>🎨 ሎጎ</h4><p>ከ50 በላይ ስራዎች</p></div>
                <div class="card"><h4>🖼️ Thumbnail</h4><p>ከ18 በላይ ስራዎች</p></div>
            </div>
        </div>

        <div id="about" class="content-section">
            <h2>ስለ እኛ (About)</h2>
            <p>እኛ ማሕቤ ቢዝነስ ማዕከል ነን። <strong>ማሕቤ</strong> ማለት <strong>"ማሕፀነ ቤተክርስቲያን ሚዲያ"</strong> ማለት ሲሆን፣ ሁለተኛ ትርጉሙ ደግሞ <strong>"ማሕቤ ሕትመት ቤት"</strong> የሚል ትርጉም ያለው የማሕፀነ ቤተክርስቲያን አንዱ ብራንች ካምፓኒ ነው።</p>
            <p>በዚህም መንፈሳዊና ዓለማዊ ለስጋችንም ለነፍሳችንም የሚጠቅሙን ነገሮች የምንገለገልበት ትልቅ ካምፓኒ ነው ።</p>
            
            <div class="card" style="margin-top: 25px;">
                <h4>🙏 መንፈሳዊ አገልግሎቶች</h4>
                <p>ቅኔ፣ ስብከተ ወንጌል፣ የመጻሕፍት ትምህርት፣ የመጻሕፍት ሽያጭ እና ሌሎችም</p>
            </div>

            <p class="creator-text">Created by Temesgen Tadesse @temu_amen on Telegram</p>
        </div>

        <div id="services" class="content-section">
            <h2>አገልግሎቶቻችን (Service)</h2>
            <div class="grid">
                <div class="card"><h4>📹 ቪዲዮ ኢዲቲንግ</h4><p>ከፍተኛ ጥራት ያለው የቪዲዮ ኤዲቲንግ አገልግሎት</p></div>
                <div class="card"><h4>🎨 ግራፊክስ ዲዛይን</h4><p>የፈጠራ ስራዎች፣ ባነር፣ ሎጎ እና ስቲከሮች</p></div>
                <div class="card"><h4>📱 ዲጅታል ማርካቲንግ</h4><p>የእርስዎን ምርትና አገልግሎት ለብዙዎች ማድረስ</p></div>
            </div>
        </div>

        <div id="gallery" class="content-section" style="text-align:center;">
            <h2>የስራዎቻችን ማሳያ (Gallery)</h2>
            <div style="background: #222; color: var(--yellow); padding: 60px 20px; border-radius: 20px; font-size: 1.6rem; font-weight: bold; box-shadow: 0 10px 20px rgba(0,0,0,0.2);">
                <i class="fas fa-images" style="font-size: 3rem; margin-bottom: 15px;"></i><br>
                እስካሁን የተሰሩ ስራዎች በፎቶ <br> 
                <span style="letter-spacing: 3px; font-size: 1.2rem; color: #fff;">COMING SOON...</span>
            </div>
        </div>

        <div class="social-footer">
            <a href="https://t.me/Mahbe_4" target="_blank" class="social-icon tg"><i class="fab fa-telegram-plane"></i></a>
            <a href="#" class="social-icon yt"><i class="fab fa-youtube"></i></a>
            <a href="#" class="social-icon tk"><i class="fab fa-tiktok"></i></a>
        </div>

        <footer>
            <p style="font-weight: bold; margin-bottom: 5px;">© 2026 ማሕቤ ቢዝነስ ማዕከል</p>
            <p>📞 0928525029 / 0971825151</p>
            <div style="margin-top: 10px; opacity: 0.7; font-size: 0.7rem;">
                https://temesgentadesse574-hub.github.io/Mahbe/
            </div>
        </footer>
    </div>

    <script>
        // Login Logic
        function checkLogin() {
            const u = document.getElementById("username").value;
            const p = document.getElementById("password").value;
            // Username: teta59649 | Password: Te@12345
            if(u === "teta59649" && p === "Te@12345") {
                document.getElementById("login-overlay").style.display = "none";
                document.getElementById("main-site").style.display = "block";
            } else {
                document.getElementById("error-msg").style.display = "block";
            }
        }

        // Section Navigation Logic
        function showSection(id) {
            const sections = document.getElementsByClassName('content-section');
            for (let s of sections) { s.style.display = 'none'; }
            document.getElementById(id).style.display = 'block';
            window.scrollTo({top: 0, behavior: 'smooth'});
        }

        // Welcome Message Animation
        const loginTitle = document.getElementById("login-msg");
        setInterval(() => {
            loginTitle.innerText = loginTitle.innerText === "እንኳን ደህና መጡ!" ? "Welcome!" : "እንኳን ደህና መጡ!";
        }, 2500);
    </script>
</body>
</html>            color: white;
        }
        .login-box {
            background: rgba(255, 255, 255, 0.1); backdrop-filter: blur(10px);
            padding: 30px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.2);
            text-align: center; width: 280px;
        }
        .login-box input { width: 90%; padding: 10px; margin: 8px 0; border-radius: 5px; border: none; }
        .login-btn { background: var(--primary-yellow); color: black; border: none; padding: 10px; width: 100%; border-radius: 5px; font-weight: bold; cursor: pointer; }

        /* Content */
        .main-content { display: none; padding-top: 70px; }
        .hero { background: var(--primary-blue); color: white; padding: 50px 20px; text-align: center; }

        section { padding: 40px 10%; }
        h2 { color: var(--primary-blue); border-bottom: 2px solid var(--primary-yellow); display: inline-block; }

        .service-card {
            background: #f9f9f9; padding: 20px; border-radius: 12px;
            margin-bottom: 15px; border-left: 5px solid var(--primary-blue);
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        /* Social Media Icons */
        .social-container { display: flex; justify-content: center; gap: 15px; padding: 20px 0; }
        .social-icon {
            width: 35px; height: 35px; border-radius: 50%; display: flex;
            align-items: center; justify-content: center; color: white;
            text-decoration: none; font-size: 18px; transition: 0.3s;
        }
        .tg { background: #0088cc; }
        .fb { background: #3b5998; }
        .yt { background: #ff0000; }
        .tk { background: #000000; }
        .ig { background: #d6249f; }
        .social-icon:hover { transform: scale(1.2); }

        footer { background: #f4f4f4; padding: 20px; text-align: center; font-size: 0.8rem; border-top: 1px solid #ddd; }
    </style>
</head>
<body>

    <div id="login-overlay">
        <div class="login-box">
            <div id="welcome-msg" style="font-size: 24px; font-weight: bold; margin-bottom: 10px;">እንኳን ደህና መጡ!</div>
            <p style="font-size: 0.8rem; color: var(--primary-yellow); margin-bottom: 15px;">በመለያዎ ገብተው ስራዎቻችንን ይዩ</p>
            <input type="text" id="username" placeholder="Username">
            <input type="password" id="password" placeholder="Password">
            <button class="login-btn" onclick="checkLogin()">Login / ግባ</button>
            <p id="error-msg" style="color: #ff4d4d; display: none; margin-top: 10px; font-weight: bold;">የተሳሳተ መረጃ!</p>
        </div>
    </div>

    <div id="main-site" class="main-content">
        <header>
            <div class="logo-container">
                <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="logo-img">
                <span class="logo-text">ማሕቤ</span>
            </div>
            <nav>
                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#services">Service</a>
                <a href="javascript:void(0)" onclick="logout()" style="color:red;">Logout</a>
            </nav>
        </header>

        <section id="home" class="hero">
            <h1>ማሕቤ ቢዝነስ ሴንተር</h1>
            <p>ጥራት ያለው አገልግሎት የእኛ መለያ ነው!</p>
        </section>

        <section id="about">
            <h2>ስለ ማሕቤ (About)</h2>
            <p>ማሕቤ ቢዝነስ ሴንተር በግራፊክስ ዲዛይን፣ በቪዲዮ ፕሮዳክሽን እና በተለያዩ መንግስታዊ አገልግሎቶች ላይ የተሰማራ ዘመናዊ የንግድ ማዕከል ነው።</p>
        </section>

        <section id="services">
            <h2>አገልግሎቶቻችን (Service)</h2>
            <div class="service-card">
                <h3>🎨 Graphics & Design</h3>
                <p>Banner, Sticker, Logo, Professional Business Card</p>
            </div>
            <div class="service-card">
                <h3>🎬 Production</h3>
                <p>Video Editing, Camera Man, All Production Works</p>
            </div>
            <div class="service-card">
                <h3>📑 Government Services</h3>
                <p>Passport Renewal, License Renewal & Issued</p>
            </div>
        </section>

        <div class="social-container">
            <a href="https://t.me/Mahbe_4" class="social-icon tg"><i class="fab fa-telegram-plane"></i></a>
            <a href="#" class="social-icon fb"><i class="fab fa-facebook-f"></i></a>
            <a href="#" class="social-icon yt"><i class="fab fa-youtube"></i></a>
            <a href="#" class="social-icon tk"><i class="fab fa-tiktok"></i></a>
            <a href="#" class="social-icon ig"><i class="fab fa-instagram"></i></a>
        </div>

        <footer>
            <p>© 2026 ማሕቤ ቢዝነስ ሴንተር | 📞 0928525029 / 0971825151</p>
        </footer>
    </div>

    <script>
        // Animation
        const messages = ["እንኳን ደህና መጡ!", "Welcome!"];
        let idx = 0;
        setInterval(() => {
            idx = (idx + 1) % messages.length;
            document.getElementById("welcome-msg").innerText = messages[idx];
        }, 2000);

        function checkLogin() {
            const user = document.getElementById("username").value;
            const pass = document.getElementById("password").value;
            if (user === "mahbe" && pass === "1234") {
                document.getElementById("login-overlay").style.display = "none";
                document.getElementById("main-site").style.display = "block";
            } else {
                document.getElementById("error-msg").style.display = "block";
            }
        }

        function logout() { location.reload(); }
    </script>
</body>
</html>
