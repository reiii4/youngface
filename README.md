<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>동안약침 피부 자가진단 | 영은한의원</title>
<link href="https://fonts.googleapis.com/css2?family=Pretendard:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --pink-deep: #c45c7a;
    --pink-mid: #e07a95;
    --pink-light: #f4a7ba;
    --pink-pale: #fde8ef;
    --pink-ultra: #fff5f8;
    --rose: #b84d68;
    --cream: #fffafb;
    --deep: #3a1a24;
    --mid: #7a4558;
    --soft: #f5dde5;
    --gold: #c47a5a;
    --green: #5a8a6a;
    --green-light: #eaf3ed;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, sans-serif;
    background: var(--cream);
    color: var(--deep);
    min-height: 100vh;
    -webkit-font-smoothing: antialiased;
  }

  /* HERO */
  .hero {
    background: linear-gradient(160deg, #3a1a24 0%, #6b2d45 50%, #c45c7a 100%);
    padding: 56px 24px 44px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -80px; left: 50%;
    transform: translateX(-50%);
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(244,167,186,0.18) 0%, transparent 65%);
    pointer-events: none;
  }
  .hero::after {
    content: '✦';
    position: absolute;
    bottom: 20px; right: 30px;
    font-size: 40px;
    color: rgba(255,255,255,0.08);
  }
  .hero-badge {
    display: inline-block;
    border: 1px solid rgba(244,167,186,0.6);
    color: var(--pink-light);
    font-size: 10px;
    letter-spacing: 4px;
    padding: 5px 18px;
    margin-bottom: 18px;
    font-weight: 500;
    border-radius: 20px;
  }
  .hero h1 {
    font-size: 26px;
    font-weight: 700;
    color: #fff;
    line-height: 1.45;
    margin-bottom: 12px;
    letter-spacing: -0.5px;
  }
  .hero h1 span { color: var(--pink-light); }
  .hero p {
    color: rgba(255,255,255,0.68);
    font-size: 13.5px;
    line-height: 1.75;
    max-width: 340px;
    margin: 0 auto 28px;
  }
  .hero-stats {
    display: flex;
    justify-content: center;
    gap: 28px;
  }
  .stat { text-align: center; }
  .stat-num {
    font-size: 22px;
    color: var(--pink-light);
    font-weight: 700;
    letter-spacing: -0.5px;
  }
  .stat-label { font-size: 11px; color: rgba(255,255,255,0.5); margin-top: 2px; }

  /* TAB NAV */
  .tab-nav {
    display: flex;
    background: var(--soft);
    border-bottom: 2px solid rgba(196,92,122,0.15);
    position: sticky;
    top: 0;
    z-index: 100;
  }
  .tab-btn {
    flex: 1;
    padding: 14px 8px;
    font-size: 13px;
    font-family: 'Noto Sans KR', sans-serif;
    font-weight: 500;
    color: var(--mid);
    background: transparent;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    border-bottom: 3px solid transparent;
    margin-bottom: -2px;
  }
  .tab-btn.active {
    color: var(--pink-deep);
    border-bottom-color: var(--pink-deep);
    background: #fff;
    font-weight: 700;
  }

  /* PROGRESS */
  .progress-wrap {
    background: #fff;
    padding: 14px 24px;
    border-bottom: 1px solid rgba(196,92,122,0.1);
  }
  .progress-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 8px;
  }
  .progress-label { font-size: 12px; color: var(--mid); }
  .progress-count { font-size: 12px; color: var(--pink-deep); font-weight: 700; }
  .progress-bar {
    height: 4px;
    background: rgba(196,92,122,0.12);
    border-radius: 2px;
    overflow: hidden;
  }
  .progress-fill {
    height: 100%;
    background: linear-gradient(90deg, var(--rose), var(--pink-light));
    border-radius: 2px;
    transition: width 0.5s ease;
    width: 0%;
  }

  /* QUIZ */
  .quiz-container {
    max-width: 600px;
    margin: 0 auto;
    padding: 0 20px 80px;
  }

  .section-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--pink-deep);
    letter-spacing: 3px;
    text-align: center;
    padding: 28px 0 6px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-title::before, .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: rgba(196,92,122,0.2);
  }

  .question-card {
    background: #fff;
    border: 1px solid rgba(196,92,122,0.12);
    border-radius: 16px;
    padding: 22px 18px;
    margin-bottom: 14px;
    opacity: 0;
    transform: translateY(18px);
    animation: fadeUp 0.45s forwards;
    box-shadow: 0 2px 16px rgba(196,92,122,0.07);
  }
  @keyframes fadeUp { to { opacity:1; transform:translateY(0); } }

  .q-num { font-size: 11px; color: var(--pink-deep); font-weight: 700; letter-spacing: 1px; margin-bottom: 8px; }
  .q-text { font-size: 14.5px; font-weight: 500; color: var(--deep); line-height: 1.65; margin-bottom: 14px; }

  .options { display: flex; flex-direction: column; gap: 7px; }
  .option-btn {
    background: var(--pink-ultra);
    border: 1.5px solid rgba(196,92,122,0.15);
    border-radius: 10px;
    padding: 11px 15px;
    font-size: 13px;
    color: var(--mid);
    cursor: pointer;
    text-align: left;
    transition: all 0.2s;
    font-family: 'Noto Sans KR', sans-serif;
    line-height: 1.5;
  }
  .option-btn:hover { border-color: var(--pink-mid); color: var(--deep); background: var(--pink-pale); }
  .option-btn.selected {
    background: linear-gradient(135deg, var(--pink-pale), #fce0e8);
    border-color: var(--pink-mid);
    color: var(--deep);
    font-weight: 500;
  }
  .option-btn.selected::before { content: '✓ '; color: var(--pink-deep); font-weight: 700; }

  /* SUBMIT */
  .submit-wrap { text-align: center; padding: 8px 0 16px; display: none; }
  .submit-wrap.show { display: block; }
  .submit-btn {
    background: linear-gradient(135deg, var(--rose), var(--pink-deep));
    color: #fff;
    border: none;
    border-radius: 50px;
    padding: 16px 48px;
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
    letter-spacing: 0.5px;
    box-shadow: 0 8px 24px rgba(196,92,122,0.3);
    transition: all 0.3s;
  }
  .submit-btn:hover { transform: translateY(-2px); box-shadow: 0 12px 32px rgba(196,92,122,0.4); }

  /* RESULT */
  .result-section { display: none; padding: 0 20px 80px; max-width: 600px; margin: 0 auto; }
  .result-section.show { display: block; animation: fadeUp 0.6s forwards; }

  .result-hero {
    background: linear-gradient(160deg, var(--rose), var(--pink-deep), var(--pink-mid));
    border-radius: 20px;
    padding: 30px 22px;
    text-align: center;
    margin: 20px 0 18px;
    position: relative;
    overflow: hidden;
  }
  .result-hero::after {
    content: '✦';
    position: absolute;
    bottom: -10px; right: 20px;
    font-size: 60px;
    color: rgba(255,255,255,0.08);
  }
  .result-type-badge {
    display: inline-block;
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.4);
    color: #fff;
    font-size: 11px;
    letter-spacing: 2px;
    padding: 4px 14px;
    border-radius: 20px;
    margin-bottom: 14px;
  }
  .result-type-name {
    font-size: 22px;
    color: #fff;
    font-weight: 700;
    margin-bottom: 10px;
    letter-spacing: -0.5px;
  }
  .result-desc { font-size: 13px; color: rgba(255,255,255,0.82); line-height: 1.8; }

  .result-card {
    background: #fff;
    border: 1px solid rgba(196,92,122,0.12);
    border-radius: 16px;
    padding: 22px 18px;
    margin-bottom: 12px;
    box-shadow: 0 2px 14px rgba(196,92,122,0.06);
  }
  .result-card-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--pink-deep);
    letter-spacing: 2px;
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .result-card-title::after { content: ''; flex: 1; height: 1px; background: rgba(196,92,122,0.15); }

  .symptom-list { list-style: none; display: flex; flex-wrap: wrap; gap: 7px; }
  .symptom-list li {
    background: var(--pink-ultra);
    border: 1px solid rgba(196,92,122,0.18);
    border-radius: 20px;
    padding: 5px 13px;
    font-size: 12px;
    color: var(--mid);
  }

  .treatment-item {
    display: flex;
    gap: 13px;
    padding: 12px 0;
    border-bottom: 1px solid var(--soft);
  }
  .treatment-item:last-child { border-bottom: none; }
  .treat-icon {
    width: 36px; height: 36px;
    background: var(--pink-pale);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 17px;
    flex-shrink: 0;
  }
  .treat-name { font-size: 14px; font-weight: 600; color: var(--deep); margin-bottom: 3px; }
  .treat-desc { font-size: 12px; color: var(--mid); line-height: 1.6; }

  /* 약침 효과 섹션 */
  .benefit-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .benefit-item {
    background: var(--pink-ultra);
    border: 1px solid rgba(196,92,122,0.12);
    border-radius: 12px;
    padding: 14px 12px;
    text-align: center;
  }
  .benefit-icon { font-size: 22px; margin-bottom: 6px; }
  .benefit-title { font-size: 13px; font-weight: 600; color: var(--deep); margin-bottom: 4px; }
  .benefit-desc { font-size: 11px; color: var(--mid); line-height: 1.5; }

  /* 한약 카드 */
  .herb-card {
    background: linear-gradient(135deg, #fff5f8, #fdeef3);
    border: 1px solid rgba(196,92,122,0.15);
    border-radius: 14px;
    padding: 16px;
    margin-bottom: 10px;
    position: relative;
  }
  .herb-card:last-child { margin-bottom: 0; }
  .herb-name { font-size: 15px; font-weight: 700; color: var(--rose); margin-bottom: 4px; letter-spacing: -0.3px; }
  .herb-hanja { font-size: 11px; color: var(--mid); margin-bottom: 8px; letter-spacing: 1px; }
  .herb-desc { font-size: 12.5px; color: var(--deep); line-height: 1.7; }
  .herb-tags { display: flex; flex-wrap: wrap; gap: 5px; margin-top: 8px; }
  .herb-tag {
    background: rgba(196,92,122,0.1);
    color: var(--pink-deep);
    font-size: 11px;
    padding: 3px 10px;
    border-radius: 10px;
    font-weight: 500;
  }

  .score-bar-wrap { margin-bottom: 11px; }
  .score-bar-label { display: flex; justify-content: space-between; font-size: 12px; color: var(--mid); margin-bottom: 5px; }
  .score-bar { height: 6px; background: var(--soft); border-radius: 3px; overflow: hidden; }
  .score-bar-fill { height: 100%; border-radius: 3px; transition: width 1s ease; }

  /* CTA */
  .cta-card {
    background: linear-gradient(135deg, var(--pink-deep), var(--rose));
    border-radius: 20px;
    padding: 26px 22px;
    text-align: center;
    margin-bottom: 12px;
  }
  .cta-card h3 { font-size: 17px; font-weight: 700; color: #fff; margin-bottom: 8px; letter-spacing: -0.3px; }
  .cta-card p { font-size: 13px; color: rgba(255,255,255,0.85); line-height: 1.7; margin-bottom: 18px; }
  .cta-btn {
    display: inline-block;
    background: #fff;
    color: var(--pink-deep);
    border: none;
    border-radius: 50px;
    padding: 13px 34px;
    font-size: 14px;
    font-weight: 700;
    text-decoration: none;
    cursor: pointer;
    box-shadow: 0 6px 18px rgba(0,0,0,0.12);
    transition: all 0.3s;
    letter-spacing: 0.3px;
  }
  .cta-btn:hover { transform: translateY(-2px); box-shadow: 0 10px 26px rgba(0,0,0,0.18); }

  .retry-btn {
    display: block; width: 100%;
    background: transparent;
    border: 1.5px solid rgba(196,92,122,0.25);
    border-radius: 50px; padding: 13px;
    font-size: 13px; color: var(--mid);
    cursor: pointer;
    font-family: 'Noto Sans KR', sans-serif;
    transition: all 0.2s;
  }
  .retry-btn:hover { border-color: var(--pink-mid); color: var(--deep); }

  /* 설문 탭 */
  .survey-container { max-width: 600px; margin: 0 auto; padding: 16px 20px 80px; }
  .survey-header {
    background: linear-gradient(135deg, var(--rose), var(--pink-deep));
    border-radius: 16px;
    padding: 20px;
    text-align: center;
    margin-bottom: 20px;
    color: #fff;
  }
  .survey-header h2 { font-size: 17px; font-weight: 700; margin-bottom: 6px; letter-spacing: -0.3px; }
  .survey-header p { font-size: 12px; opacity: 0.85; }

  .survey-card {
    background: #fff;
    border: 1px solid rgba(196,92,122,0.12);
    border-radius: 14px;
    padding: 20px 18px;
    margin-bottom: 12px;
    box-shadow: 0 2px 12px rgba(196,92,122,0.06);
  }
  .survey-q { font-size: 14px; font-weight: 600; color: var(--deep); margin-bottom: 14px; }
  .survey-q span { color: var(--pink-deep); }

  /* 통증 슬라이더 */
  .pain-slider-wrap { padding: 8px 0; }
  .pain-slider {
    -webkit-appearance: none;
    width: 100%;
    height: 6px;
    border-radius: 3px;
    background: linear-gradient(90deg, var(--pink-light) 0%, var(--pink-deep) 100%);
    outline: none;
    margin-bottom: 8px;
  }
  .pain-slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    width: 22px; height: 22px;
    border-radius: 50%;
    background: var(--pink-deep);
    cursor: pointer;
    box-shadow: 0 2px 8px rgba(196,92,122,0.4);
  }
  .pain-labels { display: flex; justify-content: space-between; font-size: 11px; color: var(--mid); }
  .pain-value {
    text-align: center;
    font-size: 28px;
    font-family: 'Noto Serif KR', serif;
    font-weight: 700;
    color: var(--pink-deep);
    margin-bottom: 4px;
  }
  .pain-desc { text-align: center; font-size: 12px; color: var(--mid); }

  /* 체크박스 그룹 */
  .check-group { display: flex; flex-direction: column; gap: 7px; }
  .check-item {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--pink-ultra);
    border: 1.5px solid rgba(196,92,122,0.12);
    border-radius: 10px;
    padding: 10px 14px;
    cursor: pointer;
    transition: all 0.2s;
  }
  .check-item:hover { border-color: var(--pink-mid); }
  .check-item.checked {
    background: var(--pink-pale);
    border-color: var(--pink-mid);
  }
  .check-item input[type="checkbox"] { display: none; }
  .check-box {
    width: 18px; height: 18px;
    border: 2px solid rgba(196,92,122,0.3);
    border-radius: 5px;
    flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
    transition: all 0.2s;
    font-size: 11px;
  }
  .check-item.checked .check-box {
    background: var(--pink-deep);
    border-color: var(--pink-deep);
    color: #fff;
  }
  .check-label { font-size: 13px; color: var(--mid); line-height: 1.4; }
  .check-item.checked .check-label { color: var(--deep); font-weight: 500; }

  /* 라디오 */
  .radio-group { display: flex; gap: 8px; flex-wrap: wrap; }
  .radio-item {
    background: var(--pink-ultra);
    border: 1.5px solid rgba(196,92,122,0.15);
    border-radius: 20px;
    padding: 8px 16px;
    font-size: 13px;
    color: var(--mid);
    cursor: pointer;
    transition: all 0.2s;
  }
  .radio-item:hover { border-color: var(--pink-mid); }
  .radio-item.selected { background: var(--pink-pale); border-color: var(--pink-mid); color: var(--deep); font-weight: 600; }

  /* 지속시간 */
  .duration-group { display: grid; grid-template-columns: 1fr 1fr; gap: 7px; }

  /* 텍스트에어리어 */
  .survey-textarea {
    width: 100%;
    background: var(--pink-ultra);
    border: 1.5px solid rgba(196,92,122,0.15);
    border-radius: 12px;
    padding: 13px;
    font-size: 13px;
    font-family: 'Noto Sans KR', sans-serif;
    color: var(--deep);
    resize: vertical;
    min-height: 90px;
    outline: none;
    transition: border-color 0.2s;
  }
  .survey-textarea:focus { border-color: var(--pink-mid); }

  /* 회차 선택 */
  .session-group { display: flex; flex-wrap: wrap; gap: 7px; }
  .session-btn {
    background: var(--pink-ultra);
    border: 1.5px solid rgba(196,92,122,0.15);
    border-radius: 8px;
    padding: 8px 14px;
    font-size: 13px;
    color: var(--mid);
    cursor: pointer;
    transition: all 0.2s;
    font-family: 'Noto Sans KR', sans-serif;
  }
  .session-btn:hover { border-color: var(--pink-mid); }
  .session-btn.selected { background: var(--pink-pale); border-color: var(--pink-deep); color: var(--deep); font-weight: 600; }

  .survey-submit-btn {
    width: 100%;
    background: linear-gradient(135deg, var(--rose), var(--pink-deep));
    color: #fff;
    border: none;
    border-radius: 50px;
    padding: 16px;
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
    letter-spacing: 0.5px;
    box-shadow: 0 8px 24px rgba(196,92,122,0.3);
    transition: all 0.3s;
    margin-top: 8px;
  }
  .survey-submit-btn:hover { transform: translateY(-2px); }

  .survey-complete {
    display: none;
    text-align: center;
    padding: 50px 20px;
  }
  .survey-complete.show { display: block; animation: fadeUp 0.5s forwards; }
  .complete-icon { font-size: 56px; margin-bottom: 16px; }
  .complete-title { font-size: 21px; font-weight: 700; color: var(--rose); margin-bottom: 10px; letter-spacing: -0.5px; }
  .complete-desc { font-size: 14px; color: var(--mid); line-height: 1.8; }

  .clinic-info { text-align: center; padding: 16px; font-size: 11.5px; color: rgba(122,69,88,0.55); line-height: 1.9; }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-badge">YOUNGEUN KOREAN MEDICINE</div>
  <h1>나의 피부 나이는<br><span>몇 살일까요?</span></h1>
  <p>한방 체질 기반 12문항 진단으로<br>맞춤 동안약침 프로토콜을 확인하세요.</p>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num">12</div><div class="stat-label">진단 문항</div></div>
    <div class="stat"><div class="stat-num">4</div><div class="stat-label">피부 유형</div></div>
    <div class="stat"><div class="stat-num">3분</div><div class="stat-label">소요 시간</div></div>
  </div>
