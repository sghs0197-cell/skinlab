<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#176b56">
<title>스킨랩 | 내 피부 고민에 맞는 제품 찾기</title>
<style>
:root {
  --bg: #f6f7f2;
  --paper: #fff;
  --ink: #213a33;
  --muted: #64766d;
  --green: #176b56;
  --soft: #eaf3e9;
  --line: #dfe7dd;
  --peach: #fbefe4;
}
* { box-sizing: border-box; }
[hidden] { display: none !important; }
html { scroll-padding-top: 24px; }
body {
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font-family: system-ui, -apple-system, "Malgun Gothic", sans-serif;
  line-height: 1.7;
  letter-spacing: -.025em;
}
button, input, select, textarea { font: inherit; }
button, a, input, select { -webkit-tap-highlight-color: transparent; }
button { cursor: pointer; }
a { color: var(--green); text-underline-offset: 4px; }
:focus-visible { outline: 3px solid #bd862e; outline-offset: 4px; }
.wrap { max-width: 1260px; margin: auto; padding: 25px; }
header {
  display: flex; justify-content: space-between; align-items: center;
  gap: 15px; padding: 0 0 22px; border-bottom: 1px solid var(--line);
}
.logo {
  display: flex; align-items: center; gap: 10px;
  color: var(--green); font-size: 29px; font-weight: 850;
  letter-spacing: -1.5px;
}
.logo-mark {
  display: grid; place-items: center; width: 41px; height: 41px;
  border-radius: 14px; background: var(--green); color: white;
}
.header-note { color: var(--muted); font-size: 12px; }
.hero {
  position: relative; overflow: hidden; display: grid;
  grid-template-columns: 1.35fr 1fr; align-items: center;
  gap: 20px; margin: 25px 0;
  padding: 39px 44px; border: 1px solid #dce6d8;
  border-radius: 30px;
  background: linear-gradient(115deg, #e7f0e3, #f1f3e6 65%, #f7eadc);
}
.eyebrow {
  color: #53745a; font-size: 11px;
  letter-spacing: 1.8px; font-weight: 800;
}
h1 {
  margin: 12px 0 16px;
  font-size: clamp(30px, 4.2vw, 48px);
  line-height: 1.28; letter-spacing: -.065em;
}
h1 em { color: var(--green); font-style: normal; }
h2 { margin: 0 0 10px; font-size: 23px; line-height: 1.45; }
h3 { margin: 0 0 8px; font-size: 16px; }
p { margin: 8px 0; }
.muted { color: var(--muted); }
.small { font-size: 12px; }
.hero-description { font-size: 15px; }
.hero-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 22px; }
.hero-tags span {
  padding: 5px 10px; border: 1px solid #cddcc9;
  border-radius: 30px; font-size: 11px;
  background: #ffffff70; color: #45634c;
}
.art {
  position: relative; display: flex; align-items: flex-end;
  justify-content: center; gap: 17px; min-height: 235px;
  padding-bottom: 20px;
}
.orbit {
  position: absolute; top: 0; width: 230px; height: 230px;
  border: 1px solid #8eaa7e55; border-radius: 50%;
  background: #ffffff35;
}
.orbit::after {
  content: ""; position: absolute; inset: 20px;
  border: 1px dashed #8eaa7e55; border-radius: 50%;
}
.bottle {
  position: relative; display: grid; align-content: center;
  justify-items: center; width: 86px; height: 150px;
  border: 1px solid #bed1b8; border-radius: 15px 15px 23px 23px;
  background: linear-gradient(100deg, #fcfff8, #dbe9d1);
  transform: rotate(-9deg);
  box-shadow: 8px 13px 18px #38582b18;
}
.bottle::before {
  content: ""; position: absolute; top: -30px; left: 22px;
  width: 40px; height: 30px; border-radius: 7px 7px 2px 2px;
  background: #396c53;
}
.bottle b { color: #3f6b4e; font-size: 15px; }
.bottle small { font-size: 8px; letter-spacing: 1px; }
.jar {
  position: relative; display: grid; align-content: center;
  justify-items: center; width: 104px; height: 78px;
  margin-bottom: -4px; border: 1px solid #dfc5af;
  border-radius: 12px 12px 23px 23px;
  background: linear-gradient(100deg, #fff3e7, #ecd2bb);
  transform: rotate(8deg); box-shadow: 7px 12px 18px #58422a13;
}
.jar::before {
  content: ""; position: absolute; top: -13px; left: -3px; right: -3px;
  height: 20px; border-radius: 9px 9px 3px 3px;
  background: #dfd4bc; border: 1px solid #cbbd9f;
}
.jar b { font-size: 14px; color: #7b6049; }
.art-label {
  position: absolute; top: 14px; right: 0;
  padding: 6px 11px; border: 1px solid white;
  border-radius: 10px; background: #ffffffda;
  font-size: 11px; transform: rotate(5deg);
}
.intro-line {
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 10px; margin: 22px 0 15px;
}
.flow { display: flex; align-items: center; gap: 10px; font-size: 13px; }
.flow strong { color: var(--green); }
.flow span { color: #90a18e; }
.tag {
  display: inline-flex; padding: 4px 10px;
  background: var(--soft); color: var(--green);
  border-radius: 30px; font-size: 11px; font-weight: 750;
}
.layout {
  display: grid; grid-template-columns: 410px minmax(0, 1fr);
  gap: 23px; align-items: start;
}
.panel {
  min-width: 0; padding: 25px; background: white;
  border: 1px solid var(--line); border-radius: 24px;
}
.panel-top {
  display: flex; justify-content: space-between; align-items: center;
  gap: 10px; margin-bottom: 15px;
}
.panel-top small { color: #6a816b; letter-spacing: 1px; font-size: 10px; }
fieldset { min-width: 0; padding: 0; margin: 24px 0; border: 0; }
legend, .label { display: block; margin-bottom: 8px; font-size: 14px; font-weight: 750; }
.group-title { margin: 18px 0 7px; color: #657d64; font-size: 11px; font-weight: 750; }
.choice {
  display: flex; align-items: flex-start; gap: 10px;
  margin-top: 7px; padding: 11px 12px; cursor: pointer;
  border: 1px solid #e2e8de; border-radius: 12px;
  background: #fcfdfb;
}
.choice:hover { border-color: #a5bfa4; }
.choice:has(input:checked) {
  border-color: #719a77; background: #edf5e9;
  box-shadow: inset 0 0 0 1px #719a77;
}
.choice input {
  width: 16px; height: 16px; flex-shrink: 0;
  margin: 5px 0 0; accent-color: var(--green);
}
.choice strong { display: block; font-size: 13px; }
.choice small { display: block; color: var(--muted); font-size: 11px; }
select, textarea {
  width: 100%; min-height: 44px; padding: 10px 11px;
  border: 1px solid #d0ddce; border-radius: 10px;
  background: #fdfefb; color: var(--ink); font-size: 13px;
}
textarea { min-height: 160px; resize: vertical; }
.field-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 13px; margin: 20px 0; }
.field-grid .label { font-size: 12px; }
.full { grid-column: 1 / -1; }
.safe-box {
  padding: 15px; background: #f8f7ed;
  border: 1px solid #e9e5d3; border-radius: 14px;
}
.safe-box select { background: white; }
.summary { margin: 18px 0 8px; color: #527251; font-size: 12px; }
.primary, .secondary, .product-link {
  min-height: 44px; border-radius: 11px; padding: 11px 14px;
  font-size: 13px; font-weight: 700;
}
.primary { width: 100%; border: 0; background: var(--green); color: white; }
.primary:hover { background: #105740; }
.secondary {
  border: 1px solid var(--line); background: #f8faf5;
  color: var(--ink);
}
.clear { width: 100%; margin-top: 9px; background: white; }
.privacy { padding-top: 13px; margin-top: 15px; border-top: 1px solid var(--line); }
.error { color: #a33f32; font-size: 12px; }
.empty { text-align: center; padding: 45px 8px 28px; }
.empty-icon {
  display: grid; place-items: center; width: 85px; height: 85px;
  margin: 0 auto 24px; border-radius: 28px;
  background: #edf4e6; font-size: 40px; transform: rotate(-7deg);
}
.empty h2 { margin-top: 12px; }
.preview-steps {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 9px; margin-top: 30px; padding-top: 25px;
  border-top: 1px dashed var(--line);
}
.preview-steps div { padding: 15px 5px; background: #f6f8f0; border-radius: 12px; }
.preview-steps small { display: block; color: #7d9872; font-size: 10px; }
.preview-steps b { font-size: 12px; }
.result-title { margin: 16px 0 12px; font-size: 27px; letter-spacing: -.05em; }
.chips { display: flex; flex-wrap: wrap; gap: 6px; margin: 12px 0; }
.chip {
  padding: 4px 9px; border: 1px solid #e0e8db;
  border-radius: 7px; background: #fafbf7; font-size: 11px; color: #5c7359;
}
.advice {
  padding: 18px; margin: 19px 0; border-radius: 15px;
  border: 1px solid #dce6d3; background: #f0f6e9;
}
.advice h3 { font-size: 14px; }
.advice p { font-size: 13px; }
.section-title {
  display: flex; justify-content: space-between; align-items: center;
  gap: 10px; margin: 25px 0 11px;
}
.section-title h3 { margin: 0; }
.product-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 14px; }
.photo { display: block; position: relative; aspect-ratio: 1 / 1; min-height: 170px; background: #fff; }
.photo img { display: block; width: 100%; height: 100%; object-fit: contain; }
.empty:has(.product-grid) { padding: 8px 0; text-align: left; }
.empty .product-grid { margin-top: 18px; }
.safe-box:disabled { opacity: .65; }
.safe-box legend { padding: 0 4px; }
.step-help { margin: 6px 0 10px; color: var(--muted); font-size: 12px; }
.product {
  min-width: 0; overflow: hidden; display: flex; flex-direction: column;
  border: 1px solid var(--line); border-radius: 17px; background: white;
}
.photo {
  display: grid; place-items: center; height: 195px;
  padding: 12px; background: #f7f8f3; text-decoration: none;
}
.photo img { width: 100%; height: 100%; min-height: 0; object-fit: contain; border-radius: 9px; }
.photo-fallback { text-align: center; color: var(--muted); font-size: 12px; }
.photo-fallback span { display: block; margin-bottom: 5px; font-size: 35px; }
.product-body { display: flex; flex-direction: column; flex: 1; gap: 8px; padding: 16px; }
.brand { margin: 0; color: var(--muted); font-size: 11px; }
.product h4 { margin: 0; font-size: 15px; line-height: 1.55; overflow-wrap: anywhere; }
.product-reason { margin: 0; font-size: 12px; }
.usage { margin: 0; color: var(--muted); font-size: 11px; }
.product-link {
  display: block; margin-top: auto; border: 1px solid #cdddc8;
  background: #edf4e8; color: #245d42; text-align: center;
  text-decoration: none;
}
.product-link:hover { background: #dfeeda; }
.search-link { text-align: center; font-size: 11px; }
.note {
  padding: 14px 16px; border: 1px solid #eee2c7;
  border-radius: 13px; background: #fff9eb; color: #76603a; font-size: 12px;
}
.routine { display: grid; grid-template-columns: 1fr 1fr; gap: 11px; margin-top: 12px; }
.routine div { padding: 16px; border-radius: 13px; background: #faf5e9; }
.routine div:last-child { background: #edf2f7; }
.routine b { font-size: 13px; }
.routine p { font-size: 12px; }
.tips { padding-left: 20px; font-size: 13px; }
.tips li { margin: 9px 0; }
.danger { padding: 23px; border: 1px solid #e9c2b6; border-radius: 17px; background: #fff2ed; color: #713c30; }
.danger h2 { color: #8d4232; font-size: 23px; }
.danger p { font-size: 14px; }
.emergency-link {
  display: inline-block; margin-top: 12px; padding: 11px 17px;
  border-radius: 10px; background: #973f2e; color: white; text-decoration: none;
}
.actions { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 20px; }
footer { padding: 30px 5px 10px; color: var(--muted); text-align: center; font-size: 11px; }
@media (max-width: 1000px) {
  .layout { grid-template-columns: 350px minmax(0, 1fr); gap: 16px; }
  .panel { padding: 21px; }
  .hero { padding: 30px; }
  .photo { height: 170px; }
}
@media (max-width: 780px) {
  .wrap { padding: 18px 16px; }
  .layout { grid-template-columns: 1fr; }
  .hero { grid-template-columns: 1fr; padding: 27px; }
  .art { min-height: 195px; margin-top: 20px; }
  .orbit { width: 195px; height: 195px; }
  .bottle { height: 125px; width: 77px; }
  .art-label { right: calc(50% - 135px); }
  .header-note { display: none; }
  .photo { height: 210px; }
  .empty { padding-top: 25px; }
}
@media (max-width: 430px) {
  .product-grid, .routine { grid-template-columns: 1fr; }
  .panel { padding: 20px; }
  .photo { height: 235px; }
  .field-grid { grid-template-columns: 1fr; }
  .full { grid-column: auto; }
  .result-title { font-size: 24px; }
  .hero { padding: 25px 22px; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { scroll-behavior: auto !important; }
}
</style>
</head>

<body>
<div class="wrap">
  <header>
    <div class="logo"><span class="logo-mark" aria-hidden="true">✳</span>skinlab.</div>
    <span class="header-note">피부 고민별 스킨케어 제품 찾기</span>
  </header>

  <section class="hero">
    <div>
      <div class="eyebrow">FIND YOUR DAILY SKINCARE</div>
      <h1>지금 내 피부에는<br><em>어떤 제품이 좋을까?</em></h1>
      <p class="muted hero-description">
        당김부터 번들거림, 오돌토돌함까지.<br>
        피부 고민을 고르고 실제 제품을 비교해 보세요.
      </p>
      <div class="hero-tags">
        <span>상세 고민 선택</span>
        <span>실제 제품 사진</span>
        <span>올리브영 상품 연결</span>
      </div>
    </div>
    <div class="art" aria-hidden="true">
      <div class="orbit"></div>
      <div class="bottle"><b>skinlab.</b><small>DAILY MOISTURE</small></div>
      <div class="jar"><b>skinlab.</b></div>
      <div class="art-label">나의 데일리 케어 찾기 🌿</div>
    </div>
  </section>

  <div class="intro-line">
    <div class="flow"><strong>01 고민 선택</strong><span>→</span><strong>02 제품 확인</strong></div>
    <span class="small muted">회원가입 없이 사용할 수 있어요</span>
  </div>

  <main class="layout">
    <section class="panel" aria-labelledby="check-title">
      <div class="panel-top">
        <small>01 / SKIN CHECK</small>
        <span class="tag">여러 고민 선택 가능</span>
      </div>
      <h2 id="check-title">어떤 점이 신경 쓰이나요?</h2>
      <p class="muted small">느껴지는 상태를 골라 주세요. 피부 질환을 진단하는 검사는 아니에요.</p>

      <form id="skin-form">
        <fieldset class="safe-box">
          <legend>먼저, 현재 상태를 확인해 주세요</legend>
          <select id="safety" required aria-label="안전 상태">
            <option value="">선택해 주세요</option>
            <option value="clear">아래의 심한 증상은 없어요</option>
            <option value="medical">심한 통증·진물·물집·심한 붓기 등이 있어요</option>
            <option value="emergency">호흡곤란 또는 입술·혀·목이 갑자기 부었어요</option>
            <option value="unsure">잘 모르겠어요</option>
          </select>
          <p class="small muted">
            빠르게 번지는 발진이나 눈의 통증도 제품 추천보다 진료가 먼저예요.
          </p>
        </fieldset>

        <fieldset>
          <legend>1. 피부 고민을 자세히 골라 주세요</legend>
          <p class="small muted">해당하는 항목을 모두 선택하세요.</p>
          <div id="concern-options"></div>
        </fieldset>

        <div id="priority-field" hidden>
          <label class="label" for="priority">가장 신경 쓰이는 고민</label>
          <select id="priority"></select>
        </div>

        <div class="field-grid">
          <div>
            <label class="label" for="area">2. 주로 어느 부위인가요?</label>
            <select id="area">
              <option value="whole">얼굴 전체</option>
              <option value="forehead">이마</option>
              <option value="nose">코·코 주변</option>
              <option value="cheeks">볼</option>
              <option value="chin">턱·입 주변</option>
              <option value="eyes">눈·눈꺼풀 주변</option>
            </select>
          </div>
          <div>
            <label class="label" for="duration">3. 언제부터 느꼈나요?</label>
            <select id="duration">
              <option value="recent">최근 며칠 이내</option>
              <option value="week">약 1~2주</option>
              <option value="long">2주 넘게 지속</option>
              <option value="repeat">자주 반복돼요</option>
            </select>
          </div>
          <div>
            <label class="label" for="sensation">4. 통증·가려움 정도</label>
            <select id="sensation">
              <option value="none">거의 없어요</option>
              <option value="mild">가볍게 느껴져요</option>
              <option value="strong">심하거나 생활에 불편해요</option>
            </select>
          </div>
          <div>
            <label class="label" for="trend">5. 상태 변화</label>
            <select id="trend">
              <option value="stable">비슷하거나 나아져요</option>
              <option value="worse">점점 심해져요</option>
              <option value="spreading">빠르게 번지고 있어요</option>
            </select>
          </div>
          <div class="full">
            <label class="label" for="new-product">6. 새 제품 사용 후 시작됐나요?</label>
            <select id="new-product">
              <option value="no">아니요 / 관련이 없어 보여요</option>
              <option value="yes">네, 새 제품 사용 후 시작됐어요</option>
              <option value="unsure">잘 모르겠어요</option>
            </select>
          </div>
          <div>
            <label class="label" for="makeup">7. 메이크업·선크림 사용</label>
            <select id="makeup">
              <option value="none">거의 사용하지 않아요</option>
              <option value="sun">선크림 위주로 사용해요</option>
              <option value="makeup">메이크업도 해요</option>
            </select>
          </div>
          <div>
            <label class="label" for="outdoor">8. 야외활동</label>
            <select id="outdoor">
              <option value="daily">등하교 등 일상 외출</option>
              <option value="long">운동 등 긴 야외활동</option>
            </select>
          </div>
        </div>

        <p id="selection-summary" class="summary" aria-live="polite">선택한 피부 고민이 없어요.</p>
        <p id="form-error" class="error" role="alert"></p>
        <button class="primary" type="submit">내 고민에 맞는 제품 보기 ↗</button>
        <button id="reset" class="secondary clear" type="button">다시 선택하기</button>
      </form>

      <p class="privacy small muted">
        선택한 정보는 저장하거나 서버에 보내지 않아요.<br>
        상품 사진은 올리브영 이미지 서버에서 불러와요.
      </p>
    </section>

    <section class="panel" aria-label="제품 추천 결과">
      <div id="empty" class="empty">
        <div class="empty-icon" aria-hidden="true">🧴</div>
        <div class="eyebrow">YOUR DAILY PICKS</div>
        <h2>고민은 자세하게,<br>제품 선택은 간단하게.</h2>
        <p class="muted small">
          피부 고민과 현재 상태를 선택하면<br>
          비교해 볼 실제 제품을 보여드려요.
        </p>
        <div class="preview-steps">
          <div><small>CHECK</small><b>고민 선택</b></div>
          <div><small>COMPARE</small><b>제품 비교</b></div>
          <div><small>OPEN</small><b>올리브영 확인</b></div>
        </div>
        <p class="small muted" style="margin-top:22px">
          특정 제품의 효과나 개인 적합성을 보장하지는 않아요.
        </p>
      </div>
      <div id="result" tabindex="-1" hidden></div>
    </section>
  </main>

  <footer>
    skinlab. · 피부 고민별 스킨케어 제품 찾기<br>
    화장품은 질환 치료제가 아닙니다. 증상이 지속되거나 악화되면 의료진과 상담하세요.<br>
    올리브영과 제휴한 서비스가 아니며 상품 구성·사진·재고는 변경될 수 있습니다.
  </footer>
</div>

<script>
"use strict";

(() => {
  const $ = id => document.getElementById(id);
  const escapeHTML = value => String(value).replace(/[&<>"']/g, char => ({
    "&": "&amp;", "<": "&lt;", ">": "&gt;",
    '"': "&quot;", "'": "&#39;"
  }[char]));

  const CONCERNS = [
    {
      id: "tight", group: "💧 건조함·당김",
      title: "세안 후 피부가 당겨요",
      description: "씻고 나면 금방 땅기거나 건조하게 느껴져요."
    },
    {
      id: "flake", group: "💧 건조함·당김",
      title: "하얀 각질이 일어나고 화장이 떠요",
      description: "코 주변·볼 등이 거칠고 들뜨는 느낌이에요."
    },
    {
      id: "oil", group: "🌿 번들거림·피지",
      title: "이마와 코가 쉽게 번들거려요",
      description: "시간이 지나면 얼굴에 유분이 많이 느껴져요."
    },
    {
      id: "combination", group: "🌿 번들거림·피지",
      title: "코는 번들거리는데 볼은 건조해요",
      description: "얼굴 부위마다 건조함과 유분감이 달라요."
    },
    {
      id: "blackhead", group: "🌿 번들거림·피지",
      title: "코의 검은 점과 피지가 신경 쓰여요",
      description: "코·턱에 작은 점이나 피지가 눈에 띄어요."
    },
    {
      id: "bumps", group: "🫧 오돌토돌함·트러블",
      title: "통증 없는 작은 오돌토돌함이 있어요",
      description: "이마·턱 등에 작게 만져져요. 원인은 확실하지 않아요."
    },
    {
      id: "pimples", group: "🫧 오돌토돌함·트러블",
      title: "가벼운 붉은 뾰루지가 생겨요",
      description: "심한 통증·진물 없이 작은 뾰루지가 신경 쓰여요."
    },
    {
      id: "painful", group: "🫧 오돌토돌함·트러블",
      title: "크고 아프거나 곪는 트러블이 있어요",
      description: "이 경우에는 제품 추천보다 진료 안내가 나와요."
    },
    {
      id: "redness", group: "🌸 붉어짐·자극",
      title: "피부가 쉽게 붉어져요",
      description: "마찰이나 제품 사용 후 붉어지는 일이 있어요."
    },
    {
      id: "itch", group: "🌸 붉어짐·자극",
      title: "피부가 가렵거나 간질거려요",
      description: "가려움이 반복되거나 건조함과 함께 느껴져요."
    },
    {
      id: "sting", group: "🌸 붉어짐·자극",
      title: "지금 제품을 바르면 따가워요",
      description: "현재 따가움이 있다면 새 제품 추천을 잠시 멈춰요."
    },
    {
      id: "marks", group: "☀ 자국·낮 시간 관리",
      title: "트러블이 지난 자리에 자국이 남았어요",
      description: "붉거나 갈색으로 보이는 흔적이 신경 쓰여요."
    },
    {
      id: "sun", group: "☀ 자국·낮 시간 관리",
      title: "낮에 사용할 선크림을 고르고 싶어요",
      description: "외출할 때 사용할 자외선 차단제를 비교하고 싶어요."
    }
  ];

  const BY_ID = Object.fromEntries(CONCERNS.map(item => [item.id, item]));
  const goodsURL = id =>
    `https://www.oliveyoung.co.kr/store/goods/getGoodsDetail.do?goodsNo=${id}`;
  const searchURL = name =>
    `https://www.oliveyoung.co.kr/store/search/getSearchMain.do?query=${encodeURIComponent(name)}`;

  // 실제 판매 페이지·브랜드관에서 확인한 상품과 이미지 주소입니다.
  // 실시간 가격·재고를 조회하는 API는 사용하지 않습니다.
  const PRODUCTS = {
    aestura: {
      brand: "에스트라",
      name: "아토베리어365 크림 80ml",
      category: "보습 크림",
      url: goodsURL("A000000261864"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0026/A00000026186405ko.jpg?l=ko",
      usage: "세안 후 보습 단계에서 사용해요. 얼굴 전체가 부담스러우면 건조한 부위의 사용감을 먼저 살펴보세요."
    },
    drg: {
      brand: "닥터지",
      name: "레드 블레미쉬 클리어 수딩크림 EX 70ml",
      category: "수딩 크림",
      url: goodsURL("A000000255752"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/400/10/0000/0025/A00000025575226ko.jpg?l=ko",
      usage: "세안 후 보습 단계의 비교 후보예요. 여드름이나 피부염을 치료하는 약은 아니에요."
    },
    snature: {
      brand: "에스네이처",
      name: "아쿠아 스쿠알란 수분크림 60ml",
      category: "수분 크림",
      url: goodsURL("A000000156230"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0015/A000000156230102ko.png?l=ko",
      usage: "보습 단계에서 다른 크림과 사용감을 비교해 보세요. 크림 여러 개를 한꺼번에 바를 필요는 없어요."
    },
    lotion: {
      brand: "라운드랩",
      name: "1025 독도 로션 200ml",
      category: "보습 로션",
      url: goodsURL("A000000145576"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0014/A00000014557626ko.jpg?l=ko",
      usage: "로션 형태의 보습제를 찾을 때 비교해 보세요. 건조한 부위와 번들거리는 부위의 양을 조절하세요."
    },
    cleanser: {
      brand: "닥터지",
      name: "약산성 클렌징 젤 폼 200ml",
      category: "세안제",
      url: goodsURL("A000000148023"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/400/10/0000/0014/A00000014802335ko.jpg?l=ko",
      usage: "제품 표시사항에 따라 부드럽게 세안하고 충분히 헹궈요. 약산성이라는 표시가 무자극을 보장하지는 않아요."
    },
    balm: {
      brand: "닥터지",
      name: "그린딥 포어 클렌징밤 100ml",
      category: "클렌징밤",
      url: goodsURL("A000000207640"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/400/10/0000/0020/A00000020764041ko.jpg?l=ko",
      usage: "메이크업·선크림 세정이 필요할 때만 고려해요. 오래 문지르거나 피지를 짜내듯 마사지하지 마세요."
    },
    sunscreen: {
      brand: "라운드랩",
      name: "자작나무 수분 선크림 50ml",
      category: "자외선 차단제",
      url: goodsURL("A000000263510"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0026/A00000026351008ko.jpg?l=ko",
      usage: "외출 전 제품 표시사항에 따라 발라요. 연결되는 상품은 1+1 기획 구성이며 구성은 바뀔 수 있어요."
    },
    mineral: {
      brand: "닥터지",
      name: "그린 마일드 업 선 플러스 50ml",
      category: "무기자차 선크림",
      url: goodsURL("A000000180162"),
      image: "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/400/10/0000/0018/A00000018016262ko.jpg?l=ko",
      usage: "다른 차단 방식의 제품을 비교하고 싶을 때 살펴보세요. 무기자차도 모든 사람에게 자극이 없는 것은 아니에요."
    }
  };

  let lastCopyText = "";

  function renderConcernOptions() {
    let group = "";
    $("concern-options").innerHTML = CONCERNS.map(item => {
      const heading = item.group !== group
        ? `<p class="group-title">${escapeHTML(item.group)}</p>` : "";
      group = item.group;
      return `${heading}
        <label class="choice">
          <input type="checkbox" name="concern" value="${item.id}">
          <span>
            <strong>${escapeHTML(item.title)}</strong>
            <small>${escapeHTML(item.description)}</small>
          </span>
        </label>`;
    }).join("");
  }

  function getInput() {
    return {
      concerns: [...document.querySelectorAll('[name="concern"]:checked')]
        .map(item => item.value).filter(value => Object.hasOwn(BY_ID, value)),
      priority: $("priority").value,
      safety: $("safety").value,
      area: $("area").value,
      duration: $("duration").value,
      sensation: $("sensation").value,
      trend: $("trend").value,
      newProduct: $("new-product").value,
      makeup: $("makeup").value,
      outdoor: $("outdoor").value
    };
  }

  function updateSelection() {
    const input = getInput();
    const oldPriority = input.priority;
    $("priority").replaceChildren();

    input.concerns.forEach(id => {
      const option = document.createElement("option");
      option.value = id;
      option.textContent = BY_ID[id].title;
      $("priority").append(option);
    });

    if (input.concerns.includes(oldPriority)) {
      $("priority").value = oldPriority;
    }

    $("priority-field").hidden = input.concerns.length < 2;
    $("selection-summary").textContent = input.concerns.length
      ? `${input.concerns.length}개 선택 · ${input.concerns.map(id => BY_ID[id].title).join(" / ")}`
      : "선택한 피부 고민이 없어요.";
  }

  function safetyCheck(input) {
    const has = id => input.concerns.includes(id);

    if (input.safety === "emergency") return {
      emergency: true,
      title: "지금은 응급 도움을 먼저 받으세요",
      message: "숨쉬기 어렵거나 입술·혀·목이 갑자기 붓는다면 즉시 119에 연락하세요. 주변 어른에게 알리고, 앱을 보거나 제품을 고르느라 도움 요청을 늦추지 마세요."
    };

    if (input.safety === "medical" || has("painful") ||
        input.sensation === "strong" || input.trend === "spreading") return {
      title: "새 화장품보다 진료가 먼저예요",
      message: "심한 통증·진물·물집·붓기, 빠르게 번지는 발진, 크고 아프거나 곪는 트러블은 화장품만으로 판단하지 마세요. 보호자에게 알리고 의료진과 상담하세요. 갑자기 심해지면 신속히 진료받으세요."
    };

    if (input.safety === "unsure") return {
      title: "현재 상태를 먼저 확인해 주세요",
      message: "상태가 심한지 잘 모르겠다면 새 제품을 추가하기보다 보호자나 의료진에게 먼저 상담해 주세요. 이 화면에서는 제품을 추천하지 않아요."
    };

    if (input.area === "eyes" && input.concerns.length) return {
      title: "눈 주변 증상은 별도로 확인해 주세요",
      message: "눈·눈꺼풀 주변의 가려움, 붉어짐, 붓기나 따가움은 얼굴용 화장품 추천으로 해결하려 하지 마세요. 눈 안에 화장품이 들어가지 않게 하고, 증상이 있으면 의료진과 상담하세요. 눈 통증이나 시력 변화가 있다면 신속히 진료받으세요."
    };

    if (has("sting") ||
        (input.newProduct === "yes" &&
         ["redness", "itch"].some(has))) return {
      title: "새 제품을 더하기보다 사용을 멈추고 확인해요",
      message: "사용 후 따갑거나 붉고 가려운 제품은 중단하세요. 지금 다른 제품으로 덮어 바르거나 필링하지 마세요. 피부에 남아 있다면 제품 표시사항에 따라 부드럽게 씻어내고, 증상이 심하거나 지속되면 진료받으세요. 처방받은 약은 임의로 변경하지 말고 의료진에게 문의하세요."
    };

    const inflamed = ["redness", "itch", "pimples", "bumps"].some(has);
    const persistent = ["long", "repeat"].includes(input.duration);

    if (input.trend === "worse" || (inflamed && persistent)) return {
      title: "계속되거나 반복되는 상태는 상담이 우선이에요",
      message: "증상이 악화되거나 붉어짐·가려움·트러블이 오래 지속되고 반복된다면 원인 확인이 필요해요. 제품을 계속 바꾸기보다 보호자와 상의하고 의료진에게 상담하세요."
    };

    return null;
  }

  function getPlan(input) {
    const has = id => input.concerns.includes(id);
    const priority = input.concerns.includes(input.priority)
      ? input.priority : input.concerns[0];
    const oily = ["oil", "combination", "blackhead", "bumps", "pimples"].some(has);
    const dry = ["tight", "flake", "combination"].some(has);
    const sensitive = ["redness", "itch"].some(has);
    const items = [];

    const add = (id, reason) => {
      if (!items.some(item => item.id === id)) items.push({ id, reason });
    };

    const sunId = sensitive ? "mineral" : "sunscreen";
    const sunReason = has("marks")
      ? "남은 자국 관리에서는 자외선 차단을 함께 챙겨요. 이미 생긴 자국이나 흉터를 없애 준다는 뜻은 아니에요."
      : "낮 시간 자외선 차단용 비교 후보예요. SPF·PA·사용법과 내수성 여부를 상품에서 확인하세요.";

    if (["marks", "sun"].includes(priority)) add(sunId, sunReason);

    if (["tight", "flake"].includes(priority) && !has("combination")) {
      add("aestura", "당김이나 각질 들뜸이 있어 보습 크림을 비교할 때 살펴볼 후보예요.");
      add("snature", "같은 보습 단계에서 사용감과 보습감을 비교할 다른 크림이에요.");
    } else if (oily) {
      add("drg", "번들거림이나 무거운 사용감이 부담스러울 때 보습용으로 비교해 볼 후보예요. 트러블 치료용은 아니에요.");
      add("lotion", has("combination")
        ? "코와 볼의 상태가 달라 로션을 기본으로 부위별 사용량을 조절하고 싶을 때 살펴보세요."
        : "크림 외에 로션 형태의 보습제를 비교하고 싶을 때 살펴보세요.");
    } else {
      add("aestura", "기본 보습 크림의 비교 후보예요. 민감함이 있다면 전성분과 이전 사용 경험을 먼저 확인하세요.");
      add("snature", "보습용 제품의 다른 선택지예요. 어느 제품이 더 편안한지는 개인마다 달라요.");
    }

    if (has("combination") && has("flake")) {
      add("aestura", "얼굴 전체에 추가하기보다 건조하고 들뜨는 부위에 사용할 크림 후보예요.");
    }

    if ((has("blackhead") || has("oil") || input.makeup !== "none") && !sensitive) {
      if (input.makeup === "makeup" && has("blackhead")) {
        add("balm", "메이크업 세정이 필요할 때 비교할 후보예요. 검은 점을 모두 블랙헤드로 판단하거나 제거 효과를 보장하지 않아요.");
      } else {
        add("cleanser", "피지·오염·선크림을 부드럽게 세정할 세안제 비교 후보예요. 씻는 횟수를 늘리라는 뜻은 아니에요.");
      }
    }

    add(sunId, sunReason);

    const tips = [];
    if (dry) tips.push("세안 후 물기를 가볍게 닦고 보습제 한 가지를 사용해 보세요. 건조하다고 여러 제품을 한꺼번에 추가할 필요는 없어요.");
    if (has("flake")) tips.push("들뜨는 각질을 손으로 떼거나 스크럽으로 강하게 밀지 마세요. 각질 들뜸만으로 각질 제거제가 필요하다고 판단하지 않아요.");
    if (has("oil")) tips.push("번들거려도 보습을 무조건 생략하지 마세요. 과도한 세안이나 뽀드득한 세정을 목표로 하지 않는 것이 좋아요.");
    if (has("combination")) tips.push("이마·코와 볼을 똑같이 관리할 필요는 없어요. 번들거리는 부위와 건조한 부위의 보습제 사용량을 달리해 보세요.");
    if (has("blackhead")) tips.push("코의 작은 점은 정상적인 피지선 필라멘트 등일 수도 있어요. 손으로 짜거나 코팩·긴 마사지를 반복하지 마세요.");
    if (has("bumps") || has("pimples")) tips.push("오돌토돌함의 원인은 앱으로 구분할 수 없어요. 짜거나 긁지 말고, 아프거나 곪고 흉터가 남으면 진료받으세요. 보습제·세안제는 치료제가 아니에요.");
    if (sensitive) tips.push("향료 무첨가 표시와 전성분을 확인하고, 이미 알레르기가 있거나 이전에 반응한 제품은 피하세요. ‘시카’·‘천연’·‘무기자차’도 무자극을 보장하지 않아요.");
    if (has("marks")) tips.push("붉은 자국·갈색 자국·패인 흉터는 서로 달라요. 강한 미백 제품이나 필링을 임의로 겹쳐 쓰지 말고, 오래 남거나 걱정되면 상담하세요.");
    if (input.duration === "long" || input.duration === "repeat") tips.push("가벼운 건조함이라도 오래 지속되거나 반복되면 생활 관리만으로 넘기지 말고 상담해 보세요.");
    if (input.outdoor === "long") tips.push("야외활동이 길면 내수성 표시를 확인하고 모자·그늘도 활용하세요. 물·땀·수건 사용 뒤에는 제품 안내에 따라 다시 발라요.");

    const headline = has("combination")
      ? "부위마다 다르게, 보습은 가볍게"
      : ["tight", "flake"].includes(priority)
      ? "각질 제거보다 보습부터 살펴봐요"
      : ["blackhead", "bumps", "pimples", "oil"].includes(priority)
      ? "과한 세정보다, 부담 적은 기본 관리"
      : ["marks", "sun"].includes(priority)
      ? "낮 시간 자외선 차단부터 챙겨요"
      : "새 제품은 천천히, 기본 관리는 단순하게";

    return { items, tips, headline };
  }

  function productCard(entry) {
    const item = PRODUCTS[entry.id];
    const fullName = `${item.brand} ${item.name}`;
    const photo = productPhoto(item);
    return `
      <article class="product">
        <a class="photo" href="${escapeHTML(item.url)}" target="_blank"
          rel="noopener noreferrer" referrerpolicy="no-referrer"
          aria-label="${escapeHTML(fullName)} 상품 페이지 열기">
          <img src="${escapeHTML(photo.preview || item.image)}"
            data-full-photo="${escapeHTML(photo.full || '')}"
            alt="${escapeHTML(fullName)} 상품 사진"
            loading="eager" decoding="async" referrerpolicy="no-referrer">
          <div class="photo-fallback" hidden>
            <span aria-hidden="true">🧴</span>${escapeHTML(fullName)}<br>상품 사진 보기 ↗
          </div>
        </a>
        <div class="product-body">
          <div><span class="tag">${escapeHTML(item.category)}</span></div>
          <p class="brand">${escapeHTML(item.brand)}</p>
          <h4>${escapeHTML(item.name)}</h4>
          <p class="product-reason">${escapeHTML(entry.reason || '')}</p>
          <p class="usage">${escapeHTML(item.usage)}</p>
          <a class="product-link" href="${escapeHTML(item.url)}" target="_blank"
            rel="noopener noreferrer" referrerpolicy="no-referrer">올리브영에서 보기 ↗</a>
          <a class="search-link" href="${escapeHTML(searchURL(fullName))}" target="_blank"
            rel="noopener noreferrer" referrerpolicy="no-referrer">제품명으로 검색 ↗</a>
        </div>
      </article>`;
  }

  function invalidateResult() {
    $("result").hidden = true;
    $("result").replaceChildren();
    $("empty").hidden = false;
    $("form-error").textContent = "";
    lastCopyText = "";
  }

  function focusResult() {
    $("result").focus({ preventScroll: true });
    $("result").scrollIntoView({ behavior: "auto", block: "start" });
  }

  function renderSafety(alert, focus) {
    lastCopyText = "";
    $("empty").hidden = true;
    $("result").hidden = false;
    $("result").innerHTML = `
      <div class="danger" role="alert">
        <h2>${escapeHTML(alert.title)}</h2>
        <p>${escapeHTML(alert.message)}</p>
        ${alert.emergency
          ? '<a class="emergency-link" href="tel:119">119에 전화하기 ↗</a>' : ""}
        <p class="small">현재 상태에서는 제품 추천을 표시하지 않아요.</p>
      </div>`;
    if (focus) focusResult();
  }

  function showProducts(focus = false) {
    const input = getInput();
    const alert = safetyCheck(input);

    if (alert) {
      renderSafety(alert, focus);
      return;
    }

    if (!input.concerns.length) {
      $("form-error").textContent = "피부 고민을 한 가지 이상 선택해 주세요.";
      document.querySelector('[name="concern"]').focus();
      return;
    }

    if (!input.safety) {
      $("form-error").textContent = "선택한 고민 아래에서 현재 피부 상태를 선택해 주세요.";
      $("safety").focus();
      return;
    }

    $("form-error").textContent = "";
    const plan = getPlan(input);
    const areaLabel = $("area").selectedOptions[0].textContent;
    const durationLabel = $("duration").selectedOptions[0].textContent;

    $("empty").hidden = true;
    $("result").hidden = false;
    $("result").innerHTML = `
      <div class="panel-top">
        <small>02 / YOUR DAILY PICKS</small>
        <span class="tag">선택 고민별 제품 비교</span>
      </div>
      <h2 class="result-title">${escapeHTML(plan.headline)}</h2>
      <div class="chips">
        ${input.concerns.map(id => `<span class="chip">${escapeHTML(BY_ID[id].title)}</span>`).join("")}
        <span class="chip">${escapeHTML(areaLabel)}</span>
        <span class="chip">${escapeHTML(durationLabel)}</span>
      </div>

      <div class="advice">
        <h3>우선 이렇게 골라 보세요</h3>
        <p>아래 제품은 비교할 선택지예요. <strong>보습제는 우선 한 가지</strong>를 고르고,
        세안제·선크림은 현재 사용 중인 제품이 잘 맞으면 그대로 사용해도 괜찮아요.</p>
      </div>

      <div class="section-title">
        <h3>실제 제품으로 비교하기</h3>
        <span class="small muted">${plan.items.length}개 비교 후보</span>
      </div>
      <div class="product-grid">${plan.items.map(productCard).join("")}</div>
      <p class="small muted" style="margin-top:12px">
        사진을 누르면 올리브영 상품 페이지가 열려요.
        제품 구성·용량·가격은 판매 페이지에서 확인하세요.
      </p>

      <div class="section-title"><h3>아침·저녁은 간단하게</h3></div>
      <div class="routine">
        <div><b>☀ 아침</b><p>필요에 맞게 순하게 세안 → 보습제 한 가지 → 외출 전 자외선 차단</p></div>
        <div><b>☾ 저녁</b><p>메이크업·선크림·오염을 제품 표시사항에 따라 부드럽게 세정 → 보습제 한 가지</p></div>
      </div>

      <div class="section-title"><h3>선택한 고민은 이렇게 관리해요</h3></div>
      <ul class="tips">${plan.tips.map(tip => `<li>${escapeHTML(tip)}</li>`).join("")}</ul>

      <div class="note">
        자외선 차단제는 SPF 30 이상, UVA·UVB 차단 여부와 PA 표시를 확인하세요.
        야외에서는 보통 2시간마다, 물·땀·수건 사용 뒤에는 표시사항에 따라 다시 발라요.<br><br>
        새 제품은 한 번에 하나씩 도입하고, 제품 안내에 따라 좁은 부위에서 먼저 확인하세요.
        이미 알레르기가 있는 제품은 시험 삼아 사용하지 마세요.
        따갑거나 붉어지면 중단하고, 심하거나 지속되면 진료받으세요.
      </div>

      <div class="actions">
        <button class="secondary" id="copy-result" type="button">제품명·링크 복사</button>
        <button class="secondary" id="back-to-form" type="button">고민 다시 선택하기</button>
      </div>
      <p id="copy-status" class="small" role="status"></p>
      <div id="manual-copy" hidden>
        <label class="label" for="copy-text">아래 내용을 직접 복사하세요</label>
        <textarea id="copy-text" readonly></textarea>
      </div>`;

    loadProductPhotos($("result"));

    // 복사 문구에는 사용자가 고른 피부 증상·기간을 넣지 않습니다.
    lastCopyText = [
      "[스킨랩 · 비교할 제품]",
      ...plan.items.map(entry => {
        const product = PRODUCTS[entry.id];
        return `${product.brand} ${product.name}\n${product.url}`;
      }),
      "",
      "상품 링크는 올리브영으로 연결됩니다."
    ].join("\n\n");

    $("copy-result").addEventListener("click", copyResult);
    $("back-to-form").addEventListener("click", () => {
      document.querySelector('[name="concern"]').focus();
      $("skin-form").scrollIntoView({ behavior: "auto", block: "start" });
    });

    if (focus) focusResult();
  }

  async function copyResult() {
    if (!lastCopyText) return;
    const text = lastCopyText;
    const status = $("copy-status");
    const manual = $("manual-copy");
    const textarea = $("copy-text");

    try {
      if (!navigator.clipboard) throw new Error("Clipboard unavailable");
      await navigator.clipboard.writeText(text);
      if (status.isConnected) status.textContent = "제품명과 링크를 복사했어요.";
      if (manual.isConnected) manual.hidden = true;
    } catch {
      if (!textarea.isConnected) return;
      textarea.value = text;
      manual.hidden = false;
      textarea.focus();
      textarea.select();
      status.textContent = "자동 복사가 제한되어 직접 복사할 내용을 표시했어요.";
    }
  }

  $("skin-form").addEventListener("submit", event => {
    event.preventDefault();
    showProducts(true);
    removeUnwantedNotices();
  });

  $("skin-form").addEventListener("change", () => {
    updateSelection();
    invalidateResult();

    const input = getInput();
    const alert = safetyCheck(input);

    // 심한 상태나 사용 후 이상 반응은 제출 버튼을 누르기 전에도 안내합니다.
    if (alert) renderSafety(alert, false);
  });

  $("reset").addEventListener("click", () => {
    $("skin-form").reset();
    updateSelection();
    invalidateResult();
    document.querySelector('[name="concern"]')?.focus();
  });

  renderConcernOptions();
  updateSelection();

  // 실제 상품 사진의 내장 미리보기. 외부 사진 연결이 실패해도 유지합니다.
  const PHOTO_PREVIEWS = {
    astra: "UklGRpwBAABXRUJQVlA4IJABAACwCwCdASpAAEAAP1mgxFeyLKejrBqrMkArCWwAxRHRWp6TE/BW9h3hzSttUTuOEQ6xrqR21zHhlo0y/axRclyNjezyB/2Uv1ixUYklBYSV7PiCETr2DrGS8+vzq/BzMg6qce/1vAAA/orS0wwT8PtSe+Bi0ni3Wil6paktIvu2jGa+CdIzE1UWkmSb6K6lnkx+JQ8XRUN60MBoyUWxncA7/oSu3pznRrcGCikE3r6Ne5nW1UUH4g7g6HpqTU+Kn356T/X7PeAbg1AXdAxLpF9QVi7A+KFTmiOCY86JWYmpi9HNg63Qeom/EwWbA0CCaSVMgrLb+Kz5k85x3VzqW9zmOtjD+Y6aSAMdb/teN4bvIXUsGiDi3lG6FPQ8c/0mqElN+cabutEpsCUskrbunt8XMQKQsTThm8uGZ3q+hAuXxyRxWv4r0/wtfLBZ+4g1M7y3e9Ubp3uiyoGcElfEziNgUQ/4ugo65ihwd4OcR6vepjIYT1XiDmL/yXaWmVTS4NOOHzOK8EgHIf9Iey7udrAA",
    snature: "UklGRnICAABXRUJQVlA4IGYCAABQDgCdASpAAEAAP02MuFawqSUjsfxskhApiWwAt+vySqCIve4Uy9ase2HyrAl8+SIePQWXAn2ymXlp0o41A6DeJ8kSyyDTEyKgHmr9S8HMg9DvDAXiVxeE2z+VgunMgQkhPIp1oXkBn8GAnnEHuUxI9d77tppCyTNcEgAA/Mx7mqUUUKJw0pC6IipTOpvtU3CDy//sI+MidutU/dHBpBIn9ogSOMZppkscRjGyJo8W406kcd1GmQzhiNZ/ozYaOEaFzheqbKug6CcJ8Tq4eR8naTZdRdqdh/IxamhFm0WkCmXwVMwrwGOS8cK0tAWnPS6luWSEjJuAgt+nMu2eofwfbvxB8Wx/xqkEBDd5vF9F04TEe5O9FJa09DbsvBTccBHZvA9UCUBco6A0nM3VGToL7AOi3gk4ggKDj9mjA0ex7y0Ryk0bAgQCVUDZxtYQB0GNY+tbh9btUyjIER4pV7N+wCf1gE+t2s5CiwnW8YpYCZTQnxKoRBk4joK0PKTDBGGnGrCUuRuBg4BeVWJH/azCChBYLN8KLotBYBffH9zJeOh51TivFP273k/dOTNK3wnWqbecU1nIFN2B2EqJ1uySQtbPKdQZyDbyBsJum3cr0xauqTG0rt73HI/sKfIQ2BieMI0/YxRicItP1dpT1MMB48bPp49OrvtMwiwk0mEvqmwUIQ1Zs514m6IoRZUD2cbz8rJELTLlBPiRSSJf9Tip2M66dX9wsBqmDaY0TKDQpw7MEbE6TT7GVXsEGGEzu9CkOn5rwcJaiV2fvWB6eRwL36wu5p8NEMUG+0ROwWJmm0WRTUAAAA==",
    roundlab: "UklGRmACAABXRUJQVlA4IFQCAABwDwCdASpAAEAAP02IuFawqKUjs/mdUhApiWwAqSd6RRmsYkBpwA5iOZv3vlXOj+pIZI54zpZ8PmOV1KhNZ9Bzfj2yH81h3ZDBW1NOeTGeNIWoWWKwbY6xjQNZXT1f6skfKnUC8gtvk3NbSxb2epREgF7/YL3aBLLJgNSbHvt6+T5B+UAA/uhEOEPi71Ah6xMh77meo13IsnW1UpXRfpDAn2WJqQI4RHf6ZdWg6kKfB//Ci0yARquULDCRSB9QKa165UxvJ0aP47eHCavHD+P/WaQ2uh92sAI2Ixn+BU1lsrKBhY0nuMtrd9hF2MiPIVyXQumTdxa4arxLm1ErrcDLoE5u2rKqzehhNedscl5jyZqDvVguUNcPxym2O+tekulxjiPNiI9NmTOCi+mLZ5nMUY0qb+PaCttCFrNmGHRzCoThTjxhzHK5irdivuJttFkG+5zVMp8wZaJ+Goul7Xyt+Cim2mYRKxHTmV7cz8GjvdBfOmIV6YN0iNFy8sg1231KcKVsfumGO7mR4ibPLB2BwV3szj6VDHkVbXDGJbkOM2r8p8zoj8mMA2ZqXM6SfdKRLCoJDEj5dLFei39OE3uNXEyX1KuSMIlHvCkaKTwLD3FKwDlPX3bH40ELV3C+c/L8h6YSZ2zO94LOYLSk6NFR9CUg0O8s6Q0cIqfg6/hVyTXEFTdc9lX1vcM6K3JfkjLaTDfzp36A1/dPV9e3EtqCcB0wd0IMMa/isQgeahadJOF4CWJniYgCQSZTihdJlxqt4Gj2fmOBCT/LMgE0HdnOyxeAAA=="
  };

  function productPhoto(item) {
    const name = `${item.brand} ${item.name}`;
    const options = [
      [/(?:에스트라|AESTURA).*(?:아토베리어|ATOBARRIER).*(?:크림|CREAM)/i, "astra", "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0026/A00000026186405ko.jpg?l=ko"],
      [/(?:에스네이처|S.?NATURE).*(?:스쿠알란|SQUALANE).*(?:크림|CREAM)/i, "snature", "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0015/A000000156230102ko.png?l=ko"],
      [/라운드랩.*자작나무|ROUND.?LAB.*BIRCH/i, "roundlab", "https://image.oliveyoung.co.kr/cfimages/cf-goods/uploads/images/thumbnails/10/0000/0014/A00000014913573ko.png?l=ko"]
    ];
    const matched = options.find(([pattern]) => pattern.test(name));
    return matched
      ? { preview: `data:image/webp;base64,${PHOTO_PREVIEWS[matched[1]]}`, full: matched[2] }
      : { preview: item.image, full: "" };
  }

  function loadProductPhotos(root) {
    root.querySelectorAll(".photo img").forEach(image => {
      const fallback = image.nextElementSibling;
      const onError = () => {
        image.hidden = true;
        if (fallback) fallback.hidden = false;
      };
      image.addEventListener("error", onError, { once: true });
      if (image.complete && image.naturalWidth === 0) onError();
      if (image.dataset.fullPhoto) {
        const full = new Image();
        full.referrerPolicy = "no-referrer";
        full.onload = () => {
          if (!image.isConnected) return;
          image.src = full.src;
          image.hidden = false;
          if (fallback) fallback.hidden = true;
        };
        full.src = image.dataset.fullPhoto;
      }
    });
  }

  function removeUnwantedNotices() {
    document.querySelectorAll(".privacy").forEach(node => node.remove());
    const walker = document.createTreeWalker(document.body, NodeFilter.SHOW_TEXT);
    const nodes = [];
    while (walker.nextNode()) nodes.push(walker.currentNode);
    const unwanted = /저장|전송|개인정보|정보\s*수집|특정\s*제품.{0,40}효과|효과.{0,40}보장|적합.{0,25}보장|먼저\s*현재\s*(?:피부\s*)?상태.{0,20}확인/;
    nodes.forEach(node => {
      if (node.parentElement?.closest("script, style")) return;
      if (!unwanted.test(node.textContent)) return;
      const parts = node.textContent.split(/(?<=[.!?。])\s+|\n/);
      node.textContent = parts.filter(part => !unwanted.test(part)).join(" ");
    });
    document.querySelectorAll(".hero-tags span, .header-note, footer p").forEach(node => {
      if (!node.textContent.trim()) node.remove();
    });
  }

  function arrangeSkinSteps() {
    const form = $("skin-form");
    const safety = $("safety");
    const oldContainer = safety.closest(".safe-box, fieldset");
    const oldLabel = document.querySelector('label[for="safety"]');
    const section = document.createElement("fieldset");
    section.id = "current-state-step";
    section.className = "safe-box";
    const legend = document.createElement("legend");
    legend.textContent = "피부 고민을 고른 다음, 현재 상태 선택";
    const hint = document.createElement("p");
    hint.id = "state-step-help";
    hint.className = "step-help";
    const label = document.createElement("label");
    label.htmlFor = "safety";
    label.className = "label";
    label.textContent = "현재 피부 상태";
    safety.setAttribute("aria-describedby", hint.id);
    section.append(legend, hint, label, safety);
    if (oldLabel) oldLabel.remove();
    if (oldContainer && !oldContainer.querySelector("input, select, textarea, button")) oldContainer.remove();
    const submit = form.querySelector('[type="submit"]');
    let anchor = submit;
    while (anchor && anchor.parentElement !== form) anchor = anchor.parentElement;
    form.insertBefore(section, anchor || null);
    return { section, hint, safety, submit };
  }

  function showBrowseProducts() {
    const entries = Object.entries(PRODUCTS);
    const preferred = [
      entries.find(([, item]) => /(?:에스트라|AESTURA).*(?:아토베리어|ATOBARRIER).*(?:크림|CREAM)/i.test(`${item.brand} ${item.name}`)),
      entries.find(([, item]) => /(?:에스네이처|S.?NATURE).*(?:스쿠알란|SQUALANE).*(?:크림|CREAM)/i.test(`${item.brand} ${item.name}`)),
      entries.find(([, item]) => /라운드랩|ROUND.?LAB/i.test(item.brand) && /자작나무|BIRCH/i.test(item.name))
    ].filter(Boolean);
    const selected = preferred.length ? preferred : entries.slice(0, 3);
    $("empty").innerHTML = `
      <div class="panel-top"><small>PRODUCT COLLECTION</small><span class="tag">실제 제품</span></div>
      <h2>제품부터 둘러보세요</h2>
      <p class="small muted">피부 고민과 현재 상태를 선택하면 아래에 맞춰 제품을 보여드려요.</p>
      <div class="product-grid">${selected.map(([id, item]) => productCard({ id, reason: item.category })).join("")}</div>`;
    loadProductPhotos($("empty"));
  }

  function simplifyRequestedQuestions() {
    const form = $("skin-form");
    const safety = $("safety");
    const sunText = "낮에 사용할 선크림을 고르고 싶어요";

    // 선택지를 없애기 전에 체크 상태도 해제합니다.
    form.querySelectorAll("label.choice, .choice").forEach(choice => {
      if (!choice.textContent.replace(/\s+/g, "").includes(sunText.replace(/\s+/g, ""))) return;
      choice.querySelectorAll('input[type="checkbox"], input[type="radio"]').forEach(input => {
        input.checked = false;
        input.defaultChecked = false;
      });
      choice.hidden = true;
    });

    // 기존 입력값 참조는 유지하면서 6번 질문만 화면에서 제외합니다.
    const headings = [...form.querySelectorAll("legend, label.label, h3, h4, [data-question='6'], [data-step='6']")];
    headings.forEach(heading => {
      const text = heading.textContent.trim();
      const number = heading.querySelector(".step-dot, .step-number");
      const isSixth = /^(?:0?6(?:\s*번(?:\s*질문)?|[.)．:：·]|\s+)|⑥)/.test(text)
        || number?.textContent.trim() === "6"
        || heading.dataset.question === "6"
        || heading.dataset.step === "6";
      if (!isSixth) return;
      const group = heading.closest("fieldset, .form-field, .form-group, .input-group, .field");
      if (group && group !== form && !group.contains(safety)) {
        group.hidden = true;
        return;
      }
      heading.hidden = true;
      const controlId = heading.getAttribute("for");
      const control = controlId ? document.getElementById(controlId) : null;
      if (control && control !== safety) {
        control.hidden = true;
        (control.getAttribute("aria-describedby") || "").split(/\s+/).filter(Boolean).forEach(id => {
          const help = document.getElementById(id);
          if (help) help.hidden = true;
        });
      }
      let sibling = heading.nextElementSibling;
      while (sibling && sibling.matches("select, textarea, .small, .step-help")) {
        if (sibling === safety || sibling.contains(safety)) break;
        sibling.hidden = true;
        sibling = sibling.nextElementSibling;
      }
    });

    safety.querySelectorAll("option").forEach(option => {
      option.textContent = option.textContent.replace(/아래의\s*심한\s*증상은\s*없어요/g, "위의 심한 증상은 없어요");
    });
    updateSelection();
  }

  removeUnwantedNotices();
  simplifyRequestedQuestions();
  const skinSteps = arrangeSkinSteps();
  showBrowseProducts();

  function syncSkinSteps(showResult = true) {
    const input = getInput();
    const ready = input.concerns.length > 0;
    skinSteps.safety.disabled = !ready;
    skinSteps.hint.textContent = ready
      ? "선택한 고민을 확인했어요. 현재 피부 상태를 선택하면 제품이 바로 표시돼요."
      : "위에서 피부 고민을 한 가지 이상 선택해 주세요.";
    const placeholder = skinSteps.safety.querySelector('option[value=""]');
    if (placeholder) placeholder.textContent = ready
      ? "현재 피부 상태를 선택해 주세요"
      : "피부 고민을 먼저 선택해 주세요";
    if (skinSteps.submit) skinSteps.submit.textContent = "선택한 고민으로 제품 보기";
    if (!ready) {
      skinSteps.safety.value = "";
      invalidateResult();
    } else if (showResult && input.safety) {
      showProducts(false);
    }
    removeUnwantedNotices();
  }

  $("skin-form").addEventListener("change", () => syncSkinSteps(true));
  $("reset").addEventListener("click", () => syncSkinSteps(false));
  syncSkinSteps(false);
})();
</script>
</body>
</html>
