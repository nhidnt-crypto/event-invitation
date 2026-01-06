<!-- ===== RSVP MODAL (NO NEW TAB) ===== -->
<style>
  .rsvp-modal{
    position:fixed; inset:0;
    background:rgba(0,0,0,.55);
    display:none; align-items:center; justify-content:center;
    padding:18px; z-index:9999;
  }
  .rsvp-modal.is-open{ display:flex; }
  .rsvp-panel{
    width:min(860px, 100%);
    background:#f7f3ee;
    border-radius:16px;
    overflow:hidden;
    box-shadow:0 18px 50px rgba(0,0,0,.25);
    border:1px solid rgba(90,60,40,.25);
  }
  .rsvp-head{
    display:flex; align-items:center; justify-content:space-between;
    padding:12px 14px;
    background:linear-gradient(135deg,#3a2a1f 0%, #5b3e2b 60%, #8b6a4f 100%);
    color:#fff;
    font-family:Georgia, "Times New Roman", serif;
  }
  .rsvp-head .ttl{font-weight:700; letter-spacing:.06em; font-size:13px;}
  .rsvp-close{
    background:transparent; border:0; color:#fff;
    font-size:20px; cursor:pointer; line-height:1;
    padding:6px 10px; border-radius:10px;
  }
  .rsvp-close:hover{ background:rgba(255,255,255,.12); }
  .rsvp-body{ background:#fff; }
  .rsvp-iframe{
    width:100%; height:min(78vh, 720px);
    border:0; display:block;
  }
</style>

<div class="btnRow">
  <a class="btn attend" href="#" id="btnAttend">THAM DỰ</a>
  <a class="btn decline" href="#" id="btnDecline">KHÔNG THAM DỰ</a>
</div>

<div class="rsvp-modal" id="rsvpModal" aria-hidden="true">
  <div class="rsvp-panel" role="dialog" aria-modal="true" aria-label="Xác nhận tham dự">
    <div class="rsvp-head">
      <div class="ttl">XÁC NHẬN THAM DỰ • LỄ GIỖ 1 NĂM</div>
      <button class="rsvp-close" id="rsvpClose" aria-label="Đóng">✕</button>
    </div>
    <div class="rsvp-body">
      <!-- IFRAME: mở form ngay trong trang, không cần chuyển tab -->
      <iframe
        id="rsvpFrame"
        class="rsvp-iframe"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
        src="https://docs.google.com/forms/d/e/1FAIpQLSeAbEEMP7dOkfBvpq9N7Kt3Z7NTFxxC3UYFzN2UIViH9GNDXA/viewform?embedded=true">
      </iframe>
    </div>
  </div>
</div>

<script>
  // ✅ Bạn có thể dùng "prefill links" để tự chọn sẵn Tham dự / Không tham dự
  // Hiện tại mình để mặc định mở embed form.
  // Khi bạn gửi cho mình 2 prefill link (Attend/Decline), mình sẽ thay vào 2 biến dưới đây.
  const EMBED_DEFAULT = "https://docs.google.com/forms/d/e/1FAIpQLSeAbEEMP7dOkfBvpq9N7Kt3Z7NTFxxC3UYFzN2UIViH9GNDXA/viewform?embedded=true";

  // TODO: Dán prefill links vào đây (loại embedded=true hoặc pp_url đều được, miễn chạy):
  const PREFILL_ATTEND  = ""; // ví dụ: https://docs.google.com/forms/d/e/.../viewform?usp=pp_url&entry.123=Tham%20dự
  const PREFILL_DECLINE = "";

  const modal = document.getElementById("rsvpModal");
  const frame = document.getElementById("rsvpFrame");

  function openModal(url){
    frame.src = url || EMBED_DEFAULT;
    modal.classList.add("is-open");
    modal.setAttribute("aria-hidden","false");
    document.body.style.overflow = "hidden";
  }
  function closeModal(){
    modal.classList.remove("is-open");
    modal.setAttribute("aria-hidden","true");
    document.body.style.overflow = "";
  }

  document.getElementById("btnAttend").addEventListener("click", (e)=>{
    e.preventDefault();
    openModal(PREFILL_ATTEND || EMBED_DEFAULT);
  });

  document.getElementById("btnDecline").addEventListener("click", (e)=>{
    e.preventDefault();
    openModal(PREFILL_DECLINE || EMBED_DEFAULT);
  });

  document.getElementById("rsvpClose").addEventListener("click", closeModal);
  modal.addEventListener("click", (e)=>{ if(e.target === modal) closeModal(); });
  document.addEventListener("keydown", (e)=>{ if(e.key === "Escape") closeModal(); });
</script>
