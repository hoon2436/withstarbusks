---
marp: true
theme: default
paginate: true
style: |
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;700;900&display=swap');

  :root {
    --color-bg: #0d1b2a;
    --color-bg-secondary: #1b2838;
    --color-accent-gold: #c9a84c;
    --color-accent-blue: #4a9eda;
    --color-text-primary: #f0f0f0;
    --color-text-muted: #b0bec5;
    --color-border: rgba(201, 168, 76, 0.4);
  }

  section {
    background: linear-gradient(160deg, #0d1b2a 0%, #1b2838 100%);
    color: var(--color-text-primary);
    font-family: 'Noto Sans KR', 'Malgun Gothic', 'Apple SD Gothic Neo', sans-serif;
    padding: 50px 70px;
  }

  section h1 {
    color: var(--color-accent-gold);
    font-weight: 900;
    letter-spacing: -0.5px;
  }

  section h2 {
    color: var(--color-accent-blue);
    font-weight: 700;
    border-bottom: 2px solid var(--color-border);
    padding-bottom: 10px;
    margin-bottom: 28px;
  }

  section h3 {
    color: var(--color-accent-gold);
    font-weight: 700;
    font-size: 0.9em;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 8px;
  }

  section ul {
    list-style: none;
    padding-left: 0;
  }

  section ul li::before {
    content: '▸ ';
    color: var(--color-accent-gold);
    font-weight: 700;
  }

  section li {
    margin-bottom: 8px;
    line-height: 1.6;
    color: var(--color-text-primary);
  }

  section strong {
    color: var(--color-accent-gold);
  }

  section em {
    color: var(--color-accent-blue);
    font-style: normal;
    font-weight: 600;
  }

  section table {
    border-collapse: collapse;
    width: 100%;
    margin-top: 16px;
  }

  section th {
    background: rgba(201, 168, 76, 0.2);
    color: var(--color-accent-gold);
    font-weight: 700;
    padding: 10px 16px;
    border: 1px solid var(--color-border);
    text-align: center;
  }

  section td {
    padding: 10px 16px;
    border: 1px solid rgba(255,255,255,0.1);
    color: var(--color-text-primary);
    font-size: 0.88em;
    line-height: 1.5;
  }

  section td:first-child {
    color: var(--color-accent-blue);
    font-weight: 700;
    background: rgba(74, 158, 218, 0.08);
  }

  section.title-slide {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    background: linear-gradient(160deg, #070e17 0%, #0d1b2a 60%, #1b2838 100%);
  }

  section.title-slide h1 {
    font-size: 2.1em;
    line-height: 1.3;
    margin-bottom: 16px;
  }

  section.title-slide .subtitle {
    color: var(--color-text-muted);
    font-size: 1em;
    border-left: 3px solid var(--color-accent-gold);
    padding-left: 16px;
    margin-top: 8px;
  }

  section.toc-slide ol {
    counter-reset: toc-counter;
    list-style: none;
    padding: 0;
  }

  section.toc-slide ol li {
    counter-increment: toc-counter;
    padding: 10px 0 10px 48px;
    position: relative;
    border-bottom: 1px solid rgba(255,255,255,0.07);
    font-size: 1.05em;
  }

  section.toc-slide ol li::before {
    content: '0' counter(toc-counter);
    position: absolute;
    left: 0;
    color: var(--color-accent-gold);
    font-weight: 900;
    font-size: 1em;
    width: 40px;
  }

  .card-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-top: 16px;
  }

  .card {
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--color-border);
    border-radius: 8px;
    padding: 18px 20px;
  }

  .card .card-title {
    color: var(--color-accent-gold);
    font-weight: 700;
    font-size: 0.85em;
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 10px;
    display: block;
  }

  .card ul li {
    font-size: 0.88em;
    margin-bottom: 5px;
  }

  .highlight-box {
    background: rgba(201, 168, 76, 0.1);
    border-left: 4px solid var(--color-accent-gold);
    border-radius: 0 6px 6px 0;
    padding: 14px 20px;
    margin-top: 14px;
    font-size: 0.92em;
    color: var(--color-text-primary);
  }

  .step-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-top: 16px;
  }

  .step-item {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 8px;
    padding: 16px 18px;
  }

  .step-item .step-label {
    background: var(--color-accent-gold);
    color: #0d1b2a;
    font-weight: 900;
    font-size: 0.75em;
    padding: 2px 10px;
    border-radius: 20px;
    display: inline-block;
    margin-bottom: 8px;
    letter-spacing: 0.5px;
  }

  .step-item .step-period {
    color: var(--color-accent-blue);
    font-size: 0.82em;
    margin-bottom: 8px;
    display: block;
  }

  .step-item ul li {
    font-size: 0.84em;
    margin-bottom: 4px;
  }

  footer {
    color: rgba(255,255,255,0.3) !important;
    font-size: 0.7em !important;
  }

  section::after {
    color: rgba(201, 168, 76, 0.5);
    font-size: 0.75em;
  }
