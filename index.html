<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>SkyCast Weather</title>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@200;300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --sky1: #0a1d33; --glass: rgba(255,255,255,0.06);
    --glass2: rgba(255,255,255,0.11); --border: rgba(255,255,255,0.11);
    --text: #e8f4ff; --muted: rgba(200,225,255,0.5);
    --accent: #5bc8f5; --accent2: #f5c842; --danger: #f57c5b; --radius: 26px;
  }
  html, body { min-height: 100vh; font-family: 'Outfit', sans-serif; color: var(--text); background: var(--sky1); overflow-x: hidden; }
  body::before {
    content: ''; position: fixed; inset: 0; z-index: -1;
    background: radial-gradient(ellipse 80% 60% at 20% 10%, rgba(30,111,160,0.5) 0%, transparent 60%),
                linear-gradient(160deg, #0a1d33 0%, #0f2c4a 50%, #1a3a5e 100%);
  }
  .stars { position: fixed; inset: 0; z-index: -1; pointer-events: none; overflow: hidden; }
  .star { position: absolute; width: 2px; height: 2px; background: rgba(255,255,255,0.55); border-radius: 50%; animation: twinkle var(--d,3s) var(--dl,0s) infinite alternate; }
  @keyframes twinkle { from{opacity:.1} to{opacity:.8} }
  .app { max-width: 1440px; margin: 0 auto; padding: 44px 32px 72px; }
  .header { display:flex; align-items:center; justify-content:space-between; gap:28px; margin-bottom:44px; flex-wrap:wrap; }
  .brand { font-size:34px; font-weight:700; color:var(--accent); }
  .brand span { color:var(--text); font-weight:300; }
  .search-row { display:flex; gap:20px; flex:1; max-width:580px; }
  .search-row input { flex:1; padding:18px 28px; background:var(--glass2); border:1px solid var(--border); border-radius:50px; color:var(--text); font-family:'Outfit',sans-serif; font-size:21px; outline:none; transition:border-color .2s; backdrop-filter:blur(12px); }
  .search-row input::placeholder { color:var(--muted); }
  .search-row input:focus { border-color:var(--accent); }
  .search-btn { padding:18px 36px; background:var(--accent); color:#0a1d33; border:none; border-radius:50px; font-family:'Outfit',sans-serif; font-size:21px; font-weight:600; cursor:pointer; transition:background .2s,transform .15s; white-space:nowrap; }
  .search-btn:hover { background:#7ed8f9; transform:translateY(-1px); }
  
  .grid { display:grid; grid-template-columns:1fr 1fr 1.5fr; gap:28px; margin-bottom: 28px; }
  .card { background:var(--glass); backdrop-filter:blur(20px); border:1px solid var(--border); border-radius:var(--radius); padding:38px; animation:fadeUp .5s ease both; }
  @keyframes fadeUp { from{opacity:0;transform:translateY(14px)} to{opacity:1;transform:none} }

  /* Clock */
  .card-clock { display:flex; flex-direction:column; align-items:center; justify-content:center; text-align:center; }
  .clock-time { font-size:84px; font-weight:200; letter-spacing:-.03em; line-height:1; font-variant-numeric:tabular-nums; }
  .colon { animation:blink 1s step-end infinite; color:var(--accent); }
  @keyframes blink { 50%{opacity:0} }
  .clock-ampm { font-size:20px; font-weight:600; color:var(--accent); letter-spacing:.1em; margin-top:12px; }
  .clock-date { font-size:17px; color:var(--muted); margin-top:16px; letter-spacing:.04em; text-transform:uppercase; }
  .analog-wrap { margin-top:28px; position:relative; width:136px; height:136px; }
  .clock-face { width:100%; height:100%; border-radius:50%; border:2px solid var(--border); background:rgba(255,255,255,0.03); position:relative; overflow:hidden; }
  .hand { position:absolute; bottom:50%; left:50%; transform-origin:bottom center; border-radius:4px; }
  .hand-hour { width:3px; height:36px; background:var(--text); margin-left:-1.5px; }
  .hand-min  { width:2px; height:48px; background:var(--accent); margin-left:-1px; }
  .hand-sec  { width:1px; height:52px; background:var(--danger); margin-left:-.5px; }
  .clock-center { position:absolute; top:50%; left:50%; width:10px; height:10px; background:var(--accent); border-radius:50%; transform:translate(-50%,-50%); z-index:5; }
  .tick { position:absolute; top:4px; left:50%; width:1px; height:7px; background:var(--border); transform-origin:50% 64px; margin-left:-.5px; }
  .tick.major { height:14px; background:var(--muted); width:2px; margin-left:-1px; }

  /* Calendar */
  .card-calendar { padding:34px 28px; }
  .cal-header { display:flex; align-items:center; justify-content:space-between; margin-bottom:24px; }
  .cal-title { font-size:20px; font-weight:600; }
  .cal-nav { display:flex; gap:10px; }
  .cal-nav button { width:42px; height:42px; background:var(--glass2); border:1px solid var(--border); border-radius:12px; color:var(--text); font-size:18px; cursor:pointer; display:flex; align-items:center; justify-content:center; }
  .cal-nav button:hover { background:rgba(255,255,255,.2); }
  .cal-grid { display:grid; grid-template-columns:repeat(7,1fr); gap:8px; text-align:center; }
  .cal-dow { font-size:12px; font-weight:600; letter-spacing:.07em; color:var(--muted); text-transform:uppercase; padding:8px 0 10px; }
  .cal-day { font-size:16px; color:var(--muted); width:40px; height:40px; border-radius:12px; display:flex; align-items:center; justify-content:center; cursor:pointer; margin:0 auto; transition:background .15s,color .15s; position:relative; }
  .cal-day:hover { background:var(--glass2); color:var(--text); }
  .cal-day.other-month { opacity:.22; }
  .cal-day.today { background:var(--accent); color:#0a1d33; font-weight:700; }
  .cal-day.selected { background:rgba(91,200,245,.22); color:var(--accent); font-weight:600; border:1px solid rgba(91,200,245,.35); }
  .cal-day.has-weather::after { content:'•'; position:absolute; bottom:1px; font-size:11px; color:var(--accent2); }

  /* Current weather expanded with all metrics */
  .card-current { display:flex; flex-direction:column; justify-content:center; }
  .empty-state { display:none; flex-direction:column; align-items:center; justify-content:center; gap:20px; min-height:240px; color:var(--muted); font-size:19px; }
  .empty-state .icon { font-size:60px; opacity:.5; }
  .loading-state { display:flex; flex-direction:column; align-items:center; justify-content:center; gap:20px; min-height:240px; color:var(--muted); font-size:18px; }
  .error-state { display:none; flex-direction:column; align-items:center; justify-content:center; gap:20px; min-height:240px; color:var(--danger); font-size:18px; text-align:center; line-height:1.5; }
  .error-state .icon { font-size:48px; }
  .spinner { width:48px; height:48px; border:5px solid var(--border); border-top-color:var(--accent); border-radius:50%; animation:spin .7s linear infinite; }
  @keyframes spin { to{transform:rotate(360deg)} }
  .current-city { font-size:18px; text-transform:uppercase; letter-spacing:.14em; color:var(--muted); margin-bottom:10px; }
  .current-temp-wrap { display:flex; align-items: baseline; gap: 16px; }
  .current-temp { font-size:96px; font-weight:200; line-height:1; letter-spacing:-.04em; }
  .current-temp sup { font-size:38px; font-weight:400; vertical-align:super; }
  .current-desc { font-size:22px; font-weight:500; color:var(--accent); margin:14px 0 28px; }
  .current-meta { display:grid; grid-template-columns:1fr 1fr; gap:18px; }
  .meta-item { background:var(--glass2); border-radius:16px; padding:16px 22px; }
  .meta-item .lbl { font-size:12px; color:var(--muted); margin-bottom:6px; letter-spacing:.06em; text-transform:uppercase; }
  .meta-item .val { font-size:19px; font-weight:600; display:flex; align-items: center; gap: 6px; }

  /* Forecast */
  .card-forecast { margin-bottom:28px; }
  .forecast-title { font-size:16px; text-transform:uppercase; letter-spacing:.14em; color:var(--muted); margin-bottom:24px; }
  .forecast-grid { display:grid; grid-template-columns:repeat(7,1fr); gap:20px; }
  .fc-card { background:var(--glass2); border-radius:22px; padding:22px 14px; text-align:center; border:1px solid var(--border); transition:background .2s,transform .2s,border-color .2s; }
  .fc-card:hover { background:rgba(255,255,255,.14); transform:translateY(-3px); border-color:rgba(91,200,245,.3); }
  .fc-card.today-fc { border-color:rgba(91,200,245,.45); background:rgba(91,200,245,.09); }
  .fc-day  { font-size:14px; font-weight:600; letter-spacing:.07em; text-transform:uppercase; color:var(--muted); margin-bottom:12px; }
  .fc-icon { font-size:38px; margin-bottom:12px; }
  .fc-max  { font-size:24px; font-weight:600; }
  .fc-min  { font-size:15px; color:var(--muted); margin-top:6px; }
  .fc-desc { font-size:13px; color:var(--muted); margin-top:10px; line-height:1.5; }
  .tbar-wrap { height:6px; background:rgba(255,255,255,.09); border-radius:3px; margin:12px 0 8px; overflow:hidden; }
  .tbar { height:100%; border-radius:3px; background:linear-gradient(90deg,var(--accent),var(--accent2)); }

  /* Hourly Forecast Grid */
  .hourly-title { font-size:16px; text-transform:uppercase; letter-spacing:.14em; color:var(--muted); margin-bottom:24px; }
  .hourly-grid { display:grid; grid-template-columns:repeat(6,1fr); gap:20px; }
  .hr-card { background:var(--glass2); border-radius:22px; padding:22px 14px; text-align:center; border:1px solid var(--border); }
  .hr-time { font-size:14px; font-weight:600; letter-spacing:.07em; text-transform:uppercase; color:var(--muted); margin-bottom:12px; }
  .hr-temp { font-size:24px; font-weight:600; }
  .hr-desc { font-size:13px; color:var(--muted); margin-top:10px; line-height:1.5; }

  @media(max-width:1024px){
    .grid{grid-template-columns:1fr 1fr; grid-row:auto;}
    .card-current{grid-column:1/-1;}
    .forecast-grid{grid-template-columns:repeat(4,1fr); gap:12px;}
    .hourly-grid{grid-template-columns:repeat(3,1fr); gap:12px;}
  }
  @media(max-width:560px){
    .grid{grid-template-columns:1fr;}
    .forecast-grid{grid-template-columns:repeat(2,1fr);}
    .hourly-grid{grid-template-columns:repeat(2,1fr);}
    .clock-time{font-size:62px;}
    .current-temp{font-size:74px;}
    .search-row{max-width:100%;}
    .header{flex-direction:column;align-items:stretch;}
  }
</style>
</head>
<body>

<div class="stars" id="stars"></div>

<div class="app">
  <div class="header">
    <div class="brand">sky<span>cast</span></div>
    <div class="search-row">
      <input type="text" id="cityInput" value="Juja" placeholder="Search city…" onkeydown="if(event.key==='Enter')getWeather()"/>
      <button class="search-btn" onclick="getWeather()">Search</button>
    </div>
  </div>

  <div class="grid">
    <div class="card card-clock">
      <div class="clock-time"><span id="hours">00</span><span class="colon">:</span><span id="minutes">00</span></div>
      <div class="clock-ampm" id="ampm">AM</div>
      <div class="clock-date" id="dateString">Tuesday, May 5</div>
      <div class="analog-wrap">
        <div class="clock-face">
          <div class="tick"></div>
          <div class="tick" style="transform:rotate(30deg)"></div>
          <div class="tick major" style="transform:rotate(60deg)"></div>
          <div class="tick" style="transform:rotate(90deg)"></div>
          <div class="tick" style="transform:rotate(120deg)"></div>
          <div class="tick major" style="transform:rotate(150deg)"></div>
          <div class="tick" style="transform:rotate(180deg)"></div>
          <div class="tick" style="transform:rotate(210deg)"></div>
          <div class="tick major" style="transform:rotate(240deg)"></div>
          <div class="tick" style="transform:rotate(270deg)"></div>
          <div class="tick" style="transform:rotate(300deg)"></div>
          <div class="tick major" style="transform:rotate(330deg)"></div>
          <div class="hand hand-hour" id="hHand"></div>
          <div class="hand hand-min" id="mHand"></div>
          <div class="hand hand-sec" id="sHand"></div>
          <div class="clock-center"></div>
        </div>
      </div>
    </div>

    <div class="card card-calendar">
      <div class="cal-header">
        <div class="cal-title">May 2026</div>
        <div class="cal-nav">
          <button onclick="prevMonth()">‹</button>
          <button onclick="nextMonth()">›</button>
        </div>
      </div>
      <div class="cal-grid">
        <div class="cal-dow">Su</div>
        <div class="cal-dow">Mo</div>
        <div class="cal-dow">Tu</div>
        <div class="cal-dow">We</div>
        <div class="cal-dow">Th</div>
        <div class="cal-dow">Fr</div>
        <div class="cal-dow">Sa</div>
      </div>
      <div class="cal-grid" id="calDays"></div>
    </div>

    <div class="card card-current">
      <div id="loadingState" class="loading-state">
        <div class="spinner"></div>
        <div>Updating weather data for Juja...</div>
      </div>
      <div id="weatherContent" style="display:none;">
        <div class="current-city" id="weatherCity">Juja</div>
        <div class="current-temp-wrap">
          <div class="current-temp"><span id="weatherTemp">22</span><sup>°</sup>C</div>
          <div class="current-desc" id="weatherDesc">Partly Cloudy</div>
        </div>
        
        <div class="current-meta" style="margin-top: 24px;">
          <div class="meta-item">
            <div class="lbl">Humidity</div>
            <div class="val" id="weatherHumidity">💧 84%</div>
          </div>
          <div class="meta-item">
            <div class="lbl">Wind</div>
            <div class="val" id="weatherWind">🌬️ 7 km/h</div>
          </div>
          <div class="meta-item">
            <div class="lbl">UV Index</div>
            <div class="val">☀️ 3 of 10</div>
          </div>
          <div class="meta-item">
            <div class="lbl">Air Quality</div>
            <div class="val">🟢 Good</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="card card-forecast">
    <div class="forecast-title">Monday to Sunday Forecast</div>
    <div class="forecast-grid">
      <div class="fc-card today-fc">
        <div class="fc-day">Mon</div>
        <div class="fc-icon">⛅</div>
        <div class="fc-max">25°</div>
        <div class="fc-min">16°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 60%;"></div></div>
        <div class="fc-desc">Partly Cloudy</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 7 km/h</div>
      </div>
      <div class="fc-card">
        <div class="fc-day">Tue</div>
        <div class="fc-icon">⛅</div>
        <div class="fc-max">26°</div>
        <div class="fc-min">16°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 64%;"></div></div>
        <div class="fc-desc">Partly Cloudy</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 8 km/h</div>
      </div>
      <div class="fc-card">
        <div class="fc-day">Wed</div>
        <div class="fc-icon">🌧️</div>
        <div class="fc-max">24°</div>
        <div class="fc-min">16°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 56%;"></div></div>
        <div class="fc-desc">Scattered Showers</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 11 km/h</div>
      </div>
      <div class="fc-card">
        <div class="fc-day">Thu</div>
        <div class="fc-icon">🌧️</div>
        <div class="fc-max">23°</div>
        <div class="fc-min">15°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 52%;"></div></div>
        <div class="fc-desc">Showers</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 6 km/h</div>
      </div>
      <div class="fc-card">
        <div class="fc-day">Fri</div>
        <div class="fc-icon">☀️</div>
        <div class="fc-max">25°</div>
        <div class="fc-min">16°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 60%;"></div></div>
        <div class="fc-desc">Mostly Sunny</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 8 km/h</div>
      </div>
      <div class="fc-card">
        <div class="fc-day">Sat</div>
        <div class="fc-icon">⛅</div>
        <div class="fc-max">26°</div>
        <div class="fc-min">17°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 64%;"></div></div>
        <div class="fc-desc">Partly Cloudy</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 9 km/h</div>
      </div>
      <div class="fc-card">
        <div class="fc-day">Sun</div>
        <div class="fc-icon">🌦️</div>
        <div class="fc-max">25°</div>
        <div class="fc-min">16°</div>
        <div class="tbar-wrap"><div class="tbar" style="width: 60%;"></div></div>
        <div class="fc-desc">Light Rain</div>
        <div style="font-size: 13px; margin-top: 6px; color: var(--muted)">💨 8 km/h</div>
      </div>
    </div>
  </div>

  <div class="card">
    <div class="hourly-title">Hourly Forecast</div>
    <div class="hourly-grid">
      <div class="hr-card">
        <div class="hr-time">06:00 AM</div>
        <div class="hr-temp">17°C</div>
        <div class="hr-desc">Cloudy</div>
      </div>
      <div class="hr-card">
        <div class="hr-time">09:00 AM</div>
        <div class="hr-temp">20°C</div>
        <div class="hr-desc">Light Fog</div>
      </div>
      <div class="hr-card">
        <div class="hr-time">12:00 PM</div>
        <div class="hr-temp">25°C</div>
        <div class="hr-desc">Partly Cloudy</div>
      </div>
      <div class="hr-card">
        <div class="hr-time">03:00 PM</div>
        <div class="hr-temp">26°C</div>
        <div class="hr-desc">Sunny Intervals</div>
      </div>
      <div class="hr-card">
        <div class="hr-time">06:00 PM</div>
        <div class="hr-temp">21°C</div>
        <div class="hr-desc">Increasing Clouds</div>
      </div>
      <div class="hr-card">
        <div class="hr-time">09:00 PM</div>
        <div class="hr-temp">19°C</div>
        <div class="hr-desc">Cool & Humid</div>
      </div>
    </div>
  </div>
</div>

<script>
  // Clock Logic
  function updateClock() {
    const d = new Date();
    let h = d.getHours();
    const m = d.getMinutes();
    const s = d.getSeconds();
    const ampm = h >= 12 ? 'PM' : 'AM';
    h = h % 12; h = h ? h : 12;

    document.getElementById('hours').innerText = String(h).padStart(2, '0');
    document.getElementById('minutes').innerText = String(m).padStart(2, '0');
    document.getElementById('ampm').innerText = ampm;

    // Analog Hands
    const hDeg = (h % 12) * 30 + m * 0.5;
    const mDeg = m * 6;
    const sDeg = s * 6;
    document.getElementById('hHand').style.transform = `rotate(${hDeg}deg)`;
    document.getElementById('mHand').style.transform = `rotate(${mDeg}deg)`;
    document.getElementById('sHand').style.transform = `rotate(${sDeg}deg)`;
  }
  setInterval(updateClock, 1000);
  updateClock();

  // Calendar Logic
  let currentMonth = new Date().getMonth();
  let currentYear = new Date().getFullYear();
  function renderCalendar() {
    const date = new Date(currentYear, currentMonth, 1);
    const firstDay = date.getDay();
    const daysInMonth = new Date(currentYear, currentMonth + 1, 0).getDate();
    
    const container = document.getElementById('calDays');
    container.innerHTML = '';
    
    for (let i = 0; i < firstDay; i++) {
      const cell = document.createElement('div');
      cell.className = 'cal-day other-month';
      container.appendChild(cell);
    }
    
    const today = new Date();
    // Months mapping
    const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
    document.querySelector('.cal-title').innerText = `${months[currentMonth]} ${currentYear}`;

    for (let day = 1; day <= daysInMonth; day++) {
      const cell = document.createElement('div');
      cell.className = 'cal-day';
      cell.innerText = day;
      if (day === today.getDate() && currentMonth === today.getMonth() && currentYear === today.getFullYear()) {
        cell.classList.add('today');
      } else {
        cell.onclick = function() {
          const allCells = document.querySelectorAll('.cal-day');
          allCells.forEach(c => c.classList.remove('selected'));
          this.classList.add('selected');
        };
      }
      container.appendChild(cell);
    }
  }
  function prevMonth() { currentMonth--; if (currentMonth < 0) { currentMonth = 11; currentYear--; } renderCalendar(); }
  function nextMonth() { currentMonth++; if (currentMonth > 11) { currentMonth = 0; currentYear++; } renderCalendar(); }
  renderCalendar();

  // Background stars effect
  const starsContainer = document.getElementById('stars');
  for (let i = 0; i < 40; i++) {
    const star = document.createElement('div');
    star.className = 'star';
    star.style.left = `${Math.random() * 100}%`;
    star.style.top = `${Math.random() * 100}%`;
    star.style.setProperty('--d', `${1.5 + Math.random() * 3.5}s`);
    star.style.setProperty('--dl', `${Math.random() * 2}s`);
    starsContainer.appendChild(star);
  }

  // Update dates
  const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
  const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
  const today = new Date();
  document.getElementById('dateString').innerText = `${days[today.getDay()]}, ${months[today.getMonth()]} ${today.getDate()}`;

  function getWeather() {
    const cityInput = document.getElementById('cityInput').value.trim() || "Juja";
    document.getElementById('weatherContent').style.display = 'none';
    document.getElementById('loadingState').style.display = 'flex';

    setTimeout(() => {
      document.getElementById('weatherCity').innerText = cityInput;
      // Generate varying weather data based on city name for visual effect
      const hash = cityInput.split('').reduce((acc, char) => acc + char.charCodeAt(0), 0);
      document.getElementById('weatherTemp').innerText = 18 + (hash % 10);
      const conditions = ["Partly Cloudy", "Sunny", "Light Rain", "Mostly Clear", "Scattered Showers"];
      document.getElementById('weatherDesc').innerText = conditions[hash % conditions.length];
      
      const humidities = ["💧 65%", "💧 72%", "💧 84%", "💧 55%"];
      document.getElementById('weatherHumidity').innerText = humidities[hash % humidities.length];
      
      const winds = ["🌬️ 5 km/h", "🌬️ 9 km/h", "🌬️ 14 km/h", "🌬️ 7 km/h"];
      document.getElementById('weatherWind').innerText = winds[hash % winds.length];

      document.getElementById('loadingState').style.display = 'none';
      document.getElementById('weatherContent').style.display = 'block';
    }, 1200);
  }

  // Run weather once to set initial load
  getWeather();
</script>

</body>
</html>
