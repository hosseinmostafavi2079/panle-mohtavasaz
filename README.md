<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>مستندات کامل — SaaS Platform Gemini</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700&display=swap');

:root {
  --bg: #0d1117;
  --bg2: #161b22;
  --bg3: #1c2128;
  --bg4: #21262d;
  --border: #30363d;
  --border2: #484f58;
  --text: #e6edf3;
  --text2: #8b949e;
  --text3: #6e7681;
  --accent: #2f81f7;
  --accent-bg: rgba(47,129,247,.12);
  --accent-border: rgba(47,129,247,.3);
  --green: #3fb950;
  --green-bg: rgba(63,185,80,.12);
  --green-border: rgba(63,185,80,.3);
  --amber: #d29922;
  --amber-bg: rgba(210,153,34,.12);
  --amber-border: rgba(210,153,34,.3);
  --red: #f85149;
  --red-bg: rgba(248,81,73,.12);
  --red-border: rgba(248,81,73,.3);
  --purple: #a371f7;
  --purple-bg: rgba(163,113,247,.12);
  --cyan: #39d353;
  --teal: #2dd4bf;
  --teal-bg: rgba(45,212,191,.1);
}

* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }

body {
  font-family: 'Vazirmatn', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.75;
  font-size: 15px;
}

/* Sidebar */
.layout { display: flex; min-height: 100vh; }

.sidebar {
  width: 260px;
  flex-shrink: 0;
  background: var(--bg2);
  border-left: 1px solid var(--border);
  position: sticky;
  top: 0;
  height: 100vh;
  overflow-y: auto;
  padding: 0 0 40px 0;
}

.sidebar-logo {
  padding: 20px 20px 16px;
  border-bottom: 1px solid var(--border);
  margin-bottom: 12px;
}
.sidebar-logo .logo-mark {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 13px;
  font-weight: 600;
  color: var(--text);
}
.logo-icon {
  width: 28px; height: 28px;
  background: var(--accent);
  border-radius: 7px;
  display: flex; align-items: center; justify-content: center;
}
.logo-icon svg { display: block; }
.sidebar-subtitle { font-size: 11px; color: var(--text3); margin-top: 4px; }

.sidebar-group { margin-bottom: 4px; padding: 0 8px; }
.sidebar-group-label {
  font-size: 10px;
  font-weight: 600;
  color: var(--text3);
  letter-spacing: .8px;
  text-transform: uppercase;
  padding: 8px 12px 4px;
}
.sidebar-link {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 7px 12px;
  border-radius: 6px;
  font-size: 13px;
  color: var(--text2);
  text-decoration: none;
  transition: all .15s;
}
.sidebar-link:hover { background: var(--bg3); color: var(--text); }
.sidebar-link.active { background: var(--accent-bg); color: var(--accent); }
.sidebar-link .dot {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: currentColor;
  flex-shrink: 0;
}

/* Main content */
.main {
  flex: 1;
  padding: 40px 64px 80px;
  max-width: 920px;
}

