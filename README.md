<!-- Animated README - single-file HTML
Instructions: Save this file as `animated_readme.html` and open in a browser. To host live, push to a GitHub repo and enable GitHub Pages (or add to your portfolio site). Images are externally linked (GitHub stats, skillicons). You can copy parts back into README.md (GitHub strips some animations) or link this file from your GitHub Pages.
-->

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shalin Modi — Animated Profile</title>
  <style>
    :root{--bg:#0f0c29;--card:#111827;--muted:#9CA3AF;--accent1:#00FFFF;--accent2:#ff69b4}
    html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,Segoe UI,Roboto,'Helvetica Neue',Arial}
    body{background:linear-gradient(160deg,var(--bg),#021028);color:#E6EEF8;-webkit-font-smoothing:antialiased;padding:32px}
    .wrap{max-width:1100px;margin:0 auto;}

    /* Header */
    header{display:flex;gap:24px;align-items:center}
    .avatar{width:120px;height:120px;border-radius:20px;background:linear-gradient(135deg,var(--accent2),var(--accent1));display:flex;align-items:center;justify-content:center;font-weight:700;font-size:2rem;box-shadow:0 10px 30px rgba(0,0,0,.6);transform:translateY(-6px);animation:bob 4s ease-in-out infinite}
    @keyframes bob{0%{transform:translateY(-6px)}50%{transform:translateY(6px)}100%{transform:translateY(-6px)}}

    .title{flex:1}
    .title h1{margin:0;font-size:2.2rem;letter-spacing:0.4px}
    .title h3{margin:6px 0 0;font-weight:400;color:var(--muted)}

    /* typing */
    .typing{display:inline-block;white-space:nowrap;overflow:hidden;border-right:2px solid rgba(230,238,248,.6);box-sizing:content-box;animation:typing 4s steps(30,end) infinite, blink .75s step-end infinite}
    @keyframes typing{0%{width:0}50%{width:100%}100%{width:0}}
    @keyframes blink{50%{border-color:transparent}}

    /* Badges */
    .badges{margin-top:12px;display:flex;gap:10px;flex-wrap:wrap}
    .badge{display:inline-flex;align-items:center;gap:8px;padding:6px 10px;border-radius:999px;background:rgba(255,255,255,.04);backdrop-filter:blur(4px)}

    /* Section cards */
    .grid{display:grid;grid-template-columns:1fr 380px;gap:20px;margin-top:28px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01)); padding:18px;border-radius:12px;box-shadow:0 6px 20px rgba(2,6,23,.6)}

    /* Tech icons */
    .tech{display:flex;justify-content:center;flex-wrap:wrap;gap:12px;padding:12px}
    .tech img{height:48px;width:auto;filter:drop-shadow(0 6px 18px rgba(0,0,0,.6));transform:translateY(0);transition:transform .25s}
    .tech img:hover{transform:translateY(-6px)}

    /* Projects table */
    table{width:100%;border-collapse:collapse;color:#dfe9f3}
    th,td{padding:10px 8px;text-align:left;border-bottom:1px solid rgba(255,255,255,.03)}
    th{color:var(--muted);font-weight:600}
    .link{color:var(--accent2);text-decoration:none}

    /* GitHub stats animation */
    .stats img{max-width:100%;border-radius:8px;filter:drop-shadow(0 10px 24px rgba(0,0,0,.6));transform:scale(.98);transition:transform .4s}
    .stats img:hover{transform:scale(1)}

    /* Footer links */
    .contacts{display:flex;gap:12px;justify-content:center;margin-top:16px}

    /* enter animations */
    .reveal{opacity:0;transform:translateY(12px);transition:opacity .6s ease, transform .6s ease}
    .reveal.visible{opacity:1;transform:none}

    /* small screens */
    @media (max-width:900px){.grid{grid-template-columns:1fr}} 
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="avatar">SM</div>
      <div class="title">
        <h1>🌟 Hi, I'm <span style="color:var(--accent1)">Shalin Modi</span></h1>
        <h3>🤖 <span class="typing">AI/ML Enthusiast • Software Developer • Lifelong Learner</span></h3>
        <div class="badges">
          <img class="badge" src="https://komarev.com/ghpvc/?username=shalin1352004&label=Profile%20Views&color=ff6964&style=for-the-badge" alt="views"/>
        </div>
      </div>
    </header>

    <div class="grid" style="margin-top:20px">
      <div>
        <section class="card reveal" id="about">
          <h2>🚀 About Me</h2>
          <p>💡 Passionate about <strong>AI, ML, and Innovative Software Development</strong>. Currently learning <strong>FastAPI + Cloud Integrations</strong>. <em>"Code is like humor. When you have to explain it, it’s bad."</em></p>
        </section>

        <section class="card reveal" style="margin-top:16px" id="projects">
          <h2>📌 Featured Projects</h2>
          <div style="overflow:auto">
          <table>
            <thead><tr><th>Project</th><th>Description</th><th>Stack</th><th>Link</th></tr></thead>
            <tbody>
              <tr><td><strong>NextGenBuy</strong></td><td>E-commerce accessories website</td><td>Django, Python</td><td><a class="link" href="#">View</a></td></tr>
              <tr><td><strong>Student Management System</strong></td><td>Student data & result analysis</td><td>Django, Python</td><td><a class="link" href="#">View</a></td></tr>
              <tr><td><strong>SkillSwapper</strong></td><td>Skill swapping platform (Hackathon 2025)</td><td>FastAPI, Python</td><td><a class="link" href="#">View</a></td></tr>
              <tr><td><strong>ClassyKicks</strong></td><td>Shoe store with brand & price filters</td><td>Django, PostgreSQL, Tailwind</td><td><a class="link" href="#">View</a></td></tr>
              <tr><td><strong>Two-Wheeler Rental</strong></td><td>Rental booking system</td><td>Java</td><td><a class="link" href="#">View</a></td></tr>
            </tbody>
          </table>
          </div>
        </section>

        <section class="card reveal" style="margin-top:16px" id="internship">
          <h2>💼 Internship</h2>
          <p><strong>Grownited Pvt. Ltd.</strong> — 3 Months — Python, FastAPI, MongoDB, ReactJS, Razorpay, Cloudinary</p>
        </section>

      </div>

      <aside>
        <div class="card reveal stats" id="stats">
          <h3 style="margin-top:0">📊 GitHub & Analytics</h3>
          <div style="display:grid;gap:10px">
            <img src="https://github-readme-stats.vercel.app/api?username=shalin1352004&show_icons=true&theme=radical&count_private=true" alt="stats"/>
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=shalin1352004&theme=radical&date_format=j%20M%5B%20Y%5D" alt="streak"/>
          </div>
        </div>

        <div class="card reveal" style="margin-top:16px" id="tech">
          <h3 style="margin-top:0">🎨 Tech Stack</h3>
          <div class="tech">
            <img src="https://skillicons.dev/icons?i=python" alt="python"/>
            <img src="https://skillicons.dev/icons?i=java" alt="java"/>
            <img src="https://skillicons.dev/icons?i=django" alt="django"/>
            <img src="https://skillicons.dev/icons?i=fastapi" alt="fastapi"/>
            <img src="https://skillicons.dev/icons?i=react" alt="react"/>
            <img src="https://skillicons.dev/icons?i=mongodb" alt="mongodb"/>
            <img src="https://skillicons.dev/icons?i=git,github" alt="git"/>
            <img src="https://skillicons.dev/icons?i=vscode,postman" alt="tools"/>
            <img src="https://skillicons.dev/icons?i=cloudinary,render" alt="deploy"/>
          </div>
        </div>

        <div class="card reveal" style="margin-top:16px;text-align:center" id="connect">
          <h3 style="margin-top:0">🌐 Connect</h3>
          <div class="contacts">
            <a href="https://linkedin.com/in/shalinmodi60"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="li"/></a>
            <a href="https://shalin1352004.github.io/Portfolio-Shalin/"><img src="https://img.shields.io/badge/Portfolio-ff69b4?style=for-the-badge&logo=githubpages&logoColor=white" alt="site"/></a>
            <a href="mailto:shalinmodi60@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="mail"/></a>
          </div>
        </div>

      </aside>
    </div>
  </div>

  <script>
    // Reveal on scroll
    const reveals = document.querySelectorAll('.reveal');
    function revealOnScroll(){
      const h = window.innerHeight;
      reveals.forEach(r=>{
        const rect = r.getBoundingClientRect();
        if(rect.top < h - 80){ r.classList.add('visible'); }
      })
    }
    window.addEventListener('scroll', revealOnScroll);
    window.addEventListener('load', ()=>{ revealOnScroll(); });

    // Simple typing rotation (swap phrases)
    const typing = document.querySelector('.typing');
    const phrases = ['AI/ML Enthusiast • Software Developer • Lifelong Learner','FastAPI + Cloud Integrations','Open Source Contributor • Hackathon Fan'];
    let idx=0; let pause=2800;
    setInterval(()=>{
      idx=(idx+1)%phrases.length; typing.textContent = phrases[idx];
    }, pause);

  </script>
</body>
</html>
