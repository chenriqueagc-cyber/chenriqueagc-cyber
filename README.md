<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#0a0d12">
  <meta name="description" content="Portfólio de Carlos Henrique Aguiar Caldas — estudante de Inteligência Artificial, desenvolvimento de software e infraestrutura.">
  <title>Carlos Henrique Aguiar Caldas — IA & Desenvolvimento</title>
  <style>
    :root {
      color-scheme: dark;
      --bg: #090c11;
      --panel: #0e131b;
      --panel-soft: #101722;
      --text: #edf3fc;
      --muted: #9baabe;
      --subtle: #64748b;
      --line: rgba(132, 163, 204, .18);
      --blue: #70aaff;
      --blue-strong: #4389f5;
      --radius: 18px;
      --max: 1120px;
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background:
        radial-gradient(ellipse at 82% 8%, rgba(54, 112, 196, .13), transparent 31rem),
        radial-gradient(ellipse at 4% 45%, rgba(40, 81, 135, .08), transparent 26rem),
        var(--bg);
      color: var(--text);
      font: 16px/1.65 Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      letter-spacing: -.01em;
    }
    a { color: inherit; text-decoration: none; }
    a:focus-visible { outline: 2px solid var(--blue); outline-offset: 4px; border-radius: 5px; }
    .wrap { width: min(var(--max), calc(100% - 48px)); margin: 0 auto; }
    .topbar {
      display: flex; justify-content: space-between; align-items: center; gap: 20px;
      padding: 23px 0; border-bottom: 1px solid var(--line);
      color: var(--muted); font: 12px/1.5 ui-monospace, SFMono-Regular, Menlo, monospace;
    }
    .brand { display: inline-flex; align-items: center; gap: 12px; color: var(--text); }
    .brand-mark { color: var(--blue); font-size: 22px; font-weight: 800; }
    .topnav { display: flex; gap: 24px; }
    .topnav a:hover, .social:hover { color: var(--blue); }
    .hero {
      display: grid; grid-template-columns: minmax(0, 1.15fr) minmax(280px, .85fr);
      align-items: center; gap: 48px; padding: 82px 0 76px;
    }
    .eyebrow {
      margin: 0 0 12px; color: var(--muted);
      font: 13px/1.5 ui-monospace, SFMono-Regular, Menlo, monospace; letter-spacing: .08em;
    }
    h1 { margin: 0; font-size: clamp(2.6rem, 6vw, 4.65rem); line-height: 1.02; letter-spacing: -.065em; }
    .gradient { color: var(--blue); background: linear-gradient(100deg, #91c2ff, #4d91fa 70%); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent; }
    .lead { max-width: 630px; margin: 22px 0 12px; color: #cbd7e7; font-size: 1.07rem; }
    .intro { max-width: 620px; color: var(--muted); margin: 0; }
    .socials { display: flex; flex-wrap: wrap; gap: 18px; margin-top: 28px; }
    .social { display: inline-flex; align-items: center; gap: 9px; color: #d9e3f1; font-size: .9rem; transition: color .2s; }
    .social svg { width: 19px; height: 19px; }
    .hero-art { min-height: 300px; display: grid; place-items: center; position: relative; isolation: isolate; }
    .orbit { position: absolute; width: 270px; height: 270px; border: 1px solid rgba(112,170,255,.32); border-radius: 50%; }
    .orbit::after { content: ""; position: absolute; top: 28px; right: 20px; width: 8px; height: 8px; border-radius: 50%; background: var(--blue); box-shadow: 0 0 20px rgba(112,170,255,.7); }
    .terminal {
      position: relative; width: min(100%, 310px); min-height: 160px; display: flex; align-items: center;
      padding: 28px; border: 1px solid rgba(112,170,255,.5); border-radius: 18px;
      background: linear-gradient(135deg, rgba(15,22,33,.96), rgba(8,12,18,.9));
      box-shadow: 0 22px 80px rgba(0,0,0,.28), inset 0 1px rgba(255,255,255,.03);
      font: 700 4rem/1 ui-monospace, SFMono-Regular, Menlo, monospace;
    }
    .terminal .prompt { color: var(--text); }
    .terminal .cursor { color: var(--blue); animation: blink 1.2s step-end infinite; }
    .art-note { position: absolute; right: 0; bottom: 8px; color: var(--subtle); font: 11px/2 ui-monospace, monospace; letter-spacing: .14em; }
    @keyframes blink { 50% { opacity: .25; } }
    section { border-top: 1px solid var(--line); padding: 38px 0; }
    .section-head { display: flex; align-items: center; gap: 13px; margin: 0 0 22px; font-size: 1.25rem; letter-spacing: -.03em; }
    .section-head .num { color: var(--blue); font: 13px ui-monospace, monospace; }
    .tech-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; }
    .card {
      border: 1px solid var(--line); border-radius: var(--radius);
      background: linear-gradient(145deg, rgba(17,24,35,.78), rgba(11,15,22,.8));
      padding: 23px; transition: transform .2s, border-color .2s;
    }
    .card:hover { transform: translateY(-3px); border-color: rgba(112,170,255,.42); }
    .card h3 { margin: 0 0 18px; font-size: .98rem; font-weight: 600; }
    .chips { display: flex; flex-wrap: wrap; gap: 8px; }
    .chip { padding: 6px 10px; border-radius: 8px; border: 1px solid rgba(132,163,204,.16); background: rgba(132,163,204,.06); color: #c7d6e9; font-size: .78rem; }
    .details { display: grid; grid-template-columns: 1.05fr 1fr .95fr; gap: 28px; }
    .detail-col { min-width: 0; }
    .detail-col + .detail-col { border-left: 1px solid var(--line); padding-left: 28px; }
    .detail-title { display: flex; align-items: center; gap: 10px; margin: 0 0 18px; font-size: 1.05rem; }
    .detail-title .symbol { color: var(--blue); font-size: 1.2rem; }
    .project { margin: 0 0 19px; }
    .project strong { display: block; margin-bottom: 3px; font-size: .91rem; font-weight: 600; }
    .project p, .muted { margin: 0; color: var(--muted); font-size: .86rem; }
    .project strong::before { content: "↳"; margin-right: 9px; color: var(--blue); }
    .edu { margin-bottom: 22px; }
    .edu strong { display: block; font-size: .9rem; }
    .edu span { display: block; color: var(--muted); font-size: .84rem; }
    .edu .date { margin-top: 5px; color: var(--subtle); }
    .focus-box { margin-top: 23px; padding: 18px; border: 1px solid var(--line); border-radius: 14px; background: rgba(15,22,33,.55); }
    .focus-box strong { display: block; margin-bottom: 5px; color: var(--blue); font-size: .9rem; }
    .focus-box p { margin: 0; color: var(--muted); font-size: .84rem; }
    .connect {
      display: flex; justify-content: space-between; align-items: center; gap: 20px;
      padding: 26px; border: 1px solid rgba(112,170,255,.28); border-radius: var(--radius);
      background: linear-gradient(115deg, rgba(35,74,126,.17), rgba(14,19,27,.72));
    }
    .connect h2 { margin: 0 0 5px; font-size: 1.15rem; }
    .connect p { margin: 0; color: var(--muted); font-size: .9rem; }
    .button { display: inline-flex; align-items: center; justify-content: center; gap: 9px; padding: 11px 16px; border-radius: 10px; background: var(--blue); color: #07101d; font-weight: 700; font-size: .88rem; white-space: nowrap; transition: transform .2s, background .2s; }
    .button:hover { transform: translateY(-2px); background: #9ac6ff; }
    footer { display: flex; justify-content: space-between; gap: 18px; padding: 24px 0 32px; color: var(--subtle); font: 11px/1.6 ui-monospace, monospace; }
    footer .signature { color: var(--muted); }
    @media (max-width: 800px) {
      .hero { grid-template-columns: 1fr; gap: 20px; padding: 58px 0; }
      .hero-art { min-height: 230px; }
      .orbit { width: 210px; height: 210px; }
      .terminal { width: 260px; min-height: 130px; font-size: 3.4rem; }
      .art-note { right: 4%; bottom: 0; }
      .tech-grid { grid-template-columns: 1fr; }
      .details { grid-template-columns: 1fr; gap: 25px; }
      .detail-col + .detail-col { border-left: 0; border-top: 1px solid var(--line); padding: 25px 0 0; }
    }
    @media (max-width: 540px) {
      .wrap { width: min(var(--max), calc(100% - 30px)); }
      .topbar { align-items: flex-start; }
      .topnav { display: none; }
      h1 { font-size: clamp(2.45rem, 13vw, 3.7rem); }
      .lead { font-size: 1rem; }
      .socials { gap: 14px; }
      .connect { align-items: flex-start; flex-direction: column; }
      footer { flex-direction: column; }
    }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { scroll-behavior: auto !important; animation: none !important; transition: none !important; }
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header class="topbar">
      <a class="brand" href="#inicio" aria-label="Voltar ao início">
        <span class="brand-mark">&gt;_</span>
        <span>carlos-henrique-aguiar-caldas</span>
      </a>
      <nav class="topnav" aria-label="Navegação principal">
        <a href="#tecnologias">Tecnologias</a>
        <a href="#projetos">Projetos</a>
        <a href="#formacao">Formação</a>
      </nav>
    </header>

    <main>
      <section class="hero" id="inicio" style="border-top:0">
        <div>
          <p class="eyebrow">OLÁ, EU SOU</p>
          <h1>Carlos Henrique<br><span class="gradient">Aguiar Caldas.</span></h1>
          <p class="lead">Estudante de Bacharelado em Inteligência Artificial na UFDPar, com formação técnica em Informática pelo IFMA.</p>
          <p class="intro">Tenho interesse em Inteligência Artificial, desenvolvimento de software, modelos de linguagem e infraestrutura de sistemas. Gosto de explorar tecnologias, construir projetos práticos e entender como ferramentas diferentes podem resolver problemas reais.</p>
          <div class="socials">
            <a class="social" href="https://www.linkedin.com/in/carlos-henrique-aguiar-caldas-782b23254/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn (abre em nova aba)">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M20.45 2H3.55C2.69 2 2 2.68 2 3.52v16.96c0 .84.69 1.52 1.55 1.52h16.9c.86 0 1.55-.68 1.55-1.52V3.52c0-.84-.69-1.52-1.55-1.52ZM8 18H5V9h3v9ZM6.5 7.75A1.75 1.75 0 1 1 6.5 4.25a1.75 1.75 0 0 1 0 3.5ZM19 18h-3v-4.38c0-1.05-.02-2.4-1.46-2.4-1.46 0-1.68 1.14-1.68 2.32V18h-3V9h2.88v1.23h.04c.4-.7 1.38-1.45 2.84-1.45C18.66 8.78 19 10.7 19 13.2V18Z"/></svg>
              LinkedIn
            </a>
            <a class="social" href="https://github.com/" target="_blank" rel="noopener noreferrer" aria-label="GitHub — atualize o link com seu usuário">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M12 .9a11.1 11.1 0 0 0-3.51 21.63c.55.1.76-.24.76-.54v-2.1c-3.1.67-3.76-1.32-3.76-1.32-.5-1.28-1.24-1.62-1.24-1.62-1.01-.69.08-.68.08-.68 1.12.08 1.71 1.15 1.71 1.15 1 1.7 2.62 1.21 3.26.93.1-.72.39-1.21.71-1.49-2.48-.28-5.09-1.24-5.09-5.52 0-1.22.44-2.22 1.15-3-.12-.28-.5-1.42.11-2.96 0 0 .94-.3 3.05 1.14a10.6 10.6 0 0 1 5.56 0c2.11-1.44 3.04-1.14 3.04-1.14.61 1.54.23 2.68.12 2.96.71.78 1.14 1.78 1.14 3 0 4.29-2.61 5.23-5.1 5.51.4.35.76 1.03.76 2.08v3.06c0 .3.2.65.77.54A11.1 11.1 0 0 0 12 .9Z"/></svg>
              GitHub
            </a>
          </div>
        </div>
        <div class="hero-art" aria-hidden="true">
          <div class="orbit"></div>
          <div class="terminal"><span class="prompt">&gt;</span><span class="cursor">_</span></div>
          <div class="art-note">IDEIAS<br>CÓDIGO<br>INTELIGÊNCIA<br>IMPACTO</div>
        </div>
      </section>

      <section id="tecnologias">
        <h2 class="section-head"><span class="num">01 /</span> Tecnologias &amp; ferramentas</h2>
        <div class="tech-grid">
          <article class="card">
            <h3>01 — Linguagens de programação</h3>
            <div class="chips">
              <span class="chip">Python</span><span class="chip">Java</span><span class="chip">JavaScript</span><span class="chip">Shell Script</span>
            </div>
          </article>
          <article class="card">
            <h3>02 — Inteligência Artificial</h3>
            <div class="chips">
              <span class="chip">Machine Learning</span><span class="chip">LLMs</span><span class="chip">Fine-tuning</span><span class="chip">Automação com IA</span><span class="chip">Chatbots</span>
            </div>
          </article>
          <article class="card">
            <h3>03 — Sistemas &amp; infraestrutura</h3>
            <div class="chips">
              <span class="chip">Linux</span><span class="chip">Git</span><span class="chip">Redes</span><span class="chip">Servidores</span><span class="chip">Sistemas embarcados</span>
            </div>
          </article>
        </div>
      </section>

      <section id="projetos">
        <div class="details">
          <div class="detail-col">
            <h2 class="detail-title"><span class="symbol">⌘</span> Projetos &amp; exploração</h2>
            <article class="project">
              <strong>IA local &amp; modelos de linguagem</strong>
              <p>Exploração de LLMs em ambientes com recursos computacionais limitados.</p>
            </article>
            <article class="project">
              <strong>Agentes de IA</strong>
              <p>Estudos de assistentes, ferramentas e automação de tarefas.</p>
            </article>
            <article class="project">
              <strong>Linux &amp; sistemas embarcados</strong>
              <p>Experimentos com distribuições Linux, TV Boxes e hardware acessível.</p>
            </article>
            <article class="project">
              <strong>Desenvolvimento de software</strong>
              <p>Exercícios e aplicações para aprimorar habilidades de programação.</p>
            </article>
          </div>

          <div class="detail-col" id="formacao">
            <h2 class="detail-title"><span class="symbol">⌁</span> Formação</h2>
            <div class="edu">
              <strong>Bacharelado em Inteligência Artificial</strong>
              <span>UFDPar — Universidade Federal do Delta do Parnaíba</span>
              <span class="date">Início: 13 de agosto de 2026</span>
            </div>
            <div class="edu">
              <strong>Técnico em Informática</strong>
              <span>IFMA — Instituto Federal do Maranhão</span>
            </div>
            <h2 class="detail-title" style="margin-top:28px"><span class="symbol">◎</span> Foco atual</h2>
            <p class="muted">Aprofundando conhecimentos em programação, fundamentos de IA, estatística computacional, Linux e desenvolvimento de soluções práticas.</p>
          </div>

          <div class="detail-col">
            <h2 class="detail-title"><span class="symbol">↗</span> Próximos passos</h2>
            <p class="muted">Buscando oportunidades para aprender com outros desenvolvedores, contribuir com projetos e crescer nas áreas de Inteligência Artificial e Tecnologia.</p>
            <div class="focus-box">
              <strong>Vamos construir algo?</strong>
              <p>Estou aberto a trocar conhecimentos, colaborar em projetos e conhecer novas oportunidades na área de tecnologia.</p>
            </div>
          </div>
        </div>
      </section>

      <section>
        <div class="connect">
          <div>
            <h2>Vamos nos conectar?</h2>
            <p>Ideias, colaboração e tecnologia — sempre há algo novo para construir.</p>
          </div>
          <a class="button" href="https://www.linkedin.com/in/carlos-henrique-aguiar-caldas-782b23254/" target="_blank" rel="noopener noreferrer">
            Fale comigo <span aria-hidden="true">↗</span>
          </a>
        </div>
      </section>
    </main>

    <footer>
      <span>♡ &nbsp; Transformando curiosidade em conhecimento e conhecimento em projetos.</span>
      <span class="signature"><span style="color:var(--blue)">&gt;_</span> Carlos Henrique Aguiar Caldas</span>
    </footer>
  </div>
</body>
</html>
