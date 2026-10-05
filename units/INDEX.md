# 단위 목록

단위는 42개입니다. 일반 25개, 플랫폼(웹) 5개, 플랫폼(추가 플랫폼) 1개, 레포 11개입니다. ID의 첫 글자가 작업 범위입니다(A는 읽기, B는 뷰 수정, C는 화면 구성, D는 로직 포함, X는 심화).

일반 단위는 이 레포의 `units/general/`에 있습니다. 플랫폼 단위와 레포 단위는 회사마다 내용이 다르므로 이 레포에는 제목만 있고, 각 회사가 `company/units/` 아래에 씁니다. 레포 단위는 레포마다 한 벌씩 씁니다. 연습 레포에는 A6, A7, A8, B4만 쓰고, 제품 레포에는 레포 단위 전부를 씁니다. C4는 삭제한 ID이고 다시 쓰지 않습니다.

실습 단위와 일부 개념 단위에는 `exercises/`의 실습 파일이 딸려 있습니다. 목록은 `exercises/README.md`에 있습니다.

상태 표기: "초안"은 파일이 있고 검토 전, "미작성"은 파일이 없음, "회사별 작성"은 각 회사가 `company/` 아래에 쓰는 단위.

| ID | 제목 | 유형 | 선행 | 적용 대상 | 상태 |
| --- | --- | --- | --- | --- | --- |
| A0 | [이 과정이 다루는 것과 다루지 않는 것](general/A0-what-this-covers.md) | 개념 | 없음 | 일반 | 초안 |
| A1 | [개발 프로젝트는 폴더이고 코드는 텍스트 파일이다](general/A1-project-is-a-folder.md) | 개념 | 없음 | 일반 | 초안 |
| A2 | [확장자로 파일의 역할 구분하기](general/A2-file-extensions.md) | 개념 | A1 | 일반 | 초안 |
| A3 | [AI 코딩 앱에서 프로젝트 폴더를 열고 작업을 지시하기](general/A3-working-in-an-ai-coding-app.md) | 절차 | A1 | 일반 | 초안 |
| A4 | [node와 package.json: 프로젝트가 실행되는 방식과 외부 패키지를 가져다 쓰는 방식](general/A4-node-and-package-json.md) | 개념 | A1 | 일반 | 초안 |
| A5 | 디자인 시스템은 패키지로 설치되어 있다 | 개념 | A4 | 플랫폼(웹) | 회사별 작성 |
| A6 | 개발 환경 셋업과 점검 | 절차 | A3 | 레포 | 회사별 작성 |
| A7 | 로컬에서 화면 띄우기와 스토리북 열기 | 실습 | A6 | 레포 | 회사별 작성 |
| A8 | AI에게 코드에 대해 질문하기: 내 화면의 코드 위치 찾기 | 실습 | A7 | 레포 | 회사별 작성 |
| A9 | 사내 스킬 목록: 각 스킬을 언제 쓰는가 | 참조 | A3 | 플랫폼(웹) | 회사별 작성 |
| A10 | [작업에 맞는 모델과 추론 강도 고르기](general/A10-choosing-model-and-effort.md) | 절차 | A3 | 일반 | 초안 |
| B1 | [git의 구조: 커밋, 브랜치, 로컬과 리모트, PR](general/B1-git-structure.md) | 개념 | A1 | 일반 | 초안 |
| B2 | [복구 가능한 범위와 실제로 조심할 행동](general/B2-what-is-recoverable.md) | 개념 | B1 | 일반 | 초안 |
| B3 | [변경 내역(diff) 읽기](general/B3-reading-a-diff.md) | 개념 | B1 | 일반 | 초안 |
| B4 | 작업 한 번의 전체 절차: 최신 내용 받기, 브랜치, 수정, 커밋, 푸시, PR | 절차 | B1, A7 | 레포 | 회사별 작성 |
| B5 | [충돌과 "내 변경이 보이지 않는 상황"을 복구하기](general/B5-conflict-and-recovery.md) | 실습 | B2, B3 | 일반 | 초안 |
| B6 | [화면은 부모와 자식의 트리로 기술된다](general/B6-screen-is-a-tree.md) | 개념 | A2 | 일반 | 초안 |
| B7 | 디자인 토큰이 코드에 정의된 방식 | 참조 | A5, B6 | 플랫폼(웹) | 회사별 작성 |
| B8 | [Figma 컴포넌트와 코드 컴포넌트의 대응: variant와 props](general/B8-figma-and-code-components.md) | 개념 | B6 | 일반 | 초안 |
| B9 | 디자인 시스템 사용법 스킬과 스토리북으로 컴포넌트를 찾고 쓰기 | 참조 | B8, A9 | 플랫폼(웹) | 회사별 작성 |
| B10 | 같은 디자인 결정의 웹 구현과 다른 플랫폼 구현 비교 | 참조 | B7, B9 | 플랫폼(추가 플랫폼) | 회사별 작성 |
| B11 | PR 쓰기와 리뷰 받기: 설명, 전후 스크린샷, 자동 검사 실패 대응 | 절차 | B3, B4 | 레포 | 회사별 작성 |
| B12 | 첫 PR | 실습 | B5, B11 | 레포 | 회사별 작성 |
| C1 | [뷰와 모델의 분리](general/C1-view-and-model.md) | 개념 | B6 | 일반 | 초안 |
| C2 | 이 레포에서 디자이너가 수정하는 폴더와 수정하지 않는 폴더 | 참조 | C1 | 레포 | 회사별 작성 |
| C3 | [API: 화면이 데이터를 받아오는 방식](general/C3-api.md) | 개념 | C1 | 일반 | 초안 |
| C5 | [재사용 단위를 AI에게 지시하고 점검하기](general/C5-directing-reuse.md) | 절차 | B8, C1 | 일반 | 초안 |
| C6 | 디자이너용 작업 규칙 스킬 | 참조 | C5, A9 | 플랫폼(웹) | 회사별 작성 |
| C7 | [지시문 템플릿 모음](general/C7-prompt-templates.md) | 참조 | C5 | 일반 | 초안 |
| C8 | 기존 API 위에서 화면 구성 변경하기 | 실습 | C2, C3, C6 | 레포 | 회사별 작성 |
| D1 | [도메인 모델이 코드에 있는 위치: n:m 관계가 코드와 데이터베이스에서 표현되는 방식](general/D1-domain-model-in-code.md) | 개념 | C3 | 일반 | 초안 |
| D2 | API 요청과 응답 읽기 | 실습 | C3 | 레포 | 회사별 작성 |
| D3 | 로직을 포함하는 변경의 사전 합의 절차 | 절차 | C6 | 레포 | 회사별 작성 |
| D4 | [테스트가 보장하는 것](general/D4-what-tests-guarantee.md) | 개념 | C1 | 일반 | 초안 |
| D5 | 격리된 작은 로직을 포함한 변경 | 실습 | D2, D3, D4 | 레포 | 회사별 작성 |
| X1 | [데이터베이스와 ERD](general/X1-database-and-erd.md) | 개념 | D1 | 일반 | 초안 |
| X2 | [worktree: 여러 작업을 동시에 진행하기](general/X2-worktree.md) | 개념 | B1 | 일반 | 초안 |
| X3 | [rebase와 merge의 차이](general/X3-rebase-and-merge.md) | 개념 | B1 | 일반 | 초안 |
| X4 | [빌드와 배포: 머지된 코드가 사용자에게 도달하는 과정](general/X4-build-and-deploy.md) | 개념 | B1 | 일반 | 초안 |
| X5 | [nvm과 node 버전 관리](general/X5-nvm-and-node-versions.md) | 개념 | A4 | 일반 | 초안 |
| X6 | [HTML과 CSS로 형태가 기술되는 방식](general/X6-html-and-css.md) | 개념 | B6 | 일반 | 초안 |
| X7 | [터미널을 직접 쓰고 싶은 사람을 위한 최소 사용법](general/X7-terminal-minimum.md) | 절차 | A3 | 일반 | 초안 |
