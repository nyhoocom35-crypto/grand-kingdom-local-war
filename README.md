# 그란 킹덤 로컬 AI 전쟁 패치

**Grand Kingdom Local War 1.5** — Windows + Vita3K에서 개인용 AI 국가전을 플레이하는 비공식 팬 패치입니다.

![그란 킹덤 전장 패치 홍보 포스터](Grand_Kingdom_Battle_Poster.png)

## 다운로드

[최신 통합 배포본 1.5 받기](Grand_Kingdom_Local_War_1.5_Full_Distribution.zip?raw=true)

[전체 한국어 설치 안내](README_KO.txt) · [배포 ZIP 해시](SHA256SUMS.txt) · [재배포 안내](DISTRIBUTION.md)

## 주요 기능

- 네 국가의 AI 전쟁과 영토 변화, 전체 84개 전장, 30분 캠페인.
- 국가 침공·전략 병기·병영 AI 투표, 용병단 조회와 플레이어/AI 순위.
- 국가·지역·거점 이름으로 표시하는 전황 페이지.
- 파견 1분당 1전투, 최대 255전투 누적.
- 전략지령은 진영별 1회, 한 작전 양측 합계 최대 2회.
- 작전 종료·캠페인 교체 시 강제퇴각 처리 수정, 새 작전 공훈치 3배.
- 우리 용병 경험치 3배, 선택 가능한 레벨 성장 8배.
- DLC 직업 및 국가 스토리 접근 수정. 해당 콘텐츠 데이터는 별도로 필요합니다.

## 지원 환경

Windows PC, Vita3K, 일본판 **PCSG00474**, 게임 업데이트 **1.06**.
처음 설치할 때 해당 버전의 복호화 SELF `eboot.bin`이 필요합니다.
그래픽 설정은 **OpenGL / VSync OFF**를 사용하세요.

게임 본편·업데이트·DLC 데이터·펌웨어·라이선스·개인 세이브는 포함하지 않습니다.
각 PC에서 독립된 AI 전황으로 동작하며 공용 인터넷 멀티플레이와 PS Vita 실기를 지원하지 않습니다.

## 처음 설치

1. 배포 ZIP 전체를 전용 폴더에 압축 해제합니다.
2. Vita3K와 기존 GK 서버를 종료합니다.
3. `1_Install_Standard.cmd`를 실행하고 설치된 실행파일과 복호화 SELF 파일을 선택합니다.
4. `INSTALLED` 확인 후 `2_Start_Local_War.cmd`를 실행합니다.
5. `SELFTEST OK`, `Finish 37`, `READY`를 확인하고 게임의 온라인 메뉴로 접속합니다.

성장 8배를 선택하려면 `Optional_Growth_8x.cmd`를 사용하세요.
상세한 파일 선택 경로와 복원 방법은 [README_KO.txt](README_KO.txt)에 있습니다.

## 기존 설치 갱신

게임과 서버를 종료하고 배포 ZIP 전체를 **기존 패치 폴더에** 덮어 압축 해제한 뒤,
`1_Update_Existing_Install.cmd` → `2_Start_Local_War.cmd` 순서로 실행합니다.
기존 설치 기록·계정·전황·`protocol.dat`·백업은 보관하세요. 성장 모드는 유지됩니다.

## 소스와 검증

전체 서버 소스와 패치 제작 도구는 [소스 포함 패키지](grand-kingdom-local-war-github-ready.zip?raw=true)에 있습니다. 패키지의 `Source/server/`를 참고하세요.
소스 패키지를 압축 해제한 뒤 Go 1.23 이상에서 해당 폴더로 이동해 `go test ./...`로 서버 테스트를 실행할 수 있습니다.
Windows 빌드 및 네이티브 패치 검증에 필요한 입력은 [빌드 안내](BUILD.txt)를 참고하세요.

기존 배포본은 서버 테스트와 ARM 통신·작전 종료·공훈치 처리 검증을 포함합니다.
Windows 설치 UI와 실제 Vita3K 보상 화면·지급은 제작 환경에서 확인하지 못했습니다.
GitHub 배포 준비에서는 기존 배포 ZIP을 변경하지 않고 파일 해시와 포함 파일을 확인했습니다.

오류 제보에는 패치/게임/에뮬레이터 버전, 재현 순서, 오류 문구를 적어 주세요.

## 전체 소스 포함 패키지

[grand-kingdom-local-war-github-ready.zip](grand-kingdom-local-war-github-ready.zip?raw=true)에는 폴더 구조를 유지한 전체 소스·설치 도구·안내문과 배포 ZIP이 들어 있습니다.