</div>

<!-- TAB NAV -->
<div class="tab-nav">
  <button class="tab-btn active" onclick="switchTab('diagnosis')">🌸 피부 자가진단</button>
  <button class="tab-btn" onclick="switchTab('survey')">📋 시술 후 설문</button>
</div>

<!-- =================== 진단 탭 =================== -->
<div id="diagnosisTab">
  <div class="progress-wrap">
    <div class="progress-top">
      <span class="progress-label" id="progressLabel">진단을 시작해주세요</span>
      <span class="progress-count" id="progressCount">0 / 12</span>
    </div>
    <div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>
  </div>

  <div class="quiz-container" id="quizContainer">

    <div class="section-title">피부 상태</div>

    <div class="question-card" style="animation-delay:0.05s">
      <div class="q-num">Q 01</div>
      <div class="q-text">세안 후 보습 없이 30분이 지나면 피부가 어떤가요?</div>
      <div class="options">
        <button class="option-btn" data-q="1" data-v="dry" onclick="sel(this)">당기고 건조해서 당장 뭔가 발라야 해요</button>
        <button class="option-btn" data-q="1" data-v="oily" onclick="sel(this)">금방 번들거리고 기름이 올라와요</button>
        <button class="option-btn" data-q="1" data-v="combo" onclick="sel(this)">T존은 번들, 볼은 건조한 편이에요</button>
        <button class="option-btn" data-q="1" data-v="sensitive" onclick="sel(this)">따갑거나 붉어지는 느낌이 있어요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.1s">
      <div class="q-num">Q 02</div>
      <div class="q-text">거울 앞에서 피부를 봤을 때 모공 상태는?</div>
      <div class="options">
        <button class="option-btn" data-q="2" data-v="dry" onclick="sel(this)">모공이 작고 잘 보이지 않아요</button>
        <button class="option-btn" data-q="2" data-v="oily" onclick="sel(this)">코·이마 모공이 크고 뚜렷해요</button>
        <button class="option-btn" data-q="2" data-v="combo" onclick="sel(this)">T존만 모공이 두드러져요</button>
        <button class="option-btn" data-q="2" data-v="sensitive" onclick="sel(this)">모공보다 붉음증이 더 신경 쓰여요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.15s">
      <div class="q-num">Q 03</div>
      <div class="q-text">피부 톤 고민이 있다면 어느 쪽에 가깝나요?</div>
      <div class="options">
        <button class="option-btn" data-q="3" data-v="dry" onclick="sel(this)">칙칙하고 전반적으로 어두운 편이에요</button>
        <button class="option-btn" data-q="3" data-v="oily" onclick="sel(this)">번들거려서 화장이 잘 안 받아요</button>
        <button class="option-btn" data-q="3" data-v="combo" onclick="sel(this)">부위별로 톤 차이가 나요</button>
        <button class="option-btn" data-q="3" data-v="sensitive" onclick="sel(this)">쉽게 붉어지거나 홍조가 있어요</button>
      </div>
    </div>

    <div class="section-title">노화 고민</div>

    <div class="question-card" style="animation-delay:0.2s">
      <div class="q-num">Q 04</div>
      <div class="q-text">주름이 가장 신경 쓰이는 부위는?</div>
      <div class="options">
        <button class="option-btn" data-q="4" data-v="dry" onclick="sel(this)">눈 밑 잔주름, 입가 주름이 깊어지고 있어요</button>
        <button class="option-btn" data-q="4" data-v="oily" onclick="sel(this)">이마나 미간 주름이 더 걱정돼요</button>
        <button class="option-btn" data-q="4" data-v="combo" onclick="sel(this)">팔자주름·마리오네트 라인이 생겼어요</button>
        <button class="option-btn" data-q="4" data-v="sensitive" onclick="sel(this)">주름보다 피부 얇아짐이 더 걱정이에요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.25s">
      <div class="q-num">Q 05</div>
      <div class="q-text">피부 탄력·처짐에 대해 어떻게 느끼시나요?</div>
      <div class="options">
        <button class="option-btn" data-q="5" data-v="dry" onclick="sel(this)">전체적으로 탄력이 많이 떨어진 느낌이에요</button>
        <button class="option-btn" data-q="5" data-v="oily" onclick="sel(this)">피부가 무거워지고 아랫부분이 처지는 것 같아요</button>
        <button class="option-btn" data-q="5" data-v="combo" onclick="sel(this)">얼굴 윤곽이 예전보다 흐려졌어요</button>
        <button class="option-btn" data-q="5" data-v="sensitive" onclick="sel(this)">탄력보다는 피부결이 거칠어진 게 더 눈에 띄어요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.3s">
      <div class="q-num">Q 06</div>
      <div class="q-text">색소·잡티 고민은?</div>
      <div class="options">
        <button class="option-btn" data-q="6" data-v="dry" onclick="sel(this)">기미, 칙칙한 잡티가 많아졌어요</button>
        <button class="option-btn" data-q="6" data-v="oily" onclick="sel(this)">여드름 자국·흉터가 남아 있어요</button>
        <button class="option-btn" data-q="6" data-v="combo" onclick="sel(this)">크게 심하진 않지만 전반적으로 고르지 않아요</button>
        <button class="option-btn" data-q="6" data-v="sensitive" onclick="sel(this)">붉은 혈관이나 모세혈관 확장이 보여요</button>
      </div>
    </div>

    <div class="section-title">생활 & 체질</div>

    <div class="question-card" style="animation-delay:0.35s">
      <div class="q-num">Q 07</div>
      <div class="q-text">평소 수면 패턴은 어떤가요?</div>
      <div class="options">
        <button class="option-btn" data-q="7" data-v="dry" onclick="sel(this)">수면 부족이 잦고 자도 개운하지 않아요</button>
        <button class="option-btn" data-q="7" data-v="oily" onclick="sel(this)">잠은 잘 자는 편이지만 늦게 자요</button>
        <button class="option-btn" data-q="7" data-v="combo" onclick="sel(this)">불규칙한 편이에요 (교대근무·야근 등)</button>
        <button class="option-btn" data-q="7" data-v="sensitive" onclick="sel(this)">스트레스로 잠들기 어려운 편이에요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.4s">
      <div class="q-num">Q 08</div>
      <div class="q-text">소화·장 건강은 어떤가요?</div>
      <div class="options">
        <button class="option-btn" data-q="8" data-v="dry" onclick="sel(this)">소화가 약한 편이고 속이 자주 더부룩해요</button>
        <button class="option-btn" data-q="8" data-v="oily" onclick="sel(this)">음식을 잘 먹는 편, 과식하는 경향이 있어요</button>
        <button class="option-btn" data-q="8" data-v="combo" onclick="sel(this)">들쑥날쑥해요 (변비와 설사 반복)</button>
        <button class="option-btn" data-q="8" data-v="sensitive" onclick="sel(this)">긴장하면 배가 아프거나 소화가 안 돼요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.45s">
      <div class="q-num">Q 09</div>
      <div class="q-text">몸의 열감·순환은?</div>
      <div class="options">
        <button class="option-btn" data-q="9" data-v="dry" onclick="sel(this)">손발이 차고 몸이 자주 추워요</button>
        <button class="option-btn" data-q="9" data-v="oily" onclick="sel(this)">상체에 열이 많고 얼굴이 달아오를 때가 있어요</button>
        <button class="option-btn" data-q="9" data-v="combo" onclick="sel(this)">위는 뜨겁고 발은 차가운 편이에요</button>
        <button class="option-btn" data-q="9" data-v="sensitive" onclick="sel(this)">갑자기 화끈거리거나 식은땀이 나요</button>
      </div>
    </div>

    <div class="section-title">피부 반응</div>

    <div class="question-card" style="animation-delay:0.5s">
      <div class="q-num">Q 10</div>
      <div class="q-text">화장품이나 시술에 대한 피부 반응은?</div>
      <div class="options">
        <button class="option-btn" data-q="10" data-v="dry" onclick="sel(this)">자극적인 성분에 쉽게 건조해지고 당겨요</button>
        <button class="option-btn" data-q="10" data-v="oily" onclick="sel(this)">여드름이 잘 나거나 트러블이 잦아요</button>
        <button class="option-btn" data-q="10" data-v="combo" onclick="sel(this)">부위마다 반응이 달라요</button>
        <button class="option-btn" data-q="10" data-v="sensitive" onclick="sel(this)">쉽게 붉어지고 따가움·간지러움이 있어요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.55s">
      <div class="q-num">Q 11</div>
      <div class="q-text">계절이나 환경 변화에 피부가 어떻게 반응하나요?</div>
      <div class="options">
        <button class="option-btn" data-q="11" data-v="dry" onclick="sel(this)">겨울·건조한 날씨에 유독 피부가 나빠져요</button>
        <button class="option-btn" data-q="11" data-v="oily" onclick="sel(this)">여름·습한 날씨에 더 번들거리고 트러블이 생겨요</button>
        <button class="option-btn" data-q="11" data-v="combo" onclick="sel(this)">환절기에 피부가 유독 예민해져요</button>
        <button class="option-btn" data-q="11" data-v="sensitive" onclick="sel(this)">미세먼지나 자외선에 쉽게 반응해요</button>
      </div>
    </div>

    <div class="question-card" style="animation-delay:0.6s">
      <div class="q-num">Q 12</div>
      <div class="q-text">가장 원하는 피부 변화를 하나만 고른다면?</div>
      <div class="options">
        <button class="option-btn" data-q="12" data-v="dry" onclick="sel(this)">촉촉하고 생기 있는 피부로 되돌리고 싶어요</button>
        <button class="option-btn" data-q="12" data-v="oily" onclick="sel(this)">피지 조절되고 매끄러운 피부결을 원해요</button>
        <button class="option-btn" data-q="12" data-v="combo" onclick="sel(this)">탄력·리프팅으로 윤곽을 살리고 싶어요</button>
        <button class="option-btn" data-q="12" data-v="sensitive" onclick="sel(this)">피부 장벽을 회복해 예민함을 줄이고 싶어요</button>
      </div>
    </div>

    <div class="submit-wrap" id="submitWrap">
      <button class="submit-btn" onclick="showResult()">✦ 나의 피부 유형 확인하기</button>
    </div>
  </div>

  <!-- RESULT -->
  <div class="result-section" id="resultSection">
    <div id="resultContent"></div>
    <div style="padding:0 0 14px"><button class="retry-btn" onclick="retryQuiz()">↺ 다시 진단하기</button></div>
    <div class="clinic-info">영은한의원 · 서울시 서초구 동산로2길 25 2층<br>☎ 02-573-8455 · 원장 이영은</div>
  </div>
