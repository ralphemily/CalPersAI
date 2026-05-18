<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>CalPERS — Performance & Investigations AI</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
:root {
  --navy: #0a2240;
  --navy-light: #0e2d54;
  --navy-hover: #163a6b;
  --blue: #1a5fa8;
  --blue-light: #2878d4;
  --accent: #e8f2fd;
  --red: #c0392b;
  --red-bg: #fdecea;
  --orange: #d35400;
  --orange-bg: #fef0e6;
  --yellow: #b7950b;
  --yellow-bg: #fef9e7;
  --green: #1e8449;
  --green-bg: #eafaf1;
  --green-light: #27ae60;
  --text: #1a1a2e;
  --text-muted: #6b7280;
  --text-light: #9ca3af;
  --border: #e5e7eb;
  --bg: #f3f6fb;
  --white: #ffffff;
  --sidebar-w: 220px;
  --header-h: 56px;
  --ai-w: 300px;
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);font-size:13px;height:100vh;overflow:hidden;display:flex;flex-direction:column}

/* ── TOPBAR ── */
.topbar{height:var(--header-h);background:var(--navy);display:flex;align-items:center;padding:0 16px;gap:12px;flex-shrink:0;z-index:100}
.logo-area{display:flex;align-items:center;gap:10px;width:var(--sidebar-w);flex-shrink:0}
.logo-icon{width:32px;height:32px;background:white;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:var(--navy)}
.logo-text{line-height:1.2}
.logo-text .t1{font-size:13px;font-weight:600;color:white}
.logo-text .t2{font-size:10px;color:rgba(255,255,255,0.55);font-weight:400}
.search-wrap{flex:1;margin:0 auto;position:relative}
.search-wrap input{width:100%;padding:7px 12px 7px 34px;border-radius:8px;border:none;background:rgba(255,255,255,0.12);color:white;font-size:12px;font-family:inherit;outline:none}
.search-wrap input::placeholder{color:rgba(255,255,255,0.45)}
.search-wrap::before{content:'🔍';position:absolute;left:10px;top:50%;transform:translateY(-50%);font-size:12px;opacity:0.5}
.topbar-right{display:flex;align-items:center;gap:4px;margin-left:auto}
.tb-icon{position:relative;width:36px;height:36px;border-radius:8px;display:flex;align-items:center;justify-content:center;cursor:pointer;color:rgba(255,255,255,0.7);transition:background 0.15s;flex-direction:column;gap:1px}
.tb-icon:hover{background:rgba(255,255,255,0.1);color:white}
.tb-icon .icon-label{font-size:9px;color:rgba(255,255,255,0.5)}
.tb-badge{position:absolute;top:4px;right:4px;background:#e74c3c;color:white;font-size:9px;font-weight:700;border-radius:999px;min-width:14px;height:14px;display:flex;align-items:center;justify-content:center;padding:0 3px}
.user-chip{display:flex;align-items:center;gap:8px;margin-left:8px;padding:4px 10px;border-radius:8px;cursor:pointer;transition:background 0.15s}
.user-chip:hover{background:rgba(255,255,255,0.1)}
.user-avatar{width:28px;height:28px;border-radius:50%;background:var(--blue-light);display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:white}
.user-info .name{font-size:12px;font-weight:500;color:white}
.user-info .role{font-size:10px;color:rgba(255,255,255,0.5)}

/* ── BODY LAYOUT ── */
.body-layout{display:flex;flex:1;overflow:hidden}

/* ── SIDEBAR ── */
.sidebar{width:var(--sidebar-w);background:var(--navy);display:flex;flex-direction:column;flex-shrink:0;overflow-y:auto;padding-bottom:12px}
.sidebar::-webkit-scrollbar{display:none}
.nav-item{display:flex;align-items:center;gap:9px;padding:8px 14px;font-size:12.5px;color:rgba(255,255,255,0.6);cursor:pointer;transition:all 0.15s;position:relative;border-radius:0}
.nav-item:hover{background:rgba(255,255,255,0.07);color:rgba(255,255,255,0.9)}
.nav-item.active{background:rgba(255,255,255,0.13);color:white;font-weight:500}
.nav-item.active::before{content:'';position:absolute;left:0;top:0;bottom:0;width:3px;background:#4da6ff;border-radius:0 2px 2px 0}
.nav-badge{margin-left:auto;background:#e74c3c;color:white;font-size:9px;font-weight:700;border-radius:999px;min-width:18px;height:18px;display:flex;align-items:center;justify-content:center;padding:0 4px}
.nav-badge.blue{background:var(--blue-light)}
.nav-icon{font-size:14px;width:18px;text-align:center;flex-shrink:0}
.nav-divider{height:1px;background:rgba(255,255,255,0.08);margin:6px 14px}
.nav-section{font-size:10px;color:rgba(255,255,255,0.3);letter-spacing:0.07em;text-transform:uppercase;padding:10px 14px 4px;font-weight:500}
.sidebar-footer{margin-top:auto;padding:12px 14px;border-top:1px solid rgba(255,255,255,0.1)}
.sys-status{background:rgba(255,255,255,0.06);border-radius:8px;padding:10px 12px}
.sys-title{font-size:10px;color:rgba(255,255,255,0.4);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:4px}
.sys-ok{font-size:12px;color:#2ecc71;font-weight:500}
.sys-meta{font-size:10px;color:rgba(255,255,255,0.3);margin-top:4px;line-height:1.6}

/* ── MAIN ── */
.main{flex:1;overflow-y:auto;padding:20px 22px;display:flex;flex-direction:column;gap:16px}
.main::-webkit-scrollbar{width:5px}
.main::-webkit-scrollbar-thumb{background:#d1d5db;border-radius:999px}

.page-title{font-size:18px;font-weight:600;color:var(--text)}
.page-sub{font-size:12px;color:var(--text-muted);margin-top:2px}
.page-hdr{display:flex;align-items:flex-start;justify-content:space-between}
.cust-btn{display:flex;align-items:center;gap:6px;padding:7px 12px;border-radius:8px;border:1px solid var(--border);background:white;font-size:12px;cursor:pointer;color:var(--text-muted);font-family:inherit}
.cust-btn:hover{background:var(--bg)}

/* stats */
.stats-row{display:grid;grid-template-columns:repeat(6,1fr);gap:10px}
.stat{background:white;border:1px solid var(--border);border-radius:10px;padding:12px 14px;cursor:pointer;transition:box-shadow 0.15s}
.stat:hover{box-shadow:0 2px 8px rgba(0,0,0,0.08)}
.stat-icon{font-size:16px;margin-bottom:6px}
.stat-label{font-size:10px;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.04em;font-weight:500}
.stat-num{font-size:26px;font-weight:700;color:var(--text);line-height:1.1;margin:3px 0}
.stat-link{font-size:11px;color:var(--blue);cursor:pointer}
.stat-link:hover{text-decoration:underline}

/* priority queue */
.section-hdr{display:flex;align-items:center;justify-content:space-between}
.section-title{font-size:14px;font-weight:600;color:var(--text)}
.view-all{font-size:12px;color:var(--blue);cursor:pointer;display:flex;align-items:center;gap:4px}
.view-all:hover{text-decoration:underline}

.card{background:white;border:1px solid var(--border);border-radius:12px;overflow:hidden}
.table{width:100%;border-collapse:collapse}
.table th{text-align:left;padding:9px 12px;font-size:11px;font-weight:600;color:var(--text-muted);background:#f9fafb;border-bottom:1px solid var(--border);text-transform:uppercase;letter-spacing:0.04em;white-space:nowrap}
.table td{padding:11px 12px;border-bottom:1px solid #f3f4f6;vertical-align:middle}
.table tr:last-child td{border-bottom:none}
.table tr:hover td{background:#fafbfd;cursor:pointer}
.risk-badge{display:inline-flex;align-items:center;justify-content:center;padding:3px 9px;border-radius:5px;font-size:10px;font-weight:700;letter-spacing:0.04em;text-transform:uppercase}
.risk-critical{background:var(--red-bg);color:var(--red);border:1px solid #f5b7b1}
.risk-high{background:var(--orange-bg);color:var(--orange);border:1px solid #fad7a0}
.risk-medium{background:var(--yellow-bg);color:var(--yellow);border:1px solid #f9e79f}
.risk-low{background:var(--green-bg);color:var(--green);border:1px solid #a9dfbf}
.case-link{color:var(--blue);font-weight:500;font-family:'DM Mono',monospace;font-size:12px;cursor:pointer}
.case-link:hover{text-decoration:underline}
.emp-name{font-weight:500;font-size:13px;color:var(--text)}
.emp-role{font-size:11px;color:var(--text-muted)}
.deadline-date{font-weight:500;color:var(--text)}
.deadline-days{font-size:11px}
.deadline-days.overdue{color:var(--red)}
.deadline-days.soon{color:var(--orange)}
.deadline-days.ok{color:var(--green)}
.prog-wrap{width:80px}
.prog-bar{height:4px;background:#e5e7eb;border-radius:999px;overflow:hidden;margin-top:4px}
.prog-fill{height:100%;border-radius:999px}
.prog-label{font-size:11px;color:var(--text-muted)}
.owner-name{font-size:12px;font-weight:500}
.more-btn{width:28px;height:28px;border-radius:6px;display:flex;align-items:center;justify-content:center;color:var(--text-muted);cursor:pointer;transition:background 0.15s}
.more-btn:hover{background:var(--bg)}

/* risk legend */
.risk-legend{display:flex;align-items:center;gap:12px;padding:8px 12px;background:#f9fafb;border-top:1px solid var(--border)}
.legend-item{display:flex;align-items:center;gap:5px;font-size:11px;color:var(--text-muted)}
.legend-dot{width:8px;height:8px;border-radius:50%}

/* bottom row */
.bottom-row{display:grid;grid-template-columns:1fr 1fr 1fr;gap:14px}
.bottom-card{background:white;border:1px solid var(--border);border-radius:12px;padding:14px}
.bc-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px}
.bc-title{font-size:13px;font-weight:600;color:var(--text)}
.bc-link{font-size:11px;color:var(--blue);cursor:pointer}

/* deadlines */
.deadline-item{display:flex;align-items:flex-start;gap:10px;padding:7px 0;border-bottom:1px solid #f3f4f6}
.deadline-item:last-child{border-bottom:none}
.dl-cal{width:32px;height:32px;border-radius:7px;display:flex;flex-direction:column;align-items:center;justify-content:center;flex-shrink:0;font-size:8px;font-weight:700;text-transform:uppercase;line-height:1.1}
.dl-cal .day{font-size:14px;font-weight:700;line-height:1}
.dl-red{background:#fdecea;color:#c0392b}
.dl-orange{background:#fef0e6;color:#d35400}
.dl-blue{background:#e8f2fd;color:#1a5fa8}
.dl-info .title{font-size:12px;font-weight:500;color:var(--text)}
.dl-info .meta{font-size:11px;color:var(--text-muted);margin-top:1px}
.dl-overdue{font-size:10px;color:var(--red);font-weight:600}

/* compliance donut */
.donut-wrap{display:flex;align-items:center;gap:16px;margin-bottom:12px}
.donut-svg{flex-shrink:0}
.donut-center{text-align:center}
.donut-pct{font-size:22px;font-weight:700;color:var(--text)}
.donut-label{font-size:10px;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.05em}
.comp-items{display:flex;flex-direction:column;gap:5px;flex:1}
.comp-row{display:flex;align-items:center;justify-content:space-between;font-size:11px}
.comp-name{color:var(--text-muted);display:flex;align-items:center;gap:5px}
.comp-name::before{content:'';width:6px;height:6px;border-radius:50%;background:currentColor;flex-shrink:0}
.comp-status{font-weight:500}
.comp-done{color:var(--green)}
.comp-pending{color:var(--yellow)}
.comp-overdue{color:var(--red)}

/* pie / donut chart */
.pie-wrap{display:flex;align-items:center;gap:14px}
.pie-legend{display:flex;flex-direction:column;gap:5px;flex:1}
.pie-row{display:flex;align-items:center;gap:6px;font-size:11px;color:var(--text-muted)}
.pie-dot{width:10px;height:10px;border-radius:2px;flex-shrink:0}

/* recent activity */
.activity-row{display:flex;align-items:flex-start;gap:8px;padding:6px 0;border-bottom:1px solid #f3f4f6;font-size:11px}
.activity-row:last-child{border-bottom:none}
.act-icon{font-size:13px;flex-shrink:0;margin-top:1px}
.act-text{color:var(--text)}
.act-bold{font-weight:500}
.act-meta{color:var(--text-muted);margin-top:2px}

/* ── AI PANEL ── */
.ai-panel{width:var(--ai-w);flex-shrink:0;background:white;border-left:1px solid var(--border);display:flex;flex-direction:column;overflow:hidden}
.ai-hdr{padding:12px 14px 0;border-bottom:1px solid var(--border)}
.ai-title-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px}
.ai-title{display:flex;align-items:center;gap:7px;font-size:14px;font-weight:600;color:var(--text)}
.ai-star{color:#f59e0b;font-size:15px}
.ai-beta{font-size:9px;font-weight:700;background:#e8f2fd;color:var(--blue);padding:2px 6px;border-radius:4px;letter-spacing:0.05em}
.ai-close{width:24px;height:24px;border-radius:5px;display:flex;align-items:center;justify-content:center;cursor:pointer;color:var(--text-muted);font-size:14px}
.ai-close:hover{background:var(--bg)}
.ai-tabs{display:flex;gap:0}
.ai-tab{padding:7px 12px;font-size:12px;color:var(--text-muted);cursor:pointer;border-bottom:2px solid transparent;transition:all 0.15s;font-weight:500}
.ai-tab:hover{color:var(--text)}
.ai-tab.active{color:var(--blue);border-bottom-color:var(--blue)}
.ai-body{flex:1;overflow-y:auto;padding:12px 14px;display:flex;flex-direction:column;gap:8px}
.ai-body::-webkit-scrollbar{width:4px}
.ai-body::-webkit-scrollbar-thumb{background:#e5e7eb;border-radius:999px}
.ai-msg{display:flex;gap:8px}
.ai-avatar{width:28px;height:28px;border-radius:50%;background:linear-gradient(135deg,#1a5fa8,#2878d4);display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:14px}
.ai-bubble{background:#f8fafc;border:1px solid var(--border);border-radius:10px;padding:10px 12px;font-size:12.5px;line-height:1.6;color:var(--text)}
.ai-bubble ul{padding-left:14px;margin-top:5px}
.ai-bubble li{margin-bottom:2px;color:var(--text-muted)}
.ai-quick{display:flex;flex-direction:column;gap:5px;padding:8px 14px;border-top:1px solid var(--border);border-bottom:1px solid var(--border)}
.quick-btn{text-align:left;padding:8px 10px;border-radius:8px;border:1px solid var(--border);background:#f9fafb;font-size:11.5px;color:var(--text);cursor:pointer;font-family:inherit;transition:all 0.15s;line-height:1.4}
.quick-btn:hover{background:#e8f2fd;border-color:#bfdbfe;color:var(--blue)}
.ai-footer{padding:10px 14px;border-top:1px solid var(--border);display:flex;flex-direction:column;gap:6px}
.ai-input-row{display:flex;gap:6px;align-items:center}
.ai-input{flex:1;padding:8px 10px;border:1px solid var(--border);border-radius:8px;font-size:12px;font-family:inherit;outline:none;color:var(--text)}
.ai-input:focus{border-color:var(--blue);box-shadow:0 0 0 3px rgba(26,95,168,0.1)}
.ai-send{width:32px;height:32px;border-radius:8px;background:var(--blue);border:none;color:white;font-size:14px;cursor:pointer;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.ai-send:hover{background:var(--blue-light)}
.ai-disclaimer{font-size:10px;color:var(--text-light);line-height:1.4;display:flex;align-items:flex-start;gap:4px}
.ai-footer-links{display:flex;justify-content:space-between}
.ai-flink{font-size:11px;color:var(--blue);cursor:pointer;display:flex;align-items:center;gap:4px}

/* bottom bar */
.bottombar{height:32px;background:var(--navy);display:flex;align-items:center;justify-content:space-between;padding:0 20px;flex-shrink:0}
.bb-left{font-size:11px;color:rgba(255,255,255,0.5)}
.bb-center{display:flex;gap:16px}
.bb-link{font-size:10px;color:rgba(255,255,255,0.4);cursor:pointer}
.bb-link:hover{color:rgba(255,255,255,0.7)}
.bb-right{font-size:11px;color:rgba(255,255,255,0.4);display:flex;align-items:center;gap:5px}
.bb-lock{color:#2ecc71}
</style>
</head>
<body>

<!-- TOPBAR -->
<div class="topbar">
  <div class="logo-area">
    <div class="logo-icon">▲</div>
    <div class="logo-text">
      <div class="t1">CalPERS</div>
      <div class="t2">Performance &amp; Investigations AI</div>
    </div>
  </div>
  <div class="search-wrap">
    <input type="text" placeholder="Search cases, employees, policies, documents..."/>
  </div>
  <div class="topbar-right">
    <div class="tb-icon">🔔<span class="tb-badge">5</span><span class="icon-label">Alerts</span></div>
    <div class="tb-icon">💬<span class="tb-badge" style="background:#2878d4">3</span><span class="icon-label">Messages</span></div>
    <div class="tb-icon">❓<span class="icon-label">Help</span></div>
    <div class="user-chip">
      <div class="user-avatar">JD</div>
      <div class="user-info">
        <div class="name">Jane Doe</div>
        <div class="role">Senior Investigator</div>
      </div>
      <span style="color:rgba(255,255,255,0.4);font-size:11px;margin-left:2px">▾</span>
    </div>
  </div>
</div>

<!-- BODY -->
<div class="body-layout">

  <!-- SIDEBAR -->
  <div class="sidebar">
    <div class="nav-item active"><span class="nav-icon">⊞</span> Dashboard</div>
    <div class="nav-item"><span class="nav-icon">📋</span> Active Cases <span class="nav-badge">42</span></div>
    <div class="nav-item"><span class="nav-icon">✓</span> Closed Cases</div>
    <div class="nav-item"><span class="nav-icon">⚠</span> High-Risk Cases <span class="nav-badge">8</span></div>
    <div class="nav-divider"></div>
    <div class="nav-item"><span class="nav-icon">🔍</span> Compliance Monitoring <span class="nav-badge blue">5</span></div>
    <div class="nav-item"><span class="nav-icon">✦</span> AI Draft Assistant</div>
    <div class="nav-item"><span class="nav-icon">⚖</span> Legal Knowledge Center</div>
    <div class="nav-item"><span class="nav-icon">📅</span> Deadlines &amp; Calendar <span class="nav-badge">13</span></div>
    <div class="nav-divider"></div>
    <div class="nav-item"><span class="nav-icon">🗂</span> Evidence Repository</div>
    <div class="nav-item"><span class="nav-icon">👥</span> Personnel &amp; Contacts</div>
    <div class="nav-item"><span class="nav-icon">📊</span> Reports &amp; Analytics</div>
    <div class="nav-item"><span class="nav-icon">📄</span> Audit Logs</div>
    <div class="nav-divider"></div>
    <div class="nav-item"><span class="nav-icon">⚙</span> Settings &amp; Permissions</div>
    <div class="sidebar-footer">
      <div class="sys-status">
        <div class="sys-title">System Status</div>
        <div class="sys-ok">● All Systems Operational</div>
        <div class="sys-meta">Last Login: May 7, 2026 8:15 AM<br/>IP: 192.168.1.14</div>
      </div>
    </div>
  </div>

  <!-- MAIN -->
  <div class="main">

    <!-- Header -->
    <div class="page-hdr">
      <div>
        <div class="page-title">Dashboard Overview</div>
        <div class="page-sub">Welcome back, Jane.</div>
      </div>
      <button class="cust-btn">⚙ Customize Dashboard</button>
    </div>

    <!-- Stats -->
    <div class="stats-row">
      <div class="stat">
        <div class="stat-icon">📋</div>
        <div class="stat-label">Active Cases</div>
        <div class="stat-num">42</div>
        <div class="stat-link">View all active cases →</div>
      </div>
      <div class="stat">
        <div class="stat-icon" style="color:var(--orange)">⚠</div>
        <div class="stat-label">High Risk</div>
        <div class="stat-num" style="color:var(--orange)">8</div>
        <div class="stat-link">View high risk cases →</div>
      </div>
      <div class="stat">
        <div class="stat-icon">📅</div>
        <div class="stat-label">Deadlines This Week</div>
        <div class="stat-num">13</div>
        <div class="stat-link">View my deadlines →</div>
      </div>
      <div class="stat">
        <div class="stat-icon" style="color:var(--red)">🕐</div>
        <div class="stat-label">Overdue Actions</div>
        <div class="stat-num" style="color:var(--red)">3</div>
        <div class="stat-link">View overdue items →</div>
      </div>
      <div class="stat">
        <div class="stat-icon">🚩</div>
        <div class="stat-label">Compliance Flags</div>
        <div class="stat-num">5</div>
        <div class="stat-link">View compliance issues →</div>
      </div>
      <div class="stat">
        <div class="stat-icon">👤</div>
        <div class="stat-label">Open Investigations</div>
        <div class="stat-num">17</div>
        <div class="stat-link">View investigations →</div>
      </div>
    </div>

    <!-- Priority Queue -->
    <div>
      <div class="section-hdr" style="margin-bottom:10px">
        <div class="section-title">Priority Case Queue</div>
        <div class="view-all">View All Cases →</div>
      </div>
      <div class="card">
        <table class="table">
          <thead>
            <tr>
              <th style="width:90px">Risk</th>
              <th style="width:100px">Case ID</th>
              <th>Employee / Subject</th>
              <th>Issue Type</th>
              <th>Division</th>
              <th>Deadline</th>
              <th style="width:130px">Status</th>
              <th>Owner</th>
              <th style="width:36px"></th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><span class="risk-badge risk-critical">Critical</span></td>
              <td><span class="case-link">PI-2026-018</span></td>
              <td><div class="emp-name">John Smith</div><div class="emp-role">Specialist, IT Services</div></td>
              <td>Retaliation</td>
              <td>IT Services Division</td>
              <td><div class="deadline-date">May 9, 2026</div><div class="deadline-days overdue">2 days overdue</div></td>
              <td>
                <div class="prog-label">Interview Phase</div>
                <div class="prog-bar"><div class="prog-fill" style="width:55%;background:#1a5fa8"></div></div>
              </td>
              <td class="owner-name">Jane Doe</td>
              <td><div class="more-btn">⋯</div></td>
            </tr>
            <tr>
              <td><span class="risk-badge risk-high">High</span></td>
              <td><span class="case-link">PI-2026-031</span></td>
              <td><div class="emp-name">Alexandra Doe</div><div class="emp-role">Analyst, Health Policy</div></td>
              <td>Harassment</td>
              <td>Health Policy &amp; Planning</td>
              <td><div class="deadline-date">May 12, 2026</div><div class="deadline-days soon">5 days</div></td>
              <td>
                <div class="prog-label">Evidence Review</div>
                <div class="prog-bar"><div class="prog-fill" style="width:35%;background:#d35400"></div></div>
              </td>
              <td class="owner-name">Michael Lee</td>
              <td><div class="more-btn">⋯</div></td>
            </tr>
            <tr>
              <td><span class="risk-badge risk-medium">Medium</span></td>
              <td><span class="case-link">PI-2026-027</span></td>
              <td><div class="emp-name">Michael Lee</div><div class="emp-role">Retirement Specialist</div></td>
              <td>Attendance</td>
              <td>Member Services Division</td>
              <td><div class="deadline-date">May 17, 2026</div><div class="deadline-days ok">10 days</div></td>
              <td>
                <div class="prog-label">Drafting</div>
                <div class="prog-bar"><div class="prog-fill" style="width:70%;background:#27ae60"></div></div>
              </td>
              <td class="owner-name">Sarah Chen</td>
              <td><div class="more-btn">⋯</div></td>
            </tr>
            <tr>
              <td><span class="risk-badge risk-medium">Medium</span></td>
              <td><span class="case-link">PI-2026-033</span></td>
              <td><div class="emp-name">Taylor Johnson</div><div class="emp-role">Benefits Analyst</div></td>
              <td>Performance</td>
              <td>Benefits Division</td>
              <td><div class="deadline-date">May 20, 2026</div><div class="deadline-days ok">13 days</div></td>
              <td>
                <div class="prog-label">Intake</div>
                <div class="prog-bar"><div class="prog-fill" style="width:15%;background:#b7950b"></div></div>
              </td>
              <td class="owner-name">David Brown</td>
              <td><div class="more-btn">⋯</div></td>
            </tr>
            <tr>
              <td><span class="risk-badge risk-low">Low</span></td>
              <td><span class="case-link">PI-2026-041</span></td>
              <td><div class="emp-name">Jordan Patel</div><div class="emp-role">Accounting Officer</div></td>
              <td>Misconduct</td>
              <td>Finance Division</td>
              <td><div class="deadline-date">May 26, 2026</div><div class="deadline-days ok">19 days</div></td>
              <td>
                <div class="prog-label">Intake</div>
                <div class="prog-bar"><div class="prog-fill" style="width:8%;background:#27ae60"></div></div>
              </td>
              <td class="owner-name">Lisa Wong</td>
              <td><div class="more-btn">⋯</div></td>
            </tr>
          </tbody>
        </table>
        <div class="risk-legend">
          <span style="font-size:11px;color:var(--text-muted);font-weight:500;margin-right:4px">Risk Levels:</span>
          <div class="legend-item"><div class="legend-dot" style="background:var(--red)"></div> Critical</div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--orange)"></div> High</div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--yellow)"></div> Medium</div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--green-light)"></div> Low</div>
        </div>
      </div>
    </div>

    <!-- Bottom Row -->
    <div class="bottom-row">

      <!-- My Deadlines -->
      <div class="bottom-card">
        <div class="bc-hdr">
          <div class="bc-title">My Deadlines</div>
          <div class="bc-link">View Calendar →</div>
        </div>
        <div class="deadline-item">
          <div class="dl-cal dl-red"><span style="font-size:8px">MAY</span><span class="day">9</span></div>
          <div class="dl-info">
            <div class="title">Interview w/ Witness: R. Martinez</div>
            <div class="meta">PI-2026-018 · <span class="dl-overdue">2 days overdue</span></div>
          </div>
        </div>
        <div class="deadline-item">
          <div class="dl-cal dl-orange"><span style="font-size:8px">MAY</span><span class="day">12</span></div>
          <div class="dl-info">
            <div class="title">Skelly Meeting</div>
            <div class="meta">PI-2026-031 · 5 days</div>
          </div>
        </div>
        <div class="deadline-item">
          <div class="dl-cal dl-blue"><span style="font-size:8px">MAY</span><span class="day">15</span></div>
          <div class="dl-info">
            <div class="title">Draft Findings Report</div>
            <div class="meta">PI-2026-018 · 8 days</div>
          </div>
        </div>
        <div class="deadline-item">
          <div class="dl-cal dl-blue"><span style="font-size:8px">MAY</span><span class="day">17</span></div>
          <div class="dl-info">
            <div class="title">Management Review</div>
            <div class="meta">PI-2026-027 · 10 days</div>
          </div>
        </div>
      </div>

      <!-- Compliance Health -->
      <div class="bottom-card">
        <div class="bc-hdr">
          <div class="bc-title">Compliance Health</div>
          <div class="bc-link">View Compliance →</div>
        </div>
        <div class="donut-wrap">
          <svg class="donut-svg" width="80" height="80" viewBox="0 0 80 80">
            <circle cx="40" cy="40" r="30" fill="none" stroke="#e5e7eb" stroke-width="10"/>
            <circle cx="40" cy="40" r="30" fill="none" stroke="#27ae60" stroke-width="10"
              stroke-dasharray="118.4 188.5" stroke-dashoffset="47.1" stroke-linecap="round" transform="rotate(-90 40 40)"/>
            <circle cx="40" cy="40" r="30" fill="none" stroke="#e74c3c" stroke-width="10"
              stroke-dasharray="47.1 188.5" stroke-dashoffset="-71.3" stroke-linecap="round" transform="rotate(-90 40 40)"/>
            <text x="40" y="37" text-anchor="middle" font-size="14" font-weight="700" fill="#1a1a2e" font-family="DM Sans">78%</text>
            <text x="40" y="48" text-anchor="middle" font-size="8" fill="#6b7280" font-family="DM Sans">At Risk</text>
          </svg>
          <div class="comp-items">
            <div class="comp-row"><span class="comp-name" style="color:var(--green)">Witness interviews</span><span class="comp-status comp-done">Completed</span></div>
            <div class="comp-row"><span class="comp-name" style="color:var(--green)">Required approvals</span><span class="comp-status comp-done">Completed</span></div>
            <div class="comp-row"><span class="comp-name" style="color:var(--yellow)">Skelly reviews</span><span class="comp-status comp-pending">Pending</span></div>
            <div class="comp-row"><span class="comp-name" style="color:var(--red)">Retention reviews</span><span class="comp-status comp-overdue">Overdue</span></div>
            <div class="comp-row"><span class="comp-name" style="color:var(--green)">Legal notifications</span><span class="comp-status comp-done">Completed</span></div>
          </div>
        </div>
      </div>

      <!-- Case Status Distribution -->
      <div class="bottom-card">
        <div class="bc-hdr">
          <div class="bc-title">Case Status Distribution</div>
          <div class="bc-link">View Reports →</div>
        </div>
        <div class="pie-wrap">
          <svg width="90" height="90" viewBox="0 0 90 90">
            <circle cx="45" cy="45" r="38" fill="none" stroke="#1a5fa8" stroke-width="20" stroke-dasharray="71.6 167.6" stroke-dashoffset="0" transform="rotate(-90 45 45)"/>
            <circle cx="45" cy="45" r="38" fill="none" stroke="#27ae60" stroke-width="20" stroke-dasharray="52.3 167.6" stroke-dashoffset="-71.6" transform="rotate(-90 45 45)"/>
            <circle cx="45" cy="45" r="38" fill="none" stroke="#f59e0b" stroke-width="20" stroke-dasharray="41.9 167.6" stroke-dashoffset="-123.9" transform="rotate(-90 45 45)"/>
            <circle cx="45" cy="45" r="38" fill="none" stroke="#e74c3c" stroke-width="20" stroke-dasharray="25.1 167.6" stroke-dashoffset="-165.8" transform="rotate(-90 45 45)"/>
            <circle cx="45" cy="45" r="38" fill="none" stroke="#9ca3af" stroke-width="20" stroke-dasharray="25.1 167.6" stroke-dashoffset="-190.9" transform="rotate(-90 45 45)"/>
            <text x="45" y="41" text-anchor="middle" font-size="16" font-weight="700" fill="#1a1a2e" font-family="DM Sans">42</text>
            <text x="45" y="52" text-anchor="middle" font-size="8" fill="#6b7280" font-family="DM Sans">Total</text>
          </svg>
          <div class="pie-legend">
            <div class="pie-row"><div class="pie-dot" style="background:#1a5fa8"></div>Interview Phase — 12 (29%)</div>
            <div class="pie-row"><div class="pie-dot" style="background:#27ae60"></div>Evidence Review — 9 (21%)</div>
            <div class="pie-row"><div class="pie-dot" style="background:#f59e0b"></div>Drafting — 7 (17%)</div>
            <div class="pie-row"><div class="pie-dot" style="background:#e74c3c"></div>Intake — 8 (19%)</div>
            <div class="pie-row"><div class="pie-dot" style="background:#9ca3af"></div>Closed — 6 (14%)</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Recent Activity -->
    <div>
      <div class="section-hdr" style="margin-bottom:10px">
        <div class="section-title">Recent Activity</div>
        <div class="view-all">View All Activity →</div>
      </div>
      <div class="card" style="padding:6px 14px">
        <div class="activity-row">
          <div class="act-icon">📄</div>
          <div>
            <div class="act-text">Document uploaded: <span class="act-bold">Interview_Notes_RMartinez.pdf</span></div>
            <div class="act-meta">PI-2026-018 · Jane Doe · May 7, 2026 10:15 AM</div>
          </div>
        </div>
        <div class="activity-row">
          <div class="act-icon">🔄</div>
          <div>
            <div class="act-text">Case status updated to <span class="act-bold">Interview Phase</span></div>
            <div class="act-meta">PI-2026-031 · Michael Lee · May 7, 2026 9:42 AM</div>
          </div>
        </div>
        <div class="activity-row">
          <div class="act-icon">📅</div>
          <div>
            <div class="act-text">Deadline updated: <span class="act-bold">Skelly Meeting</span></div>
            <div class="act-meta">PI-2026-031 · May 7, 2026 9:30 AM</div>
          </div>
        </div>
      </div>
    </div>

  </div><!-- /main -->

  <!-- AI PANEL -->
  <div class="ai-panel">
    <div class="ai-hdr">
      <div class="ai-title-row">
        <div class="ai-title"><span class="ai-star">✦</span> AI Assistant <span class="ai-beta">BETA</span></div>
        <div class="ai-close">✕</div>
      </div>
      <div class="ai-tabs">
        <div class="ai-tab active">Chat</div>
        <div class="ai-tab">Draft</div>
        <div class="ai-tab">Research</div>
        <div class="ai-tab">Lookup</div>
      </div>
    </div>
    <div class="ai-body" id="ai-body">
      <div class="ai-msg">
        <div class="ai-avatar">✦</div>
        <div class="ai-bubble">
          Hello Jane, how can I assist you today?<br/><br/>I can help you with:
          <ul>
            <li>Drafting documents</li>
            <li>Legal and policy questions</li>
            <li>Case summaries</li>
            <li>Finding information</li>
            <li>Locating contacts</li>
            <li>Compliance guidance</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="ai-quick">
      <button class="quick-btn" onclick="sendQuick('Summarize case PI-2026-018')">Summarize case PI-2026-018</button>
      <button class="quick-btn" onclick="sendQuick('What are the requirements for a Skelly meeting?')">What are the requirements for a Skelly meeting?</button>
      <button class="quick-btn" onclick="sendQuick('Draft an interview question list')">Draft an interview question list</button>
      <button class="quick-btn" onclick="sendQuick('Find similar retaliation cases')">Find similar retaliation cases</button>
      <button class="quick-btn" onclick="sendQuick('Who can approve disciplinary action?')">Who can approve disciplinary action?</button>
    </div>
    <div class="ai-footer">
      <div class="ai-input-row">
        <input class="ai-input" id="ai-input" type="text" placeholder="Ask a question..." onkeydown="if(event.key==='Enter')sendAI()"/>
        <button class="ai-send" onclick="sendAI()">➤</button>
      </div>
      <div class="ai-disclaimer">⚠ AI-generated responses may contain errors. Verify important information.</div>
      <div class="ai-footer-links">
        <div class="ai-flink">📎 View Sources</div>
        <div class="ai-flink">🗑 Clear Chat</div>
      </div>
    </div>
  </div>

</div><!-- /body-layout -->

<!-- BOTTOM BAR -->
<div class="bottombar">
  <div class="bb-left">CalPERS Performance &amp; Investigations AI System</div>
  <div class="bb-center">
    <span class="bb-link">Privacy &amp; Security</span>
    <span class="bb-link">Terms of Use</span>
    <span class="bb-link">Accessibility</span>
    <span class="bb-link">Contact HR Support</span>
  </div>
  <div class="bb-right"><span class="bb-lock">🔒</span> © 2026 CalPERS. All rights reserved. &nbsp;|&nbsp; Secure Connection</div>
</div>

<script>
const R = {
  'summarize case pi-2026-018': 'Case PI-2026-018 Summary\n\nEmployee: John Smith, IT Services\nIssue: Retaliation complaint filed March 14, 2026\nStatus: Interview Phase — currently 2 days overdue\n\nKey facts: Complainant alleges adverse action following a protected disclosure. Three witnesses identified. R. Martinez interview notes uploaded today.\n\nNext step: Complete witness interviews and proceed to findings draft by May 15.',
  'what are the requirements for a skelly meeting': 'A Skelly meeting (Skelly v. State Personnel Board) is required before imposing major discipline in California civil service. Requirements:\n\n1. Written notice of proposed action with specific charges\n2. Copy of all materials relied upon\n3. Opportunity for employee to respond orally or in writing\n4. Response period of at least 5 business days\n5. Decision-maker must be someone with authority to impose discipline\n\nCalPERS policy requires HR and legal sign-off before scheduling.',
  'draft an interview question list': 'Interview Question List — Retaliation Investigation\n\n1. Describe your working relationship with [Subject] prior to the incident.\n2. When did you first notice a change in treatment?\n3. Did you make any protected disclosures or complaints before the alleged retaliation?\n4. Can you describe specific incidents with dates, times, and witnesses?\n5. Were there any other employees who witnessed or experienced similar treatment?\n6. Did you report the conduct to anyone? What was the response?\n7. How has this affected your work environment and performance?\n\nNote: Consult legal before adding case-specific questions.',
  'find similar retaliation cases': 'Similar Retaliation Cases (Last 24 months)\n\n• PI-2024-007 — IT Division, substantiated, settled\n• PI-2024-019 — Member Services, unsubstantiated\n• PI-2025-003 — Finance Division, substantiated, disciplinary action taken\n• PI-2025-041 — Health Policy, pending\n\nPattern note: 3 of 4 similar cases involved supervisor-level subjects. Recommend reviewing supervisor training records for PI-2026-018.',
  'who can approve disciplinary action': 'Disciplinary Action Approval — CalPERS Authority Matrix\n\n• Written reprimand: Division Chief\n• Suspension (1–5 days): Deputy Director + HR\n• Suspension (6+ days): Executive Director + HR + Legal\n• Demotion or dismissal: Executive Director + Legal + CalHR notification\n\nFor union-represented employees, additional union notification requirements apply per MOU. Contact Employee Relations before finalizing any action above written reprimand.'
};

function getReply(m) {
  const k = m.toLowerCase().replace(/[?]/g,'').trim();
  for (const r in R) {
    const words = r.split(' ');
    if (words.filter(w => k.includes(w) && w.length > 3).length >= 2) return R[r];
  }
  return "I've reviewed the available information. For this specific query, I recommend consulting the Legal Knowledge Center or escalating to your supervisor if compliance risk is identified. Would you like me to draft a communication or look up a specific policy?";
}

function addMsg(text, isUser) {
  const body = document.getElementById('ai-body');
  const wrap = document.createElement('div');
  wrap.className = 'ai-msg' + (isUser ? '' : '');
  wrap.style.cssText = isUser ? 'justify-content:flex-end' : '';
  if (!isUser) {
    const av = document.createElement('div');
    av.className = 'ai-avatar'; av.textContent = '✦';
    wrap.appendChild(av);
  }
  const bubble = document.createElement('div');
  bubble.className = 'ai-bubble';
  bubble.style.cssText = isUser ? 'background:#e8f2fd;border-color:#bfdbfe;max-width:85%' : '';
  bubble.style.whiteSpace = 'pre-wrap';
  bubble.textContent = text;
  wrap.appendChild(bubble);
  body.appendChild(wrap);
  body.scrollTop = body.scrollHeight;
}

function addTyping() {
  const body = document.getElementById('ai-body');
  const w = document.createElement('div'); w.className = 'ai-msg'; w.id = 'typing';
  const av = document.createElement('div'); av.className = 'ai-avatar'; av.textContent = '✦';
  const b = document.createElement('div'); b.className = 'ai-bubble';
  b.innerHTML = '<span style="display:flex;gap:4px;align-items:center"><span style="animation:blink 1.2s infinite;background:#9ca3af;width:6px;height:6px;border-radius:50%;display:inline-block"></span><span style="animation:blink 1.2s infinite 0.2s;background:#9ca3af;width:6px;height:6px;border-radius:50%;display:inline-block"></span><span style="animation:blink 1.2s infinite 0.4s;background:#9ca3af;width:6px;height:6px;border-radius:50%;display:inline-block"></span></span>';
  w.appendChild(av); w.appendChild(b); body.appendChild(w);
  body.scrollTop = body.scrollHeight;
}

function sendAI() {
  const inp = document.getElementById('ai-input');
  const txt = inp.value.trim(); if (!txt) return;
  inp.value = ''; addMsg(txt, true); addTyping();
  setTimeout(() => {
    const t = document.getElementById('typing'); if (t) t.remove();
    addMsg(getReply(txt), false);
  }, 800 + Math.random() * 400);
}

function sendQuick(t) {
  document.getElementById('ai-input').value = t; sendAI();
}

const style = document.createElement('style');
style.textContent = '@keyframes blink{0%,80%,100%{opacity:0.2}40%{opacity:1}}';
document.head.appendChild(style);
</script>
</body>
</html>
