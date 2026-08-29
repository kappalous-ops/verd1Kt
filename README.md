<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VERDICT | System Admin</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0a0a1a;
            color: #fff;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            max-width: 900px;
            padding: 40px 20px;
            text-align: center;
        }

        /* ===== GRADIENT ANIMATION ===== */
        .gradient-text {
            background: linear-gradient(270deg, #0033cc, #0088ff, #66ccff, #ffffff, #66ccff, #0088ff, #0033cc);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientMove 8s ease infinite;
        }

        @keyframes gradientMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* ===== ASCII ART ===== */
        .ascii-art {
            font-family: 'Courier New', monospace;
            font-size: 10px;
            line-height: 1.2;
            white-space: pre;
            color: #0088ff;
            text-shadow: 0 0 10px rgba(0, 136, 255, 0.3);
            margin-bottom: 20px;
            overflow-x: auto;
        }

        .ascii-art:hover {
            color: #66ccff;
            text-shadow: 0 0 20px rgba(102, 204, 255, 0.5);
            transition: all 0.5s ease;
        }

        /* ===== HEADER ===== */
        h1 {
            font-size: 48px;
            font-weight: 900;
            margin-bottom: 10px;
            letter-spacing: 2px;
        }

        .subtitle {
            font-size: 20px;
            color: #66ccff;
            margin-bottom: 30px;
            opacity: 0.8;
        }

        /* ===== BLOCKQUOTE ===== */
        blockquote {
            border-left: 4px solid #0088ff;
            padding: 15px 25px;
            margin: 20px auto;
            max-width: 700px;
            background: rgba(0, 136, 255, 0.05);
            border-radius: 8px;
            font-size: 18px;
            color: #aaddff;
        }

        blockquote strong {
            color: #66ccff;
        }

        /* ===== TABLE ===== */
        .info-table {
            margin: 20px auto;
            border-collapse: collapse;
            max-width: 700px;
            width: 100%;
        }

        .info-table td {
            padding: 12px 15px;
            border: 1px solid rgba(0, 136, 255, 0.2);
            text-align: left;
            color: #cceeff;
        }

        .info-table td:first-child {
            text-align: center;
            font-size: 20px;
            width: 50px;
        }

        .info-table tr:hover td {
            background: rgba(0, 136, 255, 0.05);
            border-color: #0088ff;
        }

        /* ===== SKILLS ===== */
        .skills-section {
            margin: 30px 0;
        }

        .skills-section h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: #66ccff;
        }

        .skills-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 10px 0;
        }

        .skill-badge {
            background: rgba(0, 136, 255, 0.1);
            border: 1px solid rgba(0, 136, 255, 0.3);
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 13px;
            color: #aaddff;
            transition: all 0.3s ease;
            cursor: default;
        }

        .skill-badge:hover {
            background: rgba(0, 136, 255, 0.2);
            border-color: #66ccff;
            color: #fff;
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(0, 136, 255, 0.2);
        }

        /* ===== IMAGE BADGES ===== */
        .badge-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 15px 0;
        }

        .badge-row a {
            display: inline-block;
            transition: transform 0.3s ease;
        }

        .badge-row a:hover {
            transform: scale(1.05);
        }

        /* ===== CONTACT ===== */
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }

        .contact-btn {
            padding: 12px 30px;
            border-radius: 30px;
            font-size: 16px;
            font-weight: 600;
            text-decoration: none;
            color: #fff;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .contact-btn.telegram {
            background: #0088cc;
            border-color: #0088cc;
        }

        .contact-btn.telegram:hover {
            background: transparent;
            color: #0088cc;
            box-shadow: 0 0 30px rgba(0, 136, 204, 0.3);
        }

        .contact-btn.discord {
            background: #5865F2;
            border-color: #5865F2;
        }

        .contact-btn.discord:hover {
            background: transparent;
            color: #5865F2;
            box-shadow: 0 0 30px rgba(88, 101, 242, 0.3);
        }

        .contact-btn.tiktok {
            background: #000;
            border-color: #fff;
        }

        .contact-btn.tiktok:hover {
            background: #fff;
            color: #000;
            box-shadow: 0 0 30px rgba(255, 255, 255, 0.2);
        }

        /* ===== FOOTER ===== */
        .footer-badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(0, 136, 255, 0.1);
        }

        .footer-badge {
            padding: 6px 18px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 500;
            color: #fff;
        }

        .footer-badge.active {
            background: #00cc66;
        }

        .footer-badge.admin {
            background: #0088ff;
        }

        .footer-badge.engineer {
            background: #ff8800;
        }

        /* ===== SNAKE IMAGE ===== */
        .snake-img {
            max-width: 100%;
            margin: 20px 0;
            border-radius: 10px;
            opacity: 0.8;
            transition: opacity 0.5s ease;
        }

        .snake-img:hover {
            opacity: 1;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 600px) {
            h1 { font-size: 32px; }
            .ascii-art { font-size: 6px; }
            .contact-btn { padding: 10px 20px; font-size: 14px; }
            .info-table td { padding: 8px 10px; font-size: 14px; }
        }
    </style>