</div>

<!-- =================== 설문 탭 =================== -->
<div id="surveyTab" style="display:none">
  <div class="survey-container">

    <div class="survey-header">
      <h2>동안약침 시술 후 설문조사</h2>
      <p>시술 결과 개선을 위해 솔직하게 답해주세요 💕</p>
    </div>

    <!-- 기본 정보 -->
    <div class="survey-card">
      <div class="survey-q"><span>시술 횟차</span>를 선택해주세요</div>
      <div class="session-group" id="sessionGroup">
        <button class="session-btn" onclick="selectSession(this)">1회차</button>
        <button class="session-btn" onclick="selectSession(this)">2회차</button>
        <button class="session-btn" onclick="selectSession(this)">3회차</button>
        <button class="session-btn" onclick="selectSession(this)">4회차</button>
        <button class="session-btn" onclick="selectSession(this)">5회차</button>
        <button class="session-btn" onclick="selectSession(this)">6회차</button>
        <button class="session-btn" onclick="selectSession(this)">7회차</button>
        <button class="session-btn" onclick="selectSession(this)">8회차+</button>
      </div>
    </div>

    <!-- Q1 통증 -->
    <div class="survey-card">
      <div class="survey-q"><span>Q1.</span> 시술 시 통증은 어느 정도였나요?</div>
      <div class="pain-slider-wrap">
        <div class="pain-value" id="painValue">0</div>
        <div class="pain-desc" id="painDesc">전혀 아프지 않았어요</div>
        <input type="range" class="pain-slider" min="0" max="10" value="0" oninput="updatePain(this.value)">
        <div class="pain-labels"><span>0 전혀 없음</span><span>5 보통</span><span>10 매우 심함</span></div>
      </div>
    </div>

    <!-- Q2 발적 -->
    <div class="survey-card">
      <div class="survey-q"><span>Q2.</span> 시술 후 발적(붉어짐)이 있었나요?</div>
      <div class="radio-group" id="rednessGroup">
        <div class="radio-item" onclick="selectRadio('rednessGroup', this)">있었어요</div>
        <div class="radio-item" onclick="selectRadio('rednessGroup', this)">없었어요</div>
      </div>
      <div id="durationWrap" style="display:none; margin-top:14px;">
        <div style="font-size:13px; color:var(--mid); margin-bottom:8px;">얼마나 지속되었나요?</div>
        <div class="duration-group" id="durationGroup">
          <div class="radio-item" onclick="selectRadio('durationGroup', this)">30분 이내</div>
          <div class="radio-item" onclick="selectRadio('durationGroup', this)">30분~2시간</div>
          <div class="radio-item" onclick="selectRadio('durationGroup', this)">2시간~6시간</div>
          <div class="radio-item" onclick="selectRadio('durationGroup', this)">6시간 이상</div>
        </div>
      </div>
    </div>

    <!-- Q3 피부 변화 -->
    <div class="survey-card">
      <div class="survey-q"><span>Q3.</span> 다음 날 아침, 피부 변화가 있었나요? <small style="color:var(--mid); font-weight:400;">(복수 선택 가능)</small></div>
      <div class="check-group">
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">💧 피부 당김이 줄었어요 (반나절 이상 안 땡김)</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">✨ 피부가 쫀쫀해지는 느낌</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🎈 얼굴이 팽팽한 느낌</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🍑 피부가 탱글탱글해짐</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🪞 피부가 매끈해짐</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">✦ 피부가 반짝반짝해짐 (광채)</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🌸 얼굴이 전반적으로 깨끗해짐</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">💄 화장이 잘 받아요</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">〰️ 팔자주름·잔주름이 줄었어요</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">⬆️ 리프팅된 느낌</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">📐 얼굴이 작아진 느낌 (라인 개선)</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">— 아직 변화가 없어요</span>
        </label>
      </div>
    </div>

    <!-- Q4 잔여 증상 -->
    <div class="survey-card">
      <div class="survey-q"><span>Q4.</span> 다음 날 아침 남아있는 증상이 있으신가요? <small style="color:var(--mid); font-weight:400;">(복수 선택)</small></div>
      <div class="check-group">
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">✅ 없어요 (이상 없음)</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🔴 얼굴이 아직 발적이 있어요</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">😖 시술 부위가 아파요</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">💧 얼굴이 조금 부은 느낌</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🤔 가렵거나 간지러워요</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">⚠️ 염증 소견이 보여요</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">😬 턱 부위 뻐근함 / 저작 시 불편함</span>
        </label>
        <label class="check-item" onclick="toggleCheck(this)">
          <div class="check-box">✓</div>
          <span class="check-label">🤕 측두부 당김 / 두통</span>
        </label>
      </div>
    </div>

    <!-- Q5 자유 의견 -->
    <div class="survey-card">
      <div class="survey-q"><span>Q5.</span> 시술과 관련해 하고 싶은 말씀이 있으시면 적어주세요 😊</div>
      <textarea class="survey-textarea" placeholder="불편했던 점, 좋았던 점, 궁금한 점 등 자유롭게 적어주세요!"></textarea>
    </div>

    <button class="survey-submit-btn" onclick="submitSurvey()">✦ 설문 제출하기</button>

    <div class="survey-complete" id="surveyComplete">
      <div class="complete-icon">🌸</div>
      <div class="complete-title">소중한 답변 감사해요!</div>
      <div class="complete-desc">원장님이 꼼꼼히 확인하여<br>더 나은 시술에 반영하겠습니다.<br><br>다음 방문도 기대해주세요 💕</div>
      <br>
      <a class="cta-btn" href="https://m.booking.naver.com/booking/13/bizes/650417?theme=place&service-target=map-pc&lang=ko&area=plt&map-search=1" target="_blank" style="display:inline-block; background:linear-gradient(135deg, var(--rose), var(--pink-deep)); color:#fff; padding:14px 32px; border-radius:50px; text-decoration:none; font-family:'Noto Serif KR',serif; font-weight:700; font-size:14px; margin-top:8px;">📅 다음 예약 바로가기</a>
    </div>

    <div class="clinic-info">영은한의원 · 서울시 서초구 동산로2길 25 2층<br>☎ 02-573-8455 · 원장 이영은</div>
  </div>
