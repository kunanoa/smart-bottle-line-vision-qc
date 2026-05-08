# 페트병 이미지 파일명 매핑표

채택 외 한글 이미지 15장의 영문 snake_case 파일명 매핑.

## 📋 매핑 표

### Station 1 PatchCore 결과 — 1회차 (2장)

| 영문 파일명 | 원본 한글명 | Score | 분류 |
|---|---|---:|---|
| `station1_round1_scratch.png` | 1차실험 - 스크래치.png | 0.6960 | 검출 성공 (NG) |
| `station1_round1_detected_white_paper.png` | 1차실험 - 하얀종이뭉치NG.png | 0.5091 | 검출 성공 (NG) |

### Station 1 PatchCore 결과 — 2회차 (4장)

| 영문 파일명 | 원본 한글명 | Score | 분류 |
|---|---|---:|---|
| `station1_round2_normal.png` | 2차실험 - 정상패턴.png | 0.2928 | 정상 (OK) |
| `station1_round2_boardmarker.png` | 2차실험 - 보드마카.png | 0.6935 | 검출 성공 (NG) |
| `station1_round2_detected_scratch.png` | 2차실험 - 스크래치NG.png | 0.5099 | 검출 성공 (NG) |
| `station1_round2_colored_paper.png` | 2차실험 - 유색종이뭉치.png | 0.6264 | 검출 성공 (NG) |

### 데이터 raw 이미지 — 1회차 (4장)

| 영문 파일명 | 원본 한글명 | 내용 |
|---|---|---|
| `raw_round1_incoming_boardmarker.png` | 1차실험 - 입고단계 - 보드마카.png | 빈 페트병 + 보드마카 표시 |
| `raw_round1_incoming_pairi.png` | 1차실험 - 입고단계 - 파이리출현.png | 빈 페트병 + 파이리 인형 (sanity check) |
| `raw_round1_assembly_cap_tilted.png` | 1차실험 - 조립후단계 - 캡기울어짐.png | 완제품 + 캡 NG |
| `raw_round1_assembly_pairi.png` | 1차실험 - 조립후단계 - 파이리출현.png | 완제품 + 파이리 인형 |

### 환경 셋업 사진 (4장)

| 영문 파일명 | 원본 한글명 | 비고 |
|---|---|---|
| `setup_round1.png` | 1차실험 - 촬영 환경.png | 1회차 셋업 |
| `setup_round2_alt1.png` | 2차실험 - 촬영 환경1.png | 2회차 셋업 (대안 앵글) |
| `setup_round2_alt2.png` | 2차실험 - 촬영 환경2.png | 2회차 셋업 (대안 앵글) |
| `setup_round2_alt3.png` | 2차실험 - 촬영 환경3.png | 2회차 셋업 (대안 앵글) |

### GUI 캡처 — 채택본 (1장, 한글본 영문화)

| 영문 파일명 | 원본 한글명 | 비고 |
|---|---|---|
| `gui_station2_label_misalign.png` | 객체탐지(yolo.v11) 모델 사용.png | README 채택 — 한글본 보관용으로 함께 제공 |

---

## 📁 네이밍 컨벤션

향후 같은 프로젝트의 새 이미지 추가 시 일관성 유지용:

| 접두어 | 용도 | 예시 |
|---|---|---|
| `gui_` | 통합 GUI 캡처 | `gui_station1_main.png` |
| `station1_round1_*` | Station 1 PatchCore 출력 — 1회차 | `station1_round1_normal.png` |
| `station1_round2_*` | Station 1 PatchCore 출력 — 2회차 | `station1_round2_normal.png` |
| `raw_round1_*` / `raw_round2_*` | 카메라 raw 이미지 (UI 없음) | `raw_round1_incoming_boardmarker.png` |
| `setup_*` | 환경 셋업 사진 | `setup_round1.png`, `setup_round2.png` |
| `data_sample_*` | 데이터 샘플 (대표 이미지) | `data_sample_incoming.png` |

### 상태 표시 단어 (검출 결과)

| 단어 | 의미 |
|---|---|
| `detected_` | 결함 검출 성공 (NG 판정) |
| `missed_` | 결함 미검 (OK 오판) |
| `normal` | 정상 페트병 |

---

## 💡 향후 활용 시나리오

이 15장은 README에는 안 들어갔지만 다음 용도로 쓸 수 있습니다:

1. **자기소개서 보강 자료** — 1회차 검출 성공 사례(`station1_round1_scratch`)는 "1회차에도 다른 결함은 잘 검출됐다"는 근거로 활용 가능
2. **기술블로그 포스트** — raw 이미지 4장으로 "데이터 파이프라인" 글 작성
3. **발표 자료** — 환경 셋업 4장 비교로 "1회차 vs 2회차 환경 변화" 비주얼 시퀀스 구성
4. **면접 라이브 시연 자료** — `station1_round2_colored_paper.png`로 "유색 이물질도 잘 잡혔다" 정성 답변 보강
