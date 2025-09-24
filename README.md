
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Security Simulation</title>
  <style>
    /* Reset-ish */
    html,body { margin:0; padding:0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial; background:#fff; color:#111; }

    /* Banner image - full width, very large, responsive */
    .banner {
      position: relative;
      width: 100%;
      height: 80vh;              /* big: fills 80% of the viewport height */
      max-height: 1000px;        /* cap so extremely tall monitors don't blow it up */
      overflow: hidden;
      display:block;
      background: #000;
    }
    .banner img {
      width: 100%;
      height: 100%;
      object-fit: cover;         /* crop to fill while keeping aspect ratio */
      display: block;
    }

    /* Overlay text centered on the banner */
    .overlay {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%,-50%);
      text-align: center;
      padding: 1.2rem 1.6rem;
      background: rgba(0,0,0,0.45);
      border-radius: 12px;
      color: #fff;
      box-shadow: 0 8px 24px rgba(0,0,0,0.4);
    }
    .overlay h1 { margin: 0 0 .25rem 0; font-size: clamp(28px, 6vw, 64px); letter-spacing: 1px; }
    .overlay p { margin: 0; font-size: clamp(14px, 2.2vw, 20px); opacity: 0.95; }

    /* Content area under the banner */
    .container {
      max-width: 900px;
      margin: 2rem auto;
      padding: 0 1rem;
      line-height: 1.5;
    }
    .btn {
      display:inline-block;
      margin-top:1rem;
      padding: .6rem 1rem;
      border-radius: 8px;
      text-decoration:none;
      background:#0b67d0;
      color:#fff;
      font-weight:600;
    }

    /* Small screens: reduce banner height */
    @media (max-width:480px) {
      .banner { height: 55vh; }
      .overlay h1 { font-size: clamp(20px, 8vw, 38px); }
    }
  </style>
</head>
<body>

<!-- GIF banner -->
<div class="banner" role="img" aria-label="Penguin animation">
  <img src="pengu.gif" alt="PENGU animation" style="width:100%; height:80vh; object-fit:cover; display:block;">
  <div class="overlay">
    <h1>GOTCHA!</h1>
    <p>This was a simulated phishing exercise.</p>
    <p>Max is disappointed.</p>
  </div>
</div>

  <!-- Content explaining the simulation and next steps -->
  <main class="container">
    <h2>Phishing Simulation — What just happened</h2>
    <p>
      This page is part of a company-run security training exercise. The link you clicked was intentionally simulated
      to help everyone learn how to spot and report phishing attempts.
    </p>

    <p><strong>Next steps:</strong></p>
    <ul>
      <li>If you entered any credentials on the original page, please change them immediately and notify IT.</li>
      <li>Report this click to the Security Team at <a href="mailto:security@yourcompany.example">security@yourcompany.example</a>.</li>
      <li>Review the short phishing-awareness guide we sent earlier (or visit the training portal).</li>
    </ul>

    <a class="btn" href="mailto:security@yourcompany.example">Report to Security</a>
  </main>

</body>
</html>