---

<!-- _class: title-slide -->

# AI 기반 프리미엄<br>'나' 자서전<br>& 퍼스널 브랜딩

<div class="subtitle">평생학습을 위한 창업과 기업가 정신 | 6조 발표</div>

---
<!-- _class: toc-slide -->

## 목차

<ol>
  <li>사업 소개 및 목적</li>
  <li>시장 및 고객 분석</li>
  <li>경쟁 및 환경 분석</li>
  <li>비즈니스 모델 구성</li>
  <li>조직 및 운영 전략</li>
  <li>실행 계획 및 기대 효과</li>
</ol>

---

## 01 사업 소개 및 목적

### 핵심 타겟

- 대구 **수성구** 등 부촌 거주 **6075 고소득·고학력 시니어**
- 자녀 독립 후 자신의 삶을 정리하고 **영구적 기록**을 원하는 세대

### 서비스 구조

- 일대일 **전담 코치**와의 심층 대화를 통해 콘텐츠 수집
- *Invisible AI* (LLM, STT, 보이스 클로닝)가 백그라운드에서 작동
- 에이전시형 서비스 — **아바타 구축 & 프리미엄 자서전** 완성

<div class="highlight-box">
  <strong>핵심 목적:</strong> 첨단 AI 기술과 하이터치 인간 서비스를 융합하여<br>
  개인의 삶과 가치를 <strong>영구적인 디지털 유산</strong>으로 창조한다.
</div>

---

## 02 시장 및 고객 분석 — STP

| 구분 | 내용 |
|------|------|
| **Segmentation** | 대졸 이상 상위 10% 전문직 시니어 · 사회적 영향력 유지 욕구 · 프리미엄 소비 성향 보유층 |
| **Targeting** | 대구 수성구 거주 6075 세대<br>*서브 타겟:* 특별한 선물을 원하는 3040 고소득 자녀층 |
| **Positioning** | Invisible AI · Tangible Result · Human Touch |

<div class="highlight-box">
  "당신의 위대한 기록, AI로 완성하는 디지털 유산"
</div>

---

## 03 경쟁 및 환경 분석

<div class="card-grid">
  <div class="card">
    <span class="card-title">자사 핵심 강점 (3C - Company)</span>
    <ul>
      <li>최신 AI 기술 <strong>내재화</strong> 역량</li>
      <li>LLM · STT · 보이스 클로닝 파이프라인</li>
      <li>프리미엄 서비스 기반 <strong>압도적 마진율</strong></li>
      <li>1:1 밀착 케어로 타사 대비 차별화</li>
    </ul>
  </div>
  <div class="card">
    <span class="card-title">시장 환경 (PEST)</span>
    <ul>
      <li><em>액티브 시니어</em> 구매력 지속 상승</li>
      <li>웰 에이징 · 자아실현 소비 트렌드</li>
      <li>디지털 유산에 대한 사회적 관심 증대</li>
      <li>AI 생성 콘텐츠 산업의 급속 성장</li>
    </ul>
  </div>
</div>

---

## 04 SWOT 분석 및 전략

| | 기회 (O) | 위협 (T) |
|-|----------|----------|
| **강점 (S)** | **SO:** VIP 맞춤형 패키지 출시<br>디지털 유산 선도 브랜드 확립 | **ST:** 특허·저작권 기반 기술 진입장벽 구축 |
| **약점 (W)** | **WO:** PB센터·검진센터 제휴 마케팅<br>신뢰 채널 기반 추천제 운영 | **WT:** Human-Centric 브랜딩 강화<br>기술 거부감 해소용 오프라인 체험 제공 |

<div class="highlight-box">
  <strong>약점(W):</strong> 초기 인지도 부족 &nbsp;|&nbsp; <strong>기회(O):</strong> 디지털 유산 수요 급확대 &nbsp;|&nbsp; <strong>위협(T):</strong> 경쟁 심화 · 기술 거부감
</div>

---

## 05 비즈니스 모델 캔버스

