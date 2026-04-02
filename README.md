<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Shinywave - Website</title>
  <meta name="description" content="Shinywave official website">

  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: #0f172a;
      color: white;
    }

    /* TOPBAR */
    .topbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      background: #020617;
      padding: 10px 20px;
      border-bottom: 2px solid #00ffcc;
    }

    .left {
      font-weight: bold;
      font-size: 18px;
      color: #00ffcc;
    }

    .middle {
      display: flex;
      gap: 10px;
    }

    .middle button {
      padding: 8px 12px;
      background: #1e293b;
      border: none;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }

    .middle button:hover {
      background: #00ffcc;
      color: black;
    }

    .right {
      text-align: right;
      font-size: 14px;
    }

    .role {
      font-size: 12px;
      color: #94a3b8;
    }

    /* CONTENT */
    .content {
      padding: 40px;
      text-align: center;
    }

    /* FOOTER */
    .footer {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: #020617;
      padding: 10px;
      border-top: 2px solid #00ffcc;
      font-size: 14px;
    }

    /* MOBILE */
    @media (max-width: 600px) {
      .middle {
        overflow-x: auto;
      }

      .middle button {
        flex-shrink: 0;
      }
    }
  </style>
</head>

<body>

<!-- TOPBAR -->
<div class="topbar">
  <div class="left">Shinywave</div>

  <div class="middle">
    <button onclick="changePage('about')">About</button>
    <button onclick="changePage('more')">More</button>
  </div>

  <div class="right">
    <div id="username">Guest</div>
    <div class="role">New User</div>
  </div>
</div>

<!-- CONTENT -->
<div class="content" id="content">
  <h1>Welcome 👋</h1>
  <p>Select a page above</p>
</div>

<!-- FOOTER -->
<div class="footer">
  Powered by Shinywave
</div>

<script>
function changePage(page) {
  let content = document.getElementById("content");

  if(page === "about") {
    content.innerHTML = "<h1>About</h1><p>This is about Shinywave 😎</p>";
  }

  if(page === "more") {
    content.innerHTML = "<h1>More</h1><p>More features soon 🔥</p>";
  }
}
</script>

</body>
</html>
