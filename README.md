<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lễ Giỗ 1 Năm • Thiếu Tướng Mai Xuân Tần</title>

  <meta property="og:title" content="LỄ GIỖ 1 NĂM • Thiếu Tướng Mai Xuân Tần">
  <meta property="og:description" content="Trân trọng kính mời tham dự Lễ Giỗ 1 Năm • 12.01.2026 • Điện Biên Phủ, TP.HCM">
  <meta property="og:type" content="website">

  <style>
    :root{
      --wood-dark:#3a2a1f;
      --wood:#5b3e2b;
      --wood-light:#8b6a4f;
      --text:#2b1d14;
      --paper:#fbf8f4;
    }
    *{ box-sizing:border-box; }

    body{
      margin:0;
      font-family:"Georgia","Times New Roman",serif;
      color:var(--text);
      background:
        radial-gradient(900px 420px at 12% 10%, rgba(139,106,79,.16), transparent 60%),
        radial-gradient(900px 420px at 88% 90%, rgba(58,42,31,.16), transparent 62%),
        linear-gradient(180deg,#efe7dd 0%, #f9f6f2 100%);
    }

    .wrap{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px;
    }

    .frame{
      width:min(980px, 100%);
      background:var(--paper);
      border:1.5px solid rgba(58,42,31,.40);
      box-shadow:0 18px 50px rgba(0,0,0,.10);
      padding:14px;
    }
    .frame-inner{
      border:1px solid rgba(58,42,31,.22);
      padding:22px;
      background:
        radial-gradient(900px 420px at 12% 18%, rgba(245,111,32,.06), transparent 60%),
        radial-gradient(900px 420px at 88% 70%, rgba(2,115,81,.05), transparent 62%),
        linear-gradient(180deg, #fffdfb 0%, #fbf8f4 100%);
    }

    .grid{
      display:grid;
      grid-template-columns: 320px 1fr;
      gap:22px;
      align-items:start;
    }

    /* LEFT */
    .left{ padding-top:6px; }
    .photo-wrap{
      display:flex;
      justify-content:center;
      margin-top:10px;
    }

    .photo-frame{
      width:260px;
      height:320px;
      border-radius:180px;
      position:relative;
      background:linear-gradient(180deg,#fff 0%, #f4efe8 100%);
      border:1px solid rgba(90,60,40,.28);
      box-shadow:0 16px 40px rgba(0,0,0,.10);
      overflow:hidden;
    }
    .photo-frame:before{
      content:"";
      position:absolute;
      inset:10px;
      border-radius:170px;
      border:2px dotted rgba(139,106,79,.35);
      pointer-events:none;
    }
    .photo{
      position:absolute;
      inset:18px;
      border-radius:160px;
      overflow:hidden;
      display:flex;
      align-items:center;
      justify-content:center;
      background:linear-gradient(180deg,#f7f3ee 0%, #efe7dd 100%);
    }
    .photo img{
      width:100%;
      height:100%;
      object-fit:cover;
      display:block;
    }
    .photo-placeholder{
      text-align:center;
      padding:18px;
      color:#6b5442;
      font-size:14px;
      line-height:1.5;
      display:none;
    }

    .program{
      margin-top:18px;
      padding:14px 14px 12px;
      border:1px solid rgba(90,60,40,.22);
      background:#fff;
    }
    .program h3{
      margin:0 0 10px;
      font-size:16px;
      letter-spacing:.10em;
      text-transform:uppercase;
      color:var(--wood-dark);
    }
    .program ul{
      margin:0;
      padding-left:18px;
      color:#4a382c;
      font-size:14px;
      line-height:1.7;
    }

    /* RIGHT */
    .right{
      text-align:center;
      padding-top:4px;
    }
    .title-small{
      letter-spacing:.18em;
      font-size:13px;
      color:var(--wood-light);
      text-transform:uppercase;
    }
    h1{
      margin:12px 0 6px;
      font-size:34px;
      font-weight:700;
      color:var(--wood-dark);
    }
    .subtitle{
      font-size:16px;
      color:#5a4637;
    }
    .divider{
      width:120px;
      height:2px;
      background:linear-gradient(90deg,transparent,var(--wood),transparent);
      margin:16px auto 14px;
    }

    .person{
      margin-top:4px;
      line-height:1.7;
    }
    .person .rank{
      font-size:15px;
      letter-spacing:.06em;
      color:#6b5442;
      text-transform:uppercase;
    }
    .person .name{
      font-size:22px;
      font-weight:700;
      color:var(--wood-dark);
      margin-top:3px;
    }

    .note{
      margin-top:14px;
      font-size:15px;
      color:#4a382c;
      line-height:1.75;
    }
    .note .strong{
      font-weight:700;
      color:var(--wood-dark);
    }

    .subnote{
      margin-top:10px;
      font-size:14px;
      color:#5a4637;
      line-height:1.7;
    }

    .info{
      margin-top:18px;
      border-top:1px solid rgba(90,60,40,.22);
      border-bottom:1px solid rgba(90,60,40,.22);
      padding:16px 10px;
    }
    .info-row{ margin:12px 0; }
    .label{
      font-size:12px;
      letter-spacing:.12em;
      color:#6b5442;
      text-transform:uppercase;
    }
    .value{
      margin-top:6px;
      font-size:18px;
      font-weight:600;
      color:#3b2a1f;
    }

    /* RSVP */
    .rsvpBox{ margin-top:16px; }
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
      margin-top:12px;
    }
    .btnRSVP{
      padding:12px 18px;
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
      box-shadow:0 6px 16px rgba(0,0,0,.18);
    }
    .btnDecline{
      background:transparent;
      color:var(--wood-dark);
      border:1px solid rgba(90,60,40,.35);
    }
    .rsvpMsg{
      display:none;
      margin-top:10px;
      font-size:14px;
      color:#4a382c;
    }
    .rsvpMsg.show{ display:block; }

    .footer{
      margin-top:16px;
      font-size:12.5px;
      color:#7a6757;
      line-height:1.6;
      text-align:center;
    }

    @media (max-width:860px){
      .grid{ grid-template-columns: 1fr; }
      .left{ order:2; }
      .right{ order:1; }
      .photo-frame{ width:240px; height:300px; }
    }
    @media (max-width:520px){
      h1{ font-size:28px; }
      .frame-inner{ padding:18px; }
      .photo-frame{ width:220px; height:280px; }
      .person .name{ font-size:20px; }
    }
  </style>
</head>

<body>
  <div class="wrap">
    <div class="frame">
      <div class="frame-inner">
        <div class="grid">

          <!-- LEFT COLUMN -->
          <div class="left">
            <div class="photo-wrap">
              <div class="photo-frame">
                <div class="photo">
                  <!-- ✅ DÁN LINK ẢNH TRỰC TIẾP (.jpg/.png) -->
                  <img
                    id="portrait"
                    src="PHOTO_DIRECT_URL_HERE"
                    alt="Chân dung"
                    onerror="this.style.display='none';document.getElementById('ph').style.display='block';"
                  >

                  <div class="photo-placeholder" id="ph">
                    Ảnh chưa tải được.<br/>
                    Vui lòng thay <strong>PHOTO_DIRECT_URL_HERE</strong><br/>
                    bằng link ảnh <strong>.jpg/.png</strong> trực tiếp.
                  </div>
                </div>
              </div>
            </div>

            <div class="program">
              <h3>Chương trình</h3>
              <ul>
                <li>Đón tiếp</li>
                <li>Tưởng niệm &amp; thắp hương</li>
                <li>Gặp gỡ gia đình</li>
              </ul>
            </div>
          </div>

          <!-- RIGHT COLUMN -->
          <div class="right">
            <div class="title-small">TRÂN TRỌNG KÍNH MỜI</div>

            <h1>LỄ GIỖ 1 NĂM</h1>
            <div class="subtitle">Tưởng niệm &amp; tri ân</div>

            <div class="divider"></div>

            <div class="person">
              <div class="rank">Thiếu Tướng</div>
              <div class="name">MAI XUÂN TẦN</div>
            </div>

            <div class="note">
              Nhân ngày giỗ <span class="strong">một năm</span> của
              <span class="strong">Thiếu Tướng Mai Xuân Tần</span>,<br/>
              gia đình chúng tôi trân trọng kính mời quý thân bằng quyến thuộc,
              bằng hữu đến tham dự lễ giỗ và cùng gia đình tưởng niệm người đã khuất.
            </div>

            <div class="subnote">
              Người mời: <span class="strong">Ông Mai Xuân Đức</span>
            </div>

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
              Sự hiện diện của quý vị là nguồn động viên lớn đối với gia đình.<br/>
              Kính mong quý vị dành chút thời gian đến thắp nén hương lòng tưởng nhớ.
            </div>

            <div class="rsvpBox">
              <div class="label">XÁC NHẬN THAM DỰ</div>

              <input id="guestName" class="rsvpInput" type="text" placeholder="Họ và tên" required>

              <iframe name="hidden_iframe" style="display:none;"></iframe>

              <form
                id="rsvpForm"
                action="https://docs.google.com/forms/d/e/1FAIpQLSeAbEEMP7dOkfBvpq9N7Kt3Z7NTFxxC3UYFzN2UIViH9GNDXA/formResponse"
                method="POST"
                target="hidden_iframe">
                <input type="hidden" name="entry.2035054770" id="f_name">
                <input type="hidden" name="entry.1484132997" id="f_attend">
              </form>

              <div class="btnRow">
                <button class="btnRSVP btnAttend" type="button" onclick="submitRSVP('Tham dự')">THAM DỰ</button>
                <button class="btnRSVP btnDecline" type="button" onclick="submitRSVP('Không tham dự')">KHÔNG THAM DỰ</button>
              </div>

              <div class="rsvpMsg" id="rsvpMsg">Gia đình đã ghi nhận. Xin chân thành cảm ơn.</div>
            </div>

            <div class="footer">(Vui lòng xác nhận để gia đình tiện sắp xếp.)</div>
          </div>

        </div>
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
