THƯ MỜI LỄ GIỖ ĐẦU
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lễ Giỗ ĐẦU • Ông Mai Xuân Tần</title>

  <!-- Open Graph (share Facebook/Zalo) -->
  <meta property="og:title" content="LỄ GIỖ ĐẦU • Ông Mai Xuân Tần">
  <meta property="og:description" content="Trân trọng kính mời tham dự Lễ Giỗ Đầu • 18.01.2026 • TP.HCM">
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://nhidnt-crypto.github.io/event-invitation/">
  <meta property="og:image" content="https://i.postimg.cc/hjzSLMqq/Ong-cua-Bac-1.png">
  <meta name="theme-color" content="#efe7dd">

  <!-- ✅ FONT VIETNAMESE SAFE -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Serif:ital,wght@0,400;0,600;0,700;1,400&display=swap&subset=vietnamese" rel="stylesheet">

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
    html,body{ height:100%; }
    body{
      margin:0;
      font-family:"Noto Serif","Times New Roman",serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-rendering: geometricPrecision;
      font-kerning: normal;

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

      height:auto;
      min-height:440px;

      border-radius:20px;
      z-index:20;
      isolation:isolate;
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

    /* ====== COVER TEXT on envelope ====== */
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
      z-index:12;
      pointer-events:none;
    }
    .coverText .a1{
      font-size:28px;
      font-weight:700;
      letter-spacing:.02em;
      color:var(--wood-dark);
    }
    .coverText .a2{
      margin-top:8px;
      font-size:16px;
      letter-spacing:.12em;
      text-transform:uppercase;
      color:#6b5442;
    }
    .coverText .a3{
      margin-top:6px;
      font-size:22px;
      font-weight:700;
      letter-spacing:.02em;
      color:var(--wood-dark);
      text-transform:uppercase;
      font-feature-settings:"kern" 1, "liga" 1;
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

    /* Pocket */
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
      will-change:transform;
    }

    /* Seal */
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
      z-index:11;
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

    /* Backdrop */
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
      top:22px;
      transform:translateX(-50%) translateY(240px) scale(.985);
      width:min(980px, 100%);
      z-index:40;
      transition: transform 950ms cubic-bezier(.2,.85,.2,1), opacity 500ms ease;
      opacity:0;
      pointer-events:none;
    }
    .open .cardWrap{
      transform:translateX(-50%) translateY(-8px) scale(1);
      opacity:1;
      pointer-events:auto;
    }
    .open .env-flap{ transform: rotateX(165deg); }

    /* ✅ card không tràn màn hình */
    .cardWrap .wrap{
      padding:24px;
      max-height:calc(100vh - 70px);
      overflow:auto;
      -webkit-overflow-scrolling: touch;
    }

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
      align-items:start;
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
      border-radius:10px;
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
      letter-spacing:.02em;
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
      letter-spacing:.10em;
      color:#6b5442;
      text-transform:uppercase;
    }
    .person .name{
      font-size:22px;
      font-weight:700;
      color:var(--wood-dark);
      letter-spacing:.04em;
      font-feature-settings:"kern" 1, "liga" 1;
    }

    .note{
      margin-top:14px;
      font-size:15.5px;
      line-height:1.85;
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

    /* ===== RSVP CLOSED NOTICE ===== */
    .rsvpClosed{
      margin-top:18px;
      width:min(520px, 100%);
      margin-left:auto;
      margin-right:auto;
      padding:14px 14px;
      border-radius:14px;
      border:1px solid rgba(90,60,40,.22);
      background:rgba(255,255,255,.70);
      box-shadow:0 10px 22px rgba(0,0,0,.06);
      text-align:center;
    }
    .rsvpClosed__title{
      font-size:12px;
      letter-spacing:.16em;
      text-transform:uppercase;
      color:#6b5442;
      font-weight:800;
    }
    .rsvpClosed__msg{
      margin-top:10px;
      font-size:16px;
      line-height:1.8;
      color:#4a382c;
      font-weight:700;
    }
    .rsvpClosed__sub{
      margin-top:8px;
      font-size:12.5px;
      color:#7a6757;
      line-height:1.7;
    }

    .footer{
      margin-top:16px;
      font-size:12.5px;
      color:#7a6757;
    }

    /* ✅ Tablet / Mobile */
    @media(max-width:860px){
      .grid{ grid-template-columns:1fr; gap:18px; }
      .envelope{ min-height:480px; }

      .coverText{ top:45%; width:calc(100% - 44px); padding:16px 14px; }
      .coverText .a1{ font-size:26px; }
      .coverText .a3{ font-size:20px; }

      .closeBtn{ top:-10px; right:-10px; }
      .seal{ top:69%; }

      .frame-inner{ padding:18px; }
      h1{ font-size:30px; }
      .value{ font-size:16.5px; }
    }

    /* ✅ Mobile nhỏ */
    @media(max-width:420px){
      .photo-frame{ width:240px; height:305px; }
      .program{ width:240px; }
      .cardWrap .wrap{ padding:18px; max-height:calc(100vh - 60px); }
      .frame{ padding:12px; }
      .frame-inner{ padding:16px; }
      .coverText .a1{ font-size:24px; }
      .coverText .a2{ letter-spacing:.10em; }
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

        <div class="coverText" aria-hidden="true">
          <div class="a1">Lễ Giỗ Đầu</div>
          <div class="a2">Ông</div>
          <div class="a3">Mai Xuân Tần</div>
          <div class="line"></div>
          <div class="openHint">MỞ THIỆP</div>
        </div>

        <div class="clickOpen" onclick="openEnvelope()"></div>

        <div class="env-flap" aria-hidden="true"></div>

        <div class="seal" aria-hidden="true" onclick="openEnvelope()" title="Mở thiệp">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <path d="M7 10l5 5 5-5" stroke="rgba(58,42,31,.78)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>

        <div class="env-pocket" aria-hidden="true"></div>

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
                        <img
                          src="https://i.postimg.cc/hjzSLMqq/Ong-cua-Bac-1.png"
                          alt="Ông Mai Xuân Tần"
                          loading="lazy"
                        >
                      </div>
                    </div>

                    <div class="program">
                      <h3>Chương trình</h3>
                      <ul>
                        <li>Tưởng niệm &amp; thắp hương</li>
                        <li>Dùng bữa thân mật</li>
                      </ul>
                    </div>
                  </div>

                  <!-- RIGHT -->
                  <div class="right">
                    <div class="title-small">TRÂN TRỌNG KÍNH MỜI</div>
                    <h1>LỄ GIỖ ĐẦU</h1>
                    <div class="subtitle">Tưởng niệm &amp; tri ân</div>
                    <div class="divider"></div>

                    <div class="person">
                      <div class="rank">Ông</div>
                      <div class="name">MAI XUÂN TẦN</div>
                    </div>

                    <div class="note">
                      Ông/Bố kính yêu của chúng tôi: <span class="strong">Mai Xuân Tần</span>.<br>
                      Nhân ngày giỗ đầu của Ông/Bố, gia đình chúng tôi trân trọng kính mời quý thân bằng quyến thuộc,
                      bà con, bạn hữu đến dự lễ giỗ và dùng bữa cơm thân mật, cùng gia đình tưởng nhớ đến Ông/Bố.
                    </div>

                    <div class="info">
                      <div>
                        <div class="label">THỜI GIAN</div>
                        <div class="value">11:00 • Ngày 18 tháng 01 năm 2026</div>
                      </div>
                      <div style="margin-top:12px">
                        <div class="label">ĐỊA ĐIỂM</div>
                        <div class="value">Nhà hàng Biển Dương 6, 205 Cách Mạng Tháng Tám, Phường Xuân Hòa, TP. Hồ Chí Minh.</div>
                      </div>
                    </div>

                    <!-- ✅ RSVP REMOVED / CLOSED NOTICE -->
                    <div class="rsvpClosed" role="note" aria-label="Thông báo xác nhận tham dự">
                      
                      <div class="rsvpClosed__msg">Đã hết thời gian đăng ký tham dự.</div>
                      <div class="rsvpClosed__sub">(Gia đình xin chân thành cảm ơn.)</div>
                    </div>

                    <div class="footer">(Trân trọng.)</div>
                  </div>

                </div>
              </div>
            </div>
          </div>

        </div>
      </div>

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

    window.addEventListener('keydown', (e)=>{
      if(e.key === 'Escape'){
        if(env.classList.contains('open')) closeEnvelope();
      }
    });
  </script>
</body>
</html>
