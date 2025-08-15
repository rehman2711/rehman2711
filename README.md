<div align="center">
  <style>
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
    }
    
    @keyframes glow {
      0%, 100% { text-shadow: 0 0 5px #06b6d4; }
      50% { text-shadow: 0 0 20px #06b6d4, 0 0 30px #06b6d4; }
    }
    
    @keyframes typing {
      0% { width: 0; }
      100% { width: 100%; }
    }
    
    @keyframes blink {
      0%, 50% { border-right-color: transparent; }
      51%, 100% { border-right-color: #06b6d4; }
    }
    
    .floating-banner {
      animation: float 3s ease-in-out infinite;
      border-radius: 20px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    
    .floating-banner:hover {
      transform: scale(1.05);
      box-shadow: 0 20px 40px rgba(6, 182, 212, 0.4);
    }
    
    .glow-title {
      animation: glow 2s ease-in-out infinite alternate;
      background: linear-gradient(45deg, #06b6d4, #0ea5e9, #3b82f6);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      font-size: 2.5rem;
      font-weight: bold;
      margin: 20px 0;
    }
    
    .typing-effect {
      font-family: 'Courier New', monospace;
      font-size: 1.2rem;
      color: #0ea5e9;
      border-right: 2px solid #06b6d4;
      white-space: nowrap;
      overflow: hidden;
      animation: typing 4s steps(40, end) infinite, blink 1s step-end infinite;
      margin: 20px 0;
    }
    
    .interactive-badge {
      display: inline-block;
      margin: 5px;
      transition: all 0.3s ease;
      border-radius: 25px;
      position: relative;
      overflow: hidden;
    }
    
    .interactive-badge:hover {
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }
    
    .interactive-badge::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
      transition: left 0.5s;
    }
    
    .interactive-badge:hover::before {
      left: 100%;
    }
    
    .stats-card {
      background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
      border: 1px solid #0ea5e9;
      border-radius: 15px;
      padding: 20px;
      margin: 10px;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    
    .stats-card::after {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: conic-gradient(transparent, rgba(6, 182, 212, 0.1), transparent 30%);
      animation: rotate 4s linear infinite;
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    
    .stats-card:hover::after {
      opacity: 1;
    }
    
    .stats-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(6, 182, 212, 0.2);
    }
    
    @keyframes rotate {
      100% { transform: rotate(1turn); }
    }
    
    .project-card {
      background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
      border: 1px solid #64748b;
      border-radius: 12px;
      padding: 15px;
      margin: 10px;
      transition: all 0.3s ease;
      cursor: pointer;
    }
    
    .project-card:hover {
      border-color: #0ea5e9;
      box-shadow: 0 10px 30px rgba(14, 165, 233, 0.3);
      transform: translateY(-5px);
    }
    
    .code-block {
      background: #0f172a;
      border: 1px solid #1e293b;
      border-radius: 10px;
      padding: 20px;
      font-family: 'Courier New', monospace;
      position: relative;
      overflow: hidden;
      margin: 20px 0;
    }
    
    .code-block::before {
      content: '● ● ●';
      position: absolute;
      top: 10px;
      left: 15px;
      color: #ef4444;
      font-size: 12px;
    }
    
    .code-line {
      margin: 8px 0;
      transition: all 0.3s ease;
    }
    
    .code-line:hover {
      background: rgba(6, 182, 212, 0.1);
      padding: 2px 5px;
      border-radius: 4px;
    }
    
    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin: 20px 0;
    }
    
    .tech-item {
      transition: all 0.3s ease;
      filter: grayscale(0%);
    }
    
    .tech-item:hover {
      transform: scale(1.1) rotate(5deg);
      filter: drop-shadow(0 0 10px rgba(6, 182, 212, 0.5));
    }
    
    .fun-fact {
      background: linear-gradient(45deg, #1e293b, #334155);
      border-left: 4px solid #0ea5e9;
      border-radius: 8px;
      padding: 15px;
      margin: 15px 0;
      transition: all 0.3s ease;
      cursor: pointer;
    }
    
    .fun-fact:hover {
      background: linear-gradient(45deg, #334155, #475569);
      border-left-width: 8px;
      transform: translateX(10px);
    }
    
    .wave {
      animation: wave 2s ease-in-out infinite;
      display: inline-block;
      transform-origin: 70% 70%;
    }
    
    @keyframes wave {
      0%, 100% { transform: rotate(0deg); }
      25% { transform: rotate(20deg); }
      75% { transform: rotate(-10deg); }
    }
    
    .interactive-section {
      margin: 40px 0;
      padding: 20px;
      background: rgba(30, 41, 59, 0.3);
      border-radius: 15px;
      border: 1px solid rgba(6, 182, 212, 0.2);
      transition: all 0.3s ease;
    }
    
    .interactive-section:hover {
      background: rgba(30, 41, 59, 0.5);
      border-color: rgba(6, 182, 212, 0.5);
    }
  </style>
</div>

<!-- ANIMATED BANNER -->
<div align="center">
  <img class="floating-banner" src="https://user-images.githubusercontent.com/74038190/213910845-af37a709-8995-40d6-be59-724526e3c3d7.gif" alt="Animated Banner">
</div>

<br>

<!-- ANIMATED CONTRIBUTION GRAPH -->
<div align="center">
    <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/output/pacman-contribution-graph-dark.svg">
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/output/pacman-contribution-graph.svg">
        <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/output/pacman-contribution-graph.svg" style="border-radius: 10px; transition: transform 0.3s ease;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">
    </picture>
</div>

<!-- INTERACTIVE TITLE -->
<div align="center" class="interactive-section">
  <h1 class="glow-title">Hi there, I'm Rehman Kalawant <span class="wave">👋</span></h1>
  
  <div class="typing-effect">
    REACT Developer | Frontend Developer | Backend Developer | Fullstack Developer
  </div>
</div>

---

<!-- INTERACTIVE SOCIAL LINKS -->
<div align="center" class="interactive-section">
    <h3>🌐 Let's Connect!</h3>
    <br>
    <a href="https://www.linkedin.com/in/nihalsheikh/" class="interactive-badge">
        <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
    </a>
    <a href="https://github.com/nihalsheikh" class="interactive-badge">
        <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=gold" alt="GitHub">
    </a>
    <a href="mailto:nihalsheikh585@gmail.com" class="interactive-badge">
        <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
    </a>
    <a href="https://flowcv.me/nihalsheikh" class="interactive-badge">
        <img src="https://img.shields.io/static/v1?message=portfolio&logo=ko-fi&label=&color=gold&logoColor=black&labelColor=&style=for-the-badge" alt="Portfolio">
    </a>
</div>

---

## 🚀 Interactive Stats

<div align="center" class="interactive-section">
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;" align="center">
    <div class="stats-card">
      <img src="https://v0-git-hub-streak-score-card-phi.vercel.app/api/card-with-avatar?username=rehman2711&theme=%7B%22backgroundColor%22%3A%22%230f172a%22%2C%22textColor%22%3A%22%23e2e8f0%22%2C%22accentColor%22%3A%22%230ea5e9%22%2C%22borderColor%22%3A%22%231e293b%22%2C%22waterColor%22%3A%22%230ea5e9%22%2C%22streakColor%22%3A%22%2306b6d4%22%7D&v=1755267867951" alt="GitHub Streak">
    </div>
    <div class="stats-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=rehman2711&theme=gotham&hide_border=true&include_all_commits=false&count_private=false&layout=compact" alt="Top Languages">
    </div>
  </div>
</div>

---

## 💫 Interactive About Me

<div class="interactive-section">
  <div class="code-block">
    <div style="margin-top: 25px;">
      <div class="code-line"><span style="color: #f59e0b;">const</span> <span style="color: #06b6d4;">developer</span> <span style="color: #e2e8f0;">=</span> <span style="color: #10b981;">{</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">name:</span> <span style="color: #84cc16;">"Rehman Kalawant"</span><span style="color: #e2e8f0;">,</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">role:</span> <span style="color: #84cc16;">"Full Stack Developer"</span><span style="color: #e2e8f0;">,</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">location:</span> <span style="color: #84cc16;">"📍 Your City, Country"</span><span style="color: #e2e8f0;">,</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">code:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"JavaScript"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"TypeScript"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"Python"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"HTML"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"CSS"</span><span style="color: #e2e8f0;">],</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">askMeAbout:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"web dev"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"tech"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"app dev"</span><span style="color: #e2e8f0;">],</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">currentFocus:</span> <span style="color: #84cc16;">"Building awesome user experiences"</span><span style="color: #e2e8f0;">,</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">funFact:</span> <span style="color: #84cc16;">"I debug with console.log and I'm proud of it! 🐛"</span></div>
      <div class="code-line"><span style="color: #10b981;">};</span></div>
    </div>
  </div>
</div>

---

## 🛠️ Interactive Tech Stack

<div class="interactive-section">
  <h3 align="center">Frontend Technologies</h3>
  <div class="tech-stack">
    <img class="tech-item" src="https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB" alt="React">
    <img class="tech-item" src="https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D" alt="Vue.js">
    <img class="tech-item" src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
    <img class="tech-item" src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E" alt="JavaScript">
    <img class="tech-item" src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
    <img class="tech-item" src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  </div>
  
  <h3 align="center">Styling & UI</h3>
  <div class="tech-stack">
    <img class="tech-item" src="https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="TailwindCSS">
    <img class="tech-item" src="https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white" alt="Sass">
    <img class="tech-item" src="https://img.shields.io/badge/MUI-%230081CB.svg?style=for-the-badge&logo=mui&logoColor=white" alt="Material-UI">
    <img class="tech-item" src="https://img.shields.io/badge/Framer-black?style=for-the-badge&logo=framer&logoColor=blue" alt="Framer Motion">
  </div>
  
  <h3 align="center">Tools & Others</h3>
  <div class="tech-stack">
    <img class="tech-item" src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white" alt="Git">
    <img class="tech-item" src="https://img.shields.io/badge/webpack-%238DD6F9.svg?style=for-the-badge&logo=webpack&logoColor=black" alt="Webpack">
    <img class="tech-item" src="https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white" alt="Vite">
    <img class="tech-item" src="https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white" alt="Figma">
  </div>
</div>

---

## 🎯 Featured Projects

<div align="center" class="interactive-section">
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
    <div class="project-card">
      <a href="https://github.com/rehman2711/gearshift" target="_blank">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=rehman2711&repo=gearshift&theme=gotham&hide_border=true" alt="GearShift Project">
      </a>
    </div>
    <div class="project-card">
      <a href="https://github.com/rehman2711/gearshift-api" target="_blank">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=rehman2711&repo=gearshift-api&theme=gotham&hide_border=true" alt="GearShift API">
      </a>
    </div>
  </div>
</div>

---

## 🏆 GitHub Trophies

<div align="center" class="interactive-section">
  <img src="https://github-profile-trophy.vercel.app/?username=rehman2711&theme=gotham&no-frame=true&no-bg=false&margin-w=4" alt="GitHub Trophies" style="border-radius: 10px; transition: all 0.3s ease;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">
</div>

---

## 📈 Contribution Graph

<div align="center" class="interactive-section">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=rehman2711&custom_title=Contribution%20Graph&bg_color=0D1117&color=F85D7F&line=F85D7F&point=FFFFFF&area_color=F85D7F&title_color=FFFFFF&area=true" alt="Activity Graph" style="border-radius: 10px; transition: all 0.3s ease;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
</div>

---

## 🎨 Design Philosophy

<div class="interactive-section">
  <blockquote style="border-left: 4px solid #0ea5e9; padding-left: 20px; font-style: italic; color: #94a3b8; background: rgba(30, 41, 59, 0.3); padding: 15px; border-radius: 8px; margin: 20px 0;">
    "Good design is as little design as possible" - Dieter Rams
  </blockquote>

  I believe in creating **intuitive**, **accessible**, and **performant** web experiences. My approach combines:

  <div class="fun-fact">🎯 <strong>User-Centered Design</strong> - Understanding user needs comes first</div>
  <div class="fun-fact">⚡ <strong>Performance Optimization</strong> - Fast, efficient, and scalable solutions</div>
  <div class="fun-fact">📱 <strong>Responsive Design</strong> - Seamless experience across all devices</div>
  <div class="fun-fact">♿ <strong>Accessibility</strong> - Inclusive design for everyone</div>
  <div class="fun-fact">🧪 <strong>Testing</strong> - Reliable code through comprehensive testing</div>
</div>

---

## 📚 Currently Learning

<div class="interactive-section">
  <div class="code-block">
    <div style="margin-top: 25px;">
      <div class="code-line"><span style="color: #f59e0b;">const</span> <span style="color: #06b6d4;">currentlyLearning</span> <span style="color: #e2e8f0;">=</span> <span style="color: #10b981;">{</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">frameworks:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"Next.js 14"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"SvelteKit"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"Astro"</span><span style="color: #e2e8f0;">],</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">languages:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"Rust"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"Go"</span><span style="color: #e2e8f0;">],</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">tools:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"Three.js"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"GSAP"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"Framer Motion"</span><span style="color: #e2e8f0;">],</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">concepts:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"Web3"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"PWAs"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"Micro-frontends"</span><span style="color: #e2e8f0;">],</span></div>
      <div class="code-line" style="margin-left: 20px;"><span style="color: #f59e0b;">design:</span> <span style="color: #e2e8f0;">[</span><span style="color: #84cc16;">"Motion Design"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"3D Graphics"</span><span style="color: #e2e8f0;">,</span> <span style="color: #84cc16;">"AR/VR"</span><span style="color: #e2e8f0;">]</span></div>
      <div class="code-line"><span style="color: #10b981;">};</span></div>
      <br>
      <div class="code-line"><span style="color: #06b6d4;">console</span><span style="color: #e2e8f0;">.</span><span style="color: #f59e0b;">log</span><span style="color: #e2e8f0;">(</span><span style="color: #84cc16;">"Always growing, always learning! 🚀"</span><span style="color: #e2e8f0;">);</span></div>
    </div>
  </div>
</div>

---

---

<div align="center" class="interactive-section">
  <h3>💭 Random Dev Quote</h3>
  <img src="https://quotes-github-readme.vercel.app/api?quote=Code%20is%20poetry%20written%20for%20machine%20and%20human%20communication&quoteColor=CFEFFD&backgroundColor=001219&type=horizontal" alt="Dev Quote" style="border-radius: 10px; margin: 20px 0;">
</div>

---

<div align="center" class="interactive-section">
  <img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" alt="Snake animation" style="border-radius: 10px;">
</div>

<div align="center" style="margin-top: 30px;">
  <h3 style="color: #0ea5e9;">⭐ Thanks for visiting! Don't forget to star some repositories if you find them interesting! ⭐</h3>
</div>
