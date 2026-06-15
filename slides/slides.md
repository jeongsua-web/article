---
marp: true
paginate: true
size: 16:9
header: 'articleBuddy'
style: |
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css');

  section {
    font-family: 'Inter', 'Apple SD Gothic Neo', system-ui, sans-serif;
    background: #ffffff;
    color: #0f172a;
    font-size: 23px;
    padding: 56px 68px;
    letter-spacing: -0.01em;
  }
  header { color: #94a3b8; font-size: 13px; font-weight: 600; }
  section::after { color: #94a3b8; font-weight: 600; }

  h1 { font-weight: 900; letter-spacing: -0.03em; color: #0f172a; }
  h2 { font-weight: 900; font-size: 38px; color: #0f172a; margin: 0 0 4px; }
  strong { color: #0f172a; }
  code { background: #f1f5f9; color: #1e293b; padding: 1px 7px; border-radius: 6px; font-size: 0.85em; }
  a { color: #2563eb; }

  /* eyebrow + lead */
  .eyebrow { font-size: 13px; font-weight: 800; text-transform: uppercase; letter-spacing: 0.18em; color: #94a3b8; margin: 0 0 8px; }
  .lead { color: #64748b; font-size: 20px; font-weight: 500; }
  .muted { color: #94a3b8; font-size: 16px; }

  /* layout */
  .cols { display: grid; grid-template-columns: 1fr 1fr; gap: 28px; margin-top: 18px; }
  .cards4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 26px; }
  .grid5 { display: grid; grid-template-columns: repeat(5, 1fr); gap: 14px; margin-top: 24px; }

  /* card */
  .card { background: #fff; border: 1px solid #e2e8f0; border-radius: 22px; padding: 24px 26px; box-shadow: 0 1px 2px rgba(15,23,42,.04); }
  .card-c { text-align: center; padding: 22px 14px; }
  .ct { font-weight: 800; font-size: 19px; margin-top: 10px; }
  .cs { color: #64748b; font-size: 15px; margin-top: 4px; }
  .logos { display: flex; align-items: center; justify-content: center; gap: 12px; height: 46px; }
  .logo { height: 40px; width: auto; }

  /* icon chip */
  .chip { width: 42px; height: 42px; border-radius: 13px; display: inline-flex; align-items: center; justify-content: center; font-size: 17px; }
  .c-blue   { background: #eff6ff; color: #3b82f6; }
  .c-indigo { background: #eef2ff; color: #6366f1; }
  .c-violet { background: #f5f3ff; color: #8b5cf6; }
  .c-emerald{ background: #ecfdf5; color: #10b981; }
  .c-rose   { background: #fff1f2; color: #f43f5e; }
  .c-amber  { background: #fffbeb; color: #f59e0b; }
  .chead { display: flex; align-items: center; gap: 12px; margin-bottom: 14px; }
  .chead .t { font-weight: 800; font-size: 20px; }

  /* pills / tags */
  .pill { display: inline-block; font-size: 14px; font-weight: 700; padding: 3px 11px; border-radius: 999px; background: #eff6ff; color: #2563eb; border: 1px solid #dbeafe; }
  .pill-gray { background: #f1f5f9; color: #475569; border-color: #e2e8f0; }
  .pill-amber{ background: #fffbeb; color: #b45309; border-color: #fde68a; }

  ul { line-height: 1.55; }
  table { font-size: 19px; border-collapse: collapse; }
  th, td { border: 1px solid #e2e8f0; padding: 7px 12px; }
  th { background: #f8fafc; color: #475569; }

  /* ADR cards */
  .adr { display: block; border: 1px solid #e2e8f0; border-radius: 14px; padding: 13px 14px; text-decoration: none; color: inherit; transition: border-color .15s, box-shadow .15s, transform .15s; }
  a.adr:hover { border-color: #93c5fd; box-shadow: 0 4px 14px rgba(37,99,235,.12); transform: translateY(-2px); }
  .adr .n { font-size: 13px; color: #94a3b8; font-weight: 700; }
  .adr .t { font-weight: 800; font-size: 17px; margin-top: 5px; }
  .adr .s { color: #64748b; font-size: 14px; margin-top: 4px; }

  /* deep-dive ADR cards (3선) */
  .adr3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 22px; margin-top: 26px; }
  .adrx { display: flex; flex-direction: column; border: 1px solid #e2e8f0; border-radius: 20px; padding: 24px 24px 20px; text-decoration: none; color: inherit; transition: border-color .15s, box-shadow .15s, transform .15s; }
  a.adrx:hover { border-color: #93c5fd; box-shadow: 0 8px 24px rgba(37,99,235,.14); transform: translateY(-3px); }
  .adrx .n { display: inline-block; align-self: flex-start; font-size: 15px; font-weight: 800; color: #2563eb; background: #eff6ff; border: 1px solid #dbeafe; padding: 4px 12px; border-radius: 999px; margin: 0 0 12px; }
  .adrx .t { font-weight: 900; font-size: 26px; line-height: 1.2; }
  .adrx .d { color: #475569; font-size: 19px; margin-top: 12px; line-height: 1.55; flex: 1; }
  .adrx .go { font-size: 18px; font-weight: 700; color: #2563eb; margin-top: 18px; }

  /* cover */
  section.cover { background: #ffffff; align-items: center; justify-content: center; text-align: center; }
  section.cover h1 { font-size: 84px; line-height: 1; margin: 18px 0 22px; }
  .brand-a { color: #0f172a; }
  .brand-b { color: #2563eb; }
  .badge { display: inline-flex; align-items: center; gap: 8px; font-size: 14px; font-weight: 700; color: #1d4ed8; background: #eff6ff; border: 1px solid #dbeafe; padding: 6px 14px; border-radius: 999px; }
  .badge .dot { width: 7px; height: 7px; background: #3b82f6; border-radius: 999px; }
  .tags { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; margin-top: 30px; }
  .tag { font-size: 14px; font-weight: 600; color: #475569; background: #f1f5f9; padding: 6px 14px; border-radius: 999px; }
  .tag i { color: #94a3b8; margin-right: 6px; }

  /* full-bleed WBS tree */
  section.wbs { padding: 0; overflow: hidden; }
  .wbs-frame { width: 100%; height: 100%; border: 0; display: block; }

  /* full-bleed demo video */
  section.video { padding: 0; overflow: hidden; background: #0f172a; align-items: center; justify-content: center; }
  .demo-video { max-width: 100%; max-height: 100%; display: block; }
---

<!-- _class: cover -->
<!-- _paginate: false -->
<!-- _header: '' -->

<div class="badge"><span class="dot"></span> 최종 발표 · 2026</div>

# <span class="brand-a">article</span><span class="brand-b">Buddy</span>

<p class="lead">내가 가져온 영어 기사를 AI와 함께 읽는 학습 앱</p>

<div class="tags">
<span class="tag"><i class="fa-solid fa-mobile-screen"></i>React Native</span>
<span class="tag"><i class="fa-solid fa-cloud"></i>Supabase</span>
<span class="tag"><i class="fa-solid fa-robot"></i>AI 통합</span>
<span class="tag"><i class="fa-solid fa-users"></i>소셜 학습</span>
</div>

---

<p class="eyebrow">Problem &amp; Vision</p>

## 비전 & 문제 정의

<div class="cols">
<div class="card">
<div class="chead"><span class="chip c-rose"><i class="fa-solid fa-circle-exclamation"></i></span><span class="t">문제 정의</span></div>

- 기사 읽기 → 사전 앱 전환 → 단어 복사 → 노트 저장 → **잊어버림**
- 기사가 **내 수준에 맞는지** 모르고 시작
- 혼자 공부하면 며칠 빠져도 아무도 모름 → 동기 소실
- 모르는 부분을 물어볼 곳이 없음

</div>
<div class="card">
<div class="chead"><span class="chip c-blue"><i class="fa-solid fa-rocket"></i></span><span class="t">비전</span></div>

> 기사를 가져오면, AI가 옆에서 도와주고, 친구와 함께 꾸준히 이어간다

읽기 → AI 질문 → 단어 저장 → 복습 → 출석의 **학습 루프가 앱 안에서 완결**된다.

</div>
</div>

---

<!-- _class: wbs -->
<!-- _header: '' -->
<!-- _paginate: false -->

<iframe class="wbs-frame" src="wbs_tree_ppt.html" scrolling="no"></iframe>

---

<p class="eyebrow">Tech Stack</p>

## 기술 스택

<div class="cards4">
<div class="card card-c">
<div class="logos"><img class="logo" src="https://cdn.simpleicons.org/expo/000020" alt="Expo" /><img class="logo" src="https://cdn.simpleicons.org/react/61DAFB" alt="React" /></div>
<div class="ct">클라이언트</div><div class="cs">Expo · React Native</div></div>
<div class="card card-c">
<div class="logos"><img class="logo" src="https://cdn.simpleicons.org/supabase/3FCF8E" alt="Supabase" /></div>
<div class="ct">백엔드</div><div class="cs">Supabase (BaaS)</div></div>
<div class="card card-c">
<div class="logos"><img class="logo" src="https://cdn.simpleicons.org/postgresql/4169E1" alt="PostgreSQL" /></div>
<div class="ct">데이터베이스</div><div class="cs">PostgreSQL · RLS</div></div>
<div class="card card-c">
<div class="logos"><img class="logo" src="https://cdn.simpleicons.org/googlegemini/8E75B2" alt="Gemini" /></div>
<div class="ct">AI / 외부 API</div><div class="cs">Gemini · Dict · MyMemory</div></div>
</div>

<br>

- <span class="pill pill-gray">무료 정책</span> 유료 계정·API 미사용, 오픈소스·무료 티어만 채택
- <span class="pill">AI는 요약·번역에만</span> 난이도 판정은 로컬 CEFR 알고리즘으로 비용 Zero

---

<p class="eyebrow">System Architecture</p>

## 시스템 구성도

<div class="mermaid">
flowchart LR
  U([사용자]) --> APP[Expo · React Native]
  subgraph SB[Supabase BaaS]
    direction TB
    AUTH[Auth · Google OAuth]
    EF[Edge Functions<br/>parse-article · ask-ai]
    DB[(PostgreSQL<br/>users · articles · words<br/>attendance · friends)]
    AUTH --> EF --> DB
  end
  APP -->|REST / OAuth / Realtime| SB
  EF -->|AI 요청| GEM[Gemini 2.5 Flash]
  APP -.단어 조회.-> DICT[Dictionary · MyMemory]
</div>

<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true, theme: 'neutral', themeVariables: { fontFamily: 'Inter, system-ui, sans-serif', primaryColor: '#eff6ff', primaryBorderColor: '#93c5fd', lineColor: '#94a3b8' } });
</script>

---

<p class="eyebrow">Core Logic</p>

## 핵심 로직 — AI 리포트 스트리밍 파싱

<p class="muted">도착하는 대로 점진 표시해 체감 속도 향상 · <code>ask-ai/index.ts</code></p>

<div class="cols">
<div>

**1. 고정 마커 포맷 강제**
- `##SUMMARY##`, `##P1## KEY:/TRANS:` 형식으로만 응답

**2. 점진 추출**
- SSE 스트림에서 다음 마커 등장 = 블록 완료
- 완성된 블록만 클라이언트로 전달

**3. 마지막 블록**
- 스트림 종료 시 종결 마커 없이도 처리

</div>
<div class="card">
<div class="chead"><span class="chip c-emerald"><i class="fa-solid fa-shield-halved"></i></span><span class="t">견고성 장치</span></div>

- 503 오류 시 지수 백오프 재시도 3회
- `thinkingBudget: 0` — thinking 토큰이 마커 파싱을 깨지 않도록
- 깨진 JSON 청크 무시 · 최대 15문단 제한
- 모델 교체는 `GEMINI_MODEL` 환경변수 한 줄

</div>
</div>

---

<p class="eyebrow">Lessons Learned</p>

## 시행착오

<div class="cols">
<div>

**① 번역 품질 vs 속도**
- MyMemory(품질↓) → Lingva 교체(품질↑)
- 공개 인스턴스 응답 **1~5초**로 불안정 <span class="muted">(실측 3.2s·전부 실패)</span>
- → **MyMemory 복귀** <span class="muted">(실측 1.2s·전부 성공 · ADR-0005→0006)</span>

**② 난이도 판정을 AI로?**
- 이중 AI(난이도=Claude) 계획
- 무료 한도·비용·지연 부담
- → **로컬 CEFR 알고리즘** <span class="muted">(ADR-0003→0007)</span>

**③ Gemini 모델 잔혹사**
- 1.5 지원 종료 → 2.0 무료 티어 0(429)
- → **2.5-flash 안착 + 모델 ID 환경변수화** <span class="muted">(ADR-0009)</span>

</div>
<div class="card">
<div class="chead"><span class="chip c-amber"><i class="fa-solid fa-lightbulb"></i></span><span class="t">얻은 교훈</span></div>

- 가용성이 품질을 이긴다 — *전용 인프라 > 좋은 공개 인스턴스*
- AI를 **쓸 곳과 안 쓸 곳**을 나눈다 — 난이도는 결정론적 알고리즘이 적합
- 벤더 종속은 **모델 ID 한 줄**로 격리

</div>
</div>

---

<p class="eyebrow">Architecture Decision Records</p>

## 핵심 의사결정 3선

<p class="muted">카드를 누르면 해당 ADR 상세로 이동합니다</p>

<div class="adr3">
<a class="adrx" href="../pages/decisions.html?adr=4">
<span class="n">ADR-0004</span>
<span class="t">기사 파싱 — Edge Function</span>
<span class="d">CORS·본문 추출·페이월·<strong>SSRF</strong> 네 가지 제약을 서버측 파싱으로 한 번에 해결. 클라이언트 직접 fetch의 한계를 우회.</span>
<span class="go">ADR 보기 →</span>
</a>
<a class="adrx" href="../pages/decisions.html?adr=7">
<span class="n">ADR-0007</span>
<span class="t">난이도 — CEFR 어휘 기반</span>
<span class="d">단어 길이 휴리스틱은 <code>apt·wry</code>(짧지만 어려움)를 오판. MIT 라이선스 오픈 어휘목록으로 전환해 비용 Zero·정확도↑.</span>
<span class="go">ADR 보기 →</span>
</a>
<a class="adrx" href="../pages/decisions.html?adr=10">
<span class="n">ADR-0010</span>
<span class="t">무료 실기기 배포</span>
<span class="d">Debug+Metro는 <strong>로컬 네트워크 차단</strong>으로 앱이 안 켜짐. Release 케이블 설치로 통일해 $99 없이 안정 배포.</span>
<span class="go">ADR 보기 →</span>
</a>
</div>

---

<p class="eyebrow">What's Next</p>

## 확장 가능성

<div class="cols">
<div class="card">
<div class="chead"><span class="chip c-blue"><i class="fa-solid fa-graduation-cap"></i></span><span class="t">학습 고도화</span></div>

- 복습 로직을 간격 반복(SRS, SM-2)으로 전환
- CEFR 임계값 서버/클라이언트 공유 상수화
- 추출 실패 사이트군 대체 파싱 전략

<div class="chead" style="margin-top:18px;"><span class="chip c-emerald"><i class="fa-solid fa-coins"></i></span><span class="t">수익 모델</span></div>

- 서비스 운영을 위한 프리미엄 구독 모델 도입
- 구독자 대상 AI 관련 기능 확장

</div>
<div class="card">
<div class="chead"><span class="chip c-violet"><i class="fa-solid fa-users"></i></span><span class="t">소셜 & 동기</span></div>

- 친구 그룹·챌린지, 시즌 랭킹
- 학습 통계 대시보드

<div class="chead" style="margin-top:18px;"><span class="chip c-amber"><i class="fa-solid fa-arrows-left-right-to-line"></i></span><span class="t">플랫폼</span></div>

- 웹 버전(Expo Web) 확장
- 다국어 학습(영어 외 언어) 지원

</div>
</div>

---

<!-- _class: video -->
<!-- _header: '' -->
<!-- _paginate: false -->

<video class="demo-video" src="Demo.mp4" controls playsinline preload="metadata"></video>
