# Design System — InBody Presentation

## Product Context
- **What this is:** 대학교 생물학과 대상 InBody 소개 프레젠테이션 (풀스크린 웹)
- **Who it's for:** 생물학과 대학생 (1~4학년 혼합), 프로젝터 발표
- **Space/industry:** 의료기기, 체성분 분석
- **Project type:** Cinematic web presentation (dark mode, snap scroll)

## Aesthetic Direction
- **Direction:** Luxury/Refined
- **Decoration level:** Intentional (subtle grain texture, radial glows, light particles)
- **Mood:** 의료기기의 정밀함과 글로벌 기업의 신뢰감. 차분하지만 인상적.
- **Reference:** InBody 공식 사이트 (inbody.com) — 클린한 의료기기 톤을 다크모드로 재해석

## Typography
- **Display/Hero:** Instrument Serif (400/400i) — 세련된 세리프, 감성적 타이틀에 사용
- **Body:** Pretendard (300/400/600/700) — 한국어 최적화 산세리프, 현대적이고 깔끔
- **UI/Labels:** Geist Mono (400/700) — 데이터, 라벨, 숫자 표시
- **Code:** Geist Mono
- **Loading:** Pretendard CDN (cdn.jsdelivr.net/gh/orioncactus/pretendard), Google Fonts (Instrument Serif, Geist Mono)
- **Scale:** h1: clamp(2.2rem, 5vw, 4rem), h2: clamp(1.5rem, 3.5vw, 2.8rem), h3: clamp(1.1rem, 2vw, 1.5rem), body: clamp(0.9rem, 1.5vw, 1.15rem), small: clamp(0.75rem, 1vw, 0.9rem)

## Color
- **Approach:** Restrained
- **Primary (Brand):** #ac0430 — InBody 시그니처 딥 크림슨. 강조, 악센트에만 사용
- **Secondary (Gold):** #e8b73a — 성과, 수치 강조, 하이라이트
- **Tertiary (Blue):** #005b9e — 데이터, 수분 관련 시각 요소
- **Neutrals:**
  - Background: #0c1017 (가장 어두운)
  - Surface: #131921
  - Card: #1a2130
  - Border: rgba(255,255,255,0.06)
  - Text Primary: #e4e6ea
  - Text Secondary: #8a8f9a
  - Text Dim: #4a5060
- **Dark mode:** 노이즈 텍스처 오버레이로 플랫함 방지. 배경 그라데이션은 방사형(radial), 슬라이드별 분위기에 맞게.

## Spacing
- **Base unit:** 8px
- **Density:** Comfortable (프레젠테이션은 여백이 핵심)
- **Scale:** 2xs(4) xs(8) sm(16) md(24) lg(32) xl(48) 2xl(64) 3xl(96)

## Layout
- **Approach:** Presentation-specific (fullscreen snap scroll)
- **Grid:** Content centered, max-width 1100px
- **Border radius:** sm:6px, md:10px, lg:16px

## Motion
- **Approach:** Intentional
- **Easing:** enter(cubic-bezier(0.22, 1, 0.36, 1)) exit(ease-in) move(ease-in-out)
- **Duration:** micro(100ms) short(200ms) medium(500ms) long(800ms)
- **Patterns:** fadeUp on enter (opacity + translateY), stagger 150ms between elements, SVG stroke animations for diagrams

## Decisions Log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-04-01 | Initial design system | Created by /design-consultation. Luxury/Refined aesthetic for medical device presentation |
| 2026-04-01 | Pretendard over Noto Sans KR | More modern, UI-optimized, better weight distribution |
| 2026-04-01 | Instrument Serif over Libre Baskerville | More refined, pairs better with Korean body text |
| 2026-04-01 | Noise texture backgrounds | Eliminates flat-dark-screen AI slop look |
