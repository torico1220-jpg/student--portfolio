# student--portfolio
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>조현재 | 행정학 · 금융·데이터 포트폴리오</title>
  <style>
    :root {
      --bg-cream: #f6f2e9;
      --bg-card: #fcfaf5;
      --bg-soft: #ebe4d5;
      --green-deep: #1b3b2b;
      --green-mid: #2f5d46;
      --green-sage: #7ea184;
      --green-mint: #dce6dc;
      --wood-warm: #c99e74;
      --text-main: #1d2621;
      --text-muted: #58635c;
      --border-line: #ded6c6;
      --shadow-soft: 0 14px 34px rgba(27, 59, 43, 0.08);
      --radius-lg: 22px;
      --radius-md: 14px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Pretendard", "Apple SD Gothic Neo", "Malgun Gothic", sans-serif;
      background-color: var(--bg-cream);
      color: var(--text-main);
      line-height: 1.65;
      overflow-x: hidden;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font-family: inherit;
      cursor: pointer;
    }

    /* 상단 안내 배너 */
    .top-banner {
      background-color: var(--green-deep);
      color: #f4f1ea;
      text-align: center;
      font-size: 0.78rem;
      letter-spacing: 0.02em;
      padding: 8px 16px;
    }

    /* 헤더 및 내비게이션 */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      background-color: rgba(246, 242, 233, 0.92);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border-line);
    }

    .nav-container {
      max-width: 1120px;
      margin: 0 auto;
      padding: 14px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      flex-wrap: wrap;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-mark {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--green-mid), var(--green-sage));
      display: inline-flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-weight: 700;
      font-size: 0.85rem;
      flex-shrink: 0;
    }

    .brand-text {
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 0.95rem;
      font-weight: 700;
      color: var(--green-deep);
    }

    .brand-sub {
      display: block;
      font-size: 0.65rem;
      font-weight: 500;
      color: var(--text-muted);
      letter-spacing: 0.05em;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 18px;
      flex-wrap: wrap;
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--text-muted);
    }

    .nav-links a:hover,
    .nav-links a:focus-visible {
      color: var(--green-deep);
      font-weight: 700;
    }

    .motion-toggle {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 7px 13px;
      border-radius: 999px;
      border: 1px solid var(--border-line);
      background-color: var(--bg-card);
      color: var(--green-deep);
      font-size: 0.8rem;
      font-weight: 600;
      transition: background-color 0.2s ease, border-color 0.2s ease;
    }

    .motion-toggle:hover,
    .motion-toggle:focus-visible {
      background-color: var(--green-mint);
      border-color: var(--green-sage);
    }

    /* 공통 섹션 레이아웃 */
    main {
      max-width: 1120px;
      margin: 0 auto;
      padding: 0 20px 80px;
    }

    section {
      padding: 64px 0;
      border-bottom: 1px solid var(--border-line);
    }

    section:last-of-type {
      border-bottom: none;
    }

    .section-eyebrow {
      font-size: 0.76rem;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--green-mid);
      margin-bottom: 8px;
    }

    .section-title {
      font-size: clamp(1.6rem, 3vw, 2.2rem);
      font-weight: 800;
      color: var(--green-deep);
      line-height: 1.28;
      margin-bottom: 12px;
    }

    .section-desc {
      color: var(--text-muted);
      font-size: 0.96rem;
      max-width: 640px;
      margin-bottom: 32px;
    }

    /* 1. 소개(Hero) + 움직이는 작업실 */
    .hero {
      padding-top: 48px;
      display: grid;
      grid-template-columns: 1.08fr 0.92fr;
      align-items: center;
      gap: 40px;
    }

    .badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 16px;
    }

    .pill-badge {
      font-size: 0.72rem;
      font-weight: 700;
      letter-spacing: 0.04em;
      padding: 5px 11px;
      border-radius: 8px;
      background-color: var(--green-mint);
      color: var(--green-deep);
    }

    .pill-badge.warm {
      background-color: var(--bg-soft);
      color: #5c4b36;
    }

    .hero-tagline {
      font-size: 1rem;
      color: var(--text-muted);
      margin-bottom: 6px;
    }

    .hero-name-en {
      font-size: clamp(2.6rem, 5vw, 3.8rem);
      font-weight: 900;
      color: var(--green-deep);
      line-height: 1.08;
      letter-spacing: -0.02em;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .hero-asterisk {
      color: var(--green-sage);
      font-size: 2.6rem;
    }

    .hero-name-ko {
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--green-mid);
      margin: 6px 0 16px;
    }

    .hero-intro {
      font-size: 1rem;
      color: var(--text-main);
      margin-bottom: 20px;
      max-width: 520px;
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 24px;
    }

    .skill-tag {
      font-size: 0.76rem;
      font-weight: 700;
      padding: 5px 12px;
      border-radius: 999px;
      border: 1px solid var(--border-line);
      background-color: var(--bg-card);
      color: var(--green-deep);
    }

    .hero-highlights {
      border-top: 1px solid var(--border-line);
      border-bottom: 1px solid var(--border-line);
      margin-bottom: 26px;
    }

    .highlight-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      padding: 13px 4px;
      border-bottom: 1px solid var(--border-line);
      text-align: left;
      width: 100%;
      background: transparent;
      border-left: none;
      border-right: none;
      border-top: none;
    }

    .highlight-item:last-child {
      border-bottom: none;
    }

    .highlight-item:hover .highlight-title {
      color: var(--green-mid);
      text-decoration: underline;
    }

    .highlight-title {
      font-size: 0.95rem;
      font-weight: 700;
      color: var(--text-main);
      display: block;
    }

    .highlight-meta {
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .highlight-status {
      font-size: 0.82rem;
      font-weight: 700;
      color: var(--green-mid);
      white-space: nowrap;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .btn-primary {
      background-color: var(--green-deep);
      color: #fff;
      padding: 12px 22px;
      border-radius: 999px;
      font-size: 0.92rem;
      font-weight: 700;
      border: 1px solid var(--green-deep);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: background-color 0.2s ease, transform 0.2s ease;
    }

    .btn-primary:hover,
    .btn-primary:focus-visible {
      background-color: var(--green-mid);
    }

    .btn-secondary {
      background-color: var(--bg-card);
      color: var(--green-deep);
      padding: 12px 22px;
      border-radius: 999px;
      font-size: 0.92rem;
      font-weight: 700;
      border: 1px solid var(--border-line);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: background-color 0.2s ease;
    }

    .btn-secondary:hover,
    .btn-secondary:focus-visible {
      background-color: var(--bg-soft);
    }

    /* 작업실 일러스트 래퍼 */
    .studio-column {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: relative;
      z-index: 1;
    }

    .scene-motion {
      width: 100%;
      max-width: 460px;
      will-change: transform;
      transform-style: preserve-3d;
    }

    .scene-motion svg {
      width: 100%;
      height: auto;
      display: block;
      overflow: visible;
    }

    .studio-caption {
      margin-top: 14px;
      text-align: center;
      font-size: 0.84rem;
      color: var(--text-muted);
      background-color: var(--bg-card);
      border: 1px solid var(--border-line);
      border-radius: 12px;
      padding: 10px 14px;
      max-width: 420px;
    }

    /* 2. 자격증 및 핵심 역량 프로젝트 카드 (2열 구성) */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 24px;
    }

    .project-card {
      background-color: var(--bg-card);
      border: 1px solid var(--border-line);
      border-radius: var(--radius-lg);
      padding: 24px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      box-shadow: var(--shadow-soft);
      transition: transform 0.2s ease, border-color 0.2s ease;
    }

    .project-card:hover {
      transform: translateY(-4px);
      border-color: var(--green-sage);
    }

    .project-thumb {
      border-radius: var(--radius-md);
      padding: 16px;
      margin-bottom: 18px;
      background-color: var(--green-mint);
    }

    .project-thumb.sand {
      background-color: #eadfce;
    }

    .project-thumb svg {
      width: 100%;
      height: 130px;
      display: block;
    }

    .project-code {
      font-size: 0.74rem;
      font-weight: 700;
      color: var(--green-mid);
      letter-spacing: 0.04em;
      margin-bottom: 6px;
    }

    .project-title {
      font-size: 1.2rem;
      font-weight: 800;
      color: var(--green-deep);
      line-height: 1.35;
      margin-bottom: 10px;
    }

    .project-summary {
      font-size: 0.9rem;
      color: var(--text-muted);
      margin-bottom: 18px;
    }

    .project-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-bottom: 18px;
    }

    .project-tags span {
      font-size: 0.75rem;
      padding: 4px 10px;
      border-radius: 999px;
      background-color: var(--bg-cream);
      border: 1px solid var(--border-line);
      color: var(--text-main);
      font-weight: 600;
    }

    .project-detail-btn {
      align-self: flex-start;
      background: transparent;
      border: none;
      color: var(--green-deep);
      font-size: 0.9rem;
      font-weight: 800;
      padding: 6px 0;
      display: inline-flex;
      align-items: center;
      gap: 4px;
      border-bottom: 2px solid var(--green-sage);
    }

    .project-detail-btn:hover,
    .project-detail-btn:focus-visible {
      color: var(--green-mid);
    }

    /* 3. 역량 (Skills) */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .skill-box {
      background-color: var(--bg-card);
      border: 1px solid var(--border-line);
      border-radius: var(--radius-md);
      padding: 22px;
    }

    .skill-box-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 8px;
      margin-bottom: 8px;
    }

    .skill-box h3 {
      font-size: 1.05rem;
      font-weight: 800;
      color: var(--green-deep);
    }

    .skill-level {
      font-size: 0.75rem;
      font-weight: 700;
      padding: 3px 9px;
      border-radius: 999px;
      background-color: var(--green-mint);
      color: var(--green-deep);
      white-space: nowrap;
    }

    .skill-box p {
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    /* 4. 활동 기록 (Journey) */
    .journey-list {
      display: grid;
      gap: 14px;
    }

    .journey-item {
      background-color: var(--bg-card);
      border: 1px solid var(--border-line);
      border-radius: var(--radius-md);
      padding: 20px 22px;
      display: grid;
      grid-template-columns: 160px 1fr;
      gap: 16px;
      align-items: start;
    }

    .journey-period {
      font-size: 0.82rem;
      font-weight: 700;
      color: var(--green-mid);
    }

    .journey-role {
      font-size: 1.04rem;
      font-weight: 800;
      color: var(--green-deep);
      margin-bottom: 4px;
    }

    .journey-desc {
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    /* 5. 연락처 (Contact) */
    .contact-card {
      background-color: var(--green-deep);
      color: #f6f2e9;
      border-radius: var(--radius-lg);
      padding: 34px 28px;
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 28px;
      align-items: center;
    }

    .contact-card .section-eyebrow {
      color: #b8d4be;
    }

    .contact-card h2 {
      font-size: 1.65rem;
      font-weight: 800;
      margin-bottom: 12px;
      line-height: 1.3;
    }

    .contact-card p {
      font-size: 0.94rem;
      color: #dce5de;
    }

    .contact-box {
      background-color: rgba(255, 255, 255, 0.08);
      border: 1px solid rgba(255, 255, 255, 0.18);
      border-radius: var(--radius-md);
      padding: 20px;
      display: grid;
      gap: 16px;
    }

    .contact-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
      padding-bottom: 14px;
      border-bottom: 1px solid rgba(255, 255, 255, 0.14);
    }

    .contact-row:last-child {
      padding-bottom: 0;
      border-bottom: none;
    }

    .contact-label {
      font-size: 0.76rem;
      color: #b8d4be;
      margin-bottom: 2px;
    }

    .contact-value {
      font-size: 1.06rem;
      font-weight: 700;
      word-break: break-all;
    }

    .copy-btn {
      background-color: var(--bg-cream);
      color: var(--green-deep);
      border: none;
      border-radius: 999px;
      padding: 7px 14px;
      font-size: 0.8rem;
      font-weight: 700;
      white-space: nowrap;
    }

    .copy-btn:hover {
      background-color: var(--green-mint);
    }

    .copy-feedback {
      font-size: 0.82rem;
      color: #b8d4be;
      min-height: 1.2em;
    }

    footer {
      text-align: center;
      padding: 24px 20px 40px;
      font-size: 0.82rem;
      color: var(--text-muted);
    }

    /* 상세 보기 모달 */
    .modal-backdrop {
      position: fixed;
      inset: 0;
      background-color: rgba(18, 33, 25, 0.58);
      display: none;
      align-items: center;
      justify-content: center;
      padding: 16px;
      z-index: 100;
    }

    .modal-backdrop.open {
      display: flex;
    }

    .modal-dialog {
      background-color: var(--bg-card);
      border: 1px solid var(--border-line);
      border-radius: var(--radius-lg);
      width: min(100%, 620px);
      max-height: 86vh;
      overflow-y: auto;
      padding: 28px 24px;
      box-shadow: 0 24px 48px rgba(0, 0, 0, 0.22);
      position: relative;
    }

    .modal-close {
      position: absolute;
      top: 18px;
      right: 18px;
      width: 34px;
      height: 34px;
      border-radius: 50%;
      border: 1px solid var(--border-line);
      background-color: var(--bg-cream);
      color: var(--green-deep);
      font-size: 1rem;
      font-weight: 700;
    }

    .modal-badge {
      display: inline-block;
      font-size: 0.72rem;
      font-weight: 700;
      letter-spacing: 0.06em;
      padding: 4px 10px;
      border-radius: 6px;
      background-color: var(--green-mint);
      color: var(--green-deep);
      margin-bottom: 10px;
    }

    .modal-title {
      font-size: 1.4rem;
      font-weight: 800;
      color: var(--green-deep);
      margin-bottom: 18px;
      padding-right: 36px;
    }

    .modal-block {
      margin-bottom: 14px;
      padding: 14px;
      border-radius: 12px;
      background-color: var(--bg-cream);
      border: 1px solid var(--border-line);
    }

    .modal-block h4 {
      font-size: 0.82rem;
      font-weight: 800;
      color: var(--green-mid);
      margin-bottom: 4px;
    }

    .modal-block p {
      font-size: 0.92rem;
      color: var(--text-main);
    }

    /* 반응형 (태블릿 & 모바일) */
    @media (max-width: 900px) {
      .hero {
        grid-template-columns: 1fr;
        gap: 32px;
        padding-top: 32px;
      }

      .studio-column {
        order: 2;
      }

      .projects-grid {
        grid-template-columns: 1fr;
      }

      .contact-card {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 640px) {
      .skills-grid {
        grid-template-columns: 1fr;
      }

      .journey-item {
        grid-template-columns: 1fr;
        gap: 6px;
      }

      .nav-links {
        gap: 12px;
        font-size: 0.84rem;
      }
    }
  </style>
</head>
<body>
  <div class="top-banner">
    PORTFOLIO · 행정학적 통찰과 데이터 분석 역량을 연결하는 조현재의 포트폴리오입니다.
  </div>

  <header>
    <div class="nav-container">
      <a href="#about" class="brand">
        <span class="brand-mark">조</span>
        <span>
          <span class="brand-text">조현재 · 행정학 전공</span>
          <span class="brand-sub">PERSONAL PORTFOLIO</span>
        </span>
      </a>

      <nav class="nav-links" aria-label="주요 메뉴">
        <a href="#about">About</a>
        <a href="#certifications">Certifications</a>
        <a href="#skills">Skills</a>
        <a href="#journey">Journey</a>
        <a href="#contact">Contact ↗</a>
        <button type="button" id="motionToggleBtn" class="motion-toggle" aria-pressed="false">
          ⏸ 움직임 멈춤
        </button>
      </nav>
    </div>
  </header>

  <main>
    <!-- 1. 소개 영역 + 데이터 작업실 SVG -->
    <section id="about" class="hero">
      <div>
        <div class="badge-row">
          <span class="pill-badge">PUBLIC ADMINISTRATION</span>
          <span class="pill-badge warm">행정학 전공 · 조현재</span>
        </div>

        <p class="hero-tagline">근거 있는 질문에서, 합리적인 의사결정까지.</p>
        <h1 class="hero-name-en">Hyunjae <span class="hero-asterisk">*</span></h1>
        <p class="hero-name-ko">조현재 · 행정학 전공</p>

        <p class="hero-intro">
          행정학적 시각으로 조직과 제도의 문제를 구조화하고, 객관적인 데이터와 근거를 바탕으로 합리적인 대안을 설계합니다.
          <strong>투자자산운용사</strong>와 <strong>한국사능력검정 1급</strong> 자격을 갖추며 금융·경제 데이터 해석과 제도적 맥락 이해를 함께 넓혀왔습니다.
        </p>

        <div class="skill-tags">
          <span class="skill-tag">행정학</span>
          <span class="skill-tag">투자자산운용사</span>
          <span class="skill-tag">한국사능력검정 1급</span>
          <span class="skill-tag">DATA &amp; POLICY</span>
        </div>

        <div class="hero-highlights">
          <button type="button" class="highlight-item" data-project="0">
            <span>
              <span class="highlight-title">투자자산운용사 자격 취득</span>
              <span class="highlight-meta">금융투자협회 · 자산운용 및 리스크 관리 전문 자격</span>
            </span>
            <span class="highlight-status">상세 보기 ↗</span>
          </button>
          <button type="button" class="highlight-item" data-project="1">
            <span>
              <span class="highlight-title">한국사능력검정시험 1급 취득</span>
              <span class="highlight-meta">국사편찬위원회 · 심화 과정 최고 등급 인증</span>
            </span>
            <span class="highlight-status">상세 보기 ↗</span>
          </button>
        </div>

        <div class="hero-actions">
          <a href="#certifications" class="btn-primary">자격증 및 역량 보기 ↗</a>
          <a href="#contact" class="btn-secondary">연락처 확인하기</a>
        </div>
      </div>

      <!-- 움직이는 작업실 (.scene-motion) -->
      <div class="studio-column">
        <div class="scene-motion" id="studioScene" aria-label="듀얼 모니터 앞에서 데이터를 분석하는 둥근 캐릭터 작업실 일러스트">
          <svg viewBox="0 0 500 440" role="img" aria-labelledby="studioSvgTitle studioSvgDesc">
            <title id="studioSvgTitle">작은 데이터 작업실 일러스트</title>
            <desc id="studioSvgDesc">나무 책상 위 듀얼 모니터, 둥근 캐릭터, 책장, 화분, 머그컵이 배치된 입체감 있는 인라인 SVG 그림</desc>
            <defs>
              <linearGradient id="deskTopGrad" x1="0" y1="0" x2="1" y2="1">
                <stop offset="0%" stop-color="#dfb88c" />
                <stop offset="100%" stop-color="#c39364" />
              </linearGradient>
              <linearGradient id="deskFrontGrad" x1="0" y1="0" x2="0" y2="1">
                <stop offset="0%" stop-color="#b78556" />
                <stop offset="100%" stop-color="#9c6d43" />
              </linearGradient>
              <linearGradient id="sweaterGrad" x1="0" y1="0" x2="0" y2="1">
                <stop offset="0%" stop-color="#87ab8c" />
                <stop offset="100%" stop-color="#5d8364" />
              </linearGradient>
              <linearGradient id="screenGrad" x1="0" y1="0" x2="1" y2="1">
                <stop offset="0%" stop-color="#f7f4ec" />
                <stop offset="100%" stop-color="#e3eadf" />
              </linearGradient>
              <filter id="softShadow" x="-15%" y="-15%" width="130%" height="135%">
                <feDropShadow dx="0" dy="10" stdDeviation="10" flood-color="#1b3b2b" flood-opacity="0.12" />
              </filter>
              <filter id="cardShadow" x="-20%" y="-20%" width="140%" height="145%">
                <feDropShadow dx="0" dy="6" stdDeviation="6" flood-color="#1b3b2b" flood-opacity="0.14" />
              </filter>
            </defs>

            <!-- 바닥 원형 그림자 -->
            <ellipse cx="250" cy="366" rx="185" ry="42" fill="#e5dec9" />

            <!-- 배경 책장 -->
            <g opacity="0.9">
              <rect x="64" y="102" width="12" height="175" rx="4" fill="#cbb99d" />
              <rect x="148" y="90" width="12" height="175" rx="4" fill="#cbb99d" />
              <polygon points="56,134 166,118 166,127 56,143" fill="#d8c8ae" />
              <polygon points="56,184 166,168 166,177 56,193" fill="#d8c8ae" />
              <polygon points="56,234 166,218 166,227 56,243" fill="#d8c8ae" />
              <rect x="78" y="103" width="11" height="32" rx="2" fill="#6f9476" transform="rotate(-6 78 103)" />
              <rect x="92" y="101" width="11" height="32" rx="2" fill="#d68c6c" transform="rotate(-6 92 101)" />
              <rect x="106" y="99" width="12" height="32" rx="2" fill="#f3eee2" transform="rotate(-6 106 99)" />
              <rect x="82" y="154" width="38" height="10" rx="2" fill="#7ea184" transform="rotate(-8 82 154)" />
              <rect x="85" y="164" width="42" height="10" rx="2" fill="#d9c6a5" transform="rotate(-8 85 164)" />
            </g>

            <!-- 책상 다리 -->
            <rect x="128" y="242" width="14" height="112" rx="5" fill="#9c6d43" />
            <rect x="364" y="248" width="14" height="112" rx="5" fill="#9c6d43" />
            <rect x="294" y="286" width="15" height="104" rx="5" fill="#b38255" />

            <!-- 나무 책상 상판 -->
            <g filter="url(#softShadow)">
              <polygon points="106,232 276,196 404,242 252,292" fill="url(#deskTopGrad)" />
              <polygon points="106,232 252,292 252,306 106,246" fill="url(#deskFrontGrad)" />
              <polygon points="252,292 404,242 404,256 252,306" fill="#a87649" />
            </g>

            <!-- 왼쪽 모니터 (꺾은선 그래프) -->
            <g>
              <rect x="186" y="200" width="12" height="24" rx="3" fill="#2c4437" />
              <ellipse cx="192" cy="224" rx="22" ry="6" fill="#243a2e" />
              <polygon points="136,122 246,108 246,196 136,208" fill="#1f382b" stroke="#2c4a3a" stroke-width="4" />
              <polygon points="143,129 239,116 239,189 143,200" fill="url(#screenGrad)" />
              <polyline points="152,182 172,162 192,168 212,140 230,134" fill="none" stroke="#3c7356" stroke-width="4" stroke-linecap="round" stroke-linejoin="round" />
              <circle cx="212" cy="140" r="4.5" fill="#d98a5f" />
            </g>

            <!-- 오른쪽 모니터 (막대 그래프) -->
            <g>
              <rect x="304" y="206" width="12" height="24" rx="3" fill="#2c4437" />
              <ellipse cx="310" cy="230" rx="22" ry="6" fill="#243a2e" />
              <polygon points="258,108 368,124 368,214 258,198" fill="#1f382b" stroke="#2c4a3a" stroke-width="4" />
              <polygon points="265,116 361,130 361,205 265,191" fill="url(#screenGrad)" />
              <rect x="278" y="160" width="11" height="26" rx="2" fill="#89ad8f" />
              <rect x="296" y="144" width="11" height="44" rx="2" fill="#4f8266" />
              <rect x="314" y="152" width="11" height="39" rx="2" fill="#89ad8f" />
              <rect x="332" y="136" width="11" height="58" rx="2" fill="#2f5d46" />
            </g>

            <!-- 책상 위 머그컵 -->
            <g>
              <ellipse cx="144" cy="238" rx="14" ry="5" fill="#b48458" />
              <rect x="132" y="216" width="22" height="22" rx="6" fill="#fcfaf5" stroke="#dfd6c5" stroke-width="1.5" />
              <path d="M154 221 C161 221, 161 233, 154 233" fill="none" stroke="#dfd6c5" stroke-width="3" stroke-linecap="round" />
              <path d="M140 209 Q137 203 141 198" fill="none" stroke="#b9c4bc" stroke-width="2" stroke-linecap="round" />
              <path d="M147 210 Q144 204 148 199" fill="none" stroke="#b9c4bc" stroke-width="2" stroke-linecap="round" />
            </g>

            <!-- 책상 위 메모지 -->
            <polygon points="282,248 326,238 340,248 296,259" fill="#fcfaf5" stroke="#ded6c6" stroke-width="1.2" />
            <line x1="295" y1="249" x2="322" y2="243" stroke="#9eb2a3" stroke-width="2" stroke-linecap="round" />

            <!-- 오른쪽 화분과 식물 -->
            <g>
              <ellipse cx="364" cy="252" rx="18" ry="6" fill="#a87649" />
              <polygon points="349,218 379,218 374,251 354,251" fill="#c97d5d" />
              <ellipse cx="364" cy="218" rx="15" ry="4.5" fill="#8a5843" />
              <path d="M364 218 C362 198, 346 190, 342 178 C355 178, 364 192, 364 218 Z" fill="#5e8c68" />
              <path d="M364 218 C366 194, 384 186, 390 174 C376 175, 365 190, 364 218 Z" fill="#77a37f" />
              <path d="M364 215 C364 192, 364 176, 366 164 C374 176, 372 195, 364 215 Z" fill="#467050" />
            </g>

            <!-- 둥근 캐릭터 -->
            <g filter="url(#softShadow)">
              <rect x="218" y="294" width="18" height="44" rx="8" fill="#3a4f66" />
              <rect x="242" y="296" width="18" height="44" rx="8" fill="#2f4257" />
              <ellipse cx="224" cy="340" rx="12" ry="6" fill="#fcfaf5" />
              <ellipse cx="249" cy="342" rx="12" ry="6" fill="#fcfaf5" />

              <rect x="196" y="224" width="76" height="82" rx="36" fill="url(#sweaterGrad)" />
              <path d="M204 242 C188 252, 190 268, 212 268" fill="none" stroke="#6f9676" stroke-width="16" stroke-linecap="round" />
              <path d="M262 240 C278 248, 288 254, 298 252" fill="none" stroke="#7ea585" stroke-width="15" stroke-linecap="round" />
              <circle cx="299" cy="252" r="7" fill="#f5cfb8" />

              <circle cx="234" cy="192" r="33" fill="#4a372e" />
              <circle cx="236" cy="196" r="27" fill="#f7d5bf" />
              <path d="M209 190 C212 166, 258 164, 263 190 C252 178, 236 178, 224 188 C218 182, 212 185, 209 190 Z" fill="#4a372e" />
              <circle cx="230" cy="197" r="2.4" fill="#3b2b23" />
              <circle cx="248" cy="197" r="2.4" fill="#3b2b23" />
              <ellipse cx="224" cy="203" rx="4" ry="2.2" fill="#eba396" opacity="0.7" />
              <ellipse cx="253" cy="203" rx="4" ry="2.2" fill="#eba396" opacity="0.7" />
              <path d="M235 204 Q239 209 244 204" fill="none" stroke="#3b2b23" stroke-width="2" stroke-linecap="round" />
            </g>

            <!-- 의자 등받이와 바퀴 -->
            <g>
              <rect x="218" y="330" width="8" height="28" rx="3" fill="#526958" />
              <path d="M194 364 L222 354 L250 364" fill="none" stroke="#526958" stroke-width="6" stroke-linecap="round" />
              <circle cx="194" cy="367" r="4.5" fill="#2b3d30" />
              <circle cx="222" cy="369" r="4.5" fill="#2b3d30" />
              <circle cx="250" cy="367" r="4.5" fill="#2b3d30" />
              <rect x="192" y="272" width="58" height="44" rx="14" fill="#75947b" stroke="#5e7c64" stroke-width="2" />
            </g>

            <!-- 우측 상단 말풍선 카드 -->
            <g filter="url(#cardShadow)" transform="rotate(3 395 72)">
              <rect x="316" y="42" width="158" height="58" rx="10" fill="#fcfaf5" stroke="#e4dccb" stroke-width="1.5" />
              <text x="395" y="64" text-anchor="middle" font-size="9" font-weight="700" fill="#78857d" letter-spacing="0.06em">TODAY'S LITTLE QUESTION</text>
              <text x="395" y="84" text-anchor="middle" font-size="13" font-weight="800" fill="#1b3b2b">“왜 달라졌을까?”</text>
            </g>

            <!-- 좌측 하단 스튜디오 태그 -->
            <g filter="url(#cardShadow)" transform="rotate(-4 112 332)">
              <rect x="44" y="316" width="136" height="30" rx="15" fill="#e9dec8" stroke="#d8cab0" stroke-width="1.2" />
              <text x="112" y="335" text-anchor="middle" font-size="11" font-weight="700" fill="#5b4d3b">hyunjae workspace +</text>
            </g>
          </svg>
        </div>

        <p class="studio-caption">
          마우스를 움직이거나 스크롤해 보세요. 정책과 데이터를 꼼꼼히 살피는 작업 공간을 담았습니다.
        </p>
      </div>
    </section>

    <!-- 2. 보유 자격증 (Certifications) -->
    <section id="certifications">
      <p class="section-eyebrow">02 / CERTIFICATIONS &amp; QUALIFICATIONS</p>
      <h2 class="section-title">전문성을 증명하는 보유 자격증</h2>
      <p class="section-desc">
        행정학 전공 기반 위에 금융·자산운용 전문성과 인문·역사적 맥락 이해를 더해 다각도로 문제를 바라봅니다. 각 카드의 <strong>과정 살펴보기</strong>를 누르면 상세 내용을 확인할 수 있습니다.
      </p>

      <div class="projects-grid">
        <!-- 자격증 1: 투자자산운용사 -->
        <article class="project-card">
          <div>
            <div class="project-thumb">
              <svg viewBox="0 0 260 130" aria-hidden="true">
                <rect x="18" y="14" width="224" height="102" rx="12" fill="#fcfaf5" />
                <polyline points="38,94 82,68 122,78 168,40 218,50" fill="none" stroke="#2f5d46" stroke-width="5" stroke-linecap="round" stroke-linejoin="round" />
                <circle cx="168" cy="40" r="7" fill="#d68c6c" />
                <rect x="38" y="28" width="64" height="10" rx="5" fill="#dce6dc" />
              </svg>
            </div>
            <p class="project-code">01 / FINANCE · 금융투자협회</p>
            <h3 class="project-title">투자자산운용사</h3>
            <p class="project-summary">
              거시경제 분석, 금융상품 이해, 포트폴리오 운용 전략 및 리스크 관리·직무윤리 전반에 걸친 전문 지식을 학습하고 자격을 취득했습니다.
            </p>
          </div>
          <div>
            <div class="project-tags">
              <span>자산운용</span>
              <span>거시경제·금융</span>
              <span>리스크 관리</span>
            </div>
            <button type="button" class="project-detail-btn" data-project="0">과정 살펴보기 ↗</button>
          </div>
        </article>

        <!-- 자격증 2: 한국사능력검정 1급 -->
        <article class="project-card">
          <div>
            <div class="project-thumb sand">
              <svg viewBox="0 0 260 130" aria-hidden="true">
                <rect x="26" y="18" width="208" height="94" rx="12" fill="#fcfaf5" />
                <rect x="46" y="36" width="96" height="10" rx="5" fill="#c99e74" />
                <rect x="46" y="56" width="76" height="9" rx="4.5" fill="#dfd5c3" />
                <rect x="46" y="74" width="88" height="9" rx="4.5" fill="#dfd5c3" />
                <circle cx="192" cy="66" r="20" fill="#2f5d46" />
                <text x="192" y="71" text-anchor="middle" font-size="13" font-weight="800" fill="#fcfaf5">1급</text>
              </svg>
            </div>
            <p class="project-code">02 / HUMANITIES · 국사편찬위원회</p>
            <h3 class="project-title">한국사능력검정 1급</h3>
            <p class="project-summary">
              한국사의 주요 흐름과 제도 변천사를 심층적으로 학습하고, 다양한 사료와 시대적 배경을 종합적으로 해석하는 역량을 검증받았습니다.
            </p>
          </div>
          <div>
            <div class="project-tags">
              <span>한국사 1급</span>
              <span>제도·정책사</span>
              <span>사료 해석</span>
            </div>
            <button type="button" class="project-detail-btn" data-project="1">과정 살펴보기 ↗</button>
          </div>
        </article>
      </div>
    </section>

    <!-- 3. 핵심 역량 (Skills) -->
    <section id="skills">
      <p class="section-eyebrow">03 / CAPABILITIES</p>
      <h2 class="section-title">전공과 자격을 연결하는 핵심 역량</h2>
      <p class="section-desc">
        제도의 원리를 이해하는 행정학적 사고력과 수치를 객관적으로 해석하는 분석 역량을 균형 있게 갖추고 있습니다.
      </p>

      <div class="skills-grid">
        <div class="skill-box">
          <div class="skill-box-header">
            <h3>행정학 기반 정책·조직 분석</h3>
            <span class="skill-level">전공 역량</span>
          </div>
          <p>공공 정책의 기획·집행·평가 과정과 조직 관리 이론을 바탕으로 문제의 원인과 제도적 개선 방향을 구조화합니다.</p>
        </div>

        <div class="skill-box">
          <div class="skill-box-header">
            <h3>금융·투자 데이터 해석 (투자자산운용사)</h3>
            <span class="skill-level">자격 검증</span>
          </div>
          <p>거시경제 지표와 금융상품 구조, 리스크·수익률 개념을 이해하고 정량적 근거를 바탕으로 합리적 판단을 내립니다.</p>
        </div>

        <div class="skill-box">
          <div class="skill-box-header">
            <h3>역사·제도 맥락 이해 (한국사 1급)</h3>
            <span class="skill-level">자격 검증</span>
          </div>
          <p>시대별 사회·제도 변천사를 입체적으로 파악하고 사료와 텍스트 자료 속 핵심 맥락을 정확히 읽어냅니다.</p>
        </div>

        <div class="skill-box">
          <div class="skill-box-header">
            <h3>데이터 정리 및 논리적 리포팅</h3>
            <span class="skill-level">실무 활용</span>
          </div>
          <p>조사한 데이터와 근거 자료를 체계적으로 정리하여 의사결정자가 한눈에 파악할 수 있는 보고서 형태로 전달합니다.</p>
        </div>
      </div>
    </section>

    <!-- 4. 학업 및 취득 이력 (Journey) -->
    <section id="journey">
      <p class="section-eyebrow">04 / JOURNEY &amp; MILESTONES</p>
      <h2 class="section-title">성장의 기반을 다진 기록</h2>
      <p class="section-desc">
        행정학 전공 학습과 전문 자격 취득을 통해 다져온 주요 이력입니다.
      </p>

      <div class="journey-list">
        <div class="journey-item">
          <div class="journey-period">MAJOR · 전공 과정</div>
          <div>
            <h3 class="journey-role">행정학 전공 심화 학습</h3>
            <p class="journey-desc">정책학, 조직론, 재무행정 등 행정학 핵심 분야를 학습하며 합리적 자원 배분과 의사결정 체계를 탐구하고 있습니다.</p>
          </div>
        </div>

        <div class="journey-item">
          <div class="journey-period">CERTIFICATION · 금융</div>
          <div>
            <h3 class="journey-role">투자자산운용사 자격 취득</h3>
            <p class="journey-desc">금융투자협회 주관 투자자산운용사 시험에 합격하여 자산운용 전략, 경제 분석 및 리스크 관리 전문 지식을 갖추었습니다.</p>
          </div>
        </div>

        <div class="journey-item">
          <div class="journey-period">CERTIFICATION · 인문</div>
          <div>
            <h3 class="journey-role">한국사능력검정시험 1급 취득</h3>
            <p class="journey-desc">국사편찬위원회 주관 심화 시험에서 최고 등급인 1급을 취득하며 역사와 제도의 흐름을 읽어내는 사고력을 검증받았습니다.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 5. 연락처 (Contact) -->
    <section id="contact">
      <div class="contact-card">
        <div>
          <p class="section-eyebrow">05 / CONTACT</p>
          <h2>함께 고민하고 성장할 기회를 기다립니다</h2>
          <p>
            행정학적 통찰과 금융·데이터 분석 역량을 바탕으로 맡은 역할에 책임감을 다하겠습니다.
            궁금한 점이나 제안이 있으시면 아래 연락처 또는 이메일로 편하게 연락해 주세요.
          </p>
        </div>

        <div class="contact-box">
          <div class="contact-row">
            <div>
              <p class="contact-label">연락처 (Phone)</p>
              <p class="contact-value" id="phoneText">010-9900-5196</p>
            </div>
            <button type="button" class="copy-btn" data-copy-target="phoneText">번호 복사</button>
          </div>

          <div class="contact-row">
            <div>
              <p class="contact-label">이메일 (Email)</p>
              <p class="contact-value" id="emailText">poiyt12@naver.com</p>
            </div>
            <button type="button" class="copy-btn" data-copy-target="emailText">이메일 복사</button>
          </div>

          <p class="copy-feedback" id="copyFeedback" role="status" aria-live="polite"></p>
        </div>
      </div>
    </section>
  </main>

  <footer>
    © 2026 조현재 (Hyunjae Cho) · 행정학 전공 포트폴리오
  </footer>

  <!-- 상세 보기 모달 -->
  <div class="modal-backdrop" id="projectModal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
    <div class="modal-dialog">
      <button type="button" class="modal-close" id="modalCloseBtn" aria-label="상세 보기 닫기">✕</button>
      <span class="modal-badge" id="modalBadge">CERTIFICATION</span>
      <h3 class="modal-title" id="modalTitle">자격증 상세</h3>

      <div class="modal-block">
        <h4>취득 배경 및 목표</h4>
        <p id="modalProblem"></p>
      </div>
      <div class="modal-block">
        <h4>핵심 학습 영역</h4>
        <p id="modalRole"></p>
      </div>
      <div class="modal-block">
        <h4>역량 적용 방향</h4>
        <p id="modalMethod"></p>
      </div>
      <div class="modal-block">
        <h4>성과와 의의</h4>
        <p id="modalResult"></p>
      </div>
    </div>
  </div>

  <script>
    // 1. 보유 자격증 상세 보기 데이터
    const projectDetails = [
      {
        badge: "CERTIFICATION · 금융투자협회",
        title: "투자자산운용사",
        problem: "행정학적 의사결정 역량에 금융·경제적 분석 시각을 더하기 위해 자본시장과 자산운용 전반의 실무 지식을 체계적으로 학습했습니다.",
        role: "대안투자 및 파생상품, 거시경제와 분산투자 전략, 투자운용결과 분석, 직무윤리 및 자본시장법규 등 핵심 과목 전반을 심화 학습했습니다.",
        method: "재무 제표와 시장 지표를 객관적으로 해석하는 능력을 갖추었으며, 공공·민간 영역 모두에서 정량적 근거에 기반한 자원 배분 및 의사결정에 활용할 수 있습니다.",
        result: "투자자산운용사 자격증 취득을 통해 금융 데이터 해석 및 리스크 관리에 대한 탄탄한 기초 전문성을 검증받았습니다."
      },
      {
        badge: "CERTIFICATION · 국사편찬위원회",
        title: "한국사능력검정 1급",
        problem: "행정학 전공자로서 국가 제도와 정책이 형성되고 변화해 온 역사적 맥락을 깊이 이해하기 위해 심화 과정 최고 등급인 1급 취득을 목표로 준비했습니다.",
        role: "고대부터 근현대사에 이르는 정치·경제·사회·문화사 전반과 주요 사료 및 시대별 제도의 인과관계를 구조화하여 정리했습니다.",
        method: "단편적인 정보 암기를 넘어 사건의 배경과 파급 효과를 입체적으로 파악하는 훈련을 통해, 복잡한 사회·정책 현안의 맥락을 읽는 사고력을 길렀습니다.",
        result: "심화 과정 1급 취득을 통해 인문학적 소양과 자료 해석 능력을 입증했습니다."
      }
    ];

    const modal = document.getElementById("projectModal");
    const modalBadge = document.getElementById("modalBadge");
    const modalTitle = document.getElementById("modalTitle");
    const modalProblem = document.getElementById("modalProblem");
    const modalRole = document.getElementById("modalRole");
    const modalMethod = document.getElementById("modalMethod");
    const modalResult = document.getElementById("modalResult");
    const modalCloseBtn = document.getElementById("modalCloseBtn");
    let lastFocusedEl = null;

    function openProjectModal(index) {
      const data = projectDetails[index];
      if (!data) return;
      lastFocusedEl = document.activeElement;
      modalBadge.textContent = data.badge;
      modalTitle.textContent = data.title;
      modalProblem.textContent = data.problem;
      modalRole.textContent = data.role;
      modalMethod.textContent = data.method;
      modalResult.textContent = data.result;
      modal.classList.add("open");
      modalCloseBtn.focus();
    }

    function closeProjectModal() {
      modal.classList.remove("open");
      if (lastFocusedEl) lastFocusedEl.focus();
    }

    document.querySelectorAll("[data-project]").forEach((btn) => {
      btn.addEventListener("click", () => {
        const idx = Number(btn.getAttribute("data-project"));
        openProjectModal(idx);
      });
    });

    modalCloseBtn.addEventListener("click", closeProjectModal);
    modal.addEventListener("click", (e) => {
      if (e.target === modal) closeProjectModal();
    });
    document.addEventListener("keydown", (e) => {
      if (e.key === "Escape" && modal.classList.contains("open")) {
        closeProjectModal();
      }
    });

    // 2. 연락처 및 이메일 복사 기능
    const copyFeedback = document.getElementById("copyFeedback");
    document.querySelectorAll("[data-copy-target]").forEach((btn) => {
      btn.addEventListener("click", async () => {
        const targetId = btn.getAttribute("data-copy-target");
        const targetEl = document.getElementById(targetId);
        if (!targetEl) return;
        const text = targetEl.textContent.trim();
        try {
          await navigator.clipboard.writeText(text);
          copyFeedback.textContent = `"${text}" 복사되었습니다.`;
        } catch {
          copyFeedback.textContent = `${text} 를 직접 선택해 복사해주세요.`;
        }
        setTimeout(() => {
          copyFeedback.textContent = "";
        }, 2500);
      });
    });

    // 3. .scene-motion 작업실 애니메이션 (requestAnimationFrame 기반)
    const studioScene = document.getElementById("studioScene");
    const motionToggleBtn = document.getElementById("motionToggleBtn");
    const reducedMotionQuery = window.matchMedia("(prefers-reduced-motion: reduce)");
    const isCoarsePointer = window.matchMedia("(pointer: coarse)").matches;

    let isPaused = reducedMotionQuery.matches;
    let rafId = null;

    let targetMouseX = 0;
    let targetMouseY = 0;
    let currentMouseX = 0;
    let currentMouseY = 0;
    let currentScrollY = 0;

    function updateToggleButton() {
      motionToggleBtn.textContent = isPaused ? "▶ 움직임 켜기" : "⏸ 움직임 멈춤";
      motionToggleBtn.setAttribute("aria-pressed", String(isPaused));
    }

    if (!isCoarsePointer) {
      window.addEventListener("mousemove", (e) => {
        if (isPaused) return;
        const normX = (e.clientX / window.innerWidth - 0.5) * 2;
        const normY = (e.clientY / window.innerHeight - 0.5) * 2;
        targetMouseX = normX;
        targetMouseY = normY;
      }, { passive: true });
    }

    function animateStudio(timestamp) {
      if (isPaused || document.hidden) {
        rafId = null;
        return;
      }

      const floatY = Math.sin((timestamp / 7000) * Math.PI * 2) * 5;
      const targetScrollOffset = -Math.min(20, Math.max(0, window.scrollY * 0.06));
      currentScrollY += (targetScrollOffset - currentScrollY) * 0.08;

      currentMouseX += (targetMouseX - currentMouseX) * 0.06;
      currentMouseY += (targetMouseY - currentMouseY) * 0.06;

      const moveX = isCoarsePointer ? 0 : currentMouseX * 8;
      const moveY = floatY + currentScrollY + (isCoarsePointer ? 0 : currentMouseY * 5);
      const tiltDeg = isCoarsePointer ? 0 : Math.max(-4, Math.min(4, currentMouseX * 4));

      studioScene.style.transform = `translate3d(${moveX.toFixed(2)}px, ${moveY.toFixed(2)}px, 0) rotate(${tiltDeg.toFixed(2)}deg)`;
      rafId = requestAnimationFrame(animateStudio);
    }

    function startMotion() {
      if (!rafId && !isPaused && !document.hidden) {
        rafId = requestAnimationFrame(animateStudio);
      }
    }

    function stopMotion(resetTransform = false) {
      if (rafId) {
        cancelAnimationFrame(rafId);
        rafId = null;
      }
      if (resetTransform) {
        studioScene.style.transform = "translate3d(0, 0, 0) rotate(0deg)";
      }
    }

    motionToggleBtn.addEventListener("click", () => {
      isPaused = !isPaused;
      updateToggleButton();
      if (isPaused) {
        stopMotion(true);
      } else {
        startMotion();
      }
    });

    reducedMotionQuery.addEventListener("change", (e) => {
      isPaused = e.matches;
      updateToggleButton();
      if (isPaused) {
        stopMotion(true);
      } else {
        startMotion();
      }
    });

    document.addEventListener("visibilitychange", () => {
      if (document.hidden) {
        stopMotion(false);
      } else if (!isPaused) {
        startMotion();
      }
    });

    updateToggleButton();
    if (!isPaused) {
      startMotion();
    }
  </script>
</body>
</html>
