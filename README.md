<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lễ Giỗ 1 Năm</title>

  <!-- Meta chia sẻ -->
  <meta property="og:title" content="LỄ GIỖ 1 NĂM">
  <meta property="og:description" content="Trân trọng kính mời tham dự Lễ Giỗ 1 Năm • 12.01.2026 • Điện Biên Phủ, TP.HCM">
  <meta property="og:type" content="website">

  <style>
    :root{
      --wood-dark:#3a2a1f;
      --wood:#5b3e2b;
      --wood-light:#8b6a4f;
      --cream:#f7f3ee;
      --line:rgba(90,60,40,.25);
      --text:#2b1d14;
    }

    *{box-sizing:border-box}

    body{
      margin:0;
      font-family:"Georgia","Times New Roman",serif;
      color:var(--text);
      background:
        radial-gradient(900px 420px at 10% 10%, rgba(139,106,79,.15), transparent 60%),
        radial-gradient(900px 420px at 90% 90%, rgba(58,42,31,.18), transparent 62%),
        linear-gradient(180deg,#efe7dd 0%, #f9f6f2 100%);
    }

    .wrap{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px;
    }

    .card{
      max-width:680px;
      width:100%;
      background:var(--cream);
      border:1px solid var(--line);
      border-radius:18px;
      box-shadow:0 18px 40px rgba(0,0,0,.12);
      padding:36px 28px 40px;
      text-align:center;
    }

    .title-small{
      letter-spacing:.18em;
      font-size:13px;
      color:var(--wood-light);
    }

    h1{
      margin:14px 0 10px;
      font-size:34px;
      font-weight:700;
      color:var(--wood-dark);
    }

    .subtitle{
      font-size:16px;
      color:#5a4637;
    }

    .divider{
      width:72px;
      height:2px;
      background:linear-gradient(90deg,transparent,var(--wood),transparent);
      margin:18px auto;
    }

    .info{
      margin-top:26px;
      border-top:1px solid var(--line);
      border-bottom:1px solid var(--line);
      padding:22px 10px;
    }

    .info-row{ margin:14px 0; }

    .label{
      font-size:13px;
      letter-spacing:.12em;
      color:#6b5442;
    }

    .value{
      margin-top:6px;
      font-size:18px;
      font-weight:600;
      color:#3b2a1f;
    }

    .note{
      margin-top:22px;
      font-size:15px;
      color:#4a382c;
      line-height:1.7;
    }

    /* ===== RSVP ===== */
    .rsvpBox{ margin-top:28px; }

    .rsvpInput{
      width:min(420px,100%);
      padding:12px 14px;
      border-radius:12px;
      border:1px solid rgba(90,60,40,.28);
      outline:none;
      font-family:inherit;
      font-size:15px;
      background:#fff;
    }

    .btnRow{
      display:flex;
      gap:10px;
      justify-content:center;
      flex-wrap:wrap;
      margin-top:14px;
    }

    .btnRSVP{
      padding:13px 20px;
      border-radius:12px;
      font-weight:700;
      font-size:15px;
      letter-spacing:.04em;
      cursor:pointer;
      border:0;
    }

    .btnAttend{
      background:var(--wood);
      color:#fff;
      box-shadow:0 6px 16px rgba(0,0,0,.22);
    }

    .btnDecline{
      background:transparent;
      color:var(--wood-dark);
      border:1px solid rgba(90,60,40,.35);
    }

    .rsvpMsg{
      display:none;
      margin-top:12px;
      font-size:14px;
      color:#4a382c;
    }

    .rsvpMsg.show{ display:block; }

    .footer{
      margin-top:24px;
      font-size:13px;
      color:#7a6757;
    }

    @media (max-width:520px){
      h1{font-size:28px}
      .card{padding:28px 20px 32px}
    }
  </style>
</head>

<body>
  <div class="wrap">
    <div class="card">
      <div class="title-small">TRÂN TRỌNG KÍNH MỜI</div>

      <h1>LỄ GIỖ 1 NĂM</h1>

      <div class="subtitle">Tưởng niệm &amp; tri ân</div>

      <div class="divider"></div>

      <div class="info">
        <div class="info-row">
          <div class="label">THỜI GIAN</div>
          <div class="value">Ngày 12 tháng 01 năm 2026</div>
        </div>

        <div class="info-row">
          <div class="label">ĐỊA ĐIỂM</div>
          <div class="value">Điện Biên Phủ, TP. Hồ Chí Minh</div>
        </div>
      </div>

      <div class="note">
        Kính mời quý thân bằng quyến thuộc, bằng hữu<br/>
        dành chút thời gian đến tham dự lễ giỗ,<br/>
        thắp nén hương lòng tưởng nhớ.
      </div>

      <!-- ===== RSVP SUBMIT BẰNG ENTRY ===== -->
      <div class="rsvpBox">
        <div class="label">XÁC NHẬN THAM DỰ</div>

        <input
          id="guestName"
          class="rsvpInput"
          type="text"
          placeholder="Họ và tên"
          required
        >

        <!-- iframe ẩn để submit không rời trang -->
        <iframe name="hidden_iframe" style="display:none;"></iframe>

        <form
          id="rsvpForm"
          action="https://docs.google.com/forms/d/e/1FAIpQLSeAbEEMP7dOkfBvpq9N7Kt3Z7NTFxxC3UYFzN2UIViH9GNDXA/formResponse"
          method="POST"
          target="hidden_iframe">

          <!-- ENTRY IDs -->
          <input type="hidden" name="entry.2035054770" id="f_name">
          <input type="hidden" name="entry.1484132997" id="f_attend">
        </form>

        <div class="btnRow">
          <button class="btnRSVP btnAttend" type="button"
            onclick="submitRSVP('Tham dự')">
            THAM DỰ
          </button>

          <button class="btnRSVP btnDecline" type="button"
            onclick="submitRSVP('Không tham dự')">
            KHÔNG THAM DỰ
          </button>
        </div>

        <div class="rsvpMsg" id="rsvpMsg">
          Gia đình đã ghi nhận. Xin chân thành cảm ơn.
        </div>
      </div>

      <div class="footer">
        Sự hiện diện của quý vị là niềm an ủi lớn lao cho gia đình
      </div>
    </div>
  </div>

  <script>
    function submitRSVP(choice){
      const name = document.getElementById('guestName').value.trim();
      if(!name){
        alert('Vui lòng nhập Họ và tên.');
        document.getElementById('guestName').focus();
        return;
      }

      document.getElementById('f_name').value = name;
      document.getElementById('f_attend').value = choice;

      document.getElementById('rsvpForm').submit();

      const msg = document.getElementById('rsvpMsg');
      msg.textContent = `Đã ghi nhận: ${choice}. Xin cảm ơn.`;
      msg.classList.add('show');
    }
  </script>
</body>
</html>
