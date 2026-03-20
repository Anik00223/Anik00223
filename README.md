<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Anik Das — GitHub README</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap');

  :root {
    --bg: #0a0a0f;
    --surface: #111118;
    --border: #1e1e2e;
    --accent1: #7c3aed;
    --accent2: #06b6d4;
    --accent3: #f59e0b;
    --text: #e2e8f0;
    --muted: #64748b;
    --green: #10b981;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    padding: 40px 20px;
  }

  .card {
    width: 100%;
    max-width: 860px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
    position: relative;
  }

  /* ── TOP BAR ── */
  .top-bar {
    height: 4px;
    background: linear-gradient(90deg, var(--accent1), var(--accent2), var(--accent3), var(--green));
    animation: shimmer 4s linear infinite;
    background-size: 300% 100%;
  }
  @keyframes shimmer {
    0%   { background-position: 0% 50%; }
    100% { background-position: 300% 50%; }
  }

  /* ── HEADER ── */
  .header {
    padding: 40px 44px 32px;
    border-bottom: 1px solid var(--border);
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 24px;
    align-items: start;
  }

  .greeting {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent2);
    margin-bottom: 10px;
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(28px, 4vw, 42px);
    font-weight: 800;
    line-height: 1.1;
    color: #fff;
    margin-bottom: 6px;
  }

  .name span {
    background: linear-gradient(135deg, var(--accent1), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .tagline {
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 0.04em;
    font-style: italic;
    margin-top: 4px;
  }

  .status-pill {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    background: rgba(16,185,129,0.08);
    border: 1px solid rgba(16,185,129,0.25);
    border-radius: 100px;
    padding: 5px 13px;
    font-size: 11px;
    color: var(--green);
    font-weight: 700;
    white-space: nowrap;
    margin-top: 6px;
  }
  .dot {
    width: 7px; height: 7px;
    background: var(--green);
    border-radius: 50%;
    animation: pulse 1.8s ease-in-out infinite;
  }
  @keyframes pulse {
    0%,100% { opacity: 1; transform: scale(1); }
    50%      { opacity: 0.4; transform: scale(0.7); }
  }

  /* ── SECTIONS ── */
  .body {
    padding: 36px 44px;
    display: flex;
    flex-direction: column;
    gap: 36px;
  }

  .section-label {
    font-family: 'Syne', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent1);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    gap: 10px;
  }

  .about-line {
    display: grid;
    grid-template-columns: 18px 1fr;
    gap: 12px;
    align-items: baseline;
    font-size: 13px;
    line-height: 1.7;
    color: #94a3b8;
  }
  .about-line .bullet {
    color: var(--accent2);
    font-size: 10px;
    padding-top: 3px;
  }

  .highlight {
    color: var(--text);
    font-weight: 700;
  }

  /* ── TECH FOCUS ── */
  .tech-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .tech-chip {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 12px;
    font-weight: 700;
    border: 1px solid;
    letter-spacing: 0.02em;
    transition: transform 0.2s;
  }
  .tech-chip:hover { transform: translateY(-2px); }

  .chip-purple {
    background: rgba(124,58,237,0.1);
    border-color: rgba(124,58,237,0.35);
    color: #a78bfa;
  }
  .chip-cyan {
    background: rgba(6,182,212,0.1);
    border-color: rgba(6,182,212,0.35);
    color: #67e8f9;
  }
  .chip-amber {
    background: rgba(245,158,11,0.1);
    border-color: rgba(245,158,11,0.35);
    color: #fcd34d;
  }

  /* ── MINDSET ── */
  .mindset-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 12px;
  }

  .mindset-card {
    background: rgba(255,255,255,0.02);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .mindset-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }
  .mindset-card:nth-child(1)::before { background: var(--accent1); }
  .mindset-card:nth-child(2)::before { background: var(--accent2); }
  .mindset-card:nth-child(3)::before { background: var(--accent3); }

  .mindset-over {
    font-size: 9px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 6px;
  }
  .mindset-word {
    font-family: 'Syne', sans-serif;
    font-size: 15px;
    font-weight: 800;
    color: #fff;
  }

  /* ── PHILOSOPHY QUOTE ── */
  .philosophy {
    background: rgba(124,58,237,0.05);
    border: 1px solid rgba(124,58,237,0.2);
    border-left: 3px solid var(--accent1);
    border-radius: 0 8px 8px 0;
    padding: 16px 20px;
    font-size: 12px;
    color: #94a3b8;
    font-style: italic;
    line-height: 1.8;
  }
  .philosophy strong {
    color: #c4b5fd;
    font-style: normal;
  }

  /* ── CONNECT ── */
  .connect-line {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.8;
    border-top: 1px solid var(--border);
    padding-top: 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
  }

  .connect-line .connect-text {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    color: var(--text);
  }
  .connect-line .connect-text span {
    color: var(--accent2);
  }

  .loop-text {
    font-size: 11px;
    font-family: 'Space Mono', monospace;
    color: var(--accent3);
    letter-spacing: 0.05em;
  }

  /* ── FOOTER ── */
  .footer {
    padding: 14px 44px;
    background: rgba(255,255,255,0.015);
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 8px;
  }
  .footer-left {
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.08em;
    font-family: 'Space Mono', monospace;
  }
  .footer-left code {
    color: var(--accent2);
  }

  .readme-badge {
    font-size: 10px;
    color: var(--muted);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 2px 8px;
    letter-spacing: 0.06em;
  }
