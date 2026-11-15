<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="description" content="TaRL Mentor Academy — a self-paced course on Teaching at the Right Level: assessment, level-based grouping, instruction and mentoring.">
<meta name="color-scheme" content="light dark">
<title>TaRL Mentor Academy</title>
<link rel="icon" href='data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16"><rect width="7" height="7" x="1" y="1" rx="1.5" fill="%23C0432E"/><rect width="7" height="7" x="8" y="1" rx="1.5" fill="%23B9860B"/><rect width="7" height="7" x="1" y="8" rx="1.5" fill="%232B63B8"/><rect width="7" height="7" x="8" y="8" rx="1.5" fill="%232E8B4E"/></svg>'>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<script>
/* Apply the saved theme before first paint to avoid a flash. */
try{
  var t = JSON.parse(localStorage.getItem('tarl-mentor-academy-v3') || '{}').theme;
  if (t === 'light' || t === 'dark') document.documentElement.setAttribute('data-theme', t);
}catch(e){}
</script>
<style>
:root{
  --bg:#F2F6F4; --surface:#FFFFFF; --surface2:#E8EFEC; --fg:#14201C; --muted:#52645E; --line:#D3DED9;
  --accent:#0E6B58; --accent-fg:#FFFFFF; --accent-soft:#D6EBE5;
  --c0:#46605A; --c1:#C0432E; --c2:#B9860B; --c3:#2B63B8; --c4:#2E8B4E; --c5:#7A4FA3;
  --ok:#1F7A45; --bad:#B3321F; --hl:#FFF1B8;
  --fd:'Bricolage Grotesque','Inter',system-ui,sans-serif;
  --fb:'Inter',system-ui,-apple-system,'Segoe UI',sans-serif;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --bg:#0D1513; --surface:#151F1C; --surface2:#1C2925; --fg:#E7F0EC; --muted:#9DB0A9; --line:#2A3A35;
    --accent:#4FC3A6; --accent-fg:#06201A; --accent-soft:#16352E;
    --c0:#8FB0A6; --c1:#EE7B66; --c2:#E5B84A; --c3:#6FA1EE; --c4:#5CC27E; --c5:#B28BDA;
    --ok:#5CC27E; --bad:#F08B79; --hl:#4A4220; color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#0D1513; --surface:#151F1C; --surface2:#1C2925; --fg:#E7F0EC; --muted:#9DB0A9; --line:#2A3A35;
  --accent:#4FC3A6; --accent-fg:#06201A; --accent-soft:#16352E;
  --c0:#8FB0A6; --c1:#EE7B66; --c2:#E5B84A; --c3:#6FA1EE; --c4:#5CC27E; --c5:#B28BDA;
  --ok:#5CC27E; --bad:#F08B79; --hl:#4A4220; color-scheme:dark;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
@media (prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}
  *,*::before,*::after{animation-duration:.001ms!important;transition-duration:.001ms!important}
}
body{
  background:var(--bg); color:var(--fg); font:16px/1.65 var(--fb); margin:0;
  padding-left:max(16px,env(safe-area-inset-left,0px));
  padding-right:max(16px,env(safe-area-inset-right,0px));
  padding-block:0;
}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:40;background:var(--surface)}
a{color:var(--accent)}
button,select,textarea,input{font:inherit;color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
.sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap;border:0}
.skip{position:absolute;left:-9999px;top:0;z-index:100;background:var(--accent);color:var(--accent-fg);padding:10px 16px;border-radius:0 0 8px 0;font-weight:600;text-decoration:none}
.skip:focus{left:0}

