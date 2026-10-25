# PS NOVA 한국어 번역 소스

이 프로젝트는 [Arks-Layer/PSNovaTranslations](https://github.com/Arks-Layer/PSNovaTranslations)의 포크입니다. 원본 이력과 자료는 유지하고 한국어 작업은 `KO` 브랜치에서 진행합니다.

## Git에서 관리하는 것

- `rmd/*.json`: 일본어 원문과 한국어 번역. 초기 이관 대상49개, 24,553항목입니다.
- `csv/NpcBaseParameter.json`: NPC 이름의 텍스트 편집용 JSON입니다. 같은 폴더의 upstream CSV와 구분합니다.
- 번역 JSON은 이 Git 저장소가 현재 기준입니다. 예전 NAS/로컬 사본을 통째로 덮어쓰지 않습니다.

각 항목의 ID, `OriginalText`, `Enabled`는 기존 값을 보존하고 번역 수정은 `Text`에만 합니다. 태그, 변수와 줄바꿈을 유지합니다. `Enabled`는 적용 여부이며 의미 검수 완료 표시는 아닙니다.

초기 소스는 사용자가 선택한 Ubuntu 최근 검수본입니다. 처음 NAS와 차이가 있던 튜토리얼 파일도 이 버전을 사용합니다. 준비 중 NAS 사본이 갱신될 수 있으므로 실제 이관 시점의 비교와 초기 해시는 기술 보관소의 이관 기록으로 구분합니다. 기존 기술/검수 이력은 그대로 보존합니다.

## NAS에서 관리하는 것

공통 용어집은 NAS의 `PSO2/Glossary` 하나입니다. 기본 작품은 NOVA이며 같은 개체/기능과 문맥인지 확인합니다. NOVA 고유어와 협업 예외를 유지하고 부분 문자열로 일괄 치환하지 않습니다.

기술 분석, 글꼴/아틀라스, 이미지/영상, 실행파일 수정, CPK/RMD 빌드 자료, 검수 근거/보류/진척 기록은 NAS의 `PSNova_Shared`에서 관리합니다. 실제 처리와 빌드는 로컬 작업본에서 하고, 완료한 결과를 충돌 확인 후 NAS에 업로드합니다.

이 포크가 이미 갖고 있던 upstream 이미지/참고 자료는 원본 이력으로 보존합니다. 새 한글 기술 자료는 여기로 가져오지 않습니다. 게임 파일, CPK/VPK, 실행파일, 덤프, 세이브, 개인용 해금 패치, 계정 정보나 개인키를 커밋하지 않습니다.

## 다른 PC에서 재개

```sh
git clone --branch KO https://github.com/gesori-pro/PSNovaTranslations.git
cd PSNovaTranslations
git remote add upstream https://github.com/Arks-Layer/PSNovaTranslations.git
git status --short --branch
```

이미 작업본이 있으면 새로 덮어쓰지 말고 로컬 변경과 브랜치를 먼저 확인합니다. 변경을 검증한 후 커밋/푸시하며 다른 PC에서는 깨끗한 작업본에서만 fast-forward로 받습니다. 강제 push/reset은 하지 않습니다.

NAS를 연결한 뒤 `PSO2/START_HERE.md`의 공통 시작 안내와 `PSNova_Shared/CURRENT.json`을 함께 봅니다. 옛 C:/G:/U:/Z: 경로를 Mac에 그대로 사용하지 않습니다.

원문/구조 검증과 실제 게임 화면 검수는 다릅니다. 이 이관만으로 의미 보류나 게임 확인을 완료 처리하지 않았습니다. 새 게임 빌드나 설치도 하지 않았습니다.