</head>
<body>
    <div class="container">

        <!-- ===== ASCII ART ===== -->
        <div class="ascii-art">
██╗   ██╗███████╗██████╗ ██████╗ ██╗ ██████╗████████╗
██║   ██║██╔════╝██╔══██╗██╔══██╗██║██╔════╝╚══██╔══╝
██║   ██║█████╗  ██████╔╝██║  ██║██║██║        ██║   
╚██╗ ██╔╝██╔══╝  ██╔══██╗██║  ██║██║██║        ██║   
 ╚████╔╝ ███████╗██║  ██║██████╔╝██║╚██████╗   ██║   
  ╚═══╝  ╚══════╝╚═╝  ╚═╝╚═════╝ ╚═╝ ╚═════╝   ╚═╝
        </div>

        <!-- ===== TITLE ===== -->
        <h1 class="gradient-text">VERDICT</h1>
        <div class="subtitle">⚡ System Administrator & Network Engineer ⚡</div>

        <br>

        <!-- ===== WHAT IS DDoS ===== -->
        <h2 class="gradient-text" style="font-size:28px;">▸ WHAT IS DDoS?</h2>
        <blockquote>
            <strong>D</strong>istributed <strong>D</strong>enial <strong>o</strong>f <strong>S</strong>ervice
        </blockquote>

        <p style="max-width:700px; margin:0 auto; color:#aaddff; font-size:16px; line-height:1.6;">
            <strong>DDoS</strong> is a distributed attack on network infrastructure where
            a massive number of requests are sent to a server simultaneously, exceeding
            its bandwidth capacity and causing a denial of service.
        </p>

        <br>

        <!-- ===== FOR WHAT ===== -->
        <h3 class="gradient-text" style="font-size:22px;">▸ FOR WHAT?</h3>

        <table class="info-table">
            <tr>
                <td>🧪</td>
                <td><strong>Stress Testing</strong> — testing your own servers' resilience to high loads</td>
            </tr>
            <tr>
                <td>🔍</td>
                <td><strong>Security Audit</strong> — identifying weak points in infrastructure</td>
            </tr>
            <tr>
                <td>📊</td>
                <td><strong>Performance Analysis</strong> — evaluating real bandwidth capacity</td>
            </tr>
            <tr>
                <td>🛡️</td>
                <td><strong>Resilience Testing</strong> — preparing for real-world attacks</td>
            </tr>
        </table>

        <br>

        <!-- ===== ATTACK TYPES ===== -->
        <h3 class="gradient-text" style="font-size:22px;">▸ ATTACK TYPES</h3>

        <div class="skills-row">
            <span class="skill-badge">VOLUMETRIC</span>
            <span class="skill-badge">PROTOCOL</span>
            <span class="skill-badge">APPLICATION LAYER</span>
            <span class="skill-badge">AMPLIFICATION</span>
            <span class="skill-badge">SYN FLOOD</span>
            <span class="skill-badge">UDP FLOOD</span>
            <span class="skill-badge">HTTP FLOOD</span>
            <span class="skill-badge">ICMP FLOOD</span>
        </div>

        <br>

        <p style="color:#8899bb; font-size:14px;">
            <strong style="color:#ff4444;">⚠ IMPORTANT:</strong> All testing is performed <strong>ONLY</strong> on authorized infrastructure.<br>
            <em style="color:#66ccff;">DDoS is a weapon. Use it wisely and legally.</em>
        </p>

        <br>

        <!-- ===== WHO AM I ===== -->
        <h3 class="gradient-text" style="font-size:22px;">▸ WHO AM I</h3>
        <div style="color:#aaddff; font-size:16px; line-height:1.8;">
            🔹 <strong>System Administrator</strong> — managing servers &amp; infrastructure<br>
            🔹 <strong>Network Engineer</strong> — designing &amp; maintaining networks<br>
            🔹 <strong>DevOps</strong> — automation &amp; CI/CD pipelines<br>
            🔹 <strong>Infrastructure Architect</strong> — building scalable systems
        </div>

        <br>

        <!-- ===== SKILLS ===== -->
        <div class="skills-section">
            <h3 class="gradient-text">▸ LANGUAGES &amp; CORE</h3>
            <div class="skills-row">
                <span class="skill-badge">Linux</span>
                <span class="skill-badge">Windows</span>
                <span class="skill-badge">Bash</span>
                <span class="skill-badge">Python</span>
                <span class="skill-badge">PHP</span>
                <span class="skill-badge">HTML/CSS</span>
                <span class="skill-badge">Git/GitHub</span>
            </div>
        </div>

        <div class="skills-section">
            <h3 class="gradient-text">▸ TOOLS</h3>
            <div class="skills-row">
                <span class="skill-badge">VS Code</span>
                <span class="skill-badge">Visual Studio</span>
                <span class="skill-badge">Figma</span>
            </div>
        </div>

        <div class="skills-section">
            <h3 class="gradient-text">▸ DEVOPS &amp; DATABASES</h3>
            <div class="skills-row">
                <span class="skill-badge">Nginx</span>
                <span class="skill-badge">Docker</span>
                <span class="skill-badge">Kubernetes</span>
                <span class="skill-badge">AWS</span>
                <span class="skill-badge">Azure</span>
                <span class="skill-badge">MySQL</span>
                <span class="skill-badge">PostgreSQL</span>
                <span class="skill-badge">Redis</span>
                <span class="skill-badge">MongoDB</span>
            </div>
        </div>

        <div class="skills-section">
            <h3 class="gradient-text">▸ NETWORKING</h3>
            <div class="skills-row">
                <span class="skill-badge">Cloudflare</span>
                <span class="skill-badge">Terraform</span>
                <span class="skill-badge">Ansible</span>
                <span class="skill-badge">Grafana</span>
                <span class="skill-badge">Prometheus</span>
            </div>
        </div>

        <br>

        <!-- ===== DDoS / LOAD TESTING ===== -->
        <div class="skills-section">
            <h3 class="gradient-text">▸ DDoS / LOAD TESTING</h3>
            <p style="color:#aaddff; font-size:15px; max-width:700px; margin:0 auto; line-height:1.8;">
                <strong>AUTHORIZED NETWORK STRESS TESTING</strong><br>
                IP-BASED LOAD TESTING • TRAFFIC ANALYSIS • NETWORK TESTING<br>
                SERVER STRESS TESTING • PERFORMANCE TESTING • DDoS RESILIENCE
            </p>
            <p style="color:#66ccff; font-size:14px; margin-top:5px;">
                <em>Test your own infrastructure before real users do.</em>
            </p>
        </div>

        <br>

        <!-- ===== QUOTE ===== -->
        <blockquote>
            <em>"A system is only as strong as its weakest link."</em>
        </blockquote>

        <br>

        <!-- ===== VISITOR COUNT ===== -->
        <div style="margin:20px 0;">
            <img src="https://count.getloli.com/@verdikta7?name=verdikta7&theme=booru-lewd" alt="visitors">
        </div>

        <br>

        <!-- ===== SNAKE ===== -->
        <img class="snake-img" src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" alt="snake">

        <br>

        <!-- ===== CONTACT ===== -->
        <h3 class="gradient-text" style="font-size:22px;">▸ CONTACT</h3>

        <div class="contact-links">
            <a href="https://t.me/celonq" class="contact-btn telegram">📱 Telegram</a>
            <a href="https://discord.com/users/verd1ktt" class="contact-btn discord">🎮 Discord</a>
            <a href="https://tiktok.com/@verdiktweb" class="contact-btn tiktok">🎵 TikTok</a>
        </div>

        <br>

        <!-- ===== FOOTER ===== -->
        <div class="footer-badges">
            <span class="footer-badge active">⚡ STATUS: ACTIVE</span>
            <span class="footer-badge admin">🛠 ROLE: SYSTEM ADMIN</span>
            <span class="footer-badge engineer">🌐 ROLE: NETWORK ENGINEER</span>
        </div>

        <p style="color:#445566; font-size:12px; margin-top:20px;">
            © 2026 VERDICT • Built with ❤️ and ☕
        </p>

    </div>
</body>
</html>