/* ---------- header ---------- */
.top{
  position:sticky;top:env(safe-area-inset-top,0px);z-index:30;background:var(--surface);
  border-bottom:1px solid var(--line);
  margin:0 calc(-1*max(16px,env(safe-area-inset-left,0px)));
  padding:10px max(16px,env(safe-area-inset-right,0px)) 10px max(16px,env(safe-area-inset-left,0px));
  display:flex;align-items:center;gap:12px;
}
.brand{font:700 18px/1.1 var(--fd);letter-spacing:-.01em;display:flex;gap:10px;align-items:center;text-decoration:none;color:var(--fg);flex:none}
.brand span:last-child{white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.dots{display:grid;grid-template-columns:repeat(2,9px);gap:2px;flex:none}
.dots i{width:9px;height:9px;border-radius:2px;display:block}
.dots i:nth-child(1){background:var(--c1)}.dots i:nth-child(2){background:var(--c2)}
.dots i:nth-child(3){background:var(--c3)}.dots i:nth-child(4){background:var(--c4)}
.prog{flex:1;display:flex;align-items:center;gap:10px;min-width:0;justify-content:flex-end}
.bar{height:8px;background:var(--surface2);border-radius:99px;overflow:hidden;flex:0 1 220px;width:100%}
.bar>b{display:block;height:100%;background:var(--accent);width:0;transition:width .3s}
.pct{font-size:13px;color:var(--muted);font-variant-numeric:tabular-nums;white-space:nowrap}
.icon-btn{background:transparent;border:1px solid var(--line);border-radius:8px;width:40px;height:40px;display:grid;place-items:center;cursor:pointer;font-size:17px;flex:none}
.icon-btn:hover{background:var(--surface2)}
#menuBtn{display:none}

/* ---------- buttons ---------- */
.btn{background:var(--accent);color:var(--accent-fg);border:0;border-radius:8px;padding:9px 16px;font-weight:600;cursor:pointer;min-height:40px;text-decoration:none;display:inline-flex;align-items:center;justify-content:center;gap:6px}
.btn:hover{filter:brightness(1.08)}
.btn.ghost{background:transparent;color:var(--accent);border:1px solid var(--accent)}
.btn.ghost:hover{background:var(--accent-soft);filter:none}
.btn.sm{padding:5px 12px;min-height:32px;font-size:14px}
.btn:disabled{opacity:.45;cursor:not-allowed}

/* ---------- layout ---------- */
.shell{display:grid;grid-template-columns:300px minmax(0,1fr);gap:32px;max-width:1240px;margin:0 auto;padding-block:24px 150px}
nav#side{position:sticky;top:calc(64px + env(safe-area-inset-top,0px));align-self:start;max-height:calc(100vh - 150px);overflow:auto;font-size:14px}
main{min-width:0;max-width:760px}
main:focus{outline:none}

/* ---------- sidebar ---------- */
.navtop{display:flex;flex-direction:column;gap:2px;padding-bottom:10px;border-bottom:1px solid var(--line);margin-bottom:10px}
.navh{font-size:11px;text-transform:uppercase;letter-spacing:.09em;color:var(--muted);margin:8px 0 4px;padding-left:8px;font-weight:600}
nav#side details{border-top:1px solid var(--line);padding:6px 0}
nav#side details:first-of-type{border-top:0}
nav#side summary{display:flex;gap:8px;align-items:center;cursor:pointer;font-weight:600;padding:6px 8px;border-radius:6px;list-style:none}
nav#side summary:hover{background:var(--surface2)}
nav#side summary::-webkit-details-marker{display:none}
nav#side summary .ttl{flex:1;min-width:0}
nav#side .cnt{font-size:12px;color:var(--muted);font-variant-numeric:tabular-nums;flex:none}
.sw{width:10px;height:10px;border-radius:3px;flex:none;display:block}
nav#side a.li{display:flex;gap:8px;align-items:flex-start;padding:6px 8px 6px 26px;text-decoration:none;color:var(--fg);border-radius:6px;line-height:1.35}
nav#side a.li:hover{background:var(--surface2)}
nav#side a.li[aria-current="page"]{background:var(--accent-soft);font-weight:600}
nav#side .navtop a.li{padding-left:8px;font-weight:600}
.ck{width:16px;height:16px;border:1.5px solid var(--line);border-radius:50%;flex:none;margin-top:2px;display:grid;place-items:center;font-size:10px;line-height:1;color:transparent}
.ck.on{background:var(--ok);border-color:var(--ok);color:#fff}

/* ---------- typography ---------- */
.crumb{font-size:13px;color:var(--muted);text-transform:uppercase;letter-spacing:.08em;display:flex;gap:8px;align-items:center;margin-bottom:6px}
h1{font:700 clamp(28px,5vw,40px)/1.12 var(--fd);letter-spacing:-.02em;margin:0 0 8px;text-wrap:balance}
h2{font:700 clamp(22px,3.4vw,28px)/1.2 var(--fd);letter-spacing:-.01em;margin:0 0 10px;text-wrap:balance}
h3{font:700 21px/1.25 var(--fd);margin:34px 0 8px;text-wrap:balance}
h4{font:700 14px/1.3 var(--fb);text-transform:uppercase;letter-spacing:.07em;margin:18px 0 6px}
p{margin:0 0 14px}
ul,ol{padding-left:22px;margin:0 0 16px}
li{margin-bottom:6px}
.lead{font-size:18px;color:var(--muted);max-width:64ch}
.meta{color:var(--muted);font-size:14px;margin-bottom:22px}
.muted{color:var(--muted)}
.callout{background:var(--accent-soft);border-radius:10px;padding:14px 16px;margin:20px 0}
.callout p:last-child{margin:0}
.callout.warn{background:var(--surface2);border:1px solid var(--line)}

/* ---------- cards / CTA ---------- */
.cta{display:flex;flex-wrap:wrap;gap:10px;margin:18px 0 26px}
.cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:12px;margin:16px 0 24px}
.card{display:flex;flex-direction:column;gap:6px;padding:14px;border:1px solid var(--line);border-radius:12px;background:var(--surface);text-decoration:none;color:var(--fg);transition:border-color .15s}
.card:hover{border-color:var(--accent)}
.card .sw{width:12px;height:12px;margin-bottom:2px}

/* ---------- tables ---------- */
.tw{overflow-x:auto;margin:16px 0;border:1px solid var(--line);border-radius:10px;background:var(--surface)}
table{border-collapse:collapse;width:100%;min-width:560px;font-size:14px;line-height:1.5}
th,td{text-align:left;vertical-align:top;padding:10px 12px;border-bottom:1px solid var(--line)}
th{background:var(--surface2);font-size:12px;text-transform:uppercase;letter-spacing:.06em}
tr:last-child td{border-bottom:0}
td.rh{font-weight:600}
.chip{display:inline-block;font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;background:var(--accent-soft);color:var(--accent);border-radius:99px;padding:1px 8px;vertical-align:middle}

/* ---------- widgets & forms ---------- */
.widget,.practice{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:16px;margin:22px 0}
.widget h4:first-child,.practice h4:first-child{margin-top:0}
.widget h4,.practice h4{color:var(--accent)}
label{display:block;font-weight:600;font-size:14px;margin-top:4px}
input[type="text"],input[type="email"],input[type="password"],select,textarea{
  width:100%;background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:10px;margin:6px 0 12px;
}
textarea{resize:vertical;min-height:96px;font-family:var(--fb);font-size:15px}
[aria-invalid="true"]{border-color:var(--bad)!important}
.err{color:var(--bad);font-size:13px;margin:-6px 0 10px}
.hint{font-size:13px;color:var(--muted);margin:0 0 12px}
fieldset{border:1px solid var(--line);border-radius:10px;padding:12px;margin:0 0 12px}
legend{font-weight:600;padding:0 6px;font-size:15px}
.opt{display:flex;gap:10px;align-items:flex-start;padding:7px 6px;border-radius:8px;cursor:pointer;font-weight:400;margin:0}
.opt:hover{background:var(--surface2)}
.opt input{margin:4px 0 0;flex:none}
.fb{margin:10px 0 0;font-size:14px}
.fb.ok{color:var(--ok)}
.fb.bad{color:var(--bad)}

/* ---------- lesson nav ---------- */
.lesson-nav{display:flex;flex-wrap:wrap;gap:10px;justify-content:space-between;align-items:center;margin:28px 0 0;padding-top:18px;border-top:1px solid var(--line)}
.lesson-nav a{max-width:46%;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;display:block}

/* ---------- certificate ---------- */
.cert{border:3px double var(--accent);border-radius:12px;padding:28px 20px;text-align:center;background:var(--surface);margin:20px 0}
.cert h2{font:700 30px/1.2 var(--fd);margin:6px 0}
.cert .nm{font:700 28px var(--fd);border-bottom:2px solid var(--line);display:inline-block;padding:0 18px 4px;margin:10px 0}

/* ---------- toasts ---------- */
.toasts{position:fixed;left:50%;transform:translateX(-50%);bottom:max(16px,env(safe-area-inset-bottom,0px));z-index:60;display:flex;flex-direction:column;gap:8px;width:min(92vw,420px);pointer-events:none}
.toast{background:var(--surface);color:var(--fg);border:1px solid var(--line);border-left:4px solid var(--accent);padding:10px 14px;border-radius:10px;font-size:14px;box-shadow:0 10px 30px rgb(0 0 0/.18);animation:tin .18s ease-out;transition:opacity .3s}
.toast.ok{border-left-color:var(--ok)}
.toast.bad{border-left-color:var(--bad)}
@keyframes tin{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}

/* ---------- responsive ---------- */
@media (max-width:900px){
  .shell{grid-template-columns:minmax(0,1fr);padding-block:18px 120px}
  #menuBtn{display:inline-flex}
  nav#side{
    display:none;position:fixed;inset:0;top:calc(58px + env(safe-area-inset-top,0px));max-height:none;
    background:var(--bg);z-index:29;
    padding:12px max(16px,env(safe-area-inset-right,0px)) 160px max(16px,env(safe-area-inset-left,0px));
    overflow:auto;
  }
  body.menu nav#side{display:block}
  body.menu{overflow:hidden}
  .pct{display:none}
  .bar{flex:1}
  .brand span:last-child{font-size:16px}
}
@media (max-width:520px){
  .brand span:last-child{display:none}
  .lesson-nav a{max-width:100%}
}

