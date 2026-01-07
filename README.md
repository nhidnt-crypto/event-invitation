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
      width:min(980px,100%);
      background:var(--paper);
      border:1.5px solid rgba(58,42,31,.40);
      box-shadow:0 18px 50px rgba(0,0,0,.10);
      padding:14px;
    }

    .frame-inner{
      border:1px solid rgba(58,42,31,.22);
      padding:26px;
      background:linear-gradient(180deg,#fffdfb 0%,#fbf8f4 100%);
    }

    /* ===== GRID FIXED ===== */
    .grid{
      display:grid;
      grid-template-columns:320px 1fr;
      gap:32px;
      align-items:center;
    }

    /* ===== LEFT COLUMN ===== */
    .leftCol{
      display:flex;
      flex-direction:column;
      align-items:center;
      gap:18px;
    }

    .photo-frame{
      width:260px;
      height:330px;
      background:#fff;
      border-radius:8px;
      border:3px solid rgba(40,32,26,.72);
      box-shadow:0 18px 45px rgba(0,0,0,.16);
      position:relative;
      overflow:hidden;
    }
    .photo-frame::before{
      content:"";
      position:absolute;
      inset:8px;
      border-radius:6px;
      border:2px solid rgba(40,32,26,.55);
      pointer-events:none;
    }
    .photo{
      position:absolute;
      inset:14px;
      border-radius:4px;
      overflow:hidden;
      background:#fff;
    }
    .photo img{
      width:100%;
      height:100%;
      object-fit:cover;
      display:block;
    }

    .program{
      width:260px;
      padding:14px;
      border:1px solid rgba(90,60,40,.22);
      background:#fff;
    }
    .program h3{
      margin:0 0 10px;
      font-size:15px;
      letter-spacing:.12em;
      text-transform:uppercase;
      color:var(--wood-dark);
    }
    .program ul{
      margin:0;
      padding-left:18px;
      font-size:14px;
      line-height:1.7;
      color:#4a382c;
    }

    /* ===== RIGHT COLUMN ===== */
    .right{
      text-align:center;
      padding:6px 10px;
    }

    .title-small{
      font-size:13px;
      letter-spacing:.18em;
      color:var(--wood-light);
      text-transform:uppercase;
    }
    h1{
      margin:12px 0 6px;
      font-size:34px;
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
      margin:16px auto;
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
    }

    .note{
      margin-top:14px;
      font-size:15px;
      line-height:1.75;
      color:#4a382c;
    }
    .note .strong{ font-weight:700; }

    .info{
      margin-top:18px;
      padding:16px 10px;
      border-top:1px solid rgba(90,60,40,.22);
      border-bottom:1px solid rgba(90,60,40,.22);
    }
    .label{
      font-size:12px;
      letter-spacing:.12em;
      text-transform:uppercase;
      color:#6b5442;
    }
    .value{
      margin-top:6px;
      font-size:18px;
      font-weight:600;
    }

    /* ===== RSVP ===== */
    .rsvpBox{ margin-top:18px; }
    .rsvpInput{
      width:min(420px,100%);
      padding:12px 14px;
      border-radius:12px;
      border:1px solid rgba(90,60,40,.28);
      font-family:inherit;
    }
    .btnRow{
      display:flex;
      gap:10px;
      justify-content:center;
      margin-top:12px;
      flex-wrap:wrap;
    }
    .btnAttend{
      background:var(--wood);
      color:#fff;
      padding:12px 18px;
      border-radius:12px;
      border:0;
      font-weight:700;
      cursor:pointer;
    }
    .btnDecline{
      background:transparent;
      border:1px solid rgba(90,60,40,.35);
      padding:12px 18px;
      border-radius:12px;
      font-weight:700;
      cursor:pointer;
    }
    .rsvpMsg{
      display:none;
      margin-top:10px;
      font-size:14px;
    }
    .rsvpMsg.show{ display:block; }

    .footer{
      margin-top:16px;
      font-size:12.5px;
      color:#7a6757;
    }

    @media(max-width:860px){
      .grid{ grid-template-columns:1fr; }
    }
  </style>
</head>

<body>
<div class="wrap">
  <div class="frame">
    <div class="frame-inner">
      <div class="grid">

        <!-- LEFT -->
        <div class="leftCol">
          <div class="photo-frame">
            <div class="photo">
              <img src="https://i.postimg.cc/zBXNdHfz/489281397-1304542471178308-1599223331279466639-n.jpg" alt="Thiếu Tướng Mai Xuân Tần">
            </div>
          </div>

          <div class="program">
            <h3>Chương trình</h3>
            <ul>
              <li>Đón tiếp</li>
              <li>Tưởng niệm &amp; thắp hương</li>
              <li>Dùng bữa thân mật</li>
            </ul>
          </div>
        </div>

        <!-- RIGHT -->
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
            <span class="strong">Thiếu Tướng Mai Xuân Tần</span>,<br>
            gia đình trân trọng kính mời quý thân bằng quyến thuộc, bằng hữu
            đến tham dự lễ giỗ và cùng gia đình tưởng niệm người đã khuất.
          </div>

          <div class="info">
            <div>
              <div class="label">THỜI GIAN</div>
              <div class="value">Ngày 12 tháng 01 năm 2026</div>
            </div>
            <div style="margin-top:12px">
              <div class="label">ĐỊA ĐIỂM</div>
              <div class="value">Điện Biên Phủ, TP. Hồ Chí Minh</div>
            </div>
          </div>

          <div class="note">
            Sự hiện diện của quý vị là nguồn động viên lớn đối với gia đình.<br><br>
            <span class="strong">Thay mặt gia đình,</span><br>
            Con trai: <span class="strong">Mai Xuân Đức</span><br>
            Con dâu: <span class="strong">Trần Phan Chung Thủy</span><br>
            Kính mời cùng các con, cháu.
          </div>

          <!-- RSVP -->
          <div class="rsvpBox">
            <div class="label">XÁC NHẬN THAM DỰ</div>
            <input id="guestName" class="rsvpInput" placeholder="Họ và tên">

            <iframe name="hidden_iframe" style="display:none"></iframe>
            <form id="rsvpForm"
              action="https://docs.google.com/forms/d/e/1FAIpQLSeAbEEMP7dOkfBvpq9N7Kt3Z7NTFxxC3UYFzN2UIViH9GNDXA/formResponse"
              method="POST" target="hidden_iframe">
              <input type="hidden" name="entry.2035054770" id="f_name">
              <input type="hidden" name="entry.1484132997" id="f_attend">
            </form>

            <div class="btnRow">
              <button type="button" class="btnAttend" onclick="submitRSVP(event,'Tham dự')">THAM DỰ</button>
              <button type="button" class="btnDecline" onclick="submitRSVP(event,'Không tham dự')">KHÔNG THAM DỰ</button>
            </div>

            <div class="rsvpMsg" id="rsvpMsg"></div>
          </div>

          <div class="footer">(Vui lòng xác nhận để gia đình tiện sắp xếp.)</div>
        </div>

      </div>
    </div>
  </div>
</div>

<script>
function submitRSVP(e, choice){
  if(e) e.preventDefault();
  const name = document.getElementById('guestName').value.trim();
  if(!name){ alert('Vui lòng nhập Họ và tên'); return; }
  document.getElementById('f_name').value = name;
  document.getElementById('f_attend').value = choice;
  document.getElementById('rsvpForm').submit();
  const msg = document.getElementById('rsvpMsg');
  msg.textContent = `Gia đình đã ghi nhận: ${choice}. Xin chân thành cảm ơn.`;
  msg.classList.add('show');
}
</script>
</body>
</html>