</style>
</head>
<body>

<div class="card">
  <div class="top-bar"></div>

  <div class="header">
    <div>
      <div class="greeting">// README.md</div>
      <div class="name">Hey 👋, I'm <span>Anik Das</span></div>
      <div class="tagline">Building. Breaking. Learning. Repeating.</div>
      <div class="status-pill">
        <div class="dot"></div>
        Open to collaborate
      </div>
    </div>
    <div style="text-align:right; padding-top:6px;">
      <div style="font-size:10px; color:var(--muted); margin-bottom:6px; letter-spacing:0.1em;">LOCATION</div>
      <div style="font-size:13px; color:var(--text); font-family:'Syne',sans-serif; font-weight:700;">Silchar, Assam 🇮🇳</div>
      <div style="font-size:10px; color:var(--muted); margin-top:12px; margin-bottom:6px; letter-spacing:0.1em;">FOCUS</div>
      <div style="font-size:12px; color:var(--accent3);">AI/ML Engineering</div>
    </div>
  </div>

  <div class="body">

    <!-- ABOUT -->
    <div>
      <div class="section-label">🌱 About Me</div>
      <div class="about-grid">
        <div class="about-line">
          <span class="bullet">▸</span>
          <span>Started with simple web pages — got obsessed with <span class="highlight">how things actually work</span> behind the screen.</span>
        </div>
        <div class="about-line">
          <span class="bullet">▸</span>
          <span>Build with <span class="highlight">HTML, CSS, JavaScript</span> and sharpen logic with <span class="highlight">Java</span>. I don't just follow steps — I experiment, fail, debug, and understand deeply.</span>
        </div>
        <div class="about-line">
          <span class="bullet">▸</span>
          <span>Currently exploring <span class="highlight">Software Engineering</span>, <span class="highlight">Databases</span>, and <span class="highlight">AI/ML fundamentals</span> to grow beyond the basics.</span>
        </div>
        <div class="about-line">
          <span class="bullet">▸</span>
          <span>I focus on projects that are <span class="highlight">useful, practical, and real</span> — not just visually good.</span>
        </div>
        <div class="about-line">
          <span class="bullet">▸</span>
          <span>If you value <span class="highlight">consistency, curiosity, and real growth</span> — we'll connect well 🤝</span>
        </div>
      </div>
    </div>

    <!-- TECH FOCUS -->
    <div>
      <div class="section-label">⚡ Tech Focus</div>
      <div class="tech-row">
        <div class="tech-chip chip-purple">💻 Frontend Development</div>
        <div class="tech-chip chip-cyan">☕ Java &amp; Problem Solving</div>
        <div class="tech-chip chip-amber">🧠 AI/ML (Learning)</div>
        <div class="tech-chip chip-purple">🗄️ DBMS</div>
        <div class="tech-chip chip-cyan">🔧 Software Engineering</div>
      </div>
    </div>

    <!-- MINDSET -->
    <div>
      <div class="section-label">📈 Mindset</div>
      <div class="mindset-grid">
        <div class="mindset-card">
          <div class="mindset-over">Discipline</div>
          <div class="mindset-word">over Motivation</div>
        </div>
        <div class="mindset-card">
          <div class="mindset-over">Consistency</div>
          <div class="mindset-word">over Intensity</div>
        </div>
        <div class="mindset-card">
          <div class="mindset-over">Learning</div>
          <div class="mindset-word">over Showing</div>
        </div>
      </div>
    </div>

    <!-- PHILOSOPHY -->
    <div class="philosophy">
      I don't want to look good on paper. I want to <strong>actually know things</strong>.<br/>
      Every project I build is a question I'm asking myself: <strong>do I really understand this?</strong><br/>
      ✨ Still learning. Still building. Still improving.
    </div>

    <!-- CONNECT -->
    <div class="connect-line">
      <div class="connect-text">
        Let's build something <span>meaningful</span> together.
      </div>
      <div class="loop-text">while(alive) { learn(); build(); repeat(); }</div>
    </div>

  </div>

  <div class="footer">
    <div class="footer-left">
      <code>AnikDas</code> / README.md &nbsp;·&nbsp; BTech CSE · Fresher
    </div>
    <div class="readme-badge">README</div>
  </div>