</div>

<script>
// ======= 탭 =======
function switchTab(tab) {
  document.querySelectorAll('.tab-btn').forEach((b,i) => b.classList.toggle('active', (i===0&&tab==='diagnosis')||(i===1&&tab==='survey')));
  document.getElementById('diagnosisTab').style.display = tab==='diagnosis' ? 'block' : 'none';
  document.getElementById('surveyTab').style.display = tab==='survey' ? 'block' : 'none';
}

// ======= 진단 =======
const answers = {};
const TOTAL = 12;

const types = {
  dry: {
    name: '음허형 건성 피부', badge: '음허 · 건조', emoji: '💧',
    desc: '몸의 진액(음)이 부족해 피부 수분 공급이 원활하지 않은 상태입니다. 피부 보습과 진액 보충이 핵심 방향입니다.',
    symptoms: ['건조함·당김', '잔주름·탄력저하', '칙칙한 피부톤', '기미·색소침착', '손발 냉감', '만성 피로'],
    score: { moisture: 28, elasticity: 52, tone: 48, sensitivity: 58 },
    treatments: [
      { icon: '🌡️', name: '수승화강약침 (MOK+V)', desc: '수기는 올리고 화기는 내려 몸의 균형을 잡아줍니다. 갱년기 홍조·열감 개선에 탁월한 핵심 약침' },
      { icon: '✨', name: '동안약침', desc: '동안 만들기·리프팅·턱살 정리. 얼굴 전체 윤곽을 가꿔주는 프리미엄 약침' },
      { icon: '🌟', name: '태반약침', desc: '신데렐라 안면 밝게·갱년기 극복. 피부 재생과 밝기 개선을 동시에' },
    ],
    herbs: [
      { name: '경옥고', hanja: '瓊玉膏', desc: '최고급 보양 처방. 기력 보충, 피부 윤기, 노화 방지에 탁월하며 건성·음허 체질에 가장 잘 맞습니다.', tags: ['보양', '노화방지', '피부윤기', '기력충전'] },
      { name: '공진단', hanja: '拱辰丹', desc: '뇌와 몸 전체의 기혈을 강화하는 황제의 보약. 피부 활력과 전신 컨디션 개선에 효과적입니다.', tags: ['기혈강화', '활력', '피부광채', '피로회복'] },
      { name: '체질탕약', hanja: '體質湯藥', desc: '사상체질(태양·태음·소양·소음)에 맞춘 1:1 맞춤 처방. 내 몸에 꼭 맞는 근본 치료를 제공합니다.', tags: ['체질맞춤', '1:1처방', '근본치료'] },
      { name: '다이어트탕약', hanja: '減重湯藥', desc: '체질과 비만 유형을 분석해 처방하는 한방 다이어트. 요요 없이 건강하게 체중을 조절합니다.', tags: ['체중조절', '체질분석', '요요방지'] }
    ],
    benefits: [
      { icon: '💧', title: '수분 충전', desc: '진액 보충으로 속부터 촉촉하게' },
      { icon: '🌡️', title: '홍조 개선', desc: '갱년기 열감·홍조 근본 조절' },
      { icon: '🌸', title: '기미 완화', desc: '색소 침착 개선, 균일한 피부톤' },
      { icon: '⏰', title: '노화 방지', desc: '잔주름 감소, 피부 탄력 회복' }
    ]
  },
  oily: {
    name: '습열형 지성 피부', badge: '습열 · 과잉', emoji: '🔥',
    desc: '체내 습(濕)과 열(熱)이 과잉되어 피지 분비가 많고 트러블이 잦은 상태입니다. 노폐물 배출과 열 조절이 핵심입니다.',
    symptoms: ['과잉 피지', '여드름·트러블', '넓은 모공', '여드름 흉터', '얼굴 달아오름', '상열감'],
    score: { moisture: 68, elasticity: 58, tone: 38, sensitivity: 48 },
    treatments: [
      { icon: '✨', name: '동안약침', desc: '동안 만들기·리프팅·턱살 정리. 지성 피부의 모공과 윤곽을 함께 개선하는 프리미엄 약침' },
      { icon: '🌡️', name: '수승화강약침 (MOK+V)', desc: '체내 열기를 아래로 내려 피지 과잉과 얼굴 열감을 근본적으로 조절' },
      { icon: '🌟', name: '태반약침', desc: '신데렐라 안면 밝게. 여드름 흉터·칙칙한 피부톤을 밝혀주는 재생 약침' },
    ],
    herbs: [
      { name: '체질탕약', hanja: '體質湯藥', desc: '소양인 등 열이 많은 체질에 맞춘 1:1 처방으로 피지 과잉과 트러블을 근본적으로 잡아줍니다.', tags: ['체질맞춤', '피지조절', '트러블', '1:1처방'] },
      { name: '다이어트탕약', hanja: '減重湯藥', desc: '습열형 비만을 함께 관리합니다. 체중 조절과 피부 개선을 동시에 달성하는 맞춤 처방입니다.', tags: ['체중조절', '습열제거', '피부개선'] },
      { name: '공진단', hanja: '拱辰丹', desc: '기혈 순환을 강화해 피부 재생력을 높입니다. 여드름 자국과 피부 활력 회복에 효과적입니다.', tags: ['기혈강화', '재생력', '피부활력'] },
      { name: '경옥고', hanja: '瓊玉膏', desc: '보양과 피부 윤기를 동시에. 트러블 이후 피부 회복과 전신 컨디션 향상에 도움을 줍니다.', tags: ['피부회복', '보양', '컨디션'] }
    ],
    benefits: [
      { icon: '🫧', title: '피지 조절', desc: '과잉 피지 균형 조절' },
      { icon: '🌿', title: '염증 진정', desc: '여드름, 트러블 근본 개선' },
      { icon: '📐', title: '모공 축소', desc: '노폐물 제거로 모공 정화' },
      { icon: '🎨', title: '흉터 개선', desc: '여드름 자국·색소 침착 완화' }
    ]
  },
  combo: {
    name: '기체형 복합 피부', badge: '기체 · 순환', emoji: '🌀',
    desc: '기(氣)의 흐름이 원활하지 않아 혈액순환과 림프 순환이 저하된 상태입니다. 부위별로 다른 피부 상태와 윤곽 변화가 특징입니다.',
    symptoms: ['부위별 복합 피부', '얼굴 처짐·윤곽 변화', '팔자주름', '칙칙한 안색', '얼굴 부종', '불규칙한 피부상태'],
    score: { moisture: 53, elasticity: 38, tone: 53, sensitivity: 43 },
    treatments: [
      { icon: '✨', name: '동안약침', desc: '동안 만들기·리프팅·턱살 정리. 기체형 피부의 처짐과 윤곽을 집중 개선하는 핵심 약침' },
      { icon: '🔮', name: 'HN약침 (인당)', desc: '인당 함몰 개선·인당울 해소·운명 바꾸기. 얼굴 중심 에너지를 바로잡아 전체 인상을 밝게' },
      { icon: '🌡️', name: '수승화강약침 (MOK+V)', desc: '순환을 개선하고 기의 흐름을 회복. 얼굴 부종과 처짐을 근본적으로 개선' },
    ],
    herbs: [
      { name: '공진단', hanja: '拱辰丹', desc: '기혈 순환을 강력하게 활성화합니다. 얼굴 처짐, 부종, 칙칙한 안색을 개선하고 리프팅 효과를 극대화합니다.', tags: ['기혈순환', '리프팅', '안색', '부종'] },
      { name: '체질탕약', hanja: '體質湯藥', desc: '체질별 순환 개선 맞춤 처방. 기체 체질의 막힌 흐름을 풀어 피부와 전신을 함께 개선합니다.', tags: ['기체해소', '체질맞춤', '순환개선'] },
      { name: '다이어트탕약', hanja: '減重湯藥', desc: '기체로 인한 부종성 비만을 함께 관리합니다. 얼굴 라인 개선과 체중 조절을 동시에 달성합니다.', tags: ['부종개선', '체중조절', '얼굴라인'] },
      { name: '경옥고', hanja: '瓊玉膏', desc: '전신 기력을 보강하고 피부에 윤기를 더합니다. 리프팅 시술 후 피부 회복력을 높이는 데 탁월합니다.', tags: ['기력보강', '윤기', '회복력'] }
    ],
    benefits: [
      { icon: '⬆️', title: '리프팅', desc: '처진 얼굴 라인 개선' },
      { icon: '🔄', title: '순환 개선', desc: '혈행·림프 순환 활성화' },
      { icon: '📏', title: '윤곽 개선', desc: '팔자주름·턱살 정리' },
      { icon: '💫', title: '안색 개선', desc: '칙칙함 해소, 생기 회복' }
    ]
  },
  sensitive: {
    name: '위기허약형 민감 피부', badge: '위기허 · 민감', emoji: '🛡️',
    desc: '피부 방어막(위기)이 약해져 외부 자극에 쉽게 반응하는 상태입니다. 피부 장벽 강화와 면역 조절이 우선 과제입니다.',
    symptoms: ['쉬운 홍조·붉어짐', '자극 반응 민감', '피부 얇아짐', '모세혈관 확장', '스트레스성 트러블', '계절 변화에 취약'],
    score: { moisture: 43, elasticity: 48, tone: 33, sensitivity: 22 },
    treatments: [
      { icon: '🌟', name: '태반약침', desc: '신데렐라 안면 밝게·갱년기 극복. 민감한 피부의 재생력을 높이고 안면을 전체적으로 밝혀줍니다' },
      { icon: '🌡️', name: '수승화강약침 (MOK+V)', desc: '갱년기 홍조 개선. 몸의 열 균형을 잡아 민감한 피부의 붉음증과 열감을 진정' },
      { icon: '🔮', name: 'HN약침 (인당)', desc: '인당 함몰 개선·인당울 해소. 피부 에너지를 바로잡아 민감도를 낮추고 피부 면역력 강화' },
    ],
    herbs: [
      { name: '경옥고', hanja: '瓊玉膏', desc: '최고급 보양 처방으로 피부 방어막을 복원합니다. 민감성 피부의 근본 체력을 끌어올립니다.', tags: ['피부장벽', '보양', '면역강화', '민감도'] },
      { name: '체질탕약', hanja: '體質湯藥', desc: '소음인 등 민감 체질에 맞춘 1:1 처방. 피부 면역을 높이고 외부 자극에 강한 피부를 만들어줍니다.', tags: ['체질맞춤', '면역', '피부강화'] },
      { name: '공진단', hanja: '拱辰丹', desc: '기혈을 강화해 피부 재생력과 면역력을 동시에 높입니다. 홍조와 민감도 개선에 효과적입니다.', tags: ['기혈강화', '재생력', '홍조개선'] },
      { name: '다이어트탕약', hanja: '減重湯藥', desc: '체질에 맞게 처방해 무리 없이 건강하게 체중을 조절합니다. 피부 트러블 없이 다이어트할 수 있습니다.', tags: ['건강다이어트', '체질맞춤', '트러블없이'] }
    ],
    benefits: [
      { icon: '🛡️', title: '장벽 강화', desc: '피부 방어막 회복' },
      { icon: '🌡️', title: '홍조 진정', desc: '붉음증, 갱년기 열감 완화' },
      { icon: '💊', title: '면역 조절', desc: '피부 면역력 향상' },
      { icon: '🌸', title: '민감도 감소', desc: '자극 반응 내성 강화' }
    ]
  }
};

