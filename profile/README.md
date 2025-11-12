* **[I5_back](https://github.com/I5-w-hack/I5_back):** 백엔드 레포지토리
* **[I5_front](https://github.com/I5-w-hack/I5_front):** 프론트엔드 레포지토리
* **[.github](https://github.com/I5-w-hack/.github):** 조직 프로필 및 관리 파

## 🚀 팀원 협업 가이드 (Forking Workflow)

- 본인 계정으로 Fork한 후 PR(Pull Request)하는 방식

### 1. 최초 1회 설정 (PC 세팅)
프로젝트에 처음 참여할 때 한 번만 실행.

**1. 원본 레포지토리 Fork (GitHub)**
   - `I5-w-hack/[레포지토리]` 페이지로 이동.
   - 우측 상단의 **[Fork]** 버튼을 눌러 `My-Username/[레포지토리]` (본인 계정)으로 복제

**2. 로컬 PC에 Clone (Git)**
   - **본인 계정**으로 포크해 온 레포(`My-Username/[레포지토리]`)에서 HTTPS 주소를 복사
   ```bash
   git clone [https://github.com/My-Username/I5_back(front).git]
   cd I5_back
  git remote add upstream [https://github.com/I5-w-hack/I5_back(front).git]
  ```
 - 연결 확인
  ```bash
  git remote -v
  ```

### 2. 이후 작업
- 기능 브랜치를 따로 생성하지 않을 경우. 동기화 & 커밋 & 푸시 & PR만 반복해도 무방

**1. 동기화
- develop 브랜치로 이동
  ```git switch develop```
- 원본(upstream)의 최신 코드를 pull
```git pull upstream develop```

**2. 기능 브랜치 생성
 ```git switch -c feature/[기능명]```

**3. 작업 및 커밋
```
git add .
git commit -m "feat: 제목"
```
**4. 내 포크(Origin)에 푸시
- u옵션은 새 기능 브랜치를 만들었을 때 첫 푸시 일때만 필요
```
git push -u origin feature/[기능명]
```

**5. Pull Request (PR) 생성 (GitHub)
- GitHub의 본인 포크 레포(My-Username/I5_back)or(My-Username/I5_front)페이지로 이동
- feature/[기능명] 브랜치가 푸시되었다는 알림에서 [Compare & pull request] 버튼을 클릭

- 병합 방향 확인
    -Base: I5-w-hack/I5_back (원본) develop
    - Head: My-Username/I5_back (내 포크) feature/[기능명]

- PR 제목과 설명을 작성하고 PR을 생성합니다.