/* Hero */
.hero {
  margin-bottom: 48px;
  padding-bottom: 32px;
  border-bottom: 1px solid var(--border);
}
.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  background: var(--accent-bg);
  border: 1px solid var(--accent-border);
  color: var(--accent);
  font-size: 11px;
  font-weight: 600;
  padding: 3px 10px;
  border-radius: 20px;
  margin-bottom: 14px;
  letter-spacing: .3px;
}
.hero h1 {
  font-size: 32px;
  font-weight: 700;
  line-height: 1.3;
  letter-spacing: -.5px;
  margin-bottom: 12px;
  background: linear-gradient(135deg, #e6edf3 0%, #8b949e 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.hero-desc {
  font-size: 15px;
  color: var(--text2);
  max-width: 600px;
  line-height: 1.8;
}

/* Section */
section {
  margin-bottom: 56px;
  scroll-margin-top: 24px;
}
h2 {
  font-size: 22px;
  font-weight: 600;
  margin-bottom: 20px;
  color: var(--text);
  display: flex;
  align-items: center;
  gap: 10px;
  padding-bottom: 12px;
  border-bottom: 1px solid var(--border);
}
h2 .section-num {
  width: 28px; height: 28px;
  border-radius: 7px;
  background: var(--accent-bg);
  border: 1px solid var(--accent-border);
  color: var(--accent);
  font-size: 12px;
  font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
}
h3 {
  font-size: 16px;
  font-weight: 600;
  color: var(--text);
  margin: 24px 0 10px;
}
h4 {
  font-size: 14px;
  font-weight: 600;
  color: var(--text2);
  margin: 16px 0 8px;
  letter-spacing: .2px;
}
p { color: var(--text2); margin-bottom: 10px; }

/* Code */
pre {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 16px 18px;
  overflow-x: auto;
  font-size: 13px;
  font-family: 'Courier New', monospace;
  margin: 12px 0;
  direction: ltr;
  text-align: left;
  line-height: 1.6;
}
code {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 2px 6px;
  font-size: 12.5px;
  font-family: 'Courier New', monospace;
  color: #79c0ff;
  direction: ltr;
}
pre code {
  background: none;
  border: none;
  padding: 0;
  color: var(--text);
}
.comment { color: #6e7681; }
.string { color: #a5d6ff; }
.keyword { color: #ff7b72; }
.number { color: #79c0ff; }
.func { color: #d2a8ff; }

/* Step boxes */
.steps { display: flex; flex-direction: column; gap: 0; }
.step {
  display: flex;
  gap: 16px;
  padding: 0 0 24px 0;
  position: relative;
}
.step::before {
  content: '';
  position: absolute;
  right: 15px;
  top: 32px;
  bottom: 0;
  width: 1px;
  background: var(--border);
}
.step:last-child::before { display: none; }
.step-num {
  width: 32px; height: 32px;
  border-radius: 50%;
  background: var(--accent);
  color: #fff;
  font-size: 13px;
  font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
  position: relative;
  z-index: 1;
}
.step-content { flex: 1; padding-top: 4px; }
.step-title { font-size: 14px; font-weight: 600; color: var(--text); margin-bottom: 6px; }
.step-desc { font-size: 13px; color: var(--text2); line-height: 1.7; }

/* Alert boxes */
.alert {
  display: flex;
  gap: 12px;
  align-items: flex-start;
  padding: 14px 16px;
  border-radius: 8px;
  margin: 14px 0;
  border: 1px solid;
  font-size: 13px;
}
.alert-icon { font-size: 16px; flex-shrink: 0; margin-top: 1px; }
.alert-content { line-height: 1.7; }
.alert-title { font-weight: 600; margin-bottom: 3px; }

.alert-info { background: var(--accent-bg); border-color: var(--accent-border); color: var(--accent); }
.alert-info .alert-content { color: #8ab4f8; }
.alert-warn { background: var(--amber-bg); border-color: var(--amber-border); color: var(--amber); }
.alert-warn .alert-content { color: #d9b072; }
.alert-success { background: var(--green-bg); border-color: var(--green-border); color: var(--green); }
.alert-success .alert-content { color: #7ee8a2; }
.alert-danger { background: var(--red-bg); border-color: var(--red-border); color: var(--red); }
.alert-danger .alert-content { color: #f28b82; }

/* File tree */
.file-tree {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 16px 18px;
  font-family: 'Courier New', monospace;
  font-size: 13px;
  direction: ltr;
  text-align: left;
  line-height: 2;
}
.ft-dir { color: #79c0ff; }
.ft-file { color: var(--text2); }
.ft-comment { color: #6e7681; margin-right: 8px; }

/* Architecture diagram */
.arch-diagram {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 24px;
  margin: 16px 0;
}
.arch-row {
  display: flex;
  gap: 12px;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin-bottom: 12px;
}
.arch-box {
  padding: 10px 16px;
  border-radius: 8px;
  font-size: 12px;
  font-weight: 600;
  text-align: center;
  min-width: 100px;
}
.arch-box.blue { background: var(--accent-bg); border: 1px solid var(--accent-border); color: var(--accent); }
.arch-box.green { background: var(--green-bg); border: 1px solid var(--green-border); color: var(--green); }
.arch-box.amber { background: var(--amber-bg); border: 1px solid var(--amber-border); color: var(--amber); }
.arch-box.purple { background: var(--purple-bg); border: 1px solid rgba(163,113,247,.3); color: var(--purple); }
.arch-box.teal { background: var(--teal-bg); border: 1px solid rgba(45,212,191,.25); color: var(--teal); }
.arch-arrow {
  font-size: 18px;
  color: var(--text3);
}
.arch-label {
  font-size: 11px;
  color: var(--text3);
  text-align: center;
  margin: 4px 0 0;
}

/* Cards */
.card-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin: 16px 0; }
.info-card {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 16px;
}
.info-card-icon { font-size: 20px; margin-bottom: 8px; }
.info-card-title { font-size: 13px; font-weight: 600; color: var(--text); margin-bottom: 4px; }
.info-card-desc { font-size: 12px; color: var(--text2); line-height: 1.6; }

/* Table */
.doc-table {
  width: 100%;
  border-collapse: collapse;
  margin: 14px 0;
  font-size: 13px;
}
.doc-table th {
  background: var(--bg4);
  border: 1px solid var(--border);
  padding: 10px 14px;
  text-align: right;
  font-weight: 600;
  color: var(--text3);
  letter-spacing: .3px;
  font-size: 12px;
}
.doc-table td {
  border: 1px solid var(--border);
  padding: 10px 14px;
  color: var(--text2);
  vertical-align: top;
}
.doc-table tr:hover td { background: var(--bg3); }
.doc-table .mono { font-family: 'Courier New', monospace; color: #79c0ff; font-size: 12px; direction: ltr; }

/* Tags */
.tag {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  font-size: 11px;
  padding: 2px 8px;
  border-radius: 12px;
  font-weight: 500;
  margin: 2px;
}
.tag-blue { background: var(--accent-bg); color: var(--accent); border: 1px solid var(--accent-border); }
.tag-green { background: var(--green-bg); color: var(--green); border: 1px solid var(--green-border); }
.tag-amber { background: var(--amber-bg); color: var(--amber); border: 1px solid var(--amber-border); }
.tag-purple { background: var(--purple-bg); color: var(--purple); border: 1px solid rgba(163,113,247,.3); }
.tag-red { background: var(--red-bg); color: var(--red); border: 1px solid var(--red-border); }

/* Scrollbar */
::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }
::-webkit-scrollbar-thumb:hover { background: var(--border2); }

/* Responsive */
@media (max-width: 900px) {
  .sidebar { display: none; }
  .main { padding: 24px 24px 60px; max-width: 100%; }
  .card-grid { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<div class="layout">

<nav class="sidebar">
  <div class="sidebar-logo">
    <div class="logo-mark">
      <div class="logo-icon">
        <svg width="14" height="14" viewBox="0 0 16 16" fill="none">
          <rect x="1" y="1" width="6" height="6" rx="1.5" fill="white" opacity=".9"/>
          <rect x="9" y="1" width="6" height="6" rx="1.5" fill="white" opacity=".6"/>
          <rect x="1" y="9" width="6" height="6" rx="1.5" fill="white" opacity=".6"/>
          <rect x="9" y="9" width="6" height="6" rx="1.5" fill="white" opacity=".35"/>
        </svg>
      </div>
      SaaS Platform Gemini
    </div>
    <div class="sidebar-subtitle">مستندات کامل فارسی — نسخه ۱.۰</div>
  </div>

  <div class="sidebar-group">
    <div class="sidebar-group-label">شروع سریع</div>
    <a href="#overview" class="sidebar-link"><span class="dot"></span>معماری پروژه</a>
    <a href="#codebase" class="sidebar-link"><span class="dot"></span>آموزش کدبیس</a>
  </div>

  <div class="sidebar-group">
    <div class="sidebar-group-label">نصب و راه‌اندازی</div>
    <a href="#prerequisites" class="sidebar-link"><span class="dot"></span>پیش‌نیازها</a>
    <a href="#docker-setup" class="sidebar-link"><span class="dot"></span>نصب داکر</a>
    <a href="#project-setup" class="sidebar-link"><span class="dot"></span>راه‌اندازی پروژه</a>
    <a href="#env-config" class="sidebar-link"><span class="dot"></span>تنظیمات محیطی</a>
    <a href="#first-run" class="sidebar-link"><span class="dot"></span>اجرای اول</a>
  </div>

  <div class="sidebar-group">
    <div class="sidebar-group-label">آموزش کد</div>
    <a href="#models" class="sidebar-link"><span class="dot"></span>مدل‌های دیتابیس</a>
    <a href="#services" class="sidebar-link"><span class="dot"></span>لایه سرویس‌ها</a>
    <a href="#views" class="sidebar-link"><span class="dot"></span>ویوها و URLها</a>
    <a href="#templates" class="sidebar-link"><span class="dot"></span>تمپلیت‌ها</a>
    <a href="#admin" class="sidebar-link"><span class="dot"></span>پنل ادمین</a>
  </div>

  <div class="sidebar-group">
    <div class="sidebar-group-label">پروداکشن</div>
    <a href="#production" class="sidebar-link"><span class="dot"></span>آماده‌سازی پروداکشن</a>
    <a href="#troubleshoot" class="sidebar-link"><span class="dot"></span>رفع خطاها</a>
    <a href="#faq" class="sidebar-link"><span class="dot"></span>سوالات متداول</a>
  </div>
</nav>

<main class="main">

  <div class="hero">
    <div class="hero-badge">📚 داکیومنت جامع</div>
    <h1>مستندات کامل پلتفرم<br>مدیریت هوشمند محصولات</h1>
    <p class="hero-desc">
      این مستند راهنمای کامل برای درک معماری، نصب از صفر، و راه‌اندازی این پلتفرم SaaS مبتنی بر Django است.
      شامل توضیح کامل کدبیس، نحوه کارکرد Docker، و تمام نکات مهم برای دپلوی می‌باشد.
    </p>
    <div style="display:flex;gap:8px;margin-top:16px;flex-wrap:wrap">
      <span class="tag tag-blue">Django 6.x</span>
      <span class="tag tag-green">Docker</span>
      <span class="tag tag-amber">PostgreSQL</span>
      <span class="tag tag-purple">WooCommerce API</span>
      <span class="tag tag-blue">OpenAI Compatible</span>
    </div>
  </div>

  <section id="overview">
    <h2><span class="section-num">۱</span>معماری کلی پروژه</h2>

    <p>این پروژه یک پلتفرم SaaS چند-مستاجری (Multi-Tenant) است که به فروشگاه‌های ووکامرس اجازه می‌دهد با استفاده از هوش مصنوعی، محصولات را به صورت خودکار تولید و منتشر کنند.</p>

    <div class="arch-diagram">
      <div class="arch-row">
        <div class="arch-box blue">🌐 Browser / User</div>
      </div>
      <div class="arch-row"><div class="arch-arrow">↕</div></div>
      <div class="arch-row">
        <div class="arch-box green">🐍 Django App<br><small style="font-weight:400;font-size:10px">Port 8000</small></div>
      </div>
      <div class="arch-row"><div class="arch-arrow">↕</div></div>
      <div class="arch-row">
        <div class="arch-box amber">🗄️ PostgreSQL<br><small style="font-weight:400;font-size:10px">Port 5432</small></div>
        <div class="arch-box purple">🤖 AI API<br><small style="font-weight:400;font-size:10px">gapgpt.app</small></div>
        <div class="arch-box teal">🛒 WooCommerce<br><small style="font-weight:400;font-size:10px">REST API</small></div>
      </div>
      <div class="arch-label">همه چیز در Docker Compose اجرا می‌شود</div>
    </div>

    <h3>ساختار پوشه‌بندی</h3>
    <div class="file-tree">
<span class="ft-dir">saas_platform-gemini/</span><br>
├── <span class="ft-dir">config/</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># تنظیمات اصلی Django</span><br>
│   ├── <span class="ft-file">__init__.py</span><br>
│   ├── <span class="ft-file">urls.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># URL های اصلی</span><br>
│   ├── <span class="ft-file">wsgi.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># سرور پروداکشن</span><br>
│   └── <span class="ft-dir">settings/</span><br>
│       ├── <span class="ft-file">base.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># تنظیمات مشترک</span><br>
│       ├── <span class="ft-file">development.py</span> &nbsp;<span class="ft-comment"># SQLite, Debug=True</span><br>
│       └── <span class="ft-file">production.py</span> &nbsp;&nbsp;<span class="ft-comment"># PostgreSQL, Debug=False</span><br>
├── <span class="ft-dir">core/</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># اپ اصلی پلتفرم</span><br>
│   ├── <span class="ft-file">models.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># مدل‌های دیتابیس</span><br>
│   ├── <span class="ft-file">views.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># لاجیک اصلی</span><br>
│   ├── <span class="ft-file">urls.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># مسیرهای URL</span><br>
│   ├── <span class="ft-file">forms.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># فرم‌های Django</span><br>
│   ├── <span class="ft-file">admin.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># تنظیمات پنل ادمین</span><br>
│   ├── <span class="ft-dir">migrations/</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># تغییرات دیتابیس</span><br>
│   ├── <span class="ft-dir">services/</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># لایه سرویس</span><br>
│   │   ├── <span class="ft-file">ai.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># ارتباط با هوش مصنوعی</span><br>
│   │   ├── <span class="ft-file">woo.py</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># ارتباط با WooCommerce</span><br>
│   │   └── <span class="ft-file">access_control.py</span> <span class="ft-comment"># کنترل دسترسی و سهمیه</span><br>
│   └── <span class="ft-dir">templates/</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># فایل‌های HTML</span><br>
│       ├── <span class="ft-file">base.html</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># قالب پایه با Navbar</span><br>
│       ├── <span class="ft-file">login.html</span> &nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># صفحه ورود</span><br>
│       ├── <span class="ft-file">dashboard.html</span><br>
│       ├── <span class="ft-file">add_product.html</span><br>
│       └── <span class="ft-file">product_manager.html</span><br>
├── <span class="ft-file">Dockerfile</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># تعریف ایمیج داکر</span><br>
├── <span class="ft-file">docker-compose.yml</span> &nbsp;&nbsp;&nbsp;<span class="ft-comment"># تعریف سرویس‌ها</span><br>
├── <span class="ft-file">requirements.txt</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># کتابخانه‌های Python</span><br>
└── <span class="ft-file">.env</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="ft-comment"># متغیرهای محیطی (ساخته می‌شود)</span>
    </div>
  </section>

  <section id="codebase">
    <h2><span class="section-num">۲</span>آموزش کامل کدبیس</h2>

    <section id="models">
      <h3>📦 مدل‌های دیتابیس (models.py)</h3>
      <p>این فایل قلب سیستم چند-مستاجری است. ۶ مدل اصلی وجود دارد:</p>

      <div class="card-grid">
        <div class="info-card">
          <div class="info-card-icon">⭐</div>
          <div class="info-card-title">Feature</div>
          <div class="info-card-desc">قابلیت‌هایی که می‌توان به پلن‌ها اضافه کرد. مثال: <code>price_manager</code></div>
        </div>
        <div class="info-card">
          <div class="info-card-icon">💰</div>
          <div class="info-card-title">Plan</div>
          <div class="info-card-desc">پلن‌های اشتراکی (مثل پایه، حرفه‌ای). هر پلن می‌تواند چند Feature داشته باشد.</div>
        </div>
        <div class="info-card">
          <div class="info-card-icon">🏪</div>
          <div class="info-card-title">Store (مستاجر)</div>
          <div class="info-card-desc">هر فروشگاه یک مستاجر است با کلیدهای API اختصاصی خودش. مهم‌ترین مدل!</div>
        </div>
        <div class="info-card">
          <div class="info-card-icon">👤</div>
          <div class="info-card-title">UserProfile</div>
          <div class="info-card-desc">کاربران Django را به یک Store وصل می‌کند. نقش: admin یا operator</div>
        </div>
        <div class="info-card">
          <div class="info-card-icon">📝</div>
          <div class="info-card-title">ProductLog</div>
          <div class="info-card-desc">هر بار که محصولی ایجاد می‌شود، یک رکورد ثبت می‌کند. برای سهمیه‌بندی استفاده می‌شود.</div>
        </div>
        <div class="info-card">
          <div class="info-card-icon">🔗</div>
          <div class="info-card-title">InternalLink</div>
          <div class="info-card-desc">لینک‌های داخلی سایت هر فروشگاه که در تولید محتوای AI استفاده می‌شوند.</div>
        </div>
      </div>

      <h4>نحوه عملکرد Multi-Tenancy</h4>
      <p>هر کاربر یک <code>UserProfile</code> دارد که به یک <code>Store</code> وصل است. وقتی کاربر وارد می‌شود، سیستم ابتدا فروشگاه مربوطه را پیدا می‌کند و تمام عملیات‌ها (ارتباط با API، گزارش‌ها، سهمیه) مختص همان فروشگاه است.</p>

<pre><span class="comment"># نحوه خواندن فروشگاه در views.py</span>
user_profile = getattr(request.user, <span class="string">'profile'</span>, None)
<span class="keyword">if not</span> user_profile:
    messages.error(request, <span class="string">"حساب متصل به فروشگاهی نیست"</span>)
    <span class="keyword">return</span> redirect(<span class="string">'dashboard'</span>)
store = user_profile.store  <span class="comment"># این فروشگاه اختصاصی کاربر است</span></pre>
    </section>

    <section id="services">
      <h3>⚙️ لایه سرویس‌ها (services/)</h3>

      <h4>🤖 AIService (ai.py)</h4>
      <p>این سرویس با API هوش مصنوعی ارتباط برقرار می‌کند. از کلید API اختصاصی هر فروشگاه استفاده می‌کند:</p>

<pre><span class="comment"># ساختار اصلی AIService</span>
<span class="keyword">class</span> <span class="func">AIService</span>:
    <span class="keyword">def</span> <span class="func">__init__</span>(self, store):
        self.client = OpenAI(
            base_url=<span class="string">"https://api.gapgpt.app/v1"</span>,
            api_key=self.store.openai_api_key  <span class="comment"># کلید اختصاصی از DB</span>
        )
    
    <span class="keyword">def</span> <span class="func">generate_slug</span>(self, product_name): ...   <span class="comment"># URL سئو شده</span>
    <span class="keyword">def</span> <span class="func">generate_short_desc</span>(self, product_name): ... <span class="comment"># توضیح کوتاه</span>
    <span class="keyword">def</span> <span class="func">generate_long_desc</span>(self, product_name): ...  <span class="comment"># توضیح HTML کامل</span></pre>

      <div class="alert alert-info">
        <div class="alert-icon">💡</div>
        <div class="alert-content">
          <div class="alert-title">نکته مهم</div>
          توجه کنید که <code>base_url</code> در ai.py روی <code>api.gapgpt.app</code> تنظیم شده که یک پروکسی ایرانی OpenAI است. اگر بخواهید از OpenAI مستقیم استفاده کنید، این آدرس را حذف کنید.
        </div>
      </div>

      <h4>🛒 WooService (woo.py)</h4>
      <p>این سرویس تمام ارتباطات با WooCommerce REST API را مدیریت می‌کند:</p>

      <table class="doc-table">
        <thead><tr><th>متد</th><th>عملکرد</th></tr></thead>
        <tbody>
          <tr><td class="mono">get_categories()</td><td>دریافت تمام دسته‌بندی‌ها با pagination</td></tr>
          <tr><td class="mono">upload_image_to_wp()</td><td>آپلود تصویر به WordPress Media Library</td></tr>
          <tr><td class="mono">create_product()</td><td>ساخت محصول جدید در WooCommerce</td></tr>
          <tr><td class="mono">get_products_filtered()</td><td>دریافت محصولات با فیلتر و pagination</td></tr>
          <tr><td class="mono">batch_update_prices()</td><td>تغییر قیمت گروهی یک دسته‌بندی</td></tr>
          <tr><td class="mono">update_product()</td><td>ویرایش یک محصول خاص</td></tr>
        </tbody>
      </table>

      <h4>🔐 AccessControlService (access_control.py)</h4>
      <p>سیستم کنترل سهمیه و دسترسی بر اساس پلن:</p>

<pre><span class="comment"># بررسی اینکه آیا فروشگاه به یک قابلیت دسترسی دارد</span>
AccessControlService.has_feature(store, <span class="string">'price_manager'</span>)

<span class="comment"># بررسی اینکه سهمیه ماهانه پر نشده</span>
AccessControlService.can_add_product(store)

<span class="comment"># تعداد محصول باقیمانده در ماه</span>
AccessControlService.get_remaining_quota(store)</pre>
    </section>

    <section id="views">
      <h3>🖥️ ویوها (views.py)</h3>
      <p>سه ویوی اصلی وجود دارد:</p>

      <h4>dashboard()</h4>
      <p>آمار ماه جاری (سهمیه باقیمانده) و ۱۰ عملیات آخر فروشگاه را نشان می‌دهد.</p>

      <h4>add_product()</h4>
      <p>مهم‌ترین ویو. جریان کار آن به این صورت است:</p>
      <div class="steps">
        <div class="step">
          <div class="step-num">۱</div>
          <div class="step-content">
            <div class="step-title">دریافت فرم و فایل‌های تصویری</div>
            <div class="step-desc">اطلاعات محصول شامل نام، قیمت، SKU، دسته‌بندی و تصاویر از فرم دریافت می‌شود.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">۲</div>
          <div class="step-content">
            <div class="step-title">تولید محتوا با هوش مصنوعی</div>
            <div class="step-desc">به ترتیب: URL-Slug انگلیسی، توضیحات کوتاه فارسی، و توضیحات HTML کامل با FAQ و لینک داخلی تولید می‌شود.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">۳</div>
          <div class="step-content">
            <div class="step-title">آپلود تصاویر در WordPress</div>
            <div class="step-desc">هر تصویر با WordPress REST API آپلود می‌شود و ID بازگشتی ذخیره می‌گردد.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">۴</div>
          <div class="step-content">
            <div class="step-title">ثبت نهایی در WooCommerce</div>
            <div class="step-desc">محصول با تمام اطلاعات تولید شده (شامل ID تصاویر) در ووکامرس منتشر می‌شود.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">۵</div>
          <div class="step-content">
            <div class="step-title">ثبت لاگ</div>
            <div class="step-desc">چه موفق چه ناموفق، یک رکورد ProductLog ذخیره می‌شود تا سهمیه حساب شود.</div>
          </div>
        </div>
      </div>

      <h4>product_manager()</h4>
      <p>سه حالت دارد: نمایش لیست (GET)، ویرایش تکی (POST با <code>single_update</code>)، و تغییر قیمت گروهی (POST با <code>bulk_update</code>).</p>
    </section>

    <section id="templates">
      <h3>🎨 تمپلیت‌ها (templates/)</h3>
      <p>تمام صفحات از <code>base.html</code> ارث می‌برند که شامل:</p>
      <ul style="list-style:none;padding:0;display:flex;flex-direction:column;gap:6px;margin:10px 0">
        <li style="display:flex;align-items:center;gap:8px;font-size:13px;color:var(--text2)"><span class="tag tag-blue">سیستم دارک‌مود</span> ذخیره‌سازی در localStorage، تغییر بدون رفرش</li>
        <li style="display:flex;align-items:center;gap:8px;font-size:13px;color:var(--text2)"><span class="tag tag-green">ناوبار ریسپانسیو</span> همبرگر منو برای موبایل</li>
        <li style="display:flex;align-items:center;gap:8px;font-size:13px;color:var(--text2)"><span class="tag tag-purple">فونت IRANSans</span> از مسیر static/fonts بارگذاری می‌شود</li>
        <li style="display:flex;align-items:center;gap:8px;font-size:13px;color:var(--text2)"><span class="tag tag-amber">Django Messages</span> پیام‌های موفقیت و خطا به صورت خودکار نمایش داده می‌شوند</li>
      </ul>
    </section>

    <section id="admin">
      <h3>⚡ پنل ادمین (admin.py)</h3>
      <p>تمام مدل‌ها در پنل ادمین Django ثبت شده‌اند. نکات مهم:</p>

      <div class="alert alert-warn">
        <div class="alert-icon">⚠️</div>
        <div class="alert-content">
          <div class="alert-title">نحوه ایجاد فروشگاه و کاربر جدید</div>
          برای اضافه کردن مستاجر جدید باید از پنل ادمین: ۱) یک <strong>Plan</strong> بسازید، ۲) یک <strong>Store</strong> با کلیدهای API ووکامرس بسازید، ۳) یک <strong>User</strong> در قسمت Users جنگو بسازید، ۴) یک <strong>UserProfile</strong> که User را به Store وصل می‌کند بسازید.
        </div>
      </div>
    </section>
  </section>

  <section id="prerequisites">
    <h2><span class="section-num">۳</span>پیش‌نیازهای سیستم</h2>

    <p>قبل از نصب، باید مطمئن شوید سیستم‌عامل شما یکی از موارد زیر باشد:</p>

    <table class="doc-table">
      <thead><tr><th>سیستم‌عامل</th><th>وضعیت</th><th>توضیح</th></tr></thead>
      <tbody>
        <tr><td>Windows 10/11 (64bit)</td><td><span class="tag tag-green">✓ پشتیبانی</span></td><td>نیاز به WSL2 یا Docker Desktop</td></tr>
        <tr><td>macOS 12+</td><td><span class="tag tag-green">✓ پشتیبانی</span></td><td>Intel و Apple Silicon هر دو</td></tr>
        <tr><td>Ubuntu 20.04+</td><td><span class="tag tag-green">✓ پشتیبانی</span></td><td>بهترین گزینه برای سرور</td></tr>
        <tr><td>Debian 11+</td><td><span class="tag tag-green">✓ پشتیبانی</span></td><td>مناسب سرور</td></tr>
      </tbody>
    </table>

    <h3>منابع حداقلی</h3>
    <div class="card-grid">
      <div class="info-card">
        <div class="info-card-icon">🖥️</div>
        <div class="info-card-title">RAM</div>
        <div class="info-card-desc">حداقل ۲ گیگابایت (توصیه شده ۴ گیگابایت)</div>
      </div>
      <div class="info-card">
        <div class="info-card-icon">💾</div>
        <div class="info-card-title">دیسک</div>
        <div class="info-card-desc">حداقل ۵ گیگابایت فضای خالی برای Docker images</div>
      </div>
      <div class="info-card">
        <div class="info-card-icon">🌐</div>
        <div class="info-card-title">اینترنت</div>
        <div class="info-card-desc">برای دانلود ایمیج‌های داکر و کتابخانه‌ها نیاز است</div>
      </div>
      <div class="info-card">
        <div class="info-card-icon">⚙️</div>
        <div class="info-card-title">Git</div>
        <div class="info-card-desc">برای کلون کردن پروژه (یا دانلود مستقیم ZIP)</div>
      </div>
    </div>
  </section>

  <section id="docker-setup">
    <h2><span class="section-num">۴</span>نصب Docker Engine — گام به گام</h2>

    <div class="alert alert-info">
      <div class="alert-icon">📌</div>
      <div class="alert-content">
        <div class="alert-title">داکر چیست؟</div>
        Docker یک ابزار است که اجازه می‌دهد اپلیکیشن را داخل «کانتینر» اجرا کنید. کانتینر مثل یک کامپیوتر مجازی کوچک است که همه چیز (Python، PostgreSQL، کدها) را درون خودش دارد و روی هر سیستم‌عاملی یکسان کار می‌کند.
      </div>
    </div>

    <h3>نصب روی Ubuntu / Debian (سرور Linux)</h3>

    <div class="steps">
      <div class="step">
        <div class="step-num">۱</div>
        <div class="step-content">
          <div class="step-title">حذف نسخه‌های قدیمی (اگر وجود دارند)</div>
<pre>sudo apt-get remove docker docker-engine docker.io containerd runc</pre>
        </div>
      </div>
      <div class="step">
        <div class="step-num">۲</div>
        <div class="step-content">
          <div class="step-title">به‌روزرسانی و نصب پیش‌نیازها</div>
<pre>sudo apt-get update
sudo apt-get install -y \
    ca-certificates \
    curl \
    gnupg \
    lsb-release</pre>
        </div>
      </div>
      <div class="step">
        <div class="step-num">۳</div>
        <div class="step-content">
          <div class="step-title">اضافه کردن کلید GPG رسمی Docker</div>
<pre>sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
    sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg</pre>
        </div>
      </div>
      <div class="step">
        <div class="step-num">۴</div>
        <div class="step-content">
          <div class="step-title">تنظیم Repository برای دریافت داکر</div>
<pre>echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null</pre>
        </div>
      </div>
      <div class="step">
        <div class="step-num">۵</div>
        <div class="step-content">
          <div class="step-title">نصب نهایی Docker Engine</div>
<pre>sudo apt-get update
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin</pre>
        </div>
      </div>
    </div>

    <div class="alert alert-success">
      <div class="alert-icon">✓</div>
      <div class="alert-content">
        <div class="alert-title">کاربران ویندوز و مک</div>
        نیاز به اجرای دستورات بالا ندارید. کافیست نرم‌افزار <strong>Docker Desktop</strong> را از سایت رسمی دانلود و با کلیک روی Next نصب کنید.
      </div>
    </div>
  </section>

  <section id="project-setup">
    <h2><span class="section-num">۵</span>راه‌اندازی پروژه و تنظیمات محیطی</h2>
    
    <h3 id="env-config">ساخت فایل .env</h3>
    <p>پروژه برای اجرا به یک فایل متغیرهای محیطی به نام <code>.env</code> در مسیر اصلی (کنار فایل <code>docker-compose.yml</code>) نیاز دارد. یک فایل جدید بسازید و مقادیر زیر را در آن قرار دهید:</p>

<pre><span class="comment"># --- تنظیمات پایه جنگو ---</span>
DJANGO_SECRET_KEY=<span class="string">your-super-secret-key-change-it</span>
DJANGO_DEBUG=<span class="string">True</span>  <span class="comment"># در سرور اصلی روی False قرار دهید</span>

<span class="comment"># --- تنظیمات دیتابیس PostgreSQL ---</span>
POSTGRES_DB=<span class="string">saas_db</span>
POSTGRES_USER=<span class="string">saas_user</span>
POSTGRES_PASSWORD=<span class="string">saas_secure_pass123</span>
POSTGRES_HOST=<span class="string">db</span>
POSTGRES_PORT=<span class="string">5432</span></pre>
  </section>

  <section id="first-run">
    <h2><span class="section-num">۶</span>اجرای اول پروژه</h2>

    <p>بعد از تنظیم فایل `.env`، وارد پوشه پروژه در ترمینال شوید و دستورات زیر را به ترتیب اجرا کنید:</p>

    <div class="steps">
      <div class="step">
        <div class="step-num">۱</div>
        <div class="step-content">
          <div class="step-title">بیلد و اجرای کانتینرها</div>
          <div class="step-desc">این دستور داکر را استارت زده و ایمیج‌ها را در پس‌زمینه دانلود/بیلد می‌کند.</div>
<pre>docker compose up -d --build</pre>
        </div>
      </div>
      <div class="step">
        <div class="step-num">۲</div>
        <div class="step-content">
          <div class="step-title">اعمال تغییرات دیتابیس (Migrate)</div>
          <div class="step-desc">ساختار جداول را در PostgreSQL ایجاد می‌کند.</div>
<pre>docker compose exec web python manage.py migrate</pre>
        </div>
      </div>
      <div class="step">
        <div class="step-num">۳</div>
        <div class="step-content">
          <div class="step-title">ساخت کاربر ارشد (Superuser)</div>
          <div class="step-desc">برای دسترسی به پنل ادمین جنگو، یک اکانت ادمین بسازید.</div>
<pre>docker compose exec web python manage.py createsuperuser</pre>
        </div>
      </div>
    </div>
    
    <p>حالا مرورگر خود را باز کنید و به آدرس <code>http://localhost:8000</code> بروید. برای پنل ادمین از <code>http://localhost:8000/admin</code> استفاده کنید.</p>
  </section>

  <section id="production">
    <h2><span class="section-num">۷</span>آماده‌سازی برای پروداکشن (سرور واقعی)</h2>
    <p>وقتی قصد دارید پروژه را روی سرور عمومی دیپلوی کنید، باید تغییرات امنیتی زیر را در فایل <code>.env</code> و تنظیمات سرور اعمال کنید:</p>

    <ul>
      <li>متغیر <code>DJANGO_DEBUG</code> را روی <strong>False</strong> قرار دهید. این کار از نمایش خطاهای حساس جلوگیری می‌کند.</li>
      <li>متغیر <code>ALLOWED_HOSTS</code> را با دامنه سایت خود (مثلاً <code>saas.example.com</code>) تنظیم کنید.</li>
      <li>رمز عبور قدرتمندی برای <code>POSTGRES_PASSWORD</code> انتخاب کنید.</li>
      <li>بهتر است از Nginx به عنوان یک Reverse Proxy استفاده کنید تا درخواست‌های پورت 80 و 443 (HTTPS) را به پورت 8000 داکر منتقل کند.</li>
    </ul>
  </section>

  <section id="troubleshoot">
    <h2 id="faq"><span class="section-num">۸</span>رفع خطاها و سوالات متداول</h2>

    <h4>❓ کانتینرها استارت نمی‌شوند یا ارور Database Connection می‌دهند</h4>
    <p>گاهی اوقات کانتینر اپلیکیشن جنگو زودتر از بالا آمدن کامل دیتابیس اجرا می‌شود. ابتدا لاگ‌ها را با دستور زیر بررسی کنید:</p>
<pre>docker compose logs -f web</pre>
    <p>اگر مشکل از دیتابیس بود، کافیست یک بار وب‌سرور را ری‌استارت کنید: <code>docker compose restart web</code></p>

    <h4>❓ چطور فایل‌های استاتیک در پروداکشن لود نمی‌شوند؟</h4>
    <p>هنگامی که <code>DEBUG=False</code> است، جنگو فایل‌های استاتیک را مستقیم سرو نمی‌کند. باید دستور زیر را داخل کانتینر اجرا کنید تا فایل‌ها جمع‌آوری شوند (در این معماری داکر، معمولاً WhiteNoise یا Nginx این کار را هندل می‌کند):</p>
<pre>docker compose exec web python manage.py collectstatic --noinput</pre>

    <h4>❓ چگونه یک ایمیج ووکامرس آپلود نمی‌شود؟</h4>
    <p>بررسی کنید که در تنظیمات وردپرس مقصد (ووکامرس)، کاربر API دسترسی <strong>Read/Write</strong> داشته باشد و آدرس سایت در دیتابیس (جدول Store) بدون خط اسلش آخر (<code>/</code>) وارد شده باشد.</p>

  </section>

</main>
</div>

</body>
</html>
