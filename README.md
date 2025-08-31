<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Nafees Hossain — Portfolio</title>
<meta name="description" content="Portfolio of Nafees Hossain — Expense Splitter style UI.">
<style>
  :root{
    --ink:#0f0f12;--bg:#f4f3ef;--card:#fff7ee;--orange:#f08a11;--pink:#ff6ea8;--green:#66db8c;--purple:#9b6af8;
    --shadow:2px 3px 0 rgba(0,0,0,.85);
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;background:var(--bg);color:var(--ink);font-family:Inter,ui-sans-serif,system-ui,-apple-system,Segoe UI,Roboto,Arial}
  .wrap{max-width:920px;margin:28px auto;padding:0 16px}
  .row{display:flex;align-items:center;gap:16px}
  .btn-square{width:64px;height:64px;border-radius:12px;box-shadow:var(--shadow);display:grid;place-items:center;border:3px solid #0b0b0d;font-weight:900}
  .btn-mic{background:#62e88c}
  .btn-img{background:#b796ff}
  .btn-send{background:#ffa7c4}
  .icon{font-size:28px}
  /* Prompt box */
  .prompt-wrap{flex:1;position:relative}
  .prompt{
    width:100%;min-height:92px;background:#fff;border-radius:18px;
    border:4px solid #0e0e12;outline:7px solid #ffffff; /* double frame look */
    padding:18px 56px 18px 22px;font-size:28px;font-weight:700;
    box-shadow:var(--shadow);
  }
  .send-fab{
    position:absolute;right:-84px;top:16px;width:76px;height:76px;border-radius:18px;border:4px solid #0e0e12;
    display:grid;place-items:center;box-shadow:var(--shadow);background:#ff8ab1;cursor:pointer;
  }
  /* Counter badge */
  .count{
    position:absolute;right:-168px;top:-16px;width:110px;height:110px;border-radius:999px;
    background:conic-gradient(#a3ff75 0 300deg,#111 300deg 360deg);
    display:grid;place-items:center;box-shadow:var(--shadow);border:6px solid #111;
  }
  .count span{background:#fff;border-radius:999px;padding:14px 18px;font-weight:900;border:3px solid #a3ff75}
  /* Section titles */
  h1,h2,h3{margin:0}
  .title{font-size:24px;margin:8px 0 18px 0;font-weight:900}
  header.site{display:flex;justify-content:space-between;align-items:center;margin-bottom:6px}
  header .brand{font-weight:900;font-size:18px}
  a{color:#111;text-decoration:none;border-bottom:2px solid #111}
  /* Orange Question Card */
  .quiz{
    margin:26px 0;padding:18px;border:4px solid #0c0c10;border-radius:16px;background:var(--card);box-shadow:var(--shadow)
  }
  .quiz .head{display:flex;align-items:center;gap:12px;margin-bottom:10px}
  .chip{background:#ff9b2d;color:#fff;padding:8px 12px;border-radius:999px;font-weight:900;border:3px solid #0e0e12;box-shadow:var(--shadow)}
  .arrow{width:34px;height:34px;border-radius:999px;background:#ff9b2d;color:#fff;display:grid;place-items:center;border:3px solid #0e0e12;box-shadow:var(--shadow);font-weight:900}
  .progress{flex:1;height:16px;border:3px solid #0e0e12;border-radius:999px;background:#fff;box-shadow:var(--shadow);position:relative}
  .progress i{position:absolute;left:0;top:0;bottom:0;width:45%;background:#0e0e12;border-radius:999px}
  .quiz p.q{font-size:20px;font-weight:800;margin:10px 0 12px 0}
  .opt{
    display:flex;align-items:center;gap:10px;background:#fff;margin:8px 0;padding:18px;border-radius:12px;
    border:4px solid #0f0f12;box-shadow:var(--shadow);font-weight:900
  }
  .opt input{width:24px;height:24px;border:3px solid #111}
  .custom{
    margin-top:8px;padding:16px;border-radius:12px;background:#fff;border:4px dashed #0f0f12;box-shadow:var(--shadow);
    font-weight:900;display:flex;align-items:center;gap:10px
  }
  /* Past sessions grid */
  .sessions{margin:24px 0}
  .grid{display:grid;grid-template-columns:repeat(3,84px);gap:14px}
  .tile{width:84px;height:84px;border-radius:8px;border:4px solid #0f0f12;box-shadow:var(--shadow);background:#e9e9ef}
  .t1{background:#f17878}.t2{background:#6fd0c0}.t3{background:#ffe061}
  .t4{background:#f79d29}.t5{background:#95dbff}.t6{background:#90d2c1}
  .t7{background:#e65454}.t8{background:#eae7f3}
  /* Responsive */
  @media(max-width:980px){
    .send-fab{right:8px;top:8px}
    .count{right:8px;top:-80px;transform:scale(.8)}
    .row{gap:10px}
    .btn-square{width:56px;height:56px}
    .prompt{min-height:84px;font-size:22px;padding-right:54px}
    .grid{grid-template-columns:repeat(3,72px)}
    .tile{width:72px;height:72px}
  }
</style>
</head>
<body>
  <div class="wrap">
    <header class="site">
      <div class="brand">Nafees Hossain</div>
      <nav><a href="https://github.com/nafeeshossain" target="_blank">GitHub</a></nav>
    </header>

    <!-- TOP ROW: Mic + Image + Prompt + Send + Counter -->
    <section aria-label="prompt-ui">
      <div class="row" style="position:relative">
        <button class="btn-square btn-mic" title="Voice"><span class="icon">🎙️</span></button>
        <button class="btn-square btn-img" title="Image"><span class="icon">🖼️</span></button>

        <div class="prompt-wrap">
          <textarea class="prompt" spellcheck="false">Create me an app called expense splitter</textarea>
          <div class="send-fab" title="Send"><span class="icon">✈️</span></div>
          <div class="count"><span>1.4k</span></div>
        </div>
      </div>
    </section>

    <!-- ORANGE QUESTION CARD -->
    <section class="quiz" aria-label="question-card">
      <div class="head">
        <div class="arrow">◀</div>
        <div class="chip">QUESTION 1/5</div>
        <div class="progress"><i></i></div>
        <div class="arrow">▶</div>
      </div>
      <p class="q">Do you want users to upload a CSV of expenses, or enter expenses manually via the UI?</p>
      <label class="opt"><input type="checkbox"> Upload CSV</label>
      <label class="opt"><input type="checkbox"> Manual Entry Form</label>
      <div class="custom">＋ Add Custom Option</div>
    </section>

    <!-- PAST SESSIONS GRID -->
    <section class="sessions" aria-label="past-sessions">
      <h3 class="title">Past Sessions</h3>
      <div class="grid">
        <div class="tile t1"></div>
        <div class="tile t6"></div>
        <div class="tile t3"></div>
        <div class="tile t4"></div>
        <div class="tile t5"></div>
        <div class="tile t8"></div>
        <div class="tile t6"></div>
        <div class="tile t7"></div>
        <div class="tile"></div>
      </div>
    </section>

    <footer style="margin:40px 0 24px 0;font-weight:700">© Nafees — built to match the exact UI from the screenshots.</footer>
  </div>

<script>
  // purely decorative: make count ring animate slightly on click
  const send = document.querySelector('.send-fab');
  const count = document.querySelector('.count');
  send.addEventListener('click', ()=>{
    count.style.transform='scale(1.06)';
    setTimeout(()=>count.style.transform='scale(1)',140);
  });
</script>
</body>
</html>