function sendKakao(e) {
  e.preventDefault();
  const t = types[Object.keys({dry:0,oily:0,combo:0,sensitive:0}).reduce((a,b) => {
    const c = {dry:0,oily:0,combo:0,sensitive:0};
    Object.values(answers).forEach(v=>c[v]++);
    return c[a]>c[b]?a:b;
  })];
  const dominant = Object.keys({dry:0,oily:0,combo:0,sensitive:0}).reduce((a,b) => {
    const c = {dry:0,oily:0,combo:0,sensitive:0};
    Object.values(answers).forEach(v=>c[v]++);
    return c[a]>=c[b]?a:b;
  });
  const tp = types[dominant];
  const msg = encodeURIComponent(
    `[영은한의원 피부진단 결과]\n\n` +
    `✦ 피부 유형: ${tp.name}\n` +
    `✦ 주요 증상: ${tp.symptoms.slice(0,3).join(', ')}\n\n` +
    `추천 약침: ${tp.treatments.map(t=>t.name).join(', ')}\n\n` +
    `상담 예약을 원합니다 😊`
  );
  window.open(`https://open.kakao.com/o/gzvehqri`, '_blank');
}


  const q = btn.dataset.q, v = btn.dataset.v;
  document.querySelectorAll(`[data-q="${q}"]`).forEach(b => b.classList.remove('selected'));
  btn.classList.add('selected');
  answers[q] = v;
  updateProgress();
}

