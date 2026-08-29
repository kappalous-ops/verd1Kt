<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>VERDICT · Admin</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            background: #0b0e1a;
            color: #d6eaff;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            display: flex;
            justify-content: center;
            padding: 40px 20px;
        }
        .wrap {
            max-width: 880px;
            width: 100%;
            text-align: center;
        }
        pre {
            font-family: 'Courier New', monospace;
            font-size: 10px;
            line-height: 1.25;
            color: #3b8cff;
            white-space: pre;
            overflow-x: auto;
            margin-bottom: 16px;
        }
        h1 {
            font-size: 46px;
            font-weight: 900;
            background: linear-gradient(90deg, #1a6aff, #8ac4ff, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: 2px;
        }
        .sub {
            font-size: 20px;
            color: #6da8ff;
            margin-bottom: 30px;
        }
        .box {
            background: rgba(20, 40, 80, 0.25);
            border: 1px solid #2a4b8a;
            border-radius: 14px;
            padding: 20px 18px;
            margin: 24px 0;
        }
        .box h2 {
            font-size: 24px;
            color: #8ac4ff;
            margin-bottom: 12px;
        }
        .box p,
        .box li {
            color: #bdd6ff;
            font-size: 16px;
            line-height: 1.6;
        }
        .badge {
            display: inline-block;
            background: #1a2d55;
            border: 1px solid #3a6bc0;
            padding: 4px 16px;
            border-radius: 30px;
            font-size: 13px;
            margin: 4px;
            color: #b0d0ff;
        }
        .btn {
            display: inline-block;
            padding: 12px 32px;
            border-radius: 40px;
            font-weight: 600;
            text-decoration: none;
            color: #fff;
            margin: 6px;
            transition: 0.2s;
            border: 1px solid transparent;
        }
        .btn-tg {
            background: #1f8cdb;
        }
        .btn-tg:hover {
            background: #006bb3;
        }
        .btn-dc {
            background: #5a6bf5;
        }
        .btn-dc:hover {
            background: #3b4edb;
        }
        .btn-tt {
            background: #111;
            border-color: #888;
        }
        .btn-tt:hover {
            background: #222;
        }
        .footer {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #1e3460;
            font-size: 14px;
            color: #5a7bb0;
        }
        .badge-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 6px 12px;
            margin: 12px 0;
        }
        .stat {
            display: inline-block;
            background: #0e1a30;
            padding: 4px 18px;
            border-radius: 30px;
            border: 1px solid #2a4f8a;
            font-size: 13px;
            color: #8ab9ff;
        }
        .stat.green {
            border-color: #2b8a5a;
            color: #80dbaa;
        }
        .stat.orange {
            border-color: #b8772a;
            color: #f0b86a;
        }
        img.snake {
            max-width: 100%;
            border-radius: 12px;
            margin: 12px 0;
            opacity: 0.85;
        }
        blockquote {
            border-left: 4px solid #3a7bd5;
            padding: 8px 20px;
            background: #0d1a30;
            border-radius: 8px;
            font-style: italic;
            color: #b0ceff;
            margin: 16px 0;
        }
        table {
            margin: 0 auto;
            border-collapse: collapse;
            text-align: left;
        }
        td {
            padding: 8px 14px;
            border-bottom: 1px solid #1f3460;
        }
        td:first-child {
            font-size: 18px;
        }
    </style>
</head>
<body>
<div class="wrap">

    <!-- ASCII -->
    <pre>
