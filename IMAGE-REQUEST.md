# InBody 프레젠테이션 — 이미지 생성 요청서

## 프로젝트 배경

InBody(인바디) 회사 소개 프레젠테이션. 대학교 의공학과 학생 대상 발표용.
풀스크린 시네마틱 웹 프레젠테이션 (HTML). 발표자는 차인준 (InBody India CEO).

**디자인 톤:** 밝은 웜톤 배경(#f2f0eb), 브랜드 레드(#ac0430), 골드(#a67a00), 블루(#005b9e). 깔끔하고 전문적인 의료기기 회사 느낌.

---

## 필요한 이미지 목록

### 1. 부종(Edema) 사진
- **파일명:** `assets/images/edema-pitting.jpg`
- **용도:** S7b 슬라이드 — "우리 몸의 50-70%는 물입니다" 페이지 왼쪽에 들어가는 의학 사진
- **사이즈:** 세로형 (3:4 비율), 최소 800x1000px
- **프롬프트:**

> A clinical medical photograph showing pitting edema on a patient's lower leg and ankle area. A doctor's finger is pressing into the swollen shin, creating a clearly visible indentation (pit) in the skin. The surrounding skin appears slightly shiny, taut, and swollen compared to normal. Shot in professional medical textbook photography style with soft, neutral lighting on a clean white/light gray medical examination background. No text, watermarks, or UI elements. Portrait orientation. Photorealistic, high resolution.

---

### 2. 5-실린더 바디 모델 (이건 코드로 SVG 만들어놨으니 선택사항)
- **파일명:** 필요시 `assets/images/5cylinder-body.png`
- **용도:** S5b 슬라이드 — InBody가 인체를 5개 실린더로 모델링해서 부위별 측정한다는 개념 설명
- **현재 상태:** SVG로 이미 구현함. 더 세련된 3D 느낌 원하면 생성.
- **프롬프트 (선택):**

> A clean technical diagram showing the human body modeled as 5 separate cylinders. The body is standing upright with arms slightly away from the torso. Each body segment is represented as a distinct colored cylinder: Right Arm (gold/amber), Left Arm (gold/amber), Trunk/Torso (red), Right Leg (blue), Left Leg (blue). Each cylinder is labeled with its abbreviation: RA, LA, TR, RL, LL. The head is shown as a simple gray circle on top (not a cylinder). Small electrode dots are visible on hands and feet (4 pairs = 8 points total). Clean white background, technical/medical illustration style, no shadows, flat design with subtle 3D depth. Landscape orientation, 800x600px.

---

### 3. 공장 사진 6장 (실제 InBody 천안 공장 사진이 가장 좋음)

**참고:** 이 사진들은 실제 InBody 공장 모습이어야 설득력이 있습니다. 회사 내부 자료(홈페이지, 브로셔, 사내 공유 폴더)에서 가져오는 것을 권장합니다. AI 생성은 차선책입니다.

AI로 생성할 경우 아래 프롬프트 사용:

#### 3-1. 공장 외관/항공
- **파일명:** `assets/images/factory-aerial.jpg`
- **프롬프트:**

> Aerial photograph of a modern medical device manufacturing facility in South Korea. A large, clean white industrial building complex with the company logo on the side, surrounded by well-maintained grounds and parking lots. Clear sky, professional corporate photography. Landscape, 800x500px.

#### 3-2. 물류 창고
- **파일명:** `assets/images/factory-warehouse.jpg`
- **프롬프트:**

> Interior of a modern, well-organized warehouse for medical device products. Neatly stacked boxes on industrial shelving racks, clean concrete floors, bright LED lighting. Workers in uniforms operating forklifts. Professional industrial photography. Landscape, 800x500px.

#### 3-3. 생산 전문가 명패
- **파일명:** `assets/images/factory-nametag.jpg`
- **프롬프트:**

> Close-up of a professional name plate/badge on a medical device assembly workstation. The nameplate is metallic/acrylic showing the assembler's name in Korean characters, attached to a clean white production desk. Shallow depth of field, warm lighting, professional photography. Landscape, 800x500px.

#### 3-4. 셀 방식 생산 라인
- **파일명:** `assets/images/factory-production.jpg`
- **프롬프트:**

> A skilled technician in a clean white uniform and gloves carefully assembling a body composition analyzer medical device at an individual workstation (cell production method). The workstation has organized tools, components, and a monitor. Clean, bright factory environment. Professional industrial photography. Landscape, 800x500px.

#### 3-5. 테스트 실험실
- **파일명:** `assets/images/factory-testlab.jpg`
- **프롬프트:**

> Interior of a quality testing laboratory for medical devices. Testing equipment, oscilloscopes, and precision instruments on clean benches. A body composition analyzer device is connected to testing equipment. Bright fluorescent lighting, organized lab environment. Professional photography. Landscape, 800x500px.

#### 3-6. 내구성 테스트
- **파일명:** `assets/images/factory-testing.jpg`
- **프롬프트:**

> A durability/reliability testing machine repeatedly pressing buttons or applying mechanical stress to a medical device component. The testing machine has a digital counter showing a high number (50,000+). Close-up shot showing the mechanical testing in progress. Professional industrial photography. Landscape, 800x500px.

---

## 이미지 저장 위치

모든 이미지는 프로젝트 폴더 내 `assets/images/` 경로에 저장하면 됩니다.
HTML 코드에서 이미 해당 경로로 참조하고 있어서, 파일만 넣으면 자동으로 표시됩니다.

## 현재 코드 상태

- **부종 사진** → `edema-pitting.jpg` 없으면 "부종 사진 추가 필요" 텍스트 자동 표시 (fallback 처리됨)
- **공장 사진** → 현재 사진 없이 텍스트 카드(ISO / Cell / 50K)로 대체해놨음. 사진 준비되면 다시 사진 레이아웃으로 변경 가능.
