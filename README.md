# spices-landing-page
mini website 8 spices cikarang
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1"/>
  <title>Terima Kasih</title>
  <style>
    body { 
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
      display:flex; align-items:center; justify-content:center; 
      min-height:100vh; margin:0; 
      background:#f9f9f9; color:#111; 
    }
    .card { 
      background:white; padding:28px; border-radius:12px; 
      box-shadow:0 6px 20px rgba(0,0,0,0.08);
      max-width:560px; text-align:center; 
    }
    h1 { margin:0 0 12px; font-size:24px; }
    p { margin:0 0 18px; color:#444; }
    .btn { 
      display:inline-block; margin:6px; padding:12px 18px; 
      border-radius:8px; text-decoration:none;
      font-weight:600; border:1px solid #ddd;
    }
    .btn-primary { background:#0b6cf3; color:white; border-color:transparent; }
    .btn-secondary { background:transparent; color:#0b6cf3; border-color:#0b6cf3; }
    small { display:block; margin-top:12px; color:#777; }
  </style>

  <script>
    // Auto redirect timer — set to 6 seconds
    const AUTO_REDIRECT_SECONDS = 6; 
    let secondsLeft = AUTO_REDIRECT_SECONDS;

    function startTimer() {
      if (AUTO_REDIRECT_SECONDS <= 0) return;
      const el = document.getElementById('countdown');
      const timer = setInterval(() => {
        secondsLeft--;
        if (el) el.textContent = secondsLeft;
        if (secondsLeft <= 0) {
          clearInterval(timer);
          window.location.href = "https://maps.app.goo.gl/13VtPZSHHxiKq6ve7";
        }
      }, 1000);
    }

    window.addEventListener('DOMContentLoaded', startTimer);
  </script>
</head>

<body>
  <div class="card">
    <h1>Terima kasih atas kunjungan Anda</h1>
    <p>Semoga pengalaman Anda menyenangkan. Anda dapat melihat lokasi dan website kami melalui tombol di bawah.</p>

    <a class="btn btn-primary" 
       href="https://maps.app.goo.gl/13VtPZSHHxiKq6ve7" 
       target="_blank" rel="noopener">
       Buka Google Maps
    </a>

    <a class="btn btn-secondary" 
       href="https://maps.app.goo.gl/2z5uRndBW4uAmSni6" 
       target="_blank" rel="noopener">
       Buka Website
    </a>

    <small>
      Anda akan dialihkan ke Google Maps dalam 
      <span id="countdown">6</span> detik.
      (Tutup halaman ini jika tidak ingin dialihkan.)
    </small>
  </div>
</body>
</html>