██╗   ██╗███████╗██████╗ ██████╗ ██╗ ██████╗████████╗
██║   ██║██╔════╝██╔══██╗██╔══██╗██║██╔════╝╚══██╔══╝
██║   ██║█████╗  ██████╔╝██║  ██║██║██║        ██║
╚██╗ ██╔╝██╔══╝  ██╔══██╗██║  ██║██║██║        ██║
 ╚████╔╝ ███████╗██║  ██║██████╔╝██║╚██████╗   ██║
  ╚═══╝  ╚══════╝╚═╝  ╚═╝╚═════╝ ╚═╝ ╚═════╝   ╚═╝
    </pre>

    <h1>VERDICT</h1>
    <div class="sub">⚡ System Admin · Network Engineer ⚡</div>

    <!-- WHAT IS DDoS -->
    <div class="box">
        <h2>▸ WHAT IS DDoS?</h2>
        <blockquote><strong>D</strong>istributed <strong>D</strong>enial <strong>o</strong>f <strong>S</strong>ervice</blockquote>
        <p>Massive flood of requests that overloads a server, causing it to become unavailable.</p>
    </div>

    <!-- FOR WHAT -->
    <div class="box">
        <h2>▸ FOR WHAT?</h2>
        <table>
            <tr><td>🧪</td><td><strong>Stress Testing</strong> — check your own server limits</td></tr>
            <tr><td>🔍</td><td><strong>Security Audit</strong> — find weak spots</td></tr>
            <tr><td>📊</td><td><strong>Performance Analysis</strong> — measure bandwidth capacity</td></tr>
            <tr><td>🛡️</td><td><strong>Resilience Testing</strong> — prepare for real attacks</td></tr>
        </table>
    </div>

    <!-- ATTACK TYPES -->
    <div class="box">
        <h2>▸ ATTACK TYPES</h2>
        <div class="badge-row">
            <span class="badge">VOLUMETRIC</span>
            <span class="badge">PROTOCOL</span>
            <span class="badge">APPLICATION</span>
            <span class="badge">AMPLIFICATION</span>
            <span class="badge">SYN FLOOD</span>
            <span class="badge">UDP FLOOD</span>
            <span class="badge">HTTP FLOOD</span>
            <span class="badge">ICMP FLOOD</span>
        </div>
        <p style="margin-top:12px; font-size:14px; color:#8899bb;">
            ⚠ Only test infrastructure you own or have permission to test.
        </p>
    </div>

    <!-- WHO AM I -->
    <div class="box">
        <h2>▸ WHO AM I</h2>
        <p>🔹 System Administrator — servers &amp; infrastructure<br>
        🔹 Network Engineer — networks &amp; routing<br>
        🔹 DevOps — automation &amp; pipelines<br>
        🔹 Infrastructure Architect — scalable systems</p>
    </div>

    <!-- SKILLS -->
    <div class="box">
        <h2>▸ SKILLS</h2>
        <div class="badge-row">
            <span class="badge">Linux</span><span class="badge">Windows</span>
            <span class="badge">Bash</span><span class="badge">Python</span>
            <span class="badge">PHP</span><span class="badge">HTML/CSS</span>
            <span class="badge">Git</span><span class="badge">Docker</span>
            <span class="badge">Kubernetes</span><span class="badge">AWS</span>
            <span class="badge">Azure</span><span class="badge">MySQL</span>
            <span class="badge">PostgreSQL</span><span class="badge">Redis</span>
            <span class="badge">MongoDB</span><span class="badge">Nginx</span>
            <span class="badge">Cloudflare</span><span class="badge">Terraform</span>
            <span class="badge">Ansible</span><span class="badge">Grafana</span>
            <span class="badge">Prometheus</span>
        </div>
    </div>

    <!-- CONTACT -->
    <div class="box" style="border-color:#3a5fa0;">
        <h2>▸ CONTACT</h2>
        <div style="display:flex; flex-wrap:wrap; justify-content:center; gap:10px;">
            <a href="https://t.me/celonq" class="btn btn-tg">📱 Telegram</a>
            <a href="https://discord.com/users/verd1ktt" class="btn btn-dc">🎮 Discord</a>
            <a href="https://tiktok.com/@verdiktweb" class="btn btn-tt">🎵 TikTok</a>
        </div>
    </div>

    <!-- COUNTER + SNAKE -->
    <div style="margin:20px 0;">
        <img src="https://count.getloli.com/@verdikta7?name=verdikta7&theme=booru-lewd" alt="visitors" />
    </div>
    <img class="snake" src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" alt="snake" />

    <!-- FOOTER -->
    <div class="footer">
        <span class="stat green">⚡ STATUS: ACTIVE</span>
        <span class="stat">🛠 ROLE: SYSTEM ADMIN</span>
        <span class="stat orange">🌐 ROLE: NETWORK ENGINEER</span>
        <br><br>
        © 2026 VERDICT
    </div>

</div>
</body>
</html>
