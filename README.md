# warikan_germany2027

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Shippori+Mincho:wght@500;700&family=Zen+Maru+Gothic:wght@400;500;700&family=JetBrains+Mono:wght@500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#FAF6ED;
    --paper-soft:#F1EADA;
    --ink:#1E3D46;
    --ink-soft:#5C7680;
    --amber:#D98E04;
    --amber-soft:#F3D48A;
    --rust:#A6432E;
    --pine:#3F7A5E;
    --line:#CBBFA8;
  }
  *{box-sizing:border-box;}
  body, .root{
    margin:0;
    font-family:'Zen Maru Gothic', sans-serif;
    color:var(--ink);
    background:transparent;
  }
  .app{
    max-width:760px;
    margin:0 auto;
    padding:8px 4px 40px;
  }
  .header{
    text-align:center;
    padding:20px 12px 22px;
    position:relative;
  }
  .header .eyebrow{
    font-family:'JetBrains Mono', monospace;
    font-size:11px;
    letter-spacing:.28em;
    color:var(--amber);
    font-weight:700;
  }
  .header h1{
    font-family:'Shippori Mincho', serif;
    font-size:30px;
    font-weight:700;
    margin:6px 0 2px;
    letter-spacing:.04em;
  }
  .header .sub{
    font-size:12.5px;
    color:var(--ink-soft);
  }
  .shared-badge{
    display:inline-block;
    margin-top:10px;
    font-size:11.5px;
    font-weight:700;
    color:var(--pine);
    background:#fff;
    border:1.5px solid var(--pine);
    border-radius:999px;
    padding:5px 12px;
  }

  .section{
    background:var(--paper);
    border:1.5px solid var(--line);
    border-radius:14px;
    padding:18px 18px 20px;
    margin-bottom:18px;
    position:relative;
  }
  .section-title{
    font-family:'Shippori Mincho', serif;
    font-size:16px;
    font-weight:700;
    display:flex;
    align-items:center;
    gap:8px;
    margin-bottom:14px;
  }
  .section-title .num{
    font-family:'JetBrains Mono', monospace;
    font-size:11px;
    color:#fff;
    background:var(--ink);
    border-radius:5px;
    padding:2px 6px;
    letter-spacing:.05em;
  }

  /* Members */
  .member-row{
    display:flex;
    flex-wrap:wrap;
    gap:8px;
    margin-bottom:12px;
  }
  .chip{
    display:flex;
    align-items:center;
    gap:6px;
    background:var(--paper-soft);
    border:1.5px solid var(--line);
    color:var(--ink);
    padding:6px 8px 6px 12px;
    border-radius:999px;
    font-size:13.5px;
    font-weight:500;
  }
  .chip button{
    border:none;
    background:transparent;
    color:var(--ink-soft);
    cursor:pointer;
    font-size:14px;
    line-height:1;
    padding:2px;
    border-radius:50%;
  }
  .chip button:hover{ color:var(--rust); background:#fff; }
  .add-member-form{
    display:flex;
    gap:8px;
  }
  input[type=text], input[type=number], input[type=date], select{
    font-family:'Zen Maru Gothic', sans-serif;
    font-size:14px;
    padding:9px 12px;
    border-radius:9px;
    border:1.5px solid var(--line);
    background:#fff;
    color:var(--ink);
    outline:none;
    width:100%;
  }
  input:focus, select:focus{ border-color:var(--amber); }
  .add-member-form input{ flex:1; width:auto; }

  .btn{
    font-family:'Zen Maru Gothic', sans-serif;
    font-size:14px;
    font-weight:700;
    padding:9px 16px;
    border-radius:9px;
    border:none;
    cursor:pointer;
    background:var(--ink);
    color:var(--paper);
    white-space:nowrap;
  }
  .btn:hover{ background:#142b32; }
  .btn.ghost{
    background:transparent;
    color:var(--ink);
    border:1.5px solid var(--ink);
  }
  .btn.small{
    padding:7px 12px;
    font-size:12.5px;
  }
  .btn:disabled{ opacity:.4; cursor:not-allowed; }

  /* Exchange rate */
  .rate-row{
    display:flex;
    align-items:center;
    gap:8px;
    flex-wrap:wrap;
  }
  .rate-row .rate-input-wrap{
    display:flex;
    align-items:center;
    gap:6px;
    font-size:13.5px;
    font-weight:700;
    white-space:nowrap;
  }
  .rate-row .rate-input-wrap input{ width:100px; }
  .rate-note{
    font-size:11.5px;
    color:var(--ink-soft);
    margin-top:8px;
  }

  /* Expense form */
  .form-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;
    margin-bottom:12px;
  }
  .form-grid .full{ grid-column:1 / -1; }
  label.field-label{
    font-size:11.5px;
    color:var(--ink-soft);
    font-weight:700;
    display:block;
    margin-bottom:4px;
    letter-spacing:.03em;
  }
  .participants-box{
    display:flex;
    flex-wrap:wrap;
    gap:6px;
  }
  .participant-toggle{
    font-size:13px;
    padding:6px 12px;
    border-radius:999px;
    border:1.5px solid var(--line);
    background:#fff;
    color:var(--ink-soft);
    cursor:pointer;
    font-weight:500;
    font-family:'Zen Maru Gothic', sans-serif;
  }
  .participant-toggle.active{
    background:var(--amber-soft);
    border-color:var(--amber);
    color:var(--ink);
  }
  .participant-toggle:hover{ border-color:var(--amber); }

  .toggle-group{
    display:flex;
    gap:6px;
  }
  .toggle-btn{
    flex:1;
    font-size:13px;
    padding:8px 10px;
    border-radius:9px;
    border:1.5px solid var(--line);
    background:#fff;
    color:var(--ink-soft);
    cursor:pointer;
    font-weight:700;
    font-family:'Zen Maru Gothic', sans-serif;
    text-align:center;
  }
  .toggle-btn.active{
    background:var(--ink);
    border-color:var(--ink);
    color:var(--paper);
  }

  .custom-share-box{
    display:flex;
    flex-direction:column;
    gap:6px;
    margin-top:8px;
    padding:10px;
    border:1.5px dashed var(--line);
    border-radius:9px;
  }
  .custom-share-row{
    display:flex;
    align-items:center;
    gap:8px;
  }
  .custom-share-row .name{
    width:80px;
    flex-shrink:0;
    font-size:13px;
    font-weight:700;
  }
  .custom-share-row input{ flex:1; }
  .custom-share-total{
    font-size:12.5px;
    color:var(--ink-soft);
    text-align:right;
    padding-top:2px;
  }
  .custom-share-total b{ color:var(--ink); font-family:'JetBrains Mono', monospace; }

  .empty-note{
    font-size:13px;
    color:var(--ink-soft);
    text-align:center;
    padding:18px 8px;
    border:1.5px dashed var(--line);
    border-radius:10px;
  }

  .edit-banner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    background:var(--amber-soft);
    border:1.5px solid var(--amber);
    border-radius:9px;
    padding:8px 12px;
    font-size:12.5px;
    font-weight:700;
    margin-bottom:12px;
  }
  .edit-banner button{
    border:none;
    background:transparent;
    color:var(--rust);
    font-weight:700;
    cursor:pointer;
    font-size:12.5px;
    text-decoration:underline;
  }

  /* Filters */
  .filter-row{
    display:grid;
    grid-template-columns:1.4fr 1fr 1fr auto;
    gap:8px;
    margin-bottom:14px;
  }
  .filter-row .full{ grid-column:1/-1; }

  /* Ticket card for each expense */
  .ticket{
    display:flex;
    background:#fff;
    border:1.5px solid var(--line);
    border-radius:10px;
    margin-bottom:10px;
    overflow:hidden;
    position:relative;
  }
  .ticket-main{
    flex:1;
    padding:12px 14px;
    min-width:0;
  }
  .ticket-main .top-row{
    display:flex;
    align-items:center;
    gap:8px;
    flex-wrap:wrap;
    margin-bottom:3px;
  }
  .ticket-main .desc{
    font-size:14px;
    font-weight:700;
    color:var(--ink);
  }
  .tag{
    font-size:10.5px;
    font-weight:700;
    color:var(--ink);
    background:var(--paper-soft);
    border:1px solid var(--line);
    border-radius:999px;
    padding:2px 8px;
    white-space:nowrap;
  }
  .tag.date-tag{
    color:var(--ink-soft);
    background:transparent;
    border:none;
    padding:2px 0;
    font-family:'JetBrains Mono', monospace;
  }
  .ticket-main .meta{
    font-size:12px;
    color:var(--ink-soft);
    margin-top:3px;
    line-height:1.5;
  }
  .ticket-main .meta b{ color:var(--ink); font-weight:700; }
  .ticket-actions{
    width:118px;
    flex-shrink:0;
    background:var(--paper-soft);
    border-left:1.5px dashed var(--line);
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    padding:8px 4px;
    position:relative;
  }
  .ticket-actions::before, .ticket-actions::after{
    content:"";
    position:absolute;
    left:-7px;
    width:14px; height:14px;
    border-radius:50%;
    background:var(--paper);
    border:1.5px solid var(--line);
  }
  .ticket-actions::before{ top:-7px; }
  .ticket-actions::after{ bottom:-7px; }
  .ticket-actions .amt{
    font-family:'JetBrains Mono', monospace;
    font-weight:700;
    font-size:14.5px;
    color:var(--amber);
    text-align:center;
  }
  .ticket-actions .amt-sub{
    font-family:'JetBrains Mono', monospace;
    font-size:10.5px;
    color:var(--ink-soft);
    margin-top:1px;
  }
  .ticket-actions .action-row{
    display:flex;
    gap:8px;
    margin-top:6px;
  }
  .ticket-actions button{
    border:none;
    background:transparent;
    color:var(--ink-soft);
    font-size:11px;
    cursor:pointer;
    text-decoration:underline;
  }
  .ticket-actions .edit-link:hover{ color:var(--pine); }
  .ticket-actions .del:hover{ color:var(--rust); }

  /* Balance summary */
  .balance-list{
    display:flex;
    flex-direction:column;
    gap:8px;
    margin-bottom:4px;
  }
  .balance-row{
    display:flex;
    align-items:center;
    justify-content:space-between;
    font-size:13.5px;
    padding:8px 12px;
    border-radius:8px;
    background:var(--paper-soft);
  }
  .balance-row .name{ font-weight:700; }
  .balance-row .val{
    font-family:'JetBrains Mono', monospace;
    font-weight:700;
  }
  .val.plus{ color:var(--pine); }
  .val.minus{ color:var(--rust); }
  .val.zero{ color:var(--ink-soft); }

  /* Settlement tickets */
  .settle-ticket{
    display:flex;
    align-items:center;
    background:linear-gradient(135deg,#fff, var(--paper-soft));
    border:1.5px solid var(--amber);
    border-radius:10px;
    padding:12px 14px;
    margin-bottom:10px;
    gap:12px;
  }
  .settle-flow{
    flex:1;
    display:flex;
    align-items:center;
    gap:8px;
    font-size:14px;
    font-weight:700;
    min-width:0;
  }
  .settle-flow .from, .settle-flow .to{
    background:var(--ink);
    color:var(--paper);
    padding:4px 10px;
    border-radius:999px;
    font-size:13px;
    white-space:nowrap;
    overflow:hidden;
    text-overflow:ellipsis;
    max-width:110px;
  }
  .settle-flow .arrow{
    color:var(--amber);
    font-size:16px;
  }
  .settle-amt{
    font-family:'JetBrains Mono', monospace;
    font-weight:700;
    font-size:16px;
    color:var(--rust);
    flex-shrink:0;
  }
  .all-settled{
    text-align:center;
    padding:22px 10px;
    font-size:14px;
    color:var(--pine);
    font-weight:700;
  }
  .all-settled .stamp{
    font-family:'JetBrains Mono', monospace;
    display:inline-block;
    border:2px solid var(--pine);
    border-radius:8px;
    padding:4px 14px;
    transform:rotate(-3deg);
    letter-spacing:.1em;
    margin-bottom:6px;
  }

  .footer-note{
    text-align:center;
    font-size:11px;
    color:var(--ink-soft);
    margin-top:6px;
  }

  ::-webkit-scrollbar{ width:6px; }
  ::-webkit-scrollbar-thumb{ background:var(--line); border-radius:3px; }

  @media (max-width:420px){
    .form-grid{ grid-template-columns:1fr; }
    .filter-row{ grid-template-columns:1fr 1fr; }
    .filter-row .full{ grid-column:1/-1; }
    .ticket-actions{ width:96px; }
  }
</style>

<div class="root">
  <div class="app">
    <div class="header">
      <div class="eyebrow">TRIP EXPENSE TICKET</div>
      <h1 id="tripTitle">旅のわりかん帳</h1>
      <div class="sub">支払いを記録して、誰が誰にいくら払うかを自動計算します</div>
      <div class="shared-badge">👥 共有モード：このリンクを開いた人は全員、記録の閲覧・追加ができます</div>
    </div>

    <!-- Members -->
    <div class="section">
      <div class="section-title"><span class="num">01</span>メンバー</div>
      <div class="member-row" id="memberChips"></div>
      <form class="add-member-form" id="addMemberForm">
        <input type="text" id="newMemberName" placeholder="名前を入力（例: 太郎）" maxlength="20" />
        <button class="btn" type="submit">追加</button>
      </form>
    </div>

    <!-- Exchange rate -->
    <div class="section">
      <div class="section-title"><span class="num">02</span>為替レート（EUR → JPY）</div>
      <div class="rate-row">
        <div class="rate-input-wrap">
          1 EUR = <input type="number" id="rateInput" step="0.01" min="1" /> 円
        </div>
        <button class="btn small ghost" type="button" id="fetchRateBtn">最新レートを取得</button>
        <button class="btn small" type="button" id="saveRateBtn">この値を保存</button>
      </div>
      <div class="rate-note" id="rateNote">現在のレート: —</div>
    </div>

    <!-- Add expense -->
    <div class="section">
      <div class="section-title"><span class="num">03</span>支払いを記録する</div>
      <div class="edit-banner" id="editBanner" style="display:none;">
        <span>✏️ 記録を編集中です</span>
        <button type="button" id="cancelEditBtn">編集をやめる</button>
      </div>
      <form id="expenseForm">
        <div class="form-grid">
          <div>
            <label class="field-label">日付</label>
            <input type="date" id="dateInput" />
          </div>
          <div>
            <label class="field-label">カテゴリ</label>
            <select id="categorySelect"></select>
          </div>
          <div>
            <label class="field-label">支払った人</label>
            <select id="payerSelect"></select>
          </div>
          <div>
            <label class="field-label">通貨</label>
            <div class="toggle-group" id="currencyToggle">
              <div class="toggle-btn active" data-currency="EUR">ユーロ €</div>
              <div class="toggle-btn" data-currency="JPY">円 ¥</div>
            </div>
          </div>
          <div class="full" id="amountFieldWrap">
            <label class="field-label" id="amountLabel">金額（合計）</label>
            <input type="number" id="amountInput" placeholder="0" min="0" step="0.01" />
          </div>
          <div class="full">
            <label class="field-label">内容（任意）</label>
            <input type="text" id="descInput" placeholder="例: 夕食代、電車代" maxlength="30" />
          </div>
          <div class="full">
            <label class="field-label">分割方法</label>
            <div class="toggle-group" id="splitModeToggle">
              <div class="toggle-btn active" data-mode="equal">均等割り</div>
              <div class="toggle-btn" data-mode="custom">個別に金額指定</div>
            </div>
          </div>
          <div class="full">
            <label class="field-label">対象者（費用を割る相手を選択）</label>
            <div class="participants-box" id="participantsBox"></div>
            <div class="custom-share-box" id="customShareBox" style="display:none;"></div>
          </div>
        </div>
        <button class="btn" type="submit" id="submitExpenseBtn" style="width:100%;">この支払いを記録する</button>
      </form>
    </div>

    <!-- Expense list -->
    <div class="section">
      <div class="section-title"><span class="num">04</span>記録一覧</div>
      <div class="filter-row">
        <input type="text" id="searchInput" placeholder="内容を検索" />
        <select id="categoryFilter"></select>
        <select id="personFilter"></select>
        <button class="btn small ghost" type="button" id="resetFilterBtn">リセット</button>
      </div>
      <div id="expenseList"></div>
    </div>

    <!-- Balances -->
    <div class="section">
      <div class="section-title"><span class="num">05</span>各自の収支（円換算）</div>
      <div class="balance-list" id="balanceList"></div>
    </div>

    <!-- Settlement -->
    <div class="section">
      <div class="section-title"><span class="num">06</span>精算リスト（最少の送金回数）</div>
      <div id="settleList"></div>
    </div>

    <div class="footer-note">共有モード：この記録はリンクを開いた友人全員から見えます</div>
  </div>
</div>

<script>
(function(){
  const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbyCnH8DkBu3zUv_maO4KXWlqd8UHOP7vZOoNGOOauFDEpy4mbynB1b99Gyg42qibgbR/exec';
  const CATEGORIES = ['食費','交通','宿泊','観光・入場料','買い物','その他'];
  const DEFAULT_RATE = 165;

  let state = { members: [], expenses: [], exchangeRate: DEFAULT_RATE };
  let selectedParticipants = new Set();
  let currentCurrency = 'EUR';
  let splitMode = 'equal';
  let customShareValues = {};
  let editingId = null;

  // element refs
  const memberChips = document.getElementById('memberChips');
  const addMemberForm = document.getElementById('addMemberForm');
  const newMemberName = document.getElementById('newMemberName');
  const rateInput = document.getElementById('rateInput');
  const fetchRateBtn = document.getElementById('fetchRateBtn');
  const saveRateBtn = document.getElementById('saveRateBtn');
  const rateNote = document.getElementById('rateNote');
  const dateInput = document.getElementById('dateInput');
  const categorySelect = document.getElementById('categorySelect');
  const payerSelect = document.getElementById('payerSelect');
  const currencyToggle = document.getElementById('currencyToggle');
  const amountFieldWrap = document.getElementById('amountFieldWrap');
  const amountLabel = document.getElementById('amountLabel');
  const amountInput = document.getElementById('amountInput');
  const descInput = document.getElementById('descInput');
  const splitModeToggle = document.getElementById('splitModeToggle');
  const participantsBox = document.getElementById('participantsBox');
  const customShareBox = document.getElementById('customShareBox');
  const expenseForm = document.getElementById('expenseForm');
  const editBanner = document.getElementById('editBanner');
  const cancelEditBtn = document.getElementById('cancelEditBtn');
  const searchInput = document.getElementById('searchInput');
  const categoryFilter = document.getElementById('categoryFilter');
  const personFilter = document.getElementById('personFilter');
  const resetFilterBtn = document.getElementById('resetFilterBtn');
  const expenseList = document.getElementById('expenseList');
  const balanceList = document.getElementById('balanceList');
  const settleList = document.getElementById('settleList');

  function uid(){ return Math.random().toString(36).slice(2,9); }
  function todayStr(){ return new Date().toISOString().slice(0,10); }
  function escapeHtml(s){
    return String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
  }
  function fmtJPY(n){
    return '¥' + Math.round(n).toLocaleString('ja-JP');
  }
  function fmtCur(amount, currency){
    if(currency === 'EUR') return '€' + Number(amount).toLocaleString('de-DE', {minimumFractionDigits:2, maximumFractionDigits:2});
    return '¥' + Math.round(amount).toLocaleString('ja-JP');
  }
  function rateOf(exp){
    return exp.currency === 'EUR' ? (exp.rateUsed || state.exchangeRate) : 1;
  }
  function amountJPY(exp){
    return exp.amount * rateOf(exp);
  }
  function shareOriginal(exp, name){
    if(exp.splitMode === 'custom'){
      return exp.customShares && exp.customShares[name] ? exp.customShares[name] : 0;
    }
    return exp.amount / exp.participants.length;
  }
  function shareJPY(exp, name){
    return shareOriginal(exp, name) * rateOf(exp);
  }

  // ---- storage ----
  async function save(){
    try{
      await fetch(SCRIPT_URL, {
        method: 'POST',
        headers: { 'Content-Type': 'text/plain;charset=utf-8' },
        body: JSON.stringify(state)
      });
    }catch(e){ console.error('save failed', e); }
  }
  async function load(){
    try{
      const res = await fetch(SCRIPT_URL);
      const parsed = await res.json();
      if(parsed && Array.isArray(parsed.members) && Array.isArray(parsed.expenses)){
        state = parsed;
        if(!state.exchangeRate) state.exchangeRate = DEFAULT_RATE;
      }
    }catch(e){ console.error('load failed', e); }
  }

  // ---- exchange rate ----
  async function fetchLatestRate(){
    fetchRateBtn.disabled = true;
    fetchRateBtn.textContent = '取得中…';
    try{
      const res = await fetch('https://api.frankfurter.app/latest?from=EUR&to=JPY');
      const data = await res.json();
      if(data && data.rates && data.rates.JPY){
        rateInput.value = Math.round(data.rates.JPY * 100) / 100;
        state.exchangeRate = parseFloat(rateInput.value);
        renderRateNote();
        save();
      }
    }catch(e){
      alert('レートの取得に失敗しました。手動で入力して「この値を保存」を押してください。');
    }
    fetchRateBtn.disabled = false;
    fetchRateBtn.textContent = '最新レートを取得';
  }
  function renderRateNote(){
    rateNote.textContent = `現在のレート: 1 EUR = ${state.exchangeRate} 円（新しい支払いを記録する際に使われます。過去の記録はその時点のレートのまま変わりません）`;
  }

  // ---- members ----
  function renderMembers(){
    memberChips.innerHTML = '';
    if(state.members.length === 0){
      const note = document.createElement('div');
      note.className = 'empty-note';
      note.style.width = '100%';
      note.textContent = 'まずは旅行メンバーを追加してください';
      memberChips.appendChild(note);
    }
    state.members.forEach(name => {
      const chip = document.createElement('div');
      chip.className = 'chip';
      const span = document.createElement('span');
      span.textContent = name;
      const btn = document.createElement('button');
      btn.type = 'button';
      btn.innerHTML = '✕';
      btn.title = '削除';
      btn.addEventListener('click', () => removeMember(name));
      chip.appendChild(span);
      chip.appendChild(btn);
      memberChips.appendChild(chip);
    });

    payerSelect.innerHTML = '';
    if(state.members.length === 0){
      const opt = document.createElement('option');
      opt.textContent = 'メンバーを追加してください';
      opt.disabled = true;
      opt.selected = true;
      payerSelect.appendChild(opt);
    }else{
      state.members.forEach(name => {
        const opt = document.createElement('option');
        opt.value = name;
        opt.textContent = name;
        payerSelect.appendChild(opt);
      });
    }

    selectedParticipants = new Set([...selectedParticipants].filter(n => state.members.includes(n)));
    if(selectedParticipants.size === 0 && !editingId){
      state.members.forEach(n => selectedParticipants.add(n));
    }
    renderParticipantsBox();

    // person filter options
    const prevPersonFilter = personFilter.value;
    personFilter.innerHTML = '<option value="">対象者: すべて</option>' +
      state.members.map(m => `<option value="${escapeHtml(m)}">${escapeHtml(m)}</option>`).join('');
    personFilter.value = state.members.includes(prevPersonFilter) ? prevPersonFilter : '';

    document.getElementById('submitExpenseBtn').disabled = state.members.length < 2;
  }

  function removeMember(name){
    const usedIn = state.expenses.some(e => e.payer === name || e.participants.includes(name));
    if(usedIn){
      const ok = confirm(`「${name}」は既に記録に使われています。削除すると関連する記録も削除されます。よろしいですか？`);
      if(!ok) return;
      state.expenses = state.expenses.filter(e => e.payer !== name && !e.participants.includes(name));
    }
    state.members = state.members.filter(m => m !== name);
    renderAll();
    save();
  }

  // ---- expense form: participants / custom shares ----
  function renderParticipantsBox(){
    participantsBox.innerHTML = '';
    state.members.forEach(name => {
      const btn = document.createElement('button');
      btn.type = 'button';
      btn.className = 'participant-toggle' + (selectedParticipants.has(name) ? ' active' : '');
      btn.textContent = name;
      btn.addEventListener('click', () => {
        if(selectedParticipants.has(name)) selectedParticipants.delete(name);
        else selectedParticipants.add(name);
        renderParticipantsBox();
        renderCustomShareBox();
      });
      participantsBox.appendChild(btn);
    });
    renderCustomShareBox();
  }

  function renderCustomShareBox(){
    if(splitMode !== 'custom'){
      customShareBox.style.display = 'none';
      amountFieldWrap.style.display = '';
      return;
    }
    customShareBox.style.display = 'flex';
    amountFieldWrap.style.display = 'none';
    customShareBox.innerHTML = '';
    const names = [...selectedParticipants];
    if(names.length === 0){
      customShareBox.innerHTML = '<div style="font-size:12.5px;color:var(--ink-soft);">対象者を選んでください</div>';
      return;
    }
    names.forEach(name => {
      const row = document.createElement('div');
      row.className = 'custom-share-row';
      const label = document.createElement('div');
      label.className = 'name';
      label.textContent = name;
      const input = document.createElement('input');
      input.type = 'number';
      input.min = '0';
      input.step = '0.01';
      input.placeholder = '0';
      input.value = customShareValues[name] != null ? customShareValues[name] : '';
      input.addEventListener('input', () => {
        customShareValues[name] = parseFloat(input.value) || 0;
        renderCustomShareTotal();
      });
      row.appendChild(label);
      row.appendChild(input);
      customShareBox.appendChild(row);
    });
    const totalDiv = document.createElement('div');
    totalDiv.className = 'custom-share-total';
    totalDiv.id = 'customShareTotal';
    customShareBox.appendChild(totalDiv);
    renderCustomShareTotal();
  }
  function renderCustomShareTotal(){
    const totalDiv = document.getElementById('customShareTotal');
    if(!totalDiv) return;
    const sum = [...selectedParticipants].reduce((s,n) => s + (customShareValues[n] || 0), 0);
    totalDiv.innerHTML = `合計: <b>${fmtCur(sum, currentCurrency)}</b>`;
  }

  // toggles
  currencyToggle.addEventListener('click', (e) => {
    const btn = e.target.closest('.toggle-btn');
    if(!btn) return;
    currentCurrency = btn.dataset.currency;
    [...currencyToggle.children].forEach(c => c.classList.toggle('active', c === btn));
    renderCustomShareTotal();
  });
  splitModeToggle.addEventListener('click', (e) => {
    const btn = e.target.closest('.toggle-btn');
    if(!btn) return;
    splitMode = btn.dataset.mode;
    [...splitModeToggle.children].forEach(c => c.classList.toggle('active', c === btn));
    renderCustomShareBox();
  });

  // ---- category selects ----
  function fillCategorySelects(){
    categorySelect.innerHTML = CATEGORIES.map(c => `<option value="${c}">${c}</option>`).join('');
    categoryFilter.innerHTML = '<option value="">カテゴリ: すべて</option>' + CATEGORIES.map(c => `<option value="${c}">${c}</option>`).join('');
  }

  // ---- expense list rendering (with filters) ----
  function getFilteredExpenses(){
    const q = searchInput.value.trim().toLowerCase();
    const cat = categoryFilter.value;
    const person = personFilter.value;
    return state.expenses
      .map((e, idx) => ({...e, __idx: idx}))
      .filter(e => {
        if(q && !(e.description || '').toLowerCase().includes(q)) return false;
        if(cat && e.category !== cat) return false;
        if(person && e.payer !== person && !e.participants.includes(person)) return false;
        return true;
      })
      .sort((a,b) => {
        if(a.date !== b.date) return a.date < b.date ? 1 : -1;
        return b.__idx - a.__idx;
      });
  }

  function renderExpenses(){
    expenseList.innerHTML = '';
    const filtered = getFilteredExpenses();
    if(state.expenses.length === 0){
      expenseList.innerHTML = '<div class="empty-note">まだ記録がありません。上のフォームから支払いを追加しましょう。</div>';
      return;
    }
    if(filtered.length === 0){
      expenseList.innerHTML = '<div class="empty-note">条件に一致する記録がありません。</div>';
      return;
    }
    filtered.forEach(exp => {
      const ticket = document.createElement('div');
      ticket.className = 'ticket';

      const main = document.createElement('div');
      main.className = 'ticket-main';

      const topRow = document.createElement('div');
      topRow.className = 'top-row';
      topRow.innerHTML = `
        <span class="desc">${escapeHtml(exp.description || '（内容なし）')}</span>
        <span class="tag">${escapeHtml(exp.category || 'その他')}</span>
        <span class="tag date-tag">${escapeHtml(exp.date || '')}</span>
      `;
      main.appendChild(topRow);

      const meta = document.createElement('div');
      meta.className = 'meta';
      let shareText;
      if(exp.splitMode === 'custom'){
        shareText = exp.participants.map(p => `${escapeHtml(p)}:${fmtCur(shareOriginal(exp,p), exp.currency)}`).join('、');
      }else{
        shareText = `${exp.participants.map(escapeHtml).join('、')}（1人あたり ${fmtCur(exp.amount/exp.participants.length, exp.currency)}）`;
      }
      meta.innerHTML = `<b>${escapeHtml(exp.payer)}</b> が立て替え ・ 対象: ${shareText}`;
      main.appendChild(meta);

      const actions = document.createElement('div');
      actions.className = 'ticket-actions';
      const amt = document.createElement('div');
      amt.className = 'amt';
      amt.textContent = fmtCur(exp.amount, exp.currency);
      actions.appendChild(amt);
      if(exp.currency === 'EUR'){
        const sub = document.createElement('div');
        sub.className = 'amt-sub';
        sub.textContent = `(${fmtJPY(amountJPY(exp))})`;
        actions.appendChild(sub);
      }
      const actionRow = document.createElement('div');
      actionRow.className = 'action-row';
      const editBtn = document.createElement('button');
      editBtn.type = 'button';
      editBtn.className = 'edit-link';
      editBtn.textContent = '編集';
      editBtn.addEventListener('click', () => startEdit(exp.id));
      const del = document.createElement('button');
      del.type = 'button';
      del.className = 'del';
      del.textContent = '削除';
      del.addEventListener('click', () => {
        state.expenses = state.expenses.filter(e => e.id !== exp.id);
        if(editingId === exp.id) cancelEdit();
        renderAll();
        save();
      });
      actionRow.appendChild(editBtn);
      actionRow.appendChild(del);
      actions.appendChild(actionRow);

      ticket.appendChild(main);
      ticket.appendChild(actions);
      expenseList.appendChild(ticket);
    });
  }

  // ---- edit flow ----
  function startEdit(id){
    const exp = state.expenses.find(e => e.id === id);
    if(!exp) return;
    editingId = id;
    dateInput.value = exp.date;
    categorySelect.value = exp.category;
    payerSelect.value = exp.payer;
    currentCurrency = exp.currency;
    [...currencyToggle.children].forEach(c => c.classList.toggle('active', c.dataset.currency === exp.currency));
    splitMode = exp.splitMode || 'equal';
    [...splitModeToggle.children].forEach(c => c.classList.toggle('active', c.dataset.mode === splitMode));
    amountInput.value = exp.amount;
    descInput.value = exp.description || '';
    selectedParticipants = new Set(exp.participants);
    customShareValues = exp.splitMode === 'custom' ? {...exp.customShares} : {};
    renderParticipantsBox();
    editBanner.style.display = 'flex';
    document.getElementById('submitExpenseBtn').textContent = 'この内容で更新する';
    window.scrollTo({top: expenseForm.offsetParent ? expenseForm.getBoundingClientRect().top + window.scrollY - 20 : 0, behavior: 'smooth'});
  }
  function cancelEdit(){
    editingId = null;
    editBanner.style.display = 'none';
    document.getElementById('submitExpenseBtn').textContent = 'この支払いを記録する';
    amountInput.value = '';
    descInput.value = '';
    dateInput.value = todayStr();
    customShareValues = {};
    selectedParticipants = new Set(state.members);
    splitMode = 'equal';
    [...splitModeToggle.children].forEach(c => c.classList.toggle('active', c.dataset.mode === 'equal'));
    renderParticipantsBox();
  }
  cancelEditBtn.addEventListener('click', cancelEdit);

  // ---- balances & settlement (always JPY) ----
  function computeBalances(){
    const balance = {};
    state.members.forEach(m => balance[m] = 0);
    state.expenses.forEach(exp => {
      balance[exp.payer] = (balance[exp.payer] || 0) + amountJPY(exp);
      exp.participants.forEach(p => {
        balance[p] = (balance[p] || 0) - shareJPY(exp, p);
      });
    });
    return balance;
  }
  function renderBalances(){
    balanceList.innerHTML = '';
    if(state.members.length === 0){
      balanceList.innerHTML = '<div class="empty-note">メンバーを追加すると収支が表示されます</div>';
      return;
    }
    const balance = computeBalances();
    state.members.forEach(name => {
      const v = balance[name] || 0;
      const row = document.createElement('div');
      row.className = 'balance-row';
      const cls = v > 0.5 ? 'plus' : (v < -0.5 ? 'minus' : 'zero');
      const sign = v > 0.5 ? '+' : '';
      row.innerHTML = `<span class="name">${escapeHtml(name)}</span><span class="val ${cls}">${sign}${fmtJPY(v)}</span>`;
      balanceList.appendChild(row);
    });
  }
  function computeSettlements(){
    const balance = computeBalances();
    const creditors = [];
    const debtors = [];
    Object.entries(balance).forEach(([name, v]) => {
      if(v > 0.5) creditors.push({name, amount: v});
      else if(v < -0.5) debtors.push({name, amount: -v});
    });
    creditors.sort((a,b) => b.amount - a.amount);
    debtors.sort((a,b) => b.amount - a.amount);
    const result = [];
    let i = 0, j = 0;
    while(i < debtors.length && j < creditors.length){
      const d = debtors[i], c = creditors[j];
      const pay = Math.min(d.amount, c.amount);
      if(pay > 0.5) result.push({from: d.name, to: c.name, amount: pay});
      d.amount -= pay;
      c.amount -= pay;
      if(d.amount <= 0.5) i++;
      if(c.amount <= 0.5) j++;
    }
    return result;
  }
  function renderSettlements(){
    settleList.innerHTML = '';
    if(state.members.length === 0){
      settleList.innerHTML = '<div class="empty-note">メンバーと支払いを記録すると精算結果が表示されます</div>';
      return;
    }
    const settlements = computeSettlements();
    if(settlements.length === 0){
      settleList.innerHTML = `<div class="all-settled"><div class="stamp">SETTLED</div><div>全員の収支が精算済みです</div></div>`;
      return;
    }
    settlements.forEach(s => {
      const card = document.createElement('div');
      card.className = 'settle-ticket';
      card.innerHTML = `
        <div class="settle-flow">
          <span class="from">${escapeHtml(s.from)}</span>
          <span class="arrow">→</span>
          <span class="to">${escapeHtml(s.to)}</span>
        </div>
        <div class="settle-amt">${fmtJPY(s.amount)}</div>
      `;
      settleList.appendChild(card);
    });
  }

  function renderAll(){
    renderMembers();
    renderExpenses();
    renderBalances();
    renderSettlements();
  }

  // ---- events ----
  addMemberForm.addEventListener('submit', (e) => {
    e.preventDefault();
    const name = newMemberName.value.trim();
    if(!name) return;
    if(state.members.includes(name)){ alert('同じ名前のメンバーが既にいます'); return; }
    state.members.push(name);
    newMemberName.value = '';
    renderAll();
    save();
  });

  fetchRateBtn.addEventListener('click', fetchLatestRate);
  saveRateBtn.addEventListener('click', () => {
    const v = parseFloat(rateInput.value);
    if(!v || v <= 0){ alert('正しいレートを入力してください'); return; }
    state.exchangeRate = v;
    renderRateNote();
    save();
  });

  searchInput.addEventListener('input', renderExpenses);
  categoryFilter.addEventListener('change', renderExpenses);
  personFilter.addEventListener('change', renderExpenses);
  resetFilterBtn.addEventListener('click', () => {
    searchInput.value = '';
    categoryFilter.value = '';
    personFilter.value = '';
    renderExpenses();
  });

  expenseForm.addEventListener('submit', (e) => {
    e.preventDefault();
    const payer = payerSelect.value;
    const description = descInput.value.trim();
    const category = categorySelect.value;
    const date = dateInput.value || todayStr();
    const participants = [...selectedParticipants];

    if(!payer){ alert('支払った人を選んでください'); return; }
    if(participants.length === 0){ alert('対象者を1人以上選んでください'); return; }

    let amount, customShares = null;
    if(splitMode === 'custom'){
      customShares = {};
      participants.forEach(p => { customShares[p] = customShareValues[p] || 0; });
      amount = participants.reduce((s,p) => s + customShares[p], 0);
      if(!amount || amount <= 0){ alert('各対象者の金額を入力してください'); return; }
    }else{
      amount = parseFloat(amountInput.value);
      if(!amount || amount <= 0){ alert('金額を正しく入力してください'); return; }
    }

    const rateUsed = currentCurrency === 'EUR' ? state.exchangeRate : null;

    if(editingId){
      const idx = state.expenses.findIndex(e => e.id === editingId);
      if(idx !== -1){
        state.expenses[idx] = {
          ...state.expenses[idx],
          date, category, payer, description,
          currency: currentCurrency, amount, rateUsed,
          splitMode, participants, customShares
        };
      }
      cancelEdit();
    }else{
      state.expenses.push({
        id: uid(), date, category, payer, description,
        currency: currentCurrency, amount, rateUsed,
        splitMode, participants, customShares
      });
      amountInput.value = '';
      descInput.value = '';
      customShareValues = {};
      renderCustomShareBox();
    }
    renderAll();
    save();
  });

  (async function init(){
    fillCategorySelects();
    dateInput.value = todayStr();
    await load();
    rateInput.value = state.exchangeRate;
    renderRateNote();
    renderAll();
    setInterval(async () => {
      try{
        const res = await fetch(SCRIPT_URL);
        const parsed = await res.json();
        if(parsed && Array.isArray(parsed.members) && Array.isArray(parsed.expenses)){
          const changed = JSON.stringify(parsed) !== JSON.stringify(state);
          if(changed && !editingId){
            state = parsed;
            if(!state.exchangeRate) state.exchangeRate = DEFAULT_RATE;
            renderAll();
          }
        }
      }catch(e){ /* 次回のポーリングに任せる */ }
    }, 4000);
  })();
})();
</script>