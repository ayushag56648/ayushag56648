<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cybersecurity Banner</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: #0a0a0a;
            font-family: 'Courier New', monospace;
        }
        
        .banner {
            width: 1000px;
            height: 400px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            position: relative;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 20px 60px rgba(102, 126, 234, 0.4);
        }
        
        .cyber-grid {
            position: absolute;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(255,255,255,0.05) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255,255,255,0.05) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: gridMove 20s linear infinite;
        }
        
        @keyframes gridMove {
            0% { transform: translateY(0); }
            100% { transform: translateY(50px); }
        }
        
        .circuit {
            position: absolute;
            width: 100%;
            height: 100%;
            opacity: 0.1;
        }
        
        .circuit-line {
            position: absolute;
            background: #fff;
            animation: pulse 3s ease-in-out infinite;
        }
        
        .circuit-line:nth-child(1) {
            width: 200px;
            height: 2px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }
        
        .circuit-line:nth-child(2) {
            width: 2px;
            height: 150px;
            top: 10%;
            right: 20%;
            animation-delay: 0.5s;
        }
        
        .circuit-line:nth-child(3) {
            width: 180px;
            height: 2px;
            bottom: 25%;
            right: 15%;
            animation-delay: 1s;
        }
        
        .circuit-line:nth-child(4) {
            width: 2px;
            height: 120px;
            bottom: 15%;
            left: 25%;
            animation-delay: 1.5s;
        }
        
        @keyframes pulse {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.8; }
        }
        
        .content {
            position: relative;
            z-index: 10;
            text-align: center;
            padding-top: 120px;
            color: white;
        }
        
        .greeting {
            font-size: 3em;
            font-weight: bold;
            margin-bottom: 20px;
            text-shadow: 0 0 20px rgba(255,255,255,0.5);
            animation: fadeInDown 1s ease-out;
        }
        
        .name {
            display: inline-block;
            animation: glow 2s ease-in-out infinite;
        }
        
        @keyframes glow {
            0%, 100% { text-shadow: 0 0 20px rgba(255,255,255,0.5); }
            50% { text-shadow: 0 0 30px rgba(255,255,255,0.8), 0 0 40px rgba(102,126,234,0.6); }
        }
        
        .subtitle {
            font-size: 1.5em;
            opacity: 0.95;
            letter-spacing: 3px;
            text-transform: uppercase;
            animation: fadeInUp 1s ease-out 0.3s both;
        }
        
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .binary {
            position: absolute;
            font-size: 12px;
            color: rgba(255,255,255,0.2);
            font-family: 'Courier New', monospace;
            animation: fall linear infinite;
            white-space: nowrap;
        }
        
        @keyframes fall {
            0% {
                transform: translateY(-100%);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(500px);
                opacity: 0;
            }
        }
        
        .lock-icon {
            position: absolute;
            top: 50%;
            left: 15%;
            transform: translateY(-50%);
            font-size: 120px;
            opacity: 0.15;
            animation: float 4s ease-in-out infinite;
        }
        
        .shield-icon {
            position: absolute;
            top: 50%;
            right: 15%;
            transform: translateY(-50%);
            font-size: 120px;
            opacity: 0.15;
            animation: float 4s ease-in-out infinite 2s;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(-50%) translateX(0);
            }
            50% {
                transform: translateY(-50%) translateX(10px);
            }
        }
        
        .terminal-cursor {
            display: inline-block;
            width: 12px;
            height: 28px;
            background: white;
            animation: blink 1s step-end infinite;
            margin-left: 5px;
        }
        
        @keyframes blink {
            50% { opacity: 0; }
        }
        
        .download-btn {
            margin-top: 30px;
            padding: 12px 30px;
            background: rgba(255,255,255,0.2);
            border: 2px solid white;
            color: white;
            font-size: 16px;
            font-family: 'Courier New', monospace;
            cursor: pointer;
            border-radius: 5px;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }
        
        .download-btn:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(255,255,255,0.3);
        }
    </style>
