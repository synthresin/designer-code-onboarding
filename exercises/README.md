# 실습

실습은 디자이너가 직접 해 보고 결과를 확인하는 과제입니다. 온보딩 진행 스킬(`skills/onboarding-guide/`)이 이 폴더의 파일을 읽고 진행시킵니다. 명령은 AI가 실행하고, 디자이너는 예상하고, 결정하고, 결과를 확인합니다.

## 실습의 세 종류

| 종류 | 필요한 것 | 두는 곳 |
| --- | --- | --- |
| 프로젝트가 필요 없는 실습 | 없음. 스킬이 연습 폴더를 그 자리에서 만듭니다 | 이 폴더. 내용 전체가 일반적입니다 |
| 웹 프로젝트가 필요한 실습 | 연습 레포 | 진행 순서는 이 폴더에, 실제 대상(파일, 컴포넌트, 명령)은 `company/exercises/`에 |
| 회사의 절차가 곧 내용인 실습 | 제품 레포 | `company/exercises/` |

지금 이 폴더에 있는 것은 첫 번째 종류인 git 실습 4개입니다. node도 디자인 시스템도 필요 없으므로 셋업(A6)을 하기 전에도 할 수 있습니다.

| ID | 제목 | 관련 단위 |
| --- | --- | --- |
| E-git-01 | 커밋하고 브랜치를 만들어 보기 | B1 |
| E-git-02 | 변경 내역에서 요청하지 않은 변경 찾기 | B3 |
| E-git-03 | 충돌을 내고 해결하기 | B5 |
| E-git-04 | 사라진 것처럼 보이는 변경을 되찾기 | B5 |

## 실습 파일의 형식

파일 맨 위에 속성을 적습니다.

| 속성 | 내용 |
| --- | --- |
| id | 바뀌지 않는 식별자 |
| title | 제목 |
| for_units | 이 실습이 딸린 단위의 ID |
| needs | 없음, 연습 레포, 제품 레포 중 하나 |
| outcome | 해 보고 나면 알게 되는 것. 한 문장 |

본문은 다음 항목으로 씁니다.

- 목표
- 시작할 때의 상태: 스킬이 실습 전에 만들어 두는 상태와 그 명령
- 진행: 단계마다 AI가 하는 일과 디자이너가 하는 일을 나눠 적습니다
- 완료 확인: 대화가 아니라 실제 상태로 확인하는 방법
- 마친 뒤에 말해 줄 것

## 공통 준비: 연습 폴더

git 실습 4개는 같은 연습 폴더를 씁니다. 실제 레포와 GitHub를 건드리지 않도록, 리모트 역할을 하는 저장소도 내 컴퓨터 안에 만듭니다.

```
~/onboarding-practice/
  remote.git/    GitHub 역할을 하는 저장소
  me/            디자이너의 복사본
  teammate/      동료 역할의 복사본. AI가 동료의 변경을 만들 때 씁니다
```

연습 폴더가 없으면 스킬이 아래 순서로 만듭니다.

```
mkdir -p ~/onboarding-practice && cd ~/onboarding-practice
git init --bare -b main remote.git
git clone remote.git me
cd me
git config user.name "나"
git config user.email "me@example.com"
```

`me` 폴더에 아래 세 파일을 만듭니다.

`copy.md`

```
# 휴가 신청 화면의 문구

- 화면 제목: 휴가 신청
- 안내 문구: 남은 휴가를 확인하고 신청하세요
- 버튼: 신청
- 완료 메시지: 신청이 접수되었습니다
```

`settings.json`

```
{
  "maxDaysPerRequest": 10,
  "allowHalfDay": true
}
```

`notes.md`

```
# 메모

- 반차는 0.5일로 계산한다
- 승인자는 팀장이다
- 취소는 시작일 전날까지 가능하다
```

그다음 첫 커밋을 만들고 동료의 복사본을 받습니다.

```
git add -A
git commit -m "연습용 파일 추가"
git push -u origin main
cd ..
git clone remote.git teammate
cd teammate
git config user.name "동료"
git config user.email "mate@example.com"
```

각 실습은 `me` 폴더에서 `main`이 리모트의 최신과 같고 커밋하지 않은 변경이 없는 상태에서 시작합니다. 실습을 시작하기 전에 `git switch main`, `git pull origin main`, `git status`로 이 상태를 확인합니다.

## 정리

실습 4개를 마친 뒤 디자이너에게 연습 폴더를 지울지 묻고, 지우겠다고 하면 `~/onboarding-practice` 폴더만 지웁니다. 다른 폴더는 지우지 않습니다.
