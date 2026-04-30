# InBody Presentation Project

InBody 대학교 의공학과 발표용 풀스크린 시네마틱 웹 프레젠테이션.
발표자: 차인준 (InBody India CEO / 영업그룹 부사장)

## 절대 규칙 (반드시 지킬 것)

### 이미지
- **SVG로 인체 일러스트 절대 금지.** 손, 발, 몸, 다리 등 사실적 인체 SVG는 항상 결과가 나쁨. 대신: (1) 실제 사진, (2) 기하학적 다이어그램(실린더/박스), (3) 텍스트+데이터 인포그래픽.
- 대화에 붙여넣은 이미지는 파일 시스템에 저장되지 않음 (Cowork 한계). **한 번만** 안내: "assets/images/ 폴더에 직접 저장해 주세요." 반복 설명 금지.
- 이미지 참조 시 파일이 실제 존재하는지 `assets/images/` 확인 후 사용할 것. 없는 파일 참조하면 깨짐.

### QR 코드
- **QR 코드 링크:** `https://kenccha.github.io/inbody-presentation/info.html`
- QR SVG 파일: `assets/qr-info.svg`
- HTML의 `<a href=` 태그도 반드시 같은 URL로 설정. 리멤버(rmbr.in) 링크 아님.
- QR 재생성 시 Python qrcode 라이브러리 사용, fill_color=#1a1a2e, back_color=#f7f5f0

### 레이아웃
- 모든 슬라이드는 `100vh` 풀스크린, `overflow:hidden` → 컨텐츠 높이 초과하면 잘림. 수정 후 반드시 높이 확인.
- 마진/갭 조정 시 `clamp()` 사용. 하드코딩 px 금지.
- 수정 요청 받으면 해당 슬라이드 HTML을 먼저 Read로 확인한 후 수정.

## 프레젠테이션 구조

- 단일 파일 HTML (`index.html`), CSS 변수 테마
- 6개 섹션 네비게이션: 시작/호기심/발견/인도/도전/마무리
- 폰트: Pretendard Variable(한글), JetBrains Mono(코드), Instrument Serif(장식)
- Canvas + HTML 하이브리드 애니메이션 (BIA 원리 S5, 세포막)
- 브랜드 컬러: --brand #ac0430, --gold #a67a00, --blue #005b9e
- 배경: --dark-bg #f2f0eb (밝은 웜톤)

## 주요 슬라이드 참고

- **S1b (data-slide="1b"):** 같은 체중 다른 체성분 — 3체형 SVG + 근육/체지방 바
- **S5 (data-slide="5"):** BIA 원리 — Canvas 파티클 애니메이션 (근육 vs 지방)
- **S5b (data-slide="5b"):** 8점 전극 — 기기사진 + 5-실린더 SVG 다이어그램 + 부위 리스트 (3단)
- **S7b (data-slide="7b"):** 부종 — 부종 사진 + 설명 + ECW/TBW 게이지 (3단)
- **S8 (data-slide="8"):** Phase Angle — 공식 θ=arctan(Xc/R)×180/π + 임상 의의
- **factory-detail:** 공장 — factory.jpg 파노라마 + ISO/Cell/0.23% 카드
- **S16 (data-slide="16"):** 세계 지도 — 유럽 라벨 겹침 주의 (방향 분산 필요)
- **S21 (data-slide="21"):** QR + 연락처 — 링크는 info.html

## 에셋 파일

- `assets/images/factory.jpg` — 천안 공장 파노라마 (1200x350)
- `assets/images/edema-pitting.jpg` — 부종 사진 (MedlinePlus 공공 이미지)
- `assets/images/inbody-970s.png` — InBody 970 기기 사진
- `assets/images/cell-membrane.png` — 세포막 배경 이미지
- `assets/qr-info.svg` — info.html QR 코드
- `assets/world-map-dots.svg` — 세계 지도

## 과거 실수 (반복 금지)

1. QR 코드 SVG는 재생성했는데 HTML `<a href>`는 안 고침 → 항상 둘 다 확인
2. 존재하지 않는 이미지 파일명을 HTML에 참조 → 깨진 이미지 표시됨
3. SVG로 손/발/몸 그림 → 사용자가 "최악"이라고 평가. 절대 반복 금지
4. 슬라이드 컨텐츠가 100vh 넘어서 잘림 → 수정 후 높이 검증 필수
5. 유럽 지도 라벨 겹침 → 라벨 방향(top/bottom/left/right)을 분산해야 함
6. Revenue chart 바 높이가 타이틀과 겹침 → 차트 높이 80% 제한
7. "부종 실제 사진 넣어라" 여러 번 요청했는데 안 넣음 → 사용자 요청은 한 번에 반영
