<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ማሕቤ ቢዝነስ ማዕከል | Mahbe Business Center</title>
    
    <meta name="description" content="ማሕቤ ቢዝነስ ማዕከል - ግራፊክስ ዲዛይን፣ ቪዲዮ ኤዲቲንግ እና የሕትመት ስራዎች።">
    <meta name="keywords" content="Mahbe, ማሕቤ, Graphics Design, Ethiopia, Printing">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --blue: #004e92;
            --yellow: #f7e017;
            --dark: #002347;
            --white: #ffffff;
        }

        body { font-family: 'Segoe UI', sans-serif; margin: 0; background-color: #f4f7f6; color: #333; }

        /* Header */
        header {
            background: var(--white); padding: 10px 5%; display: flex; 
            justify-content: space-between; align-items: center;
            position: fixed; width: 90%; top: 0; z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1); border-bottom: 3px solid var(--blue);
        }
        .logo-area { display: flex; align-items: center; gap: 8px; }
        .logo-img { height: 40px; width: 40px; border-radius: 50%; border: 2px solid var(--blue); }
        .eth-flag { width: 25px; height: 15px; }
        .logo-text { font-weight: bold; color: var(--blue); font-size: 1rem; }

        nav { display: flex; gap: 8px; }
        nav a { color: #333; text-decoration: none; font-weight: bold; font-size: 0.75rem; cursor: pointer; padding: 5px; }
        nav a:hover, nav a.active { color: var(--blue); border-bottom: 2px solid var(--yellow); }

        /* Sections Control */
        .content-section { display: none; padding: 100px 5% 40px; animation: fadeIn 0.5s ease; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* Hero/Home */
        .hero { background: var(--blue); color: white; padding: 40px 20px; text-align: center; border-radius: 20px; }
        .testimonial { background: white; color: #333; padding: 20px; border-radius: 15px; border-left: 6px solid var(--yellow); margin-top: 20px; text-align: left; }

        /* Gallery Grid */
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 15px; }
        .gallery-item img { width: 100%; border-radius: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1); transition: 0.3s; }
        .gallery-item img:hover { transform: scale(1.03); }

        /* Service Cards */
        .service-card { background: var(--dark); color: white; padding: 25px; border-radius: 15px; margin-bottom: 15px; border-bottom: 4px solid var(--yellow); }
        .service-icon { font-size: 2rem; color: var(--yellow); margin-bottom: 10px; }

        /* Comment */
        .comment-box { background: white; padding: 25px; border-radius: 20px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); max-width: 500px; margin: 0 auto; }
        .comment-box input, .comment-box textarea { width: 100%; padding: 12px; margin: 10px 0; border: 1px solid #ddd; border-radius: 10px; box-sizing: border-box; }
        .comment-btn { background: var(--blue); color: white; border: none; padding: 15px; width: 100%; border-radius: 50px; font-weight: bold; cursor: pointer; }

        footer { text-align: center; padding: 20px; font-size: 0.8rem; border-top: 1px solid #ddd; background: white; }
    </style>
</head>
<body>

    <header>
        <div class="logo-area">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="logo-img">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Flag_of_Ethiopia.svg" class="eth-flag">
            <span class="logo-text">ማሕቤ ቢዝነስ</span>
        </div>
        <nav id="main-nav">
            <a onclick="showSection('home')" class="active">Home</a>
            <a onclick="showSection('services')">Services</a>
            <a onclick="showSection('gallery')">Gallery</a>
            <a onclick="showSection('about')">About</a>
            <a onclick="showSection('comment')">Comment</a>
        </nav>
    </header>

    <div id="home" class="content-section" style="display: block;">
        <div class="hero">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" style="width:80px; border-radius:50%; border:2px solid var(--yellow);">
            <h1>እንኳን ደህና መጡ!</h1>
            <p>ጥራት እና ታማኝነት መለያችን ነው</p>
        </div>
        <div class="testimonial">
            <p style="font-style: italic;">"በጣም የሚገርም እና ደስ የሚል ስራ ነው ከፍጥነታችሁ ጥራታችሁ እኔ ሲፈጥን እንደዚህ ጥራት ይኖረዋል ብየ አልጠበኩም"</p>
            <p style="text-align: right; font-weight: bold; color: var(--blue);">— ከአንዲት ደንበኛ የተሰጠ አስተያየት ⭐⭐⭐⭐⭐</p>
        </div>
    </div>

    <div id="services" class="content-section">
        <h2>አገልግሎቶቻችን</h2>
        <div class="service-card"><i class="fas fa-palette service-icon"></i><h3>Graphics Design</h3><p>Banner, Logo, Sticker Design</p></div>
        <div class="service-card"><i class="fas fa-video service-icon"></i><h3>Production</h3><p>Video Editing & Camera Works</p></div>
        <div class="service-card"><i class="fas fa-file-alt service-icon"></i><h3>Gov. Services</h3><p>Passport & License Renewals</p></div>
    </div>

    <div id="gallery" class="content-section">
        <h2>የስራዎቻችን ማሳያ (28+)</h2>
        <div class="gallery-grid">
            <div class="gallery-item"><img src="https://i.ibb.co/zhjkJXpm/20251219-224720.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/1fwpFk6H/20251216-002122.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/QF7PbLyj/20251215-155642.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/XN9qjfN/20251210-224030.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/pj0G79js/20251210-225324.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/PZBYcCN3/20251209-234129.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/PsqD4xFT/20251202-120100.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LLrvHzJ/20251205-104728.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/fYH5CVpV/20251128-093307.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/fzPz8G2s/20251127-100038.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/zTn3fYKp/20260102-164217.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/qMk0cqCf/20251230-112306.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/qLhqKJWR/20251230-073553.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/8nwp8rkQ/20251219-132621.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LzZCXn0y/20251205-122512.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/5XVVtK0q/20251122-144552.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LhnMBPNF/20251120-202649.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/YB2q959t/20251120-200348.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/HTs32qzY/20251119-140559.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/v7RQtHD/20251118-215305.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/WNFRQj2H/20251118-200618.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/d0KmLtSN/20251114-122726.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/FLLpDNv5/20251108-122343.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/d46N12Ms/20251109-184251.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/3yv4bm2Z/20251023-182429.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/vgz9sgX/20251005-123849.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/r2JxTnM2/20251003-164027.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/21dLh2P5/20251106-082659.jpg"></div>
        </div>
    </div>

    <div id="about" class="content-section">
        <h2>ስለ ማሕቤ</h2>
        <div style="background:white; padding:20px; border-radius:15px; line-height:1.6;">
            <p><strong>ማሕቤ</strong> ማለት ሁለት ታላላቅ ትርጉሞች ያሉት ጥልቅ ስም ነው፦</p>
            <ul>
                <li><strong>ማሕፀነ ቤተክርስቲያን ሚዲያ፦</strong> መንፈሳዊ አገልግሎቶችን የምናቀርብበት ክፍል ነው።</li>
                <li><strong>ማሕቤ ሕትመት ቤት፦</strong> ማንኛውንም የግራፊክስ ዲዛይን እና የሕትመት ስራዎች የምንሰራበት ነው።</li>
            </ul>
        </div>
    </div>

    <div id="comment" class="content-section">
        <h2 style="text-align: center;">አስተያየት ይስጡ</h2>
        <div class="comment-box">
            <input type="text" id="userName" placeholder="ሙሉ ስምዎ">
            <textarea id="userComment" rows="5" placeholder="አስተያየትዎን እዚህ ይጻፉ..."></textarea>
            <button class="comment-btn" onclick="sendToTelegram()">አስተያየቴን ላክ</button>
        </div>
    </div>

    <footer>
        <p>© 2026 ማሕቤ ቢዝነስ ማዕከል | 📞 0928525029</p>
    </footer>

    <script>
        function showSection(id) {
            // ሁሉንም ገጾች ደብቅ
            const sections = document.querySelectorAll('.content-section');
            sections.forEach(s => s.style.display = 'none');
            
            // የተመረጠውን ገጽ አሳይ
            document.getElementById(id).style.display = 'block';
            
            // የሜኑ ከለር ቀይር
            const navLinks = document.querySelectorAll('nav a');
            navLinks.forEach(link => link.classList.remove('active'));
            event.target.classList.add('active');
            
            window.scrollTo(0,0);
        }

        function sendToTelegram() {
            const name = document.getElementById('userName').value;
            const comment = document.getElementById('userComment').value;
            if (name === "" || comment === "") { alert("እባክዎ ስም እና አስተያየት ያስገቡ!"); return; }
            const msg = `ሰላም ማሕቤ! አስተያየት አለኝ%0A%0Aስም፦ ${name}%0Aአስተያየት፦ ${comment}`;
            window.open(`https://t.me/temu_amen?text=${msg}`, '_blank');
        }
    </script>
</body>
</html>