function updateProgress() {
  const count = Object.keys(answers).length;
  document.getElementById('progressFill').style.width = (count/TOTAL*100) + '%';
  document.getElementById('progressCount').textContent = count + ' / ' + TOTAL;
  document.getElementById('progressLabel').textContent = count === TOTAL ? '모든 질문 완료! ✓' : `${TOTAL-count}개 남았어요`;
  document.getElementById('submitWrap').classList.toggle('show', count === TOTAL);
}

function showResult() {
  const counts = {dry:0, oily:0, combo:0, sensitive:0};
  Object.values(answers).forEach(v => counts[v]++);
  const dominant = Object.keys(counts).reduce((a,b) => counts[a]>counts[b]?a:b);
  const t = types[dominant];

  const scoreHTML = [
    {label:'수분 지수', val:t.score.moisture, color:'#c45c7a'},
    {label:'탄력 지수', val:t.score.elasticity, color:'#b84d68'},
    {label:'톤 균일도', val:t.score.tone, color:'#d4788f'},
    {label:'피부 안정도', val:t.score.sensitivity, color:'#e07a95'}
  ].map(s=>`<div class="score-bar-wrap"><div class="score-bar-label"><span>${s.label}</span><span>${s.val}%</span></div><div class="score-bar"><div class="score-bar-fill" style="width:${s.val}%;background:${s.color}"></div></div></div>`).join('');

  const benefitHTML = `<div class="benefit-grid">${t.benefits.map(b=>`<div class="benefit-item"><div class="benefit-icon">${b.icon}</div><div class="benefit-title">${b.title}</div><div class="benefit-desc">${b.desc}</div></div>`).join('')}</div>`;

  const herbHTML = t.herbs.map(h=>`<div class="herb-card"><div class="herb-name">${h.name}</div><div class="herb-hanja">${h.hanja}</div><div class="herb-desc">${h.desc}</div><div class="herb-tags">${h.tags.map(tag=>`<span class="herb-tag">${tag}</span>`).join('')}</div></div>`).join('');

  const treatHTML = t.treatments.map(tr=>`<div class="treatment-item"><div class="treat-icon">${tr.icon}</div><div><div class="treat-name">${tr.name}</div><div class="treat-desc">${tr.desc}</div></div></div>`).join('');

  document.getElementById('resultContent').innerHTML = `
    <div class="result-hero">
      <div class="result-type-badge">${t.badge}</div>
      <div class="result-type-name">${t.emoji} ${t.name}</div>
      <div class="result-desc">${t.desc}</div>
    </div>
    <div class="result-card"><div class="result-card-title">주요 증상 패턴</div><ul class="symptom-list">${t.symptoms.map(s=>`<li>${s}</li>`).join('')}</ul></div>
    <div class="result-card"><div class="result-card-title">피부 상태 분석</div>${scoreHTML}</div>
    <div class="result-card"><div class="result-card-title">동안약침이 이런 도움을 줘요</div>${benefitHTML}</div>
    <div class="result-card"><div class="result-card-title">맞춤 약침 프로토콜</div>${treatHTML}</div>
    <div class="result-card"><div class="result-card-title">함께 추천하는 한약</div>${herbHTML}</div>
    <div class="cta-card">
      <h3>결과를 원장님께 바로 전달하기</h3>
      <p>진단 결과를 카카오톡으로 보내면<br>원장님이 직접 맞춤 상담을 도와드려요 💕</p>
      <a class="cta-btn" id="kakaoSendBtn" href="#" onclick="sendKakao(event)" style="background:#FEE500;color:#3C1E1E;display:block;margin-bottom:10px;">💬 카카오톡으로 결과 전송하기</a>
      <a class="cta-btn" href="https://m.booking.naver.com/booking/13/bizes/650417?theme=place&service-target=map-pc&lang=ko&area=plt&map-search=1" target="_blank" style="display:block;">📅 네이버 예약 바로가기</a>
    </div>
  `;
  document.getElementById('quizContainer').style.display = 'none';
  document.getElementById('resultSection').classList.add('show');
  window.scrollTo({top:0, behavior:'smooth'});
}

