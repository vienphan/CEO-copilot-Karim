
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CEO Copilot – Karim</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #ffffff;
      --fg: #1a1a1a;
      --accent: #e11d48; /* NK Red */
      --muted: #6b7280;
      --card: #f9fafb;
      --radius: 16px;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--fg);
      line-height: 1.6;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: linear-gradient(135deg, var(--accent), #b91c1c);
      color: white;
      padding: 2rem;
      text-align: center;
    }

    header h1 { font-size: 1.8rem; }
    header p { opacity: 0.9; }

    main {
      flex: 1;
      display: grid;
      grid-template-columns: 1fr 300px;
      gap: 1.5rem;
      padding: 2rem;
    }

    .card {
      background: var(--card);
      border-radius: var(--radius);
      padding: 1.5rem;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    .card h2 { color: var(--accent); margin-bottom: 1rem; }
    .section-grid { display: grid; gap: 1rem; }

    /* Sidebar */
    aside {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .btn {
      display: block;
      background: var(--accent);
      color: white;
      padding: 0.8rem;
      border-radius: var(--radius);
      text-align: center;
      text-decoration: none;
      font-weight: 600;
      transition: background 0.3s;
    }

    .btn:hover { background: #be123c; }

    /* Chat dock */
    .chatbox {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background: var(--card);
      border-top: 1px solid #e5e7eb;
      padding: 1rem;
      display: flex;
      gap: 0.5rem;
    }

    .chatbox input {
      flex: 1;
      padding: 0.8rem;
      border: 1px solid #e5e7eb;
      border-radius: var(--radius);
    }

    .chatbox button {
      background: var(--accent);
      color: white;
      border: none;
      border-radius: var(--radius);
      padding: 0.8rem 1.2rem;
      cursor: pointer;
    }

    footer {
      background: #f3f4f6;
      text-align: center;
      padding: 1rem;
      font-size: 0.9rem;
    }

    @media (max-width: 768px) {
      main { grid-template-columns: 1fr; }
      .chatbox { flex-direction: column; }
      .chatbox button { width: 100%; }
    }
  </style>
</head>
<body>
  <header>
    <h1>CEO Copilot – Karim</h1>
    <p>Smart assistant for performance updates, planning, and daily briefing</p>
  </header>

  <main>
    <section class="section-grid">
      <div class="card">
        <h2>🗓 Today’s Brief</h2>
        <p>• 09:00 EXCO Meeting<br>• 11:00 Finance Review<br>• 14:00 Store Visit Planning</p>
      </div>

      <div class="card">
        <h2>📈 Latest Updates</h2>
        <ul>
          <li>3Y Plan – Version 3 (2025-10-28)</li>
          <li>Performance Review Q4 – Dashboard</li>
          <li>New Projects: Store Format Rollout</li>
        </ul>
      </div>

      <div class="card">
        <h2>📁 Quick Access</h2>
        <a href="#" class="btn">3Y Plan</a>
        <a href="#" class="btn">Performance Review</a>
        <a href="#" class="btn">New Projects</a>
        <a href="#" class="btn">Travel Docs</a>
      </div>
    </section>

    <aside>
      <div class="card">
        <h2>📅 Calendar</h2>
        <p>View upcoming meetings and events synced from CEO calendar.</p>
        <a href="#" class="btn">Open Calendar</a>
      </div>

      <div class="card">
        <h2>🔍 Search Files</h2>
        <p>Find documents by keyword, topic, or date.</p>
        <a href="#" class="btn">Search Now</a>
      </div>
    </aside>
  </main>

  <div class="chatbox">
    <input type="text" placeholder="Ask: ‘latest 3Y Plan’ or ‘agenda today’..." />
    <button>Send</button>
  </div>

  <footer>
    © <span id="year"></span> CEO Copilot • Made with ❤️ for <a href="https://vienphan.github.io/karim-profile/" style="color:#2563eb; text-decoration:none; font-weight:600;">Karim Noui</a>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
