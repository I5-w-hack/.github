* **[I5_back](https://github.com/I5-w-hack/I5_back):** 백엔드 레포지토리
* **[I5_front](https://github.com/I5-w-hack/I5_front):** 프론트엔드 레포지토리
* **[.github](https://github.com/I5-w-hack/.github):** 조직 프로필 및 관리 파일 레포지토리

# 🚀 팀원 협업 가이드

- 본인 계정으로 Fork한 후 PR(Pull Request)하는 방식

## 1. 최초 1회 설정 (PC 세팅)
프로젝트에 처음 참여할 때 한 번만 실행.

1. 원본 레포지토리 Fork (GitHub)**
   - `I5-w-hack/[레포지토리]` 페이지로 이동.
   - 우측 상단의 **[Fork]** 버튼을 눌러 `My-Username/[레포지토리]` (본인 계정)으로 복제

2. 로컬 PC에 Clone (Git)**
   - **본인 계정**으로 포크해 온 레포(`My-Username/[레포지토리]`)에서 HTTPS 주소를 복사
      ```bash
      git clone https://github.com/My-Username/I5_back(front).git
      cd I5_back(front)
      git remote add upstream https://github.com/I5-w-hack/I5_back(front).git
      ```
   - **연결 확인 명령어**
     ```bash
     git remote -v
     ```
   - 정상 연결 시
     ``` bash
     $ git remote -v
      origin  https://github.com/My-Username/I5_back.git (fetch)
      origin  https://github.com/My-Username/I5_back.git (push)
      upstream        https://github.com/I5-w-hack/I5_back(front).git (fetch)
      upstream        https://github.com/I5-w-hack/I5_back(front).git (push)
     ```
## 2-1. 이후 작업 ( feature 브랜치 생성X ) 
- **동기화+init → 커밋 → 푸시 → PR**

1. 동기화

   - 로컬 main 브랜치로 이동 
        ``` bash
        git switch main
        ```
   - 원본(upstream)의 최신 코드를 pull
        ``` bash
        git pull upstream main
        ```
        
2. 작업 및 커밋
      ``` bash
      git add .
      git commit -m "feat: 기능 설명"
      ```
   
4. 내 포크(origin)에 푸시
      ``` bash
      git push origin
      ```
5. Pull Request (PR) 생성 (GitHub)
      - GitHub의 본인 포크 레포 페이지로 이동
      - main 브랜치가 푸시되었다는 알림("main had recent pushes")에서 [Compare & pull request] 버튼을 클릭
   
      - 병합 방향 확인
          - Base: I5-w-hack/I5_back(front) (원본) main
          - Head: My-Username/I5_back(front) (내 포크) main
   
      - PR 제목과 설명을 작성하고 PR을 생성
        
  
## 2-2. 이후 작업 ( feature 브랜치 생성 )
- **동기화+init → 브랜치 생성 → 커밋 → 푸시 → PR**


1. 동기화

   - 로컬 main 브랜치로 이동 
        ```bash
        git switch main
        ```
   - 원본(upstream)의 최신 코드를 pull
        ```bash
        git pull upstream main
        ```

2. 기능 브랜치 생성
      ``` bash
      git switch -c feature/[기능명]
      ```

4. 작업 및 커밋
      ``` bash
      git add .
      git commit -m "feat: 기능 설명"
      ```
6. 내 포크(origin)에 푸시
      -  새 브랜치를 처음 푸시할 때 (-u 옵션)
         ``` bash
         git push -u origin feature/[기능명]
         ```
      - 이후 해당 브랜치에서 추가 작업 푸시
         ``` bash
         git push origin
         ```
7. Pull Request (PR) 생성 (GitHub)
      - GitHub의 본인 포크 레포 페이지로 이동
      - feature/[기능명] 브랜치가 푸시되었다는 알림에서 [Compare & pull request] 버튼을 클릭
   
      - 병합 방향 확인
          - Base: I5-w-hack/I5_back(front) (원본) main
          - Head: My-Username/I5_back(front) (내 포크) feature/[기능명]
   
      - PR 제목과 설명을 작성하고 PR을 생성