function retryQuiz() {
  Object.keys(answers).forEach(k=>delete answers[k]);
  document.querySelectorAll('.option-btn').forEach(b=>b.classList.remove('selected'));
  document.getElementById('quizContainer').style.display = 'block';
  document.getElementById('resultSection').classList.remove('show');
  document.getElementById('submitWrap').classList.remove('show');
  document.getElementById('progressFill').style.width = '0%';
  document.getElementById('progressCount').textContent = '0 / 12';
  document.getElementById('progressLabel').textContent = '진단을 시작해주세요';
  window.scrollTo({top:0, behavior:'smooth'});
}

// ======= 설문 =======
const painDescs = ['전혀 아프지 않았어요','거의 느끼지 못했어요','아주 약한 느낌','살짝 따끔했어요','약간 아팠어요','보통 수준이에요','제법 아팠어요','꽤 아팠어요','많이 아팠어요','매우 아팠어요','참기 어려웠어요'];

function updatePain(val) {
  document.getElementById('painValue').textContent = val;
  document.getElementById('painDesc').textContent = painDescs[val];
}

function selectSession(btn) {
  document.querySelectorAll('#sessionGroup .session-btn').forEach(b=>b.classList.remove('selected'));
  btn.classList.add('selected');
}

function selectRadio(groupId, el) {
  document.querySelectorAll(`#${groupId} .radio-item`).forEach(b=>b.classList.remove('selected'));
  el.classList.add('selected');
  if (groupId === 'rednessGroup') {
    document.getElementById('durationWrap').style.display = el.textContent.includes('있') ? 'block' : 'none';
  }
}

function toggleCheck(el) {
  el.classList.toggle('checked');
}

function submitSurvey() {
  document.querySelectorAll('.survey-card').forEach(c=>c.style.display='none');
  document.querySelector('.survey-submit-btn').style.display='none';
  document.querySelector('.survey-header').style.display='none';
  document.getElementById('surveyComplete').classList.add('show');
  window.scrollTo({top:0, behavior:'smooth'});
}
</script>
</body>
</html>