/* ---------- print ---------- */
@media print{
  .top,nav#side,.skip,.toasts,.no-print{display:none!important}
  body{background:#fff;color:#000;padding:0}
  body::before{display:none}
  .shell{display:block;max-width:none;padding:0}
  main{max-width:none}
  .cert{page-break-inside:avoid;border-color:#000}
  a{color:#000;text-decoration:none}
}
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>

<header class="top">
  <button id="menuBtn" class="btn ghost sm" aria-expanded="false" aria-controls="side" data-action="menu">Menu</button>
  <a class="brand" href="#/home" aria-label="TaRL Mentor Academy — course home">
    <span class="dots" aria-hidden="true"><i></i><i></i><i></i><i></i></span>
    <span>TaRL Mentor Academy</span>
  </a>
  <div class="prog">
    <div class="bar" id="pbar" role="progressbar" aria-label="Course progress" aria-valuemin="0" aria-valuemax="100" aria-valuenow="0"><b id="pfill"></b></div>
    <span class="pct" id="pct">0%</span>
  </div>
  <button class="icon-btn" id="themeBtn" data-action="theme" aria-label="Change colour theme">◐</button>
</header>

<div class="shell">
  <nav id="side" aria-label="Course outline"></nav>
  <main id="main" tabindex="-1"></main>
</div>

<div class="toasts" id="toasts" aria-live="polite" aria-atomic="false"></div>

<script>
(function () {
  'use strict';

  /* =========================================================
     Helpers
     ========================================================= */
  const $  = (s, r = document) => r.querySelector(s);
  const $$ = (s, r = document) => Array.from(r.querySelectorAll(s));
  const esc = s => String(s).replace(/[&<>"']/g, c => ({ '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;' }[c]));

  /* =========================================================
     Course content
     ========================================================= */
  const MODULES = [
    {
      id: 'm1', title: 'Foundations of TaRL', color: 'var(--c1)',
      blurb: 'Why level-based teaching works.',
      lessons: [
        {
          id: 'm1l1', title: 'The learning crisis and the TaRL logic', mins: 6,
          body: `
            <p>In most classrooms children are grouped by grade and taught from a curriculum that assumes everyone is at the same point. In practice they are not: a Grade 5 class can contain children who cannot read a paragraph alongside fluent readers.</p>
            <p>Teaching at the Right Level (TaRL) starts from a different question: <strong>what can this child actually do, and what is the next step?</strong></p>
            <ul>
              <li><strong>Assess</strong> basic reading and maths directly, one child at a time.</li>
              <li><strong>Group</strong> children by the level they have reached, not by grade.</li>
              <li><strong>Teach</strong> at that level, with activities and materials designed for it.</li>
              <li><strong>Reassess</strong> every few weeks and move children up.</li>
            </ul>
            <p>The approach was developed by Pratham in India and has been adapted in Zambia, Nigeria, Côte d'Ivoire and elsewhere, with large gains in foundational skills over short periods.</p>
            <div class="callout"><p><strong>Key idea:</strong> the curriculum tells you where children <em>should</em> be; assessment tells you where they <em>are</em>. TaRL teaches from the second and works back towards the first.</p></div>`,
          check: {
            q: 'TaRL groups children primarily by…',
            opts: ['Their grade level', 'What they can currently do', 'Their age'],
            a: 1,
            why: 'Groups are formed from the level a child has reached, and re-formed as they progress.'
          }
        },
        {
          id: 'm1l2', title: 'The five principles', mins: 5,
          body: `
            <p>TaRL looks different in every school, but the same five principles hold it together.</p>
            <ol>
              <li><strong>Assess directly.</strong> A five-minute one-to-one check tells you more than a written test the child cannot read.</li>
              <li><strong>Group by level, not grade.</strong> Children from different grades can sit in the same group.</li>
              <li><strong>Match the activity to the group.</strong> A letter group needs letter cards, not a Grade 5 textbook.</li>
              <li><strong>Keep groups fluid.</strong> Reassess every four to six weeks — movement is the point.</li>
              <li><strong>Keep it positive.</strong> Children who have failed for years need quick, visible success.</li>
            </ol>
            <div class="callout"><p><strong>Key idea:</strong> grouping is a temporary teaching decision, never a label attached to a child.</p></div>`,
          check: {
            q: 'How often should groups be reassessed?',
            opts: ['Once a year', 'Every four to six weeks', 'Only when a child complains'],
            a: 1,
            why: 'Frequent reassessment is what moves children up. Without it, groups quietly become permanent labels.'
          }
        }
      ]
    },
    {
      id: 'm2', title: 'Assessment and grouping', color: 'var(--c3)',
      blurb: 'Finding out where children actually are.',
      lessons: [
        {
          id: 'm2l1', title: 'Running a baseline assessment', mins: 7,
          body: `
            <p>The assessment is short, oral and one-to-one. Sit beside the child, away from the class, and start with something they can already do.</p>
            <h4>Reading</h4>
            <ul>
              <li>Ask the child to read a short <strong>paragraph</strong>.</li>
              <li>If they cannot, move to <strong>words</strong>, then <strong>letters</strong>.</li>
              <li>Record the highest level the child manages comfortably.</li>
            </ul>
            <h4>Maths</h4>
            <ul>
              <li><strong>Two-digit subtraction with borrowing</strong> → <strong>without borrowing</strong> → <strong>one-digit operations</strong> → <strong>number recognition 1–9</strong>.</li>
            </ul>
            <p>Use the same script with every child and never correct or coach during the assessment. Record what you see, not what you hope for.</p>
            <div class="callout warn"><p><strong>Watch out:</strong> starting with the hardest task teaches children to fail. Always begin one level below where you think they are.</p></div>`,
          check: {
            q: 'Where should you start the reading assessment?',
            opts: ['With the hardest task — the paragraph', 'With the easiest task — letters', 'With a written test for the whole class'],
            a: 1,
            why: 'Starting easy gives the child confidence and lets you find their actual level without a wall of failure.'
          }
        },
        {
          id: 'm2l2', title: 'Grouping by level, not by grade', mins: 6,
          body: `
            <p>Once the assessment is done, sort the class into four to six groups. In a typical class you might find:</p>
            <div class="tw">
              <table>
                <thead><tr><th>Group</th><th>What they can do</th><th>Typical size</th></tr></thead>
                <tbody>
                  <tr><td class="rh">Story</td><td>Read a short story and answer questions</td><td>8–12</td></tr>
                  <tr><td class="rh">Paragraph</td><td>Read a paragraph, struggling with longer words</td><td>10–15</td></tr>
                  <tr><td class="rh">Word</td><td>Read familiar words, not sentences</td><td>10–15</td></tr>
                  <tr><td class="rh">Letter</td><td>Recognise some letters and sounds</td><td>8–12</td></tr>
                  <tr><td class="rh">Beginner</td><td>Not yet recognising letters or numbers</td><td>6–10</td></tr>
                </tbody>
              </table>
            </div>
            <p>Name groups after the level, not the children. "Letter group" is fine. "Weak group" is not.</p>
            <div class="callout"><p><strong>Key idea:</strong> groups of 10–15 are small enough for the teacher to work intensively with one group while the others run independent activities.</p></div>`,
          check: {
            q: 'Which group name is appropriate?',
            opts: ['Weak readers', 'Letter group', 'Slow learners'],
            a: 1,
            why: 'Naming a group after the level describes the work, not the child — and it stops being true as soon as they move up.'
          }
        }
      ]
    },
    {
      id: 'm3', title: 'Level-based instruction', color: 'var(--c4)',
      blurb: 'What a TaRL session actually looks like.',
      lessons: [
        {
          id: 'm3l1', title: 'The TaRL class period', mins: 6,
          body: `
            <p>A TaRL session is usually a single 60–90 minute block, in three parts.</p>
            <ol>
              <li><strong>Whole group (10 min).</strong> A song, a story or a quick number game — everyone together.</li>
              <li><strong>Level groups (30–40 min).</strong> The teacher works intensively with one group while the others run activities they can do without help. Then rotate.</li>
              <li><strong>Whole group (10–15 min).</strong> Review, share, and close on a success.</li>
            </ol>
            <p>Materials live in level boxes or folders so groups can start without waiting for instructions.</p>`,
          check: {
            q: 'How long should the level-group segment last?',
            opts: ['About 5 minutes', 'About 30–40 minutes', 'The whole session'],
            a: 1,
            why: 'The level-group segment is the core of the session and needs enough time for every child to read or count.'
          }
        },
        {
          id: 'm3l2', title: 'Teaching reading in level groups', mins: 7,
          body: `
            <p>Reading groups follow the same ladder as the assessment.</p>
            <ul>
              <li><strong>Beginner:</strong> letter names and sounds, oral blending, picture talk.</li>
              <li><strong>Letter:</strong> matching letters to sounds, building simple words with letter cards.</li>
              <li><strong>Word:</strong> flashcards, word bingo, reading short sentences.</li>
              <li><strong>Paragraph:</strong> paired reading aloud, repeated reading for fluency, comprehension questions.</li>
              <li><strong>Story:</strong> longer texts, prediction, retelling, writing a sentence about the story.</li>
            </ul>
            <p>Every group should read aloud, and every child should read in every session.</p>`,
          check: {
            q: 'The reading progression runs…',
            opts: ['Stories → letters → words', 'Letters → words → paragraphs → stories', 'Paragraphs → letters → words'],
            a: 1,
            why: 'Each step builds the one below it: sounds become words, words become paragraphs, paragraphs become stories.'
          }
        },
        {
          id: 'm3l3', title: 'Teaching maths in level groups', mins: 6,
          body: `
            <p>Maths groups follow the same logic: concrete first, then pictures, then symbols.</p>
            <ul>
              <li><strong>Beginner:</strong> counting objects, recognising numbers 1–9.</li>
              <li><strong>One-digit:</strong> addition and subtraction with counters and a number line.</li>
              <li><strong>Two-digit without borrowing:</strong> bundles of ten sticks, place value.</li>
              <li><strong>Two-digit with borrowing:</strong> exchange a bundle of ten, then move to the written method.</li>
            </ul>
            <p>Games — dice, card games, "number of the day", maths bingo — keep practice high-volume and low-stress.</p>`,
          check: {
            q: 'When teaching subtraction with borrowing, start with…',
            opts: ['The written algorithm on the board', 'Concrete objects and bundles of sticks', 'Homework practice'],
            a: 1,
            why: 'Children need to physically exchange a bundle of ten before the written method means anything.'
          }
        }
      ]
    },
    {
      id: 'm4', title: 'Mentoring and coaching', color: 'var(--c5)',
      blurb: 'Turning observation into changed practice.',
      lessons: [
        {
          id: 'm4l1', title: 'The observation cycle', mins: 6,
          body: `
            <p>Mentoring is a cycle, not a visit.</p>
            <ol>
              <li><strong>Before:</strong> agree one or two focus areas with the teacher.</li>
              <li><strong>During:</strong> observe 20–30 minutes with a simple tool — grouping, materials, who is reading or counting, how the teacher moves between groups.</li>
              <li><strong>After:</strong> 10–15 minutes of feedback on the same day.</li>
              <li><strong>Next visit:</strong> follow up on the same focus.</li>
            </ol>
            <div class="callout"><p><strong>Key idea:</strong> observe practice, not paperwork. The question is what children are doing, not what the lesson plan says.</p></div>`,
          check: {
            q: "A mentor's observation should focus on…",
            opts: ['Checking attendance registers', 'Classroom practice and learner engagement', "The teacher's lesson-plan format"],
            a: 1,
            why: 'The purpose is to improve what children experience in the room, not to audit documents.'
          }
        },
        {
          id: 'm4l2', title: 'Feedback that changes practice', mins: 6,
          body: `
            <p>Feedback changes practice when it is specific, limited and evidenced.</p>
            <ul>
              <li>Ask the teacher what they noticed first.</li>
              <li>Name one thing that worked, with the evidence you saw.</li>
              <li>Agree <strong>one or two</strong> priorities — not a list of ten.</li>
              <li>Model or co-teach the change rather than describing it.</li>
              <li>Write down what you agreed, and start the next visit there.</li>
            </ul>
            <p>Praise effort that is linked to learner outcomes: "you gave the letter group four turns each" beats "great lesson".</p>`,
          check: {
            q: 'Effective feedback is…',
            opts: ['Broad and general', 'Specific, evidence-based, limited to 1–2 priorities', 'Delivered publicly in front of the class'],
            a: 1,
            why: 'A short list of concrete, agreed changes is far more likely to be acted on than a long general critique.'
          }
        }
      ]
    },
    {
      id: 'm5', title: 'Monitoring and sustaining', color: 'var(--c2)',
      blurb: 'Showing it works — and making it last.',
      lessons: [
        {
          id: 'm5l1', title: 'Tracking progress and reporting', mins: 6,
          body: `
            <p>TaRL is judged by movement between levels, not by attendance or materials.</p>
            <ul>
              <li>Reassess every four to six weeks with the same tool.</li>
              <li>Record how many children moved up, stayed, or moved down.</li>
              <li>Report by group: "12 of 18 children in the letter group now read words."</li>
              <li>Share results with school leadership and parents.</li>
            </ul>
            <p>Sustaining the approach needs the timetable, the materials and the mentoring to survive staff changes. Build the routine into the school year, not into a single project.</p>`,
          check: {
            q: 'The clearest sign that TaRL is working is…',
            opts: ['More materials in the cupboard', 'Children moving to higher level groups over time', 'Longer lessons'],
            a: 1,
            why: 'Level movement on repeated assessment is the outcome TaRL exists to produce.'
          }
        }
      ]
    }
  ];

  const LESSONS = MODULES.flatMap(m => m.lessons.map(l => Object.assign({}, l, { module: m })));
  const BY_ID = Object.fromEntries(LESSONS.map(l => [l.id, l]));
  const TOTAL = LESSONS.length;

  /* =========================================================
     State
     ========================================================= */
  const STORE_KEY = 'tarl-mentor-academy-v3';
  const ADMIN_SESSION_KEY = 'tarl-admin-unlocked';
  /* Demo gate only: a static page cannot keep a secret. Replace with real
     server-side authentication before storing anything sensitive. */
  const ADMIN_PIN = atob('NTQwMjU0MDI=');

  const DEFAULTS = { students: [], current: null, progress: {}, theme: 'system' };

  let S = (function load() {
    try {
      const raw = localStorage.getItem(STORE_KEY);
      const p = raw ? JSON.parse(raw) : null;
      if (!p || typeof p !== 'object') return Object.assign({}, DEFAULTS);
      return {
        students: Array.isArray(p.students) ? p.students.filter(s => s && typeof s.key === 'string') : [],
        current: typeof p.current === 'string' ? p.current : null,
        progress: (p.progress && typeof p.progress === 'object' && !Array.isArray(p.progress)) ? p.progress : {},
        theme: ['system', 'light', 'dark'].indexOf(p.theme) > -1 ? p.theme : 'system'
      };
    } catch (e) {
      return Object.assign({}, DEFAULTS);
    }
  })();

  function save() {
    try {
      localStorage.setItem(STORE_KEY, JSON.stringify(S));
    } catch (e) {
      toast('Could not save — storage may be full or blocked in this browser.', 'bad');
    }
  }

  if (S.current && !S.students.some(s => s.key === S.current)) S.current = null;

  const keyOf = contact => contact.trim().toLowerCase();
  const currentStudent = () => S.students.find(s => s.key === S.current) || null;

  function getProg() {
    return S.current ? (S.progress[S.current] || null) : null;
  }
  function ensureProg() {
    if (!S.current) return null;
    if (!S.progress[S.current]) S.progress[S.current] = { done: {}, notes: {}, scores: {}, certifiedAt: null };
    return S.progress[S.current];
  }
  function isDone(id) {
    const p = getProg();
    return !!(p && p.done[id]);
  }
  function doneCount() {
    const p = getProg();
    return p ? LESSONS.filter(l => p.done[l.id]).length : 0;
  }
  function pct() {
    return Math.round((doneCount() / TOTAL) * 100);
  }
  function nextLesson() {
    return LESSONS.find(l => !isDone(l.id)) || LESSONS[0];
  }

  /* =========================================================
     Toasts
     ========================================================= */
  function toast(msg, kind) {
    const wrap = $('#toasts');
    if (!wrap) return;
    const el = document.createElement('div');
    el.className = 'toast' + (kind ? ' ' + kind : '');
    el.setAttribute('role', 'status');
    el.textContent = msg;
    wrap.appendChild(el);
    setTimeout(() => {
      el.style.opacity = '0';
      setTimeout(() => el.remove(), 320);
    }, 4200);
  }

  /* =========================================================
     Routing
     ========================================================= */
  function parseRoute() {
    const raw = location.hash.replace(/^#\/?/, '');
    const parts = raw.split('/');
    return { seg: parts[0] || 'home', id: parts.slice(1).join('/') };
  }
  function go(path) {
    const target = '#/' + path;
    if (location.hash === target) render();
    else location.hash = target;
  }

  const VIEWS = {
    home: renderHome,
    register: renderRegister,
    admin: renderAdmin,
    lesson: renderLesson,
    certificate: renderCertificate
  };

  function render(focusMain) {
    const r = parseRoute();
    const view = VIEWS[r.seg] || renderHome;
    const main = $('#main');
    main.innerHTML = view(r.id);
    setMenu(false);
    updateNav(r.seg, r.id);
    updateProgress();
    if (focusMain) {
      main.focus({ preventScroll: true });
      window.scrollTo(0, 0);
    }
  }

  /* =========================================================
     Navigation
     ========================================================= */
  function buildNav() {
    $('#side').innerHTML = `
      <div class="navtop">
        <a class="li" data-route="home" href="#/home">Overview</a>
        <a class="li" data-route="register" href="#/register">Registration</a>
        <a class="li" data-route="certificate" href="#/certificate">Certificate</a>
        <a class="li" data-route="admin" href="#/admin">Admin portal</a>
      </div>
      <p class="navh">Modules</p>
      ${MODULES.map(m => `
        <details open>
          <summary>
            <span class="sw" style="background:${m.color}"></span>
            <span class="ttl">${esc(m.title)}</span>
            <span class="cnt" data-count="${m.id}">0/${m.lessons.length}</span>
          </summary>
          ${m.lessons.map(l => `
            <a class="li" href="#/lesson/${l.id}" data-lesson-link="${l.id}">
              <span class="ck" aria-hidden="true">✓</span>
              <span>${esc(l.title)}</span>
            </a>`).join('')}
        </details>`).join('')}
    `;
  }

  function updateNav(seg, id) {
    $$('#side a.li').forEach(a => a.removeAttribute('aria-current'));
    const active = seg === 'lesson'
      ? $('#side [data-lesson-link="' + CSS.escape(id) + '"]')
      : $('#side [data-route="' + CSS.escape(seg) + '"]');
    if (active) active.setAttribute('aria-current', 'page');

    const p = getProg();
    LESSONS.forEach(l => {
      const mark = $('#side [data-lesson-link="' + CSS.escape(l.id) + '"] .ck');
      if (mark) mark.classList.toggle('on', !!(p && p.done[l.id]));
    });
    MODULES.forEach(m => {
      const el = $('[data-count="' + m.id + '"]');
      if (el) el.textContent = (p ? m.lessons.filter(l => p.done[l.id]).length : 0) + '/' + m.lessons.length;
    });
  }

  function updateProgress() {
    const p = pct();
    const fill = $('#pfill');
    const bar = $('#pbar');
    if (fill) fill.style.width = p + '%';
    const label = $('#pct');
    if (label) label.textContent = p + '%';
    if (bar) {
      bar.setAttribute('aria-valuenow', String(p));
      bar.setAttribute('aria-valuetext', doneCount() + ' of ' + TOTAL + ' lessons complete');
    }
  }

  function setMenu(open) {
    document.body.classList.toggle('menu', open);
    const btn = $('#menuBtn');
    if (btn) btn.setAttribute('aria-expanded', String(open));
  }

  /* =========================================================
     Views
     ========================================================= */
  function renderHome() {
    const student = currentStudent();
    const d = doneCount();
    return `
      <div class="crumb">Professional development</div>
      <h1>Teaching at the Right Level — Mentor Academy</h1>
      <p class="lead">A self-paced course for teachers, mentors and school leaders on accelerating foundational literacy and numeracy: assess where children are, group by level, teach at that level, and coach the practice.</p>

      <div class="cta">
        ${student
          ? `<a class="btn" href="#/lesson/${nextLesson().id}">${d ? 'Continue' : 'Start'} the course</a>
             <a class="btn ghost" href="#/register">Your profile</a>`
          : `<a class="btn" href="#/register">Register to start</a>
             <a class="btn ghost" href="#/lesson/${LESSONS[0].id}">Browse a lesson</a>`}
      </div>

      ${student ? `
        <div class="callout">
          <p><strong>${esc(student.name)}</strong> · ${d} of ${TOTAL} lessons complete · ${pct()}%${pct() === 100 ? ' · <a href="#/certificate">certificate ready</a>' : ''}</p>
        </div>` : ''}

      <h3>What you'll cover</h3>
      <div class="cards">
        ${MODULES.map(m => `
          <a class="card" href="#/lesson/${m.lessons[0].id}">
            <span class="sw" style="background:${m.color}"></span>
            <strong>${esc(m.title)}</strong>
            <span class="muted">${m.lessons.length} lesson${m.lessons.length > 1 ? 's' : ''} · ${esc(m.blurb)}</span>
          </a>`).join('')}
      </div>

      <h3>How the course works</h3>
      <ul>
        <li><strong>${TOTAL} short lessons</strong> across ${MODULES.length} modules, each with a quick check.</li>
        <li><strong>Notes</strong> you write are saved on this device, per lesson.</li>
        <li><strong>Progress</strong> is tracked against your registration, so you can pick up where you left off.</li>
        <li>Finish everything to unlock a <strong>certificate</strong> you can print or save as PDF.</li>
      </ul>`;
  }

  function renderRegister() {
    const student = currentStudent();
    return `
      <h1>Registration</h1>
      <p class="muted">Register once to track your module progression and unlock your certificate. Your details are stored only in this browser.</p>

      ${student ? `
        <div class="widget">
          <h4>Currently signed in</h4>
          <p><strong>${esc(student.name)}</strong><br>
            <span class="muted">${esc(student.school)} · ${esc(student.role)} · ${esc(student.contact)}</span></p>
          <p class="muted">${doneCount()} of ${TOTAL} lessons complete (${pct()}%).</p>
          <div class="cta" style="margin-bottom:0">
            <a class="btn" href="#/lesson/${nextLesson().id}">Continue course</a>
            <button class="btn ghost" type="button" data-action="logout">Sign out</button>
          </div>
        </div>
        <h3>Register another participant</h3>
      ` : ''}

      <div class="widget">
        <form data-form="register" novalidate>
          <label for="fullname">Full name</label>
          <input id="fullname" name="fullname" type="text" autocomplete="name" maxlength="60" required placeholder="e.g. Mohammed Tura">

          <label for="school">School, cluster or organisation</label>
          <input id="school" name="school" type="text" autocomplete="organization" maxlength="100" required placeholder="e.g. Addis Ababa Primary Education">

          <label for="role">Role / grades taught</label>
          <input id="role" name="role" type="text" maxlength="60" required placeholder="e.g. Grade 3–4 teacher / mentor">

          <label for="contact">Email or phone</label>
          <input id="contact" name="contact" type="text" autocomplete="email" maxlength="80" required placeholder="e.g. name@example.org or +251 91 234 5678">
          <p class="hint">Used as your participant ID — registering again with the same contact resumes your progress.</p>

          <button class="btn" type="submit">Save registration</button>
        </form>
      </div>`;
  }

  function renderLesson(id) {
    const l = BY_ID[id];
    if (!l) return notFound();

    const student = currentStudent();
    const done = isDone(id);
    const idx = LESSONS.indexOf(l);
    const prev = LESSONS[idx - 1];
    const next = LESSONS[idx + 1];
    const p = getProg();
    const note = (p && p.notes[id]) || '';

    const quiz = l.check ? `
      <form class="quiz widget" data-form="quiz" data-lesson="${l.id}" novalidate>
        <h4>Quick check</h4>
        <fieldset>
          <legend>${esc(l.check.q)}</legend>
          ${l.check.opts.map((o, i) => `
            <label class="opt">
              <input type="radio" name="answer" value="${i}">
              <span>${esc(o)}</span>
            </label>`).join('')}
        </fieldset>
        <button class="btn sm" type="submit">Check answer</button>
        <p class="fb" role="status"></p>
      </form>` : '';

    return `
      <div class="crumb"><span class="sw" style="background:${l.module.color};margin-top:0"></span>${esc(l.module.title)}</div>
      <h1>${esc(l.title)}</h1>
      <p class="meta">Lesson ${idx + 1} of ${TOTAL} · about ${l.mins} minutes${done ? ' · <strong>completed</strong>' : ''}</p>

      ${student ? '' : `
        <div class="callout warn">
          <p>You are reading as a guest. <a href="#/register">Register</a> to save progress, notes and your certificate.</p>
        </div>`}

      ${l.body}

      ${quiz}

      <div class="widget">
        <h4>Your notes</h4>
        <label class="sr-only" for="note-${l.id}">Notes for this lesson</label>
        <textarea id="note-${l.id}" data-note="${l.id}" rows="4"
          placeholder="What will you try in your classroom?"
          ${student ? '' : 'disabled'}>${esc(note)}</textarea>
        <p class="hint">${student ? 'Saved automatically on this device.' : 'Register to save notes.'}</p>
      </div>

      <div class="lesson-nav">
        ${prev ? `<a class="btn ghost sm" href="#/lesson/${prev.id}" title="${esc(prev.title)}">← ${esc(prev.title)}</a>` : '<span></span>'}
        <button class="btn${done ? ' ghost' : ''}" type="button"
          data-action="toggle-complete" data-id="${l.id}" data-on="${done ? '0' : '1'}">
          ${done ? 'Mark as not complete' : 'Mark complete'}
        </button>
        ${next ? `<a class="btn ghost sm" href="#/lesson/${next.id}" title="${esc(next.title)}">${esc(next.title)} →</a>` : '<span></span>'}
      </div>`;
  }

  function renderCertificate() {
    const student = currentStudent();
    const p = getProg();

    if (!student) {
      return `
        <h1>Certificate</h1>
        <p>Register and complete all ${TOTAL} lessons to unlock your certificate.</p>
        <a class="btn" href="#/register">Register</a>`;
    }
    if (pct() < 100) {
      return `
        <h1>Certificate</h1>
        <div class="callout">
          <p><strong>${esc(student.name)}</strong> — you have completed ${doneCount()} of ${TOTAL} lessons (${pct()}%).</p>
          <p>Finish the remaining ${TOTAL - doneCount()} to unlock your certificate.</p>
        </div>
        <a class="btn" href="#/lesson/${nextLesson().id}">Continue the course</a>`;
    }
    const when = p && p.certifiedAt ? new Date(p.certifiedAt) : new Date();
    return `
      <h1>Certificate</h1>
      <div class="cert" id="cert">
        <p class="crumb" style="justify-content:center">TaRL Mentor Academy</p>
        <h2>Certificate of Completion</h2>
        <p>This certifies that</p>
        <p class="nm">${esc(student.name)}</p>
        <p>has completed all ${TOTAL} lessons of the TaRL Mentor Academy course.</p>
        <p class="muted">${esc(student.school)} · ${esc(student.role)}</p>
        <p class="muted">${when.toLocaleDateString(undefined, { year: 'numeric', month: 'long', day: 'numeric' })}</p>
      </div>
      <p class="no-print"><button class="btn" type="button" data-action="print">Print / save as PDF</button></p>`;
  }

  function renderAdmin() {
    if (sessionStorage.getItem(ADMIN_SESSION_KEY) !== '1') {
      return `
        <h1>Admin portal</h1>
        <p>Enter the administrator code to view participant records.</p>
        <div class="widget">
          <form data-form="admin" novalidate>
            <label for="pin">Administrator code</label>
            <input id="pin" name="pin" type="password" inputmode="numeric" autocomplete="off" required>
            <p class="err" id="admin-err" role="status"></p>
            <button class="btn" type="submit">Unlock</button>
            <p class="hint">This is a demo gate on a static page — the code is not real security, and data is stored unencrypted in this browser. Do not use it for confidential records.</p>
          </form>
        </div>`;
    }

    const rows = S.students.length === 0
      ? '<tr><td colspan="7" class="muted">No registered participants yet.</td></tr>'
      : S.students.map(st => {
          const pr = S.progress[st.key];
          const d = pr ? LESSONS.filter(l => pr.done[l.id]).length : 0;
          const pc = Math.round((d / TOTAL) * 100);
          return `<tr>
            <td class="rh">${esc(st.name)}${st.key === S.current ? ' <span class="chip">active</span>' : ''}</td>
            <td>${esc(st.school)}</td>
            <td>${esc(st.role)}</td>
            <td>${esc(st.contact)}</td>
            <td>${esc(st.date)}</td>
            <td>${d}/${TOTAL} <span class="muted">(${pc}%)</span></td>
            <td><button class="btn ghost sm" type="button" data-action="delete-student" data-id="${esc(st.key)}">Delete</button></td>
          </tr>`;
        }).join('');

    return `
      <h1>Admin dashboard</h1>
      <p class="muted">${S.students.length} participant${S.students.length === 1 ? '' : 's'} registered on this device.</p>

      <div class="cta">
        <button class="btn ghost sm" type="button" data-action="export-csv">Export CSV</button>
        <button class="btn ghost sm" type="button" data-action="export-json">Export JSON</button>
        <button class="btn ghost sm" type="button" data-action="lock-admin">Lock portal</button>
        <button class="btn ghost sm" type="button" data-action="reset-all">Reset all data</button>
      </div>

      <div class="tw">
        <table>
          <thead>
            <tr><th>Name</th><th>School / organisation</th><th>Role</th><th>Contact</th><th>Registered</th><th>Progress</th><th><span class="sr-only">Actions</span></th></tr>
          </thead>
          <tbody>${rows}</tbody>
        </table>
      </div>`;
  }

  function notFound() {
    return `
      <h1>Lesson not found</h1>
      <p>That lesson does not exist.</p>
      <a class="btn" href="#/home">Back to the course</a>`;
  }

  /* =========================================================
     Actions
     ========================================================= */
  let adminFails = 0;
  let adminLockedUntil = 0;

  function handleRegister(form) {
    const f = form.elements;
    const data = {
      name: f.fullname.value.trim().replace(/\s+/g, ' '),
      school: f.school.value.trim().replace(/\s+/g, ' '),
      role: f.role.value.trim().replace(/\s+/g, ' '),
      contact: f.contact.value.trim()
    };

    const errors = {};
    if (data.name.length < 2 || data.name.length > 60) errors.fullname = 'Enter your full name (2–60 characters).';
    if (data.school.length < 2 || data.school.length > 100) errors.school = 'Enter your school, cluster or organisation.';
    if (data.role.length < 2 || data.role.length > 60) errors.role = 'Enter your role or the grades you teach.';

    const isEmail = /^[^@\s]+@[^@\s]+\.[^@\s]{2,}$/.test(data.contact);
    const isPhone = /^\+?[\d\s()-]{7,16}$/.test(data.contact);
    if (!isEmail && !isPhone) errors.contact = 'Enter a valid email address or phone number.';

    if (!showErrors(form, errors)) {
      toast('Please check the highlighted fields.', 'bad');
      return;
    }

    const key = keyOf(data.contact);
    const existing = S.students.find(s => s.key === key);

    if (existing) {
      existing.name = data.name;
      existing.school = data.school;
      existing.role = data.role;
      S.current = key;
      save();
      toast('Welcome back, ' + data.name.split(' ')[0] + ' — your progress has been restored.', 'ok');
    } else {
      S.students.push({
        key: key,
        name: data.name,
        school: data.school,
        role: data.role,
        contact: data.contact,
        date: new Date().toLocaleDateString()
      });
      S.current = key;
      save();
      toast('Registered. Welcome, ' + data.name.split(' ')[0] + '!', 'ok');
    }
    go('home');
  }

  function showErrors(form, errors) {
    $$('.err', form).forEach(el => el.remove());
    $$('[aria-invalid]', form).forEach(el => {
      el.removeAttribute('aria-invalid');
      el.removeAttribute('aria-describedby');
    });

    const keys = Object.keys(errors);
    if (keys.length === 0) return true;

    let first = null;
    keys.forEach(k => {
      const field = form.elements[k];
      if (!field) return;
      const p = document.createElement('p');
      p.className = 'err';
      p.id = 'err-' + k;
      p.textContent = errors[k];
      field.setAttribute('aria-invalid', 'true');
      field.setAttribute('aria-describedby', p.id);
      field.insertAdjacentElement('afterend', p);
      if (!first) first = field;
    });
    if (first) first.focus();
    return false;
  }

  function handleAdmin(form) {
    const errEl = $('#admin-err');
    const now = Date.now();

    if (now < adminLockedUntil) {
      const secs = Math.ceil((adminLockedUntil - now) / 1000);
      errEl.textContent = 'Too many attempts. Try again in ' + secs + ' seconds.';
      return;
    }
    const pin = form.elements.pin.value.trim();

    if (pin === ADMIN_PIN) {
      sessionStorage.setItem(ADMIN_SESSION_KEY, '1');
      adminFails = 0;
      render();
      toast('Admin portal unlocked.', 'ok');
      return;
    }

    adminFails += 1;
    form.elements.pin.value = '';
    if (adminFails >= 5) {
      adminFails = 0;
      adminLockedUntil = Date.now() + 60000;
      errEl.textContent = 'Too many attempts. Locked for 60 seconds.';
    } else {
      errEl.textContent = 'Incorrect code. ' + (5 - adminFails) + ' attempt(s) remaining.';
    }
    form.elements.pin.focus();
  }

  function handleQuiz(form) {
    const l = BY_ID[form.dataset.lesson];
    if (!l || !l.check) return;
    const picked = form.querySelector('input[name="answer"]:checked');
    const fb = $('.fb', form);

    if (!picked) {
      fb.className = 'fb bad';
      fb.textContent = 'Choose an answer first.';
      return;
    }
    const correct = Number(picked.value) === l.check.a;
    const p = ensureProg();
    if (p) {
      p.scores[l.id] = correct ? 1 : 0;
      save();
    }
    fb.className = 'fb ' + (correct ? 'ok' : 'bad');
    fb.textContent = (correct ? 'Correct. ' : 'Not quite. ') + l.check.why;
  }

  function toggleComplete(id, on) {
    if (!S.current) {
      toast('Register first to save your progress.', 'bad');
      go('register');
      return;
    }
    const p = ensureProg();
    if (on) p.done[id] = true;
    else delete p.done[id];

    p.certifiedAt = doneCount() === TOTAL ? (p.certifiedAt || new Date().toISOString()) : null;
    save();

    const btn = $('[data-action="toggle-complete"]');
    if (btn && btn.dataset.id === id) {
      btn.dataset.on = on ? '0' : '1';
      btn.textContent = on ? 'Mark as not complete' : 'Mark complete';
      btn.classList.toggle('ghost', on);
    }
    updateProgress();
    updateNav('lesson', id);
    toast(on ? 'Lesson marked complete.' : 'Lesson marked as not complete.', on ? 'ok' : '');
  }

  function deleteStudent(key) {
    const st = S.students.find(s => s.key === key);
    if (!st) return;
    if (!window.confirm('Delete ' + st.name + ' and all of their progress? This cannot be undone.')) return;
    S.students = S.students.filter(s => s.key !== key);
    delete S.progress[key];
    if (S.current === key) S.current = null;
    save();
    render();
    toast('Participant deleted.');
  }

  function resetAll() {
    if (!window.confirm('Delete all participants, progress and settings stored on this device?')) return;
    try { localStorage.removeItem(STORE_KEY); } catch (e) {}
    sessionStorage.removeItem(ADMIN_SESSION_KEY);
    location.reload();
  }

  function download(filename, mime, text) {
    const blob = new Blob([text], { type: mime });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    a.remove();
    setTimeout(() => URL.revokeObjectURL(url), 1500);
  }

  function exportCSV() {
    const rows = [['Name', 'School', 'Role', 'Contact', 'Registered', 'Lessons complete', 'Percent']];
    S.students.forEach(st => {
      const pr = S.progress[st.key];
      const d = pr ? LESSONS.filter(l => pr.done[l.id]).length : 0;
      rows.push([st.name, st.school, st.role, st.contact, st.date, String(d), String(Math.round((d / TOTAL) * 100))]);
    });
    const csv = rows.map(r => r.map(c => '"' + String(c).replace(/"/g, '""') + '"').join(',')).join('\r\n');
    download('tarl-participants.csv', 'text/csv;charset=utf-8', '\uFEFF' + csv);
    toast('CSV exported.', 'ok');
  }

  function exportJSON() {
    const payload = {
      exported: new Date().toISOString(),
      totalLessons: TOTAL,
      participants: S.students.map(st => {
        const pr = S.progress[st.key] || {};
        return {
          name: st.name, school: st.school, role: st.role,
          contact: st.contact, registered: st.date,
          completedLessons: Object.keys(pr.done || {}),
          scores: pr.scores || {}
        };
      })
    };
    download('tarl-participants.json', 'application/json', JSON.stringify(payload, null, 2));
    toast('JSON exported.', 'ok');
  }

  /* =========================================================
     Theme
     ========================================================= */
  function applyTheme() {
    const t = S.theme;
    if (t === 'system') document.documentElement.removeAttribute('data-theme');
    else document.documentElement.setAttribute('data-theme', t);

    const btn = $('#themeBtn');
    if (btn) {
      btn.textContent = t === 'light' ? '☀' : t === 'dark' ? '☾' : '◐';
      btn.setAttribute('aria-label', 'Colour theme: ' + t + '. Activate to change.');
      btn.title = 'Colour theme: ' + t;
    }
  }

  /* =========================================================
     Event delegation
     ========================================================= */
  document.addEventListener('click', e => {
    const btn = e.target.closest('[data-action]');
    if (!btn) return;

    switch (btn.dataset.action) {
      case 'menu':
        setMenu(!document.body.classList.contains('menu'));
        break;
      case 'theme':
        S.theme = S.theme === 'system' ? 'light' : S.theme === 'light' ? 'dark' : 'system';
        save();
        applyTheme();
        break;
      case 'toggle-complete':
        toggleComplete(btn.dataset.id, btn.dataset.on === '1');
        break;
      case 'print':
        window.print();
        break;
      case 'logout':
        S.current = null;
        save();
        render();
        toast('Signed out. Your progress is saved.');
        break;
      case 'lock-admin':
        sessionStorage.removeItem(ADMIN_SESSION_KEY);
        render();
        toast('Admin portal locked.');
        break;
      case 'delete-student':
        deleteStudent(btn.dataset.id);
        break;
      case 'export-csv':
        exportCSV();
        break;
      case 'export-json':
        exportJSON();
        break;
      case 'reset-all':
        resetAll();
        break;
    }
  });

  document.addEventListener('submit', e => {
    const form = e.target;
    const kind = form.dataset.form;
    if (!kind) return;
    e.preventDefault();
    if (kind === 'register') handleRegister(form);
    else if (kind === 'admin') handleAdmin(form);
    else if (kind === 'quiz') handleQuiz(form);
  });

  /* Debounced note autosave */
  let noteTimer = null;
  document.addEventListener('input', e => {
    const ta = e.target.closest('[data-note]');
    if (!ta) return;
    clearTimeout(noteTimer);
    const id = ta.dataset.note;
    const value = ta.value.slice(0, 4000);
    noteTimer = setTimeout(() => {
      const p = ensureProg();
      if (!p) return;
      p.notes[id] = value;
      save();
    }, 500);
  });

  /* Keyboard: Escape closes the mobile menu */
  document.addEventListener('keydown', e => {
    if (e.key === 'Escape' && document.body.classList.contains('menu')) {
      setMenu(false);
      const btn = $('#menuBtn');
      if (btn) btn.focus();
    }
  });

  window.addEventListener('hashchange', () => render(true));

  /* =========================================================
     Boot
     ========================================================= */
  buildNav();
  applyTheme();
  render();
})();
</script>
</body>
</html>