</div>

</body>
</html>


## 🌐 Socials:
[![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://facebook.com/https://www.facebook.com/share/18R5FER69x/) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/https://www.instagram.com/autarch.noir?igsh=b2tuaGtzOGEwNzBy) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/https://www.linkedin.com/in/anik-das-893080395?utm_source=share_via&utm_content=profile&utm_medium=member_android) 

# 💻 Tech Stack:
![C](https://img.shields.io/badge/c-%2300599C.svg?style=plastic&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=plastic&logo=c%2B%2B&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=plastic&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=plastic&logo=html5&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=plastic&logo=openjdk&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=plastic&logo=javascript&logoColor=%23F7DF1E) ![Python](https://img.shields.io/badge/python-3670A0?style=plastic&logo=python&logoColor=ffdd54) ![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=plastic&logo=powershell&logoColor=white) ![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-%234D4D4D.svg?style=plastic&logo=windows-terminal&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=plastic&logo=amazon-aws&logoColor=white) ![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=plastic&logo=Cloudflare&logoColor=white) ![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=plastic&logo=firebase) ![Render](https://img.shields.io/badge/Render-%46E3B7.svg?style=plastic&logo=render&logoColor=white) ![Oracle](https://img.shields.io/badge/Oracle-F80000?style=plastic&logo=oracle&logoColor=white) ![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=plastic&logo=netlify&logoColor=#00C7B7) ![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=plastic&logo=vercel&logoColor=white) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=plastic&logo=google-cloud&logoColor=white) ![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=plastic&logo=bootstrap&logoColor=white) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=plastic&logo=django&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=plastic&logo=fastapi) ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=plastic&logo=flask&logoColor=white) ![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=plastic&logo=npm&logoColor=white) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=plastic&logo=node.js&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=plastic&logo=react&logoColor=%2361DAFB) ![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=plastic&logo=supabase&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=plastic&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=plastic&logo=mongodb&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=plastic&logo=sqlite&logoColor=white) ![Adobe Lightroom](https://img.shields.io/badge/Adobe%20Lightroom-31A8FF.svg?style=plastic&logo=Adobe%20Lightroom&logoColor=white) ![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=plastic&logo=figma&logoColor=white) ![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=plastic&logo=Canva&logoColor=white) ![Blender](https://img.shields.io/badge/blender-%23F5792A.svg?style=plastic&logo=blender&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=plastic&logo=Keras&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=plastic&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=plastic&logo=pandas&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=plastic&logo=PyTorch&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=plastic&logo=scikit-learn&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=plastic&logo=TensorFlow&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=plastic&logo=github&logoColor=white) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=plastic&logo=git&logoColor=white) ![Portfolio](https://img.shields.io/badge/Portfolio-%23000000.svg?style=plastic&logo=firefox&logoColor=#FF7139) ![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=plastic&logo=notion&logoColor=white) ![Meta](https://img.shields.io/badge/Meta-%230467DF.svg?style=plastic&logo=Meta&logoColor=white) ![nVIDIA](https://img.shields.io/badge/nVIDIA-%2376B900.svg?style=plastic&logo=nVIDIA&logoColor=white) ![Itch.io](https://img.shields.io/badge/Itch-%23FF0B34.svg?style=plastic&logo=Itch.io&logoColor=white) ![PlayStation Network](https://img.shields.io/badge/PSN-%230070D1.svg?style=plastic&logo=Playstation&logoColor=white) ![Riot Games](https://img.shields.io/badge/riotgames-D32936.svg?style=plastic&logo=riotgames&logoColor=white) ![Xbox](https://img.shields.io/badge/xbox-%23107C10.svg?style=plastic&logo=xbox&logoColor=white) ![Unity](https://img.shields.io/badge/unity-%23000000.svg?style=plastic&logo=unity&logoColor=white)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Anik00223&theme=great-gatsby&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://nirzak-streak-stats.vercel.app/?user=Anik00223&theme=great-gatsby&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Anik00223&theme=great-gatsby&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

## 🏆 GitHub Trophies
![](https://github-profile-trophy.vercel.app/?username=Anik00223&theme=aura&no-frame=false&no-bg=false&margin-w=4)

### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=merko)

---
[![](https://visitcount.itsvg.in/api?id=Anik00223&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