</head>
<body>
    <div class="banner" id="banner">
        <div class="cyber-grid"></div>
        <div class="circuit">
            <div class="circuit-line"></div>
            <div class="circuit-line"></div>
            <div class="circuit-line"></div>
            <div class="circuit-line"></div>
        </div>
        
        <div class="lock-icon">🔒</div>
        <div class="shield-icon">🛡️</div>
        
        <div class="content">
            <div class="greeting">
                Hi, I'm <span class="name">Ayush</span> 🔐
            </div>
            <div class="subtitle">
                Cybersecurity Enthusiast
                <span class="terminal-cursor"></span>
            </div>
            <button class="download-btn" onclick="downloadBanner()">Download Banner</button>
        </div>
    </div>

    <script>
        // Generate falling binary code
        function createBinary() {
            const banner = document.querySelector('.banner');
            const binary = document.createElement('div');
            binary.className = 'binary';
            binary.textContent = Math.random() > 0.5 ? '01010101' : '10101010';
            binary.style.left = Math.random() * 100 + '%';
            binary.style.animationDuration = (Math.random() * 3 + 5) + 's';
            banner.appendChild(binary);
            
            setTimeout(() => binary.remove(), 8000);
        }
        
        setInterval(createBinary, 800);
        
        // Download banner as image
        async function downloadBanner() {
            const banner = document.getElementById('banner');
            
            // Create canvas
            const canvas = document.createElement('canvas');
            const ctx = canvas.getContext('2d');
            canvas.width = 1000;
            canvas.height = 400;
            
            // Create temporary image from banner HTML
            const data = `
                <svg xmlns="http://www.w3.org/2000/svg" width="1000" height="400">
                    <defs>
                        <linearGradient id="grad" x1="0%" y1="0%" x2="100%" y2="100%">
                            <stop offset="0%" style="stop-color:#667eea;stop-opacity:1" />
                            <stop offset="50%" style="stop-color:#764ba2;stop-opacity:1" />
                            <stop offset="100%" style="stop-color:#f093fb;stop-opacity:1" />
                        </linearGradient>
                    </defs>
                    <rect width="1000" height="400" fill="url(#grad)"/>
                    <text x="500" y="180" font-family="Courier New" font-size="48" font-weight="bold" fill="white" text-anchor="middle">Hi, I'm Ayush 🔐</text>
                    <text x="500" y="230" font-family="Courier New" font-size="24" fill="white" text-anchor="middle" letter-spacing="3">CYBERSECURITY ENTHUSIAST</text>
                </svg>
            `;
            
            const blob = new Blob([data], { type: 'image/svg+xml' });
            const url = URL.createObjectURL(blob);
            const img = new Image();
            
            img.onload = function() {
                ctx.drawImage(img, 0, 0);
                canvas.toBlob(function(blob) {
                    const link = document.createElement('a');
                    link.download = 'github-banner-ayush.png';
                    link.href = URL.createObjectURL(blob);
                    link.click();
                });
                URL.revokeObjectURL(url);
            };
            
            img.src = url;
        }
    </script>
</body>
</html>
# Hi there! 👋 I'm Ayush

## 💻 Tech Stack:

![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white)
![Render](https://img.shields.io/badge/Render-%46E3B7.svg?style=for-the-badge&logo=render&logoColor=white)
![Heroku](https://img.shields.io/badge/heroku-%23430098.svg?style=for-the-badge&logo=heroku&logoColor=white)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Qt](https://img.shields.io/badge/Qt-%23217346.svg?style=for-the-badge&logo=Qt&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Adobe After Effects](https://img.shields.io/badge/Adobe%20After%20Effects-9999FF.svg?style=for-the-badge&logo=Adobe%20After%20Effects&logoColor=white)
![Adobe Photoshop](https://img.shields.io/badge/adobe%20photoshop-%2331A8FF.svg?style=for-the-badge&logo=adobe%20photoshop&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-%23008FBA.svg?style=for-the-badge&logo=cmake&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Xfce](https://img.shields.io/badge/Xfce-%232284F2.svg?style=for-the-badge&logo=xfce&logoColor=white)

---

## 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=ayushag56648&theme=dark&hide_border=false&include_all_commits=true&count_private=true)
![](https://github-readme-streak-stats.herokuapp.com/?user=ayushag56648&theme=dark&hide_border=false)

---

### 🌐 Connect with me:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/your-profile)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/your-profile)

---
⭐️ From [ayushag56648](https://github.com/ayushag56648)
