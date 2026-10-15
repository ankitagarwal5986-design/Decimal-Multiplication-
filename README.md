<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Complete Multiplying Decimals Quiz (All 140 Questions)</title>
  <style>
    :root {
      --primary: #2563eb;
      --bg: #f8fafc;
      --card: #ffffff;
      --border: #e2e8f0;
      --text: #1e293b;
    }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      background: var(--bg);
      color: var(--text);
      margin: 0;
      padding: 20px;
    }
    .container {
      max-width: 950px;
      margin: auto;
      background: var(--card);
      padding: 28px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.06);
    }
    h1 {
      text-align: center;
      margin-top: 0;
      color: #0f172a;
    }
    .subtitle {
      text-align: center;
      color: #64748b;
      margin-bottom: 24px;
    }
    .nav-tabs {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 24px;
      border-bottom: 2px solid var(--border);
      padding-bottom: 12px;
    }
    .tab-btn {
      padding: 8px 14px;
      border: 1px solid var(--border);
      background: #f1f5f9;
      border-radius: 6px;
      cursor: pointer;
      font-weight: 600;
      font-size: 0.85rem;
      color: #475569;
      transition: all 0.15s;
    }
    .tab-btn.active, .tab-btn:hover {
      background: var(--primary);
      color: #fff;
      border-color: var(--primary);
    }
    .section-block {
      margin-bottom: 36px;
    }
    .section-header {
      background: #1e293b;
      color: #fff;
      padding: 12px 18px;
      border-radius: 8px;
      margin-bottom: 16px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .section-header h2 {
      margin: 0;
      font-size: 1.15rem;
    }
    .questions-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
      gap: 16px;
    }
    .apply-grid {
      grid-template-columns: 1fr;
    }
    .q-card {
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 16px;
      background: #fcfcfd;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .badge {
      display: inline-block;
      font-size: 0.7rem;
      font-weight: 700;
      text-transform: uppercase;
      padding: 2px 7px;
      border-radius: 4px;
      margin-bottom: 8px;
      width: fit-content;
    }
    .badge-mcq { background: #dbeafe; color: #1e40af; }
    .badge-fib { background: #f3e8ff; color: #6b21a8; }
    .q-prompt {
      font-weight: 600;
      font-size: 1rem;
      margin-bottom: 12px;
      line-height: 1.4;
    }
    .mcq-list label {
      display: block;
      padding: 7px 10px;
      margin: 5px 0;
      border: 1px solid #cbd5e1;
      border-radius: 6px;
      background: #fff;
      cursor: pointer;
      font-size: 0.92rem;
    }
    .mcq-list label:hover {
      background: #f1f5f9;
    }
    .fib-wrap {
      display: flex;
      align-items: center;
      gap: 6px;
      margin-top: 8px;
    }
    .fib-input {
      padding: 8px 10px;
      border: 1px solid #94a3b8;
      border-radius: 6px;
      font-size: 0.95rem;
      width: 140px;
    }
    .feedback {
      margin-top: 10px;
      font-size: 0.85rem;
      font-weight: 600;
      min-height: 1.2em;
    }
    .correct { color: #15803d; }
    .incorrect { color: #b91c1c; }
    .controls {
      position: sticky;
      bottom: 16px;
      background: rgba(255,255,255,0.95);
      backdrop-filter: blur(4px);
      padding: 14px 20px;
      border: 1px solid var(--border);
      border-radius: 10px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.1);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
      margin-top: 24px;
    }
    .btn {
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    .btn-primary {
      background: var(--primary);
      color: #fff;
    }
    .btn-primary:hover {
      background: #1d4ed8;
    }
    .btn-secondary {
      background: #e2e8f0;
      color: #334155;
    }
    #scoreDisplay {
      font-weight: 700;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>Complete Multiplying Decimals Quiz</h1>
  <p class="subtitle">All 140 Questions Mapped Across Every Worksheet Section • Alternating MCQ & Fill in the Blank</p>

  <div class="nav-tabs" id="navTabs">
    <button class="tab-btn active" onclick="filterSection('all', this)">Show All (140)</button>
  </div>

  <form id="quizForm">
    <div id="quizRoot"></div>

    <div class="controls">
      <div id="scoreDisplay">Ready to check your answers!</div>
      <div>
        <button type="button" class="btn btn-secondary" onclick="resetQuiz()">Reset</button>
        <button type="button" class="btn btn-primary" onclick="gradeQuiz()">Submit & Grade All</button>
      </div>
    </div>
  </form>
</div>

<script>
const quizSections = [
  {
    id: "sec-ws1",
    title: "Part 1: Decimals Worksheet",
    isWordProblem: false,
    items: [
      { label: "1a", q: "2.87 × 60.3", a: "173.061" },
      { label: "1b", q: "96 × 5.81", a: "557.76" },
      { label: "2a", q: "0.8 × 16.1", a: "12.88" },
      { label: "2b", q: "53.196 × 5.16", a: "274.4914" },
      { label: "3a", q: "3.8 × 49.4", a: "187.72" },
      { label: "3b", q: "30.1 × 4.485", a: "134.9985" }
    ]
  },
  {
    id: "sec-w1",
    title: "Part 2: Workout — Question 1",
    isWordProblem: false,
    items: [
      { label: "1(a)", q: "1.2 × 4", a: "4.8" },
      { label: "1(b)", q: "3.2 × 3", a: "9.6" },
      { label: "1(c)", q: "5.3 × 2", a: "10.6" },
      { label: "1(d)", q: "7.3 × 3", a: "21.9" },
      { label: "1(e)", q: "1.6 × 4", a: "6.4" },
      { label: "1(f)", q: "2.9 × 5", a: "14.5" },
      { label: "1(g)", q: "4.2 × 6", a: "25.2" },
      { label: "1(h)", q: "9.5 × 7", a: "66.5" },
      { label: "1(i)", q: "6.7 × 8", a: "53.6" },
      { label: "1(j)", q: "3.8 × 9", a: "34.2" },
      { label: "1(k)", q: "12.8 × 3", a: "38.4" },
      { label: "1(l)", q: "24.3 × 4", a: "97.2" },
      { label: "1(m)", q: "37.5 × 6", a: "225" },
      { label: "1(n)", q: "52.8 × 7", a: "369.6" },
      { label: "1(o)", q: "173.2 × 3", a: "519.6" },
      { label: "1(p)", q: "215.8 × 6", a: "1294.8" },
      { label: "1(q)", q: "1243.7 × 9", a: "11193.3" },
      { label: "1(r)", q: "79.5 × 8", a: "636" }
    ]
  },
  {
    id: "sec-w2",
    title: "Part 3: Workout — Question 2",
    isWordProblem: false,
    items: [
      { label: "2(a)", q: "1.26 × 2", a: "2.52" },
      { label: "2(b)", q: "2.63 × 3", a: "7.89" },
      { label: "2(c)", q: "5.14 × 3", a: "15.42" },
      { label: "2(d)", q: "6.28 × 4", a: "25.12" },
      { label: "2(e)", q: "7.53 × 5", a: "37.65" },
      { label: "2(f)", q: "0.38 × 8", a: "3.04" },
      { label: "2(g)", q: "9.62 × 6", a: "57.72" },
      { label: "2(h)", q: "12.38 × 7", a: "86.66" },
      { label: "2(i)", q: "16.42 × 9", a: "147.78" },
      { label: "2(j)", q: "109.34 × 4", a: "437.36" },
      { label: "2(k)", q: "9.08 × 3", a: "27.24" },
      { label: "2(l)", q: "12.04 × 7", a: "84.28" },
      { label: "2(m)", q: "0.383 × 3", a: "1.149" },
      { label: "2(n)", q: "1.442 × 6", a: "8.652" },
      { label: "2(o)", q: "8.291 × 3", a: "24.873" },
      { label: "2(p)", q: "9.623 × 5", a: "48.115" },
      { label: "2(q)", q: "3.706 × 8", a: "29.648" },
      { label: "2(r)", q: "4.953 × 7", a: "34.671" },
      { label: "2(s)", q: "0.482 × 8", a: "3.856" },
      { label: "2(t)", q: "0.085 × 7", a: "0.595" },
      { label: "2(u)", q: "1.3842 × 3", a: "4.1526" },
      { label: "2(v)", q: "4.3342 × 6", a: "26.0052" },
      { label: "2(w)", q: "8.2039 × 5", a: "41.0195" },
      { label: "2(x)", q: "7.3112 × 9", a: "65.8008" },
      { label: "2(y)", q: "512.83 × 6", a: "3076.98" },
      { label: "2(z)", q: "293.421 × 4", a: "1173.684" }
    ]
  },
  {
    id: "sec-w3",
    title: "Part 4: Workout — Question 3",
    isWordProblem: false,
    items: [
      { label: "3(a)", q: "1.24 × 13", a: "16.12" },
      { label: "3(b)", q: "2.51 × 17", a: "42.67" },
      { label: "3(c)", q: "12.5 × 23", a: "287.5" },
      { label: "3(d)", q: "3.28 × 21", a: "68.88" },
      { label: "3(e)", q: "6.35 × 35", a: "222.25" },
      { label: "3(f)", q: "7.65 × 37", a: "283.05" },
      { label: "3(g)", q: "58.2 × 46", a: "2677.2" },
      { label: "3(h)", q: "4.23 × 52", a: "219.96" },
      { label: "3(i)", q: "0.28 × 57", a: "15.96" },
      { label: "3(j)", q: "0.817 × 63", a: "51.471" },
      { label: "3(k)", q: "38.43 × 19", a: "730.17" },
      { label: "3(l)", q: "5.45 × 87", a: "474.15" },
      { label: "3(m)", q: "12.32 × 73", a: "899.36" },
      { label: "3(n)", q: "2.3 × 123", a: "282.9" },
      { label: "3(o)", q: "4.7 × 253", a: "1189.1" },
      { label: "3(p)", q: "8.6 × 351", a: "3018.6" },
      { label: "3(q)", q: "2.03 × 152", a: "308.56" },
      { label: "3(r)", q: "1.02 × 607", a: "619.14" }
    ]
  },
  {
    id: "sec-w4",
    title: "Part 5: Workout — Question 4",
    isWordProblem: false,
    items: [
      { label: "4(a)", q: "0.2 × 0.3", a: "0.06" },
      { label: "4(b)", q: "0.7 × 0.2", a: "0.14" },
      { label: "4(c)", q: "0.9 × 0.4", a: "0.36" },
      { label: "4(d)", q: "0.8 × 0.6", a: "0.48" },
      { label: "4(e)", q: "0.7 × 0.7", a: "0.49" },
      { label: "4(f)", q: "0.6 × 0.5", a: "0.3" },
      { label: "4(g)", q: "0.8 × 0.5", a: "0.4" },
      { label: "4(h)", q: "0.5 × 0.4", a: "0.2" },
      { label: "4(i)", q: "0.8 × 0.1", a: "0.08" },
      { label: "4(j)", q: "0.07 × 0.5", a: "0.035" },
      { label: "4(k)", q: "0.04 × 0.2", a: "0.008" },
      { label: "4(l)", q: "0.8 × 0.07", a: "0.056" },
      { label: "4(m)", q: "0.06 × 0.9", a: "0.054" },
      { label: "4(n)", q: "0.04 × 0.06", a: "0.0024" },
      { label: "4(o)", q: "0.08 × 0.03", a: "0.0024" },
      { label: "4(p)", q: "0.02 × 0.03", a: "0.0006" },
      { label: "4(q)", q: "0.003 × 0.6", a: "0.0018" },
      { label: "4(r)", q: "0.9 × 0.002", a: "0.0018" },
      { label: "4(s)", q: "0.008 × 0.6", a: "0.0048" },
      { label: "4(t)", q: "0.005 × 0.4", a: "0.002" },
      { label: "4(u)", q: "0.007 × 0.02", a: "0.00014" },
      { label: "4(v)", q: "0.008 × 0.09", a: "0.00072" },
      { label: "4(w)", q: "0.04 × 0.004", a: "0.00016" },
      { label: "4(x)", q: "0.005 × 0.003", a: "0.000015" },
      { label: "4(y)", q: "0.008 × 0.05", a: "0.0004" },
      { label: "4(z)", q: "0.009 × 0.008", a: "0.000072" }
    ]
  },
  {
    id: "sec-w5",
    title: "Part 6: Workout — Question 5",
    isWordProblem: false,
    items: [
      { label: "5(a)", q: "3.1 × 0.5", a: "1.55" },
      { label: "5(b)", q: "6.3 × 0.3", a: "1.89" },
      { label: "5(c)", q: "5.4 × 0.7", a: "3.78" },
      { label: "5(d)", q: "9.2 × 0.6", a: "5.52" },
      { label: "5(e)", q: "4.8 × 0.9", a: "4.32" },
      { label: "5(f)", q: "2.4 × 3.2", a: "7.68" },
      { label: "5(g)", q: "9.1 × 1.3", a: "11.83" },
      { label: "5(h)", q: "5.5 × 7.7", a: "42.35" },
      { label: "5(i)", q: "1.7 × 4.3", a: "7.31" },
      { label: "5(j)", q: "9.4 × 4.9", a: "46.06" },
      { label: "5(k)", q: "0.13 × 0.7", a: "0.091" },
      { label: "5(l)", q: "0.48 × 0.3", a: "0.144" },
      { label: "5(m)", q: "0.54 × 0.9", a: "0.486" },
      { label: "5(n)", q: "0.18 × 0.17", a: "0.0306" },
      { label: "5(o)", q: "8.3 × 0.37", a: "3.071" },
      { label: "5(p)", q: "3.5 × 0.74", a: "2.59" },
      { label: "5(q)", q: "0.94 × 0.02", a: "0.0188" },
      { label: "5(r)", q: "0.38 × 0.06", a: "0.0228" },
      { label: "5(s)", q: "0.039 × 0.7", a: "0.0273" },
      { label: "5(t)", q: "0.084 × 1.2", a: "0.1008" },
      { label: "5(u)", q: "8.1 × 0.05", a: "0.405" },
      { label: "5(v)", q: "9.4 × 0.082", a: "0.7708" },
      { label: "5(w)", q: "0.0048 × 0.12", a: "0.000576" }
    ]
  },
  {
    id: "sec-w6",
    title: "Part 7: Workout — Question 6",
    isWordProblem: false,
    items: [
      { label: "6(a)", q: "1.29 × 1.4", a: "1.806" },
      { label: "6(b)", q: "3.52 × 2.4", a: "8.448" },
      { label: "6(c)", q: "4.92 × 0.34", a: "1.6728" },
      { label: "6(d)", q: "8.12 × 0.29", a: "2.3548" },
      { label: "6(e)", q: "6.3 × 2.46", a: "15.498" },
      { label: "6(f)", q: "9.2 × 7.15", a: "65.78" },
      { label: "6(g)", q: "0.843 × 1.9", a: "1.6017" },
      { label: "6(h)", q: "0.548 × 2.7", a: "1.4796" },
      { label: "6(i)", q: "6.18 × 5.1", a: "31.518" },
      { label: "6(j)", q: "18.2 × 6.4", a: "116.48" },
      { label: "6(k)", q: "5.03 × 2.8", a: "14.084" },
      { label: "6(l)", q: "40.8 × 5.3", a: "216.24" }
    ]
  },
  {
    id: "sec-apply",
    title: "Part 8: Apply (Word Problems)",
    isWordProblem: true,
    items: [
      { label: "Apply Q1", q: "Regan is paid £6.70 per hour. He works 8 hours in a week. Work out how much Regan should be paid.", a: "53.60", prefix: "£" },
      { label: "Apply Q2", q: "Function Machine: Input = 3.8 → [ × 7 ] → Output = ?", a: "26.6" },
      { label: "Apply Q3", q: "Calculate the area of a rectangle with length 19.4 cm and width 8 cm.", a: "155.2", suffix: "cm²" },
      { label: "Apply Q4", q: "A bottle of cola costs £1.29. Calculate the total cost of 6 bottles of cola.", a: "7.74", prefix: "£" },
      { label: "Apply Q5", q: "Mr and Mrs Jones (2 adults) bring their 5 children to a museum. Adults: £17.60 each, Children: £7.55 each. Work out the total cost for the family.", a: "72.95", prefix: "£" },
      { label: "Apply Q6", q: "Class 8A are going on a trip to a windmill. The trip costs £3.70 each and there are 26 students in 8A. How much money should be collected?", a: "96.20", prefix: "£" },
      { label: "Apply Q7", q: "Mr. Jenkins is building a fence for his garden. The fence costs £12.60 per metre to build and is 5.3 metres long. Work out the total cost of building the fence.", a: "66.78", prefix: "£" },
      { label: "Apply Q8", q: "Calculate the area of a rectangle with length 6.8 cm and width 2.7 cm.", a: "18.36", suffix: "cm²" },
      { label: "Apply Q9", q: "Fruit shop prices: Apples £0.97/kg, Oranges £1.07/kg, Bananas £1.46/kg. Find the total cost of 1.2kg of apples, 3.5kg of oranges and 1.9kg of bananas.", a: "7.68", prefix: "£" }
    ]
  }
];

function generateDistractors(correctStr) {
  const num = parseFloat(correctStr);
  const decimals = (correctStr.split('.')[1] || '').length;
  const set = new Set([correctStr]);

  // Plausible place-value shifts and close arithmetic offsets
  const candidates = [
    (num * 10).toFixed(Math.max(0, decimals - 1)),
    (num / 10).toFixed(decimals + 1),
    (num + Math.pow(10, -decimals) * 2).toFixed(decimals),
    (num - Math.pow(10, -decimals) * 2).toFixed(decimals),
    (num + 1).toFixed(decimals),
    (num * 0.5).toFixed(decimals)
  ];

  for (let c of candidates) {
    if (set.size >= 4) break;
    if (parseFloat(c) > 0 && parseFloat(c) !== num) {
      set.add(c);
    }
  }
  while (set.size < 4) {
    const r = (num + (Math.random() * 4 - 2)).toFixed(decimals);
    if (parseFloat(r) > 0 && parseFloat(r) !== num) set.add(r);
  }

  return Array.from(set).sort((a, b) => parseFloat(a) - parseFloat(b));
}

let globalIndex = 0;
const answerRegistry = [];

function buildQuiz() {
  const root = document.getElementById('quizRoot');
  const nav = document.getElementById('navTabs');

  quizSections.forEach((sec) => {
    // Create Tab Button
    const tabBtn = document.createElement('button');
    tabBtn.type = "button";
    tabBtn.className = "tab-btn";
    tabBtn.textContent = `${sec.title.split(':')[0]} (${sec.items.length})`;
    tabBtn.onclick = () => filterSection(sec.id, tabBtn);
    nav.appendChild(tabBtn);

    // Create Section Container
    const secEl = document.createElement('div');
    secEl.className = "section-block";
    secEl.id = sec.id;

    secEl.innerHTML = `
      <div class="section-header">
        <h2>${sec.title}</h2>
        <span>${sec.items.length} Questions</span>
      </div>
      <div class="questions-grid ${sec.isWordProblem ? 'apply-grid' : ''}" id="grid-${sec.id}"></div>
    `;
    root.appendChild(secEl);

    const gridEl = secEl.querySelector(`#grid-${sec.id}`);

    sec.items.forEach((item) => {
      const isMCQ = globalIndex % 2 === 0; // Strictly alternate MCQ and Fill in the Blank
      const qId = `q_${globalIndex}`;
      const prefix = item.prefix || "";
      const suffix = item.suffix ? " " + item.suffix : "";

      answerRegistry.push({
        id: qId,
        type: isMCQ ? 'mcq' : 'fib',
        correctStr: item.a,
        correctNum: parseFloat(item.a),
        prefix,
        suffix
      });

      const card = document.createElement('div');
      card.className = "q-card";

      let inputHTML = "";
      if (isMCQ) {
        const options = generateDistractors(item.a);
        inputHTML = `<div class="mcq-list">` + options.map(opt => `
          <label>
            <input type="radio" name="${qId}" value="${opt}">
            ${prefix}${opt}${suffix}
          </label>
        `).join('') + `</div>`;
      } else {
        inputHTML = `
          <div class="fib-wrap">
            ${prefix ? `<span>${prefix}</span>` : ''}
            <input type="text" class="fib-input" id="${qId}" placeholder="Type answer..." autocomplete="off">
            ${suffix ? `<span>${suffix}</span>` : ''}
          </div>
        `;
      }

      card.innerHTML = `
        <div>
          <span class="badge ${isMCQ ? 'badge-mcq' : 'badge-fib'}">
            ${isMCQ ? 'Multiple Choice' : 'Fill in the Blank'}
          </span>
          <div class="q-prompt">${item.label}: ${item.q}</div>
          ${inputHTML}
        </div>
        <div class="feedback" id="fb-${qId}"></div>
      `;

      gridEl.appendChild(card);
      globalIndex++;
    });
  });
}

function filterSection(secId, btn) {
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');

  document.querySelectorAll('.section-block').forEach(block => {
    block.style.display = (secId === 'all' || block.id === secId) ? 'block' : 'none';
  });
}

function gradeQuiz() {
  let correctCount = 0;

  answerRegistry.forEach((entry) => {
    const fb = document.getElementById(`fb-${entry.id}`);
    let userVal = "";

    if (entry.type === 'mcq') {
      const checked = document.querySelector(`input[name="${entry.id}"]:checked`);
      userVal = checked ? checked.value : "";
    } else {
      const input = document.getElementById(entry.id);
      userVal = input ? input.value.trim().replace(/[£$,\s]/g, '') : "";
    }

    const userNum = parseFloat(userVal);
    const isCorrect = userVal !== "" && !isNaN(userNum) && Math.abs(userNum - entry.correctNum) < 1e-9;

    if (isCorrect) {
      correctCount++;
      fb.textContent = "✓ Correct!";
      fb.className = "feedback correct";
    } else {
      fb.textContent = `✗ Answer: ${entry.prefix}${entry.correctStr}${entry.suffix}`;
      fb.className = "feedback incorrect";
    }
  });

  const total = answerRegistry.length;
  const pct = Math.round((correctCount / total) * 100);
  document.getElementById('scoreDisplay').textContent = `Score: ${correctCount} / ${total} (${pct}%)`;
}

function resetQuiz() {
  document.getElementById('quizForm').reset();
  answerRegistry.forEach(entry => {
    const fb = document.getElementById(`fb-${entry.id}`);
    fb.textContent = "";
    fb.className = "feedback";
  });
  document.getElementById('scoreDisplay').textContent = "Ready to check your answers!";
}

buildQuiz();
</script>

</body>
</html>
