# 이준형 자기소개 웹페이지 (OSS Assign 01)

AI를 활용하여 제작한 자기소개 프로필 페이지입니다.  
`index.html`은 AI로 생성한 원본이고, `index2.html`은 직접 수정한 버전입니다.

## 배포 URL

| 항목 | URL |
|------|-----|
| Vercel Deploy URL | https://2026-oss-assign01-phi.vercel.app/ |
| index.html | https://2026-oss-assign01-phi.vercel.app/index.html |
| index2.html | https://2026-oss-assign01-phi.vercel.app/index2.html |

## GitHub Repository

https://github.com/2026-2-OSS/assign01-c01-21901037

---

## Weekly Review

### Key Learning

1. **AI를 활용한 웹페이지 제작** — AI 도구에 자기소개 내용을 요청하여 HTML/CSS 코드를 생성하고, `index.html`을 완성했습니다.
2. **Git/GitHub 버전 관리** — Git 명령어마다 역할과 사용 시점이 다르다는 것을 익혔습니다.
   - **`git clone`** — GitHub 저장소를 로컬 컴퓨터로 **처음 내려받을 때** 필요합니다. 원격 저장소 전체를 복사해 작업 폴더를 만듭니다.
   - **`git remote add`** — 로컬에서 새로 만든 프로젝트를 GitHub와 **연결할 때** 필요합니다. (`clone`을 쓰면 remote는 자동 설정됨)
   - **`git add`** — 수정한 파일을 커밋 대상으로 올릴 때 필요합니다. 커밋 전에 반드시 거치는 단계입니다.
   - **`git commit -m`** — 스테이징된 변경 사항을 로컬에 저장할 때 필요합니다. `-m`으로 커밋 메시지를 함께 남깁니다.
   - **`git push`** — 로컬 커밋을 GitHub 원격 저장소에 업로드할 때 필요합니다.
3. **Bash(터미널) 기본 명령어** — VS Code 터미널에서 프로젝트 폴더를 이동하고 파일을 확인하는 기본 명령어를 익혔습니다.
   - **`pwd`** — 현재 위치한 폴더 경로 확인
   - **`ls`** — 현재 폴더의 파일·폴더 목록 보기
   - **`cd 폴더명`** — 다른 폴더로 이동 (`cd ..`은 상위 폴더로)
   - **`mkdir 폴더명`** — 새 폴더 만들기
   - **`clear`** — 터미널 화면 지우기
4. **Vercel 자동 배포** — GitHub Repository를 Vercel에 연결하면 Push할 때마다 웹사이트가 자동으로 재배포되는 CI/CD 흐름을 경험했습니다.

### Development Flow

```
VS Code → HTML 작성 → Git Commit → GitHub Push → Vercel Auto Deploy → Web
```

1. GitHub Repository 클론 (최초 1회)

```bash
git clone https://github.com/2026-2-OSS/assign01-c01-21901037
cd assign01-c01-21901037
```

2. VS Code에서 프로젝트 폴더 열고 `index.html` 작성 (AI 활용)

3. 터미널 기본 명령어로 작업 폴더 확인

```bash
pwd          # 현재 경로 확인
ls           # 파일 목록 보기
cd 폴더명     # 폴더 이동
```

4. GitHub Repository 추가 연결 (개인 저장소, 최초 1회)

```bash
git remote add mine https://github.com/donkeyears0402-star/2026OSS_assign01
```

5. 파일 수정 후 버전 관리 (작업할 때마다 반복)

```bash
git add .                        # 변경된 파일을 스테이징
git commit -m "커밋 메시지"       # 로컬에 변경 이력 저장
git push origin main             # 수업용 저장소에 업로드
git push mine main               # 개인 저장소에 업로드
```

6. Vercel이 GitHub 변경 사항을 감지하여 자동 배포
7. 배포 URL로 웹페이지 접속 확인

### Code Modification (index.html → index2.html)

| 수정 항목 | index.html (원본) | index2.html (수정) |
|-----------|-------------------|---------------------|
| **스타일** | 밝은 테마 (`style.css` 기본) | 다크 테마 적용 (`#172033` 배경, 글꼴·색상 변경) |
| **헤더 내용** | "안녕하세요, 이준형입니다." | "새로운 것을 배우고 직접 만들어갑니다." |
| **페이지 구성** | ABOUT ME ~ PROJECT 5개 섹션 | INTEREST ~ NAVIGATION으로 섹션 재구성 |
| **HTML 요소** | — | `<hr>`, `<strong>` 태그 추가 |
| **취미** | 3개 항목 | "웹사이트 만들어보기" 항목 추가 (4개) |
| **외부 링크** | GitHub 링크 1개 | GitHub + 네이버(`https://www.naver.com/`) 링크 추가 |
| **학습 목표** | index.html 내 LEARNING 섹션 | GOAL 섹션으로 별도 정리 및 내용 보강 |

### Problem & Solution

**문제:** Vercel에 처음 배포했을 때 GitHub Repository와 연결이 제대로 되지 않아 배포가 실패했습니다.

**해결:** Vercel 대시보드에서 GitHub 계정을 다시 연결하고, 올바른 Repository(`2026OSS_assign01`)를 Import한 뒤 재배포하여 정상 동작을 확인했습니다.

### Reflection

DevTools에서 CSS를 임시로 변경해도 실제 파일에는 저장되지 않는다는 점이 인상 깊었습니다. 브라우저에서 디자인을 실험한 뒤, 최종 결과는 반드시 소스 파일(`index2.html`)에 직접 반영해야 한다는 웹 개발의 기본 흐름을 이해하게 되었습니다.
