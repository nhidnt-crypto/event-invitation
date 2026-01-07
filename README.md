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

      --env:#f7f2ea;
      --env2:#efe5d8;
      --envStroke:rgba(58,42,31,.22);
      --shadow:rgba(0,0,0,.16);
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
      overflow-x:hidden;
    }

    .stage{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:26px 16px;
    }

    .scene{
      width:min(1040px, 100%);
      position:relative;
      perspective:1400px;
    }

    /* ====== ENVELOPE ====== */
    .envelope{
      position:relative;
      width:min(900px, 100%);
      margin:0 auto;
      height:440px;
      border-radius:20px;

      filter:none;         /* FIX stacking bug */
      z-index:20;
    }
    .envelope.open{ z-index:60; }

    .env-base{
      position:absolute;
      inset:0;
      border-radius:20px;
      background:linear-gradient(180deg, var(--env) 0%, var(--env2) 100%);
      border:1px solid var(--envStroke);
      overflow:hidden;

      box-shadow:0 24px 50px var(--shadow);
    }
    .env-base::before{
      content:"";
      position:absolute;
      inset:14px;
      border-radius:16px;
      border:1px solid rgba(58,42,31,.18);
      pointer-events:none;
    }

    /* ====== COVER TEXT on envelope (FIX: not hidden by flap) ====== */
    .coverText{
      position:absolute;
      left:50%;
      top:46%;
      transform:translate(-50%,-50%);
      text-align:center;
      width:min(560px, calc(100% - 70px));
      padding:18px 16px;
      border-radius:16px;
      background:rgba(255,255,255,.55);
      border:1px solid rgba(58,42,31,.18);
      box-shadow:0 10px 26px rgba(0,0,0,.08);

      z-index:12; /* ✅ ABOVE flap (6) and pocket (5) */
      pointer-events:none; /* click passes through */
    }
    .coverText .a1{
      font-size:28px;
      font-weight:700;
      letter-spacing:.03em;
      color:var(--wood-dark);
    }
    .coverText .a2{
      margin-top:8px;
      font-size:16px;
      letter-spacing:.14em;
      text-transform:uppercase;
      color:#6b5442;
    }
    .coverText .a3{
      margin-top:6px;
      font-size:22px;
      font-weight:700;
      letter-spacing:.04em;
      color:var(--wood-dark);
      text-transform:uppercase;
    }
    .coverText .line{
      width:140px;
      height:2px;
      background:linear-gradient(90deg,transparent,var(--wood),transparent);
      margin:14px auto 10px;
      opacity:.9;
    }
    .coverText .openHint{
      font-size:12px;
      letter-spacing:.18em;
      text-transform:uppercase;
      color:rgba(58,42,31,.70);
    }

    .open .coverText{
      opacity:0;
      transform:translate(-50%,-50%) scale(.98);
      transition:opacity 180ms ease, transform 180ms ease;
    }

    /* Pocket (front) */
    .env-pocket{
      position:absolute;
      left:0; right:0;
      bottom:0;
      height:60%;
      background:linear-gradient(180deg, rgba(255,255,255,.52) 0%, rgba(239,229,216,.94) 100%);
      border-top:1px solid rgba(58,42,31,.10);
      clip-path: polygon(0 0, 50% 58%, 100% 0, 100% 100%, 0 100%);
      z-index:5;
    }

    /* Flap */
    .env-flap{
      position:absolute;
      left:0; right:0;
      top:0;
      height:64%;
      transform-origin: top center;
      background:linear-gradient(180deg, #fffdfb 0%, #f2e7da 100%);
      clip-path: polygon(0 0, 100% 0, 50% 72%);
      border-bottom:1px solid rgba(58,42,31,.10);
      z-index:6;
      transform: rotateX(0deg);
      transition: transform 900ms cubic-bezier(.2,.85,.2,1);
      backface-visibility:hidden;
    }

    /* Seal button (no text on top) */
    .seal{
      position:absolute;
      left:50%;
      top:67%;
      transform:translate(-50%,-50%);
      width:56px;
      height:56px;
      border-radius:16px;
      background:rgba(255,255,255,.62);
      border:1px solid rgba(58,42,31,.20);
      display:flex;
      align-items:center;
      justify-content:center;
      z-index:11; /* below coverText (12), still above flap */
      box-shadow:0 10px 24px rgba(0,0,0,.10);
      cursor:pointer;
    }
    .seal svg{ display:block; opacity:.75; }
    .open .seal{
      opacity:0;
      transition:opacity 220ms ease;
      pointer-events:none;
    }

    /* Click anywhere closed */
    .clickOpen{
      position:absolute;
      inset:0;
      z-index:9;
      cursor:pointer;
    }
    .open .clickOpen{ display:none; }

    /* ====== BACKDROP (click to close after open) ====== */
    .backdrop{
      position:fixed;
      inset:0;
      background:rgba(0,0,0,.22);
      backdrop-filter: blur(2px);
      opacity:0;
      pointer-events:none;
      transition:opacity 250ms ease;
      z-index:10;
    }
    .open + .backdrop{
      opacity:1;
      pointer-events:auto;
    }

    /* ====== CARD SLIDE OUT ====== */
    .cardWrap{
      position:absolute;
      left:50%;
      top:26px;
      transform:translateX(-50%) translateY(240px) scale(.985);
      width:min(980px, 100%);
      z-index:40;
      transition: transform 950ms cubic-bezier(.2,.85,.2,1), opacity 500ms ease;
      opacity:0;
      pointer-events:none;
    }
    .open .cardWrap{
      transform:translateX(-50%) translateY(-12px) scale(1);
      opacity:1;
      pointer-events:auto;
    }
    .open .env-flap{ transform: rotateX(165deg); }

    /* Close button */
    .closeBtn{
      position:absolute;
      top:-14px;
      right:-14px;
      width:44px;
      height:44px;
      border-radius:14px;
      border:1px solid rgba(90,60,40,.28);
      background:rgba(255,255,255,.78);
      color:var(--wood-dark);
      font-weight:900;
      font-size:18px;
      cursor:pointer;
      box-shadow:0 14px 30px rgba(0,0,0,.12);
      display:flex;
      align-items:center;
      justify-content:center;
      z-index:41;
    }
    .closeBtn:active{ transform:translateY(1px); }

    /* ====== CARD CONTENT ====== */
    .wrap{
      min-height:unset;
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
      margin:0 auto;
    }

    .frame-inner{
      border:1px solid rgba(58,42,31,.22);
      padding:26px;
      background:linear-gradient(180deg,#fffdfb 0%,#fbf8f4 100%);
    }

    .grid{
      display:grid;
      grid-template-columns:320px 1fr;
      gap:32px;
      align-items:center;
    }

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
      .envelope{ height:480px; }
      .coverText{ top:45%; width:calc(100% - 44px); }
      .coverText .a1{ font-size:26px; }
      .closeBtn{ top:-10px; right:-10px; }
      .seal{ top:69%; }
    }

    @media (prefers-reduced-motion: reduce){
      .env-flap, .cardWrap, .backdrop{ transition:none !important; }
    }
  </style>
</head>

<body>
  <div class="stage">
    <div class="scene">

      <div class="envelope" id="env">
        <div class="env-base"></div>

        <!-- ✅ Outside envelope text (NOT hidden by flap) -->
        <div class="coverText" aria-hidden="true">
          <div class="a1">Lễ Giỗ 1 Năm</div>
          <div class="a2">Thiếu Tướng</div>
          <div class="a3">Mai Xuân Tần</div>
          <div class="line"></div>
          <div class="openHint">MỞ THIỆP</div>
        </div>

        <!-- click anywhere on closed envelope -->
        <div class="clickOpen" onclick="openEnvelope()"></div>

        <!-- flap -->
        <div class="env-flap" aria-hidden="true"></div>

        <!-- seal icon button -->
        <div class="seal" aria-hidden="true" onclick="openEnvelope()" title="Mở thiệp">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <path d="M7 10l5 5 5-5" stroke="rgba(58,42,31,.78)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>

        <!-- pocket front -->
        <div class="env-pocket" aria-hidden="true"></div>

        <!-- CARD slides out -->
        <div class="cardWrap" id="cardWrap" role="dialog" aria-modal="true" aria-label="Thiệp mời">
          <button class="closeBtn" type="button" onclick="closeEnvelope()" aria-label="Đóng thiệp">×</button>

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

        </div>
      </div>

      <!-- Backdrop right after envelope -->
      <div class="backdrop" id="backdrop" onclick="closeEnvelope()" aria-hidden="true"></div>

    </div>
  </div>

  <script>
    const env = document.getElementById('env');

    function openEnvelope(){
      env.classList.add('open');
      setTimeout(()=>{ window.scrollTo({top:0, behavior:'smooth'}); }, 60);
    }

    function closeEnvelope(){
      env.classList.remove('open');
      setTimeout(()=>{ window.scrollTo({top:0, behavior:'smooth'}); }, 60);
    }

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

    window.addEventListener('keydown', (e)=>{
      if(e.key === 'Enter' || e.key === ' '){
        if(!env.classList.contains('open')) openEnvelope();
      }
      if(e.key === 'Escape'){
        if(env.classList.contains('open')) closeEnvelope();
      }
    });
  </script>
</body>
</html>
