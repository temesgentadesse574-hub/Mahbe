<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ማሕቤ ቢዝነስ ሴንተር | Mahbe Business Center</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-blue: #004e92;
            --primary-yellow: #f7e017;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            margin: 0; padding: 0;
            background-color: #ffffff; /* ነጭ ዳራ */
            color: #333; scroll-behavior: smooth;
        }

        /* Header */
        header {
            background: linear-gradient(90deg, var(--primary-blue), var(--primary-yellow));
            padding: 10px 5%;
            display: flex; justify-content: space-between; align-items: center;
            position: fixed; width: 90%; top: 0; z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .logo-container { display: flex; align-items: center; gap: 10px; }
        .logo-img { height: 40px; width: 40px; border-radius: 50%; border: 2px solid white; object-fit: cover; }
        .logo-text { font-size: 18px; font-weight: bold; color: black; }

        /* Navigation Menu */
        nav { display: flex; gap: 12px; }
        nav a { color: black; text-decoration: none; font-weight: bold; font-size: 0.8rem; transition: 0.3s; }
        nav a:hover { color: white; }

        /* Login Overlay */
        #login-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(135deg, var(--primary-blue), #002a4d);
            display: flex; justify-content: center; align-items: center; z-index: 3000;
            color: white;
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
