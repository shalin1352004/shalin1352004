<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Shalin Modi — Live Animated Profile</title>
  <style>
    :root{--bg1:#0f0c29;--bg2:#302b63;--accent1:#00FFFF;--accent2:#ff69b4}
    html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",Roboto,'Helvetica Neue',Arial}
    body{background:linear-gradient(135deg,var(--bg1),var(--bg2));color:#e6eef8;overflow-x:hidden}
    /* Container */
    .wrap{max-width:1100px;margin:40px auto;padding:28px;border-radius:16px;background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(0,0,0,0.05));box-shadow:0 10px 40px rgba(2,6,23,0.6);backdrop-filter:blur(6px)}
    header{display:flex;align-items:center;gap:20px}
    .avatar{width:96px;height:96px;border-radius:14px;overflow:hidden;flex:0 0 96px;border:2px solid rgba(255,255,255,0.06)}
    .title{flex:1}
    h1{font-size:28px;margin:0 0 6px;display:flex;align-items:center;gap:10px}
    .name{background:linear-gradient(90deg,var(--accent1),#00c6ff);-webkit-background-clip:text;background-clip:text;color:transparent;font-weight:700}
    .subtitle{margin:0;color:rgba(230,238,248,0.8)}

    /* typing */
    .typing{font-family:monospace;color:var(--accent2);display:inline-block;margin-left:6px}
    .cursor{display:inline-block;width:8px;height:18px;background:var(--accent1);margin-left:6px;vertical-align:bottom;animation:blink 1s steps(2) infinite}
    @keyframes blink{50%{opacity:0}}

    /* badges */
    .badges{display:flex;gap:10px;margin-top:12px}
    .badge{padding:6px 10px;border-radius:999px;background:linear-gradient(90deg,rgba(255,255,255,0.03),rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);font-weight:600}
    .badge img{vertical-align:middle;height:18px}

    /* grid */
    .grid{display:grid;grid-template-columns:1fr 360px;gap:22px;margin-top:26px}

    /* panel */
    .panel{background:linear-gradient(180deg,rgba(255,255,255,0.017),rgba(0,0,0,0.03));padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .about p{margin:0 0 8px}

    /* tech icons row */
    .tech{display:flex;flex-wrap:wrap;gap:10px;margin-top:12px}
    .tech img{width:44px;height:44px;border-radius:8px;padding:6px;background:rgba(255,255,255,0.02);transform:translateY(0);transition:transform .28s ease}
    .tech img:hover{transform:translateY(-6px)}

    /* projects table */
    table{width:100%;border-collapse:collapse;color:inherit}
    th,td{padding:10px;border-bottom:1px dashed rgba(255,255,255,0.03);text-align:left}
    th{font-weight:700;color:rgba(255,255,255,0.9)}

    /* right column cards */
    .card{display:flex;flex-direction:column;gap:12px}
    .stat{display:flex;gap:12px;align-items:center}
    .stat img{height:60px;border-radius:8px;filter:drop-shadow(0 4px 20px rgba(0,0,0,0.6))}

    /* animated contributions strip */
    .graph-wrap{overflow:hidden;border-radius:10px}
    .graph{width:200%;transform:translateX(0);animation:slide 10s linear infinite}
    @keyframes slide{0%{transform:translateX(0)}50%{transform:translateX(-50%)}100%{transform:translateX(0)}}

    /* footer social */
    .socials{display:flex;gap:10px;flex-wrap:wrap}
    .btn{padding:8px 12px;border-radius:10px;background:linear-gradient(90deg,var(--accent1),var(--accent2));color:#03131a;text-decoration:none;font-weight:700}

    /* particles canvas */
    #particles{position:fixed;left:0;top:0;pointer-events:none;width:100%;height:100%;z-index:0}

    /* responsive */
    @media(max-width:920px){.grid{grid-template-columns:1fr}.avatar{width:80px;height:80px}}
  </style>
</head>
<body>
  <canvas id="particles"></canvas>
  <div class="wrap" style="position:relative;z-index:1">
    <header>
      <div class="avatar"><img src="https://avatars.githubusercontent.com/u/placeholder?s=400&v=4" alt="avatar" style="width:100%;height:100%;object-fit:cover" /></div>
      <div class="title">
        <h1>🌟 Hi, I'm <span class="name">Shalin Modi</span> <span class="badge" style="font-size:14px;margin-left:8px;display:inline-block;animation:float 3s ease-in-out infinite">✨</span></h1>
        <p class="subtitle">🤖 AI/ML Enthusiast &nbsp;|&nbsp; 💻 Software Developer &nbsp;|&nbsp; 🌱 Lifelong Learner</p>
        <div class="badges">
          <div class="badge"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="lnk"/></div>
          <div class="badge">FastAPI • Cloud Integrations</div>
          <div class="badge">Open to work</div>
        </div>
      </div>
      <div style="text-align:right">
        <div style="font-family:monospace;color:rgba(255,255,255,0.7)">Profile Views</div>
        <img src="https://komarev.com/ghpvc/?username=shalin1352004&label=Profile%20Views&color=ff6964&style=for-the-badge" alt="views" style="margin-top:8px;border-radius:8px"/>
      </div>
    </header>

    <div class="grid">
      <div>
        <section class="panel about">
          <h3 style="margin:0 0 8px">🚀 About Me <small style="color:rgba(255,255,255,0.5);font-weight:600">— animated</small></h3>
          <p>💡 Passionate about <strong>AI, ML, and innovative software development</strong>. Currently exploring <strong>FastAPI + Cloud</strong> and building full-stack apps.</p>
          <p style="margin-top:6px"><em>"Code is like humor. When you have to explain it, it’s bad."</em> — Cory House</p>

          <div style="margin-top:12px">
            <div style="display:flex;align-items:center;gap:12px">
              <div style="font-weight:800">Status:</div>
              <div style="background:linear-gradient(90deg,var(--accent1),var(--accent2));padding:6px 10px;border-radius:999px;color:#021518;font-weight:800;animation:pulse 2s infinite">Open to internship & collaborations</div>
            </div>
          </div>

          <div style="margin-top:14px">
            <div class="tech">
              <img src="https://skillicons.dev/icons?i=python,java,django,fastapi,react,mongodb,git,github,vscode,postman,cloudinary,render&perline=10" alt="tech" />
            </div>
          </div>

        </section>

        <section class="panel" style="margin-top:16px">
          <h3 style="margin:0 0 8px">📌 Featured Projects</h3>
          <table>
            <thead><tr><th>Project</th><th>Description</th><th>Tech</th></tr></thead>
            <tbody>
              <tr><td><strong>NextGenBuy</strong></td><td>E-commerce accessories website</td><td>Django, Python</td></tr>
              <tr><td><strong>Student Management System</strong></td><td>Student data & result analysis</td><td>Django, Python</td></tr>
              <tr><td><strong>SkillSwapper</strong></td><td>Skill swapping platform (Hackathon 2025)</td><td>FastAPI, Python</td></tr>
              <tr><td><strong>ClassyKicks</strong></td><td>Shoe store with filters</td><td>Django, PostgreSQL, Tailwind</td></tr>
              <tr><td><strong>Two-Wheeler Rental</strong></td><td>Rental booking system</td><td>Java</td></tr>
            </tbody>
          </table>
        </section>

      </div>

      <aside>
        <div class="card">
          <div class="panel stat">
            <div style="flex:1">
              <h4 style="margin:0">💼 Internship</h4>
              <div style="color:rgba(255,255,255,0.7);margin-top:6px">Grownited Pvt. Ltd. — Python, FastAPI, MongoDB, ReactJS</div>
            </div>
            <img src="https://www.grownited.com/wp-content/uploads/2021/03/cropped-favicon-32x32.png" alt="grownited"/>
          </div>

          <div class="panel">
            <h4 style="margin:0 0 8px">📊 GitHub Analytics</h4>
            <div class="graph-wrap" style="background:rgba(255,255,255,0.02);padding:8px;border-radius:8px">
              <div class="graph">
                <img src="https://github-readme-stats.vercel.app/api?username=shalin1352004&show_icons=true&theme=radical&count_private=true" style="height:120px;margin-right:10px;display:inline-block"/>
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=shalin1352004&theme=radical&date_format=j%20M%5B%20Y%5D" style="height:120px;display:inline-block"/>
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=shalin1352004&layout=compact&theme=gruvbox&langs_count=10" style="height:120px;margin-left:10px;display:inline-block"/>
              </div>
            </div>
          </div>

          <div class="panel" style="text-align:center">
            <h4 style="margin:0 0 10px">🌐 Connect With Me</h4>
            <div class="socials">
              <a class="btn" href="https://linkedin.com/in/shalinmodi60" target="_blank">LinkedIn</a>
              <a class="btn" href="https://shalin1352004.github.io/Portfolio-Shalin/" target="_blank">Portfolio</a>
              <a class="btn" href="mailto:shalinmodi60@gmail.com">Email</a>
            </div>
          </div>

        </div>
      </aside>

    </div>

    <footer style="margin-top:18px;text-align:center;color:rgba(255,255,255,0.6)">
      <small>Made with ❤️ — Animated single-file HTML. Save as <code>index.html</code> and host on GitHub Pages for a live profile page.</small>
    </footer>
  </div>

  <script>
    // Typing effect for subtitle
    const phrases = ['AI/ML Enthusiast','Software Developer','Lifelong Learner'];
    let i=0,j=0,forward=true;const el=document.querySelector('.typing');
    // create typing element
    const typingWrap = document.createElement('span');typingWrap.className='typing';document.querySelector('.subtitle').appendChild(typingWrap);
    const cursor = document.createElement('span');cursor.className='cursor';document.querySelector('.subtitle').appendChild(cursor);
    function typeLoop(){
      const text=phrases[i];
      if(forward){typingWrap.textContent = text.slice(0,j+1);j++;if(j===text.length){forward=false;setTimeout(typeLoop,900);return}}
      else{typingWrap.textContent = text.slice(0,j-1);j--;if(j===0){forward=true;i=(i+1)%phrases.length;setTimeout(typeLoop,300);return}}
      setTimeout(typeLoop,80);
    }
    typeLoop();

    // Particles background (lightweight)
    const canvas=document.getElementById('particles');const ctx=canvas.getContext('2d');let W, H, particles=[];
    function resize(){W=canvas.width=innerWidth;H=canvas.height=innerHeight}
    window.addEventListener('resize',resize);resize();
    function rand(min,max){return Math.random()*(max-min)+min}
    for(let k=0;k<80;k++){particles.push({x:rand(0,W),y:rand(0,H),r:rand(0.6,2.6),vx:rand(-0.3,0.3),vy:rand(-0.2,0.2)})}
    function draw(){ctx.clearRect(0,0,W,H);for(const p of particles){ctx.beginPath();ctx.globalAlpha=0.9;ctx.fillStyle='rgba(255,255,255,0.03)';ctx.arc(p.x,p.y,p.r,0,Math.PI*2);ctx.fill();p.x+=p.vx;p.y+=p.vy;if(p.x<0)p.x=W; if(p.x>W)p.x=0; if(p.y<0)p.y=H; if(p.y>H)p.y=0}requestAnimationFrame(draw)}
    draw();

    // small animations
    const badges = document.querySelectorAll('.badge');badges.forEach((b,idx)=>{b.style.animationDelay=(idx*200)+'ms'});

    // pulse animation injection
    const style = document.createElement('style');style.textContent='@keyframes pulse{0%{transform:scale(1)}50%{transform:scale(1.04)}100%{transform:scale(1)}}@keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-6px)}100%{transform:translateY(0)}}';document.head.appendChild(style);
  </script>
</body>
</html>