<div class="card-grid">
  <div class="card">
    <span class="card-title">핵심 가치 제안</span>
    <ul>
      <li>디지털 유산의 <strong>영구적 보존</strong></li>
      <li>삶의 궤적을 통한 <strong>명예적 가치 증명</strong></li>
      <li>1:1 전담 밀착 코칭 서비스</li>
      <li>AI 기반 아바타 · 자서전 · 굿즈 패키지</li>
    </ul>
  </div>
  <div class="card">
    <span class="card-title">수익 구조</span>
    <ul>
      <li><em>고단가 패키지:</em> 자서전 + 아바타 풀패키지</li>
      <li><em>프리미엄 출판:</em> 한정 제본 자서전 및 굿즈</li>
      <li><em>SaaS 구독:</em> 디지털 아바타 보존 월정액</li>
      <li>법인·기관 대상 B2B 패키지 확장</li>
    </ul>
  </div>
</div>

---

## 06 조직 및 운영 전략 — 7S

<div class="card-grid">
  <div class="card">
    <span class="card-title">Structure (하드 요소)</span>
    <ul>
      <li>기술 부서 ↔ 크리에이티브 부서 <strong>유기적 결합</strong></li>
      <li>고객별 전담 <strong>TF(Task Force) 구조</strong></li>
      <li>프라이빗 클라우드 기반 <strong>데이터 보안</strong> 체계</li>
      <li>내부 권한 통제 및 접근 로그 관리</li>
    </ul>
  </div>
  <div class="card">
    <span class="card-title">Style & Staff (소프트 요소)</span>
    <ul>
      <li>디테일 중심 <strong>완벽주의</strong> 조직 문화</li>
      <li>AI 엔지니어 + 크리에이티브 코치 <em>협업 모델</em></li>
      <li>고객 신뢰 최우선 서비스 철학</li>
      <li>지속 학습 기반 역량 내재화</li>
    </ul>
  </div>
</div>

---

## 07 단계별 실행 계획

<div class="step-grid">
  <div class="step-item">
    <span class="step-label">STEP 1</span>
    <span class="step-period">1 ~ 3개월 · 기반 구축</span>
    <ul>
      <li>AI 파이프라인 최적화 완료</li>
      <li>크리에이티브 코치 선발 및 훈련</li>
      <li>서비스 프로토타입 구축</li>
    </ul>
  </div>
  <div class="step-item">
    <span class="step-label">STEP 2</span>
    <span class="step-period">4 ~ 6개월 · 시장 진입</span>
    <ul>
      <li>수성구 PB센터 · 대형 검진센터 제휴</li>
      <li>VIP 오프라인 설명회 개최</li>
      <li>소규모 파일럿 고객 유치</li>
    </ul>
  </div>
  <div class="step-item">
    <span class="step-label">STEP 3</span>
    <span class="step-period">7 ~ 12개월 · 본격 운영</span>
    <ul>
      <li>10차시 정식 프로그램 가동</li>
      <li>출판기념회 개최 및 PR 활용</li>
      <li>고객 레퍼런스 구축</li>
    </ul>
  </div>
  <div class="step-item">
    <span class="step-label">STEP 4</span>
    <span class="step-period">13개월~ · 확장</span>
    <ul>
      <li>SaaS 아바타 구독 모델 정식 도입</li>
      <li>인접 도시 (부산·서울) 확장</li>
      <li>B2B 법인 패키지 출시</li>
    </ul>
  </div>
</div>

---

## 08 리스크 대응 및 기대 효과

<div class="card-grid">
  <div class="card">
    <span class="card-title">리스크 대응 전략</span>
    <ul>
      <li><strong>개인정보 보안:</strong> 내부 권한 통제 · 암호화 저장 · 접근 로그 감사</li>
      <li><strong>타겟 모집 난이도:</strong> 신뢰 기반 추천제 (Referral) 운영, 기존 고객 네트워크 활용</li>
      <li><strong>기술 거부감:</strong> 오프라인 체험 중심 온보딩, AI 비가시화 전략 유지</li>
    </ul>
  </div>
  <div class="card">
    <span class="card-title">기대 효과</span>
    <ul>
      <li>고단가 + 구독 병행 <em>안정적 고수익</em> 달성</li>
      <li>은퇴 세대 자아실현 및 세대 간 소통 촉진</li>
      <li><strong>인생을 자산화하는</strong> 독보적 실버테크 브랜드 확립</li>
    </ul>
  </div>
</div>

<div class="highlight-box">
  AI 기술과 인간 감성의 융합으로 대한민국 액티브 시니어의<br>
  <strong>디지털 유산 산업을 개척하는 선도 기업</strong>으로 성장한다.
</div>
