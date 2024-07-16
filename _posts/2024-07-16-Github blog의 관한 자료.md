---
layout: post
title: GitHub blog 
date: 16-07-2024
categories: [GitHub]
tag: [like, comment, subscribe]
---






# GitHub Blog란
 GitHub Pages라는 기능을 통해 사용자가 손쉽게 정적 웹사이트를 만들고 호스팅할 수 있도록 지원합니다. GitHub Pages를 사용하면 주로 다음과 같은 용도로 활용됩니다:

1. **프로젝트 문서화**: 오픈 소스 프로젝트의 문서화 작업을 쉽게 할 수 있습니다.
2. **개인 블로그**: 개인 프로그래밍 프로젝트, 학습 기록, 기술 블로그 등 다양한 내용을 작성할 수 있습니다.
3. **포트폴리오 사이트**: 개인 포트폴리오를 만들어서 자신의 작업물을 소개할 수 있습니다.

GitHub Pages를 통해 블로그를 만드는 방법을 단계별로 설명하면 다음과 같습니다:

### 1. GitHub 저장소 생성
GitHub Pages 사이트를 만들기 위해 먼저 GitHub에 새 저장소를 생성해야 합니다. 이 저장소는 사용자명.github.io 형식으로 만들어야 합니다.

### 2. 정적 사이트 생성
정적 사이트 생성 도구(예: Jekyll, Hugo, Gatsby 등)를 사용하거나, 단순한 HTML/CSS 파일을 작성하여 사이트를 구성할 수 있습니다. Jekyll은 GitHub Pages와 통합이 잘 되어 있어서 많이 사용됩니다.

### 3. 저장소에 사이트 파일 업로드
사이트 파일을 저장소의 루트 디렉토리 또는 `docs` 디렉토리에 업로드합니다.

### 4. GitHub Pages 설정
저장소의 `Settings` 탭에서 `Pages` 섹션으로 이동하여 GitHub Pages를 활성화합니다. 여기서 소스 브랜치와 폴더를 선택할 수 있습니다.

### 5. 사이트 배포 및 확인
설정을 완료하면 GitHub이 자동으로 사이트를 빌드하고 배포합니다. 배포된 사이트는 `https://사용자명.github.io`에서 확인할 수 있습니다.

### 예제
Jekyll을 사용하여 블로그를 만드는 간단한 예제를 보겠습니다.

1. 로컬에 Jekyll 설치:
    ```bash
    gem install jekyll bundler
    ```

2. 새 Jekyll 사이트 생성:
    ```bash
    jekyll new myblog
    cd myblog
    ```

3. 사이트 테스트:
    ```bash
    bundle exec jekyll serve
    ```

4. GitHub에 배포:
    - 사이트 파일을 저장소에 커밋하고 푸시:
      ```bash
      git init
      git add .
      git commit -m "Initial commit"
      git remote add origin https://github.com/사용자명/사용자명.github.io.git
      git push -u origin master
      ```

5. GitHub Pages 설정 및 확인:
    - 위 단계를 마치면 자동으로 배포가 진행됩니다. 이후 `https://사용자명.github.io`에서 사이트를 확인할 수 있습니다.

### 참고 자료
- [GitHub Pages 공식 문서](https://docs.github.com/en/pages)
- [Jekyll 공식 사이트](https://jekyllrb.com/)



[python] GitHub Pages를 통해 여러 개의 블로그를 만들 수 있습니다. 각 블로그는 사용자 또는 조직 계정의 저장소에 호스팅되며, 다음과 같은 방식으로 여러 블로그를 관리할 수 있습니다:

### 1. 사용자/조직 사이트
사용자/조직 사이트는 한 계정당 하나만 만들 수 있습니다. 이 사이트는 `https://사용자명.github.io` 형식의 주소를 갖습니다.

### 2. 프로젝트 사이트
프로젝트 사이트는 계정당 여러 개 만들 수 있습니다. 각 프로젝트 사이트는 `https://사용자명.github.io/저장소명` 형식의 주소를 갖습니다.

### 여러 블로그 만들기
1. **사용자 사이트**:
   - 하나의 사용자 사이트만 만들 수 있습니다.
   - 저장소 이름: `사용자명.github.io`.

2. **프로젝트 사이트**:
   - 여러 개의 프로젝트 사이트를 만들 수 있습니다.
   - 각 프로젝트마다 별도의 저장소를 생성합니다.
   - 예: `https://사용자명.github.io/project1`, `https://사용자명.github.io/project2` 등.

### 프로젝트 사이트 만들기
다음은 프로젝트 사이트를 만드는 방법입니다:

#### 1. 새 저장소 생성
GitHub에서 새 저장소를 생성합니다. 저장소 이름은 원하는 이름으로 설정할 수 있습니다. 예를 들어, `project1`.

#### 2. 정적 사이트 파일 추가
로컬에서 정적 사이트 생성 도구(예: Jekyll, Hugo, Gatsby)를 사용하여 사이트 파일을 생성하고, 이를 저장소에 업로드합니다.

#### 3. GitHub Pages 설정
저장소의 `Settings` 탭에서 `Pages` 섹션으로 이동하여 GitHub Pages를 활성화합니다. 소스 브랜치와 폴더(기본적으로 `main` 브랜치와 `/` 또는 `docs/` 디렉토리)를 선택합니다.

#### 4. 사이트 배포 및 확인
설정을 완료하면 GitHub이 자동으로 사이트를 빌드하고 배포합니다. 배포된 사이트는 `https://사용자명.github.io/project1`에서 확인할 수 있습니다.

### 예제
`project1`이라는 프로젝트 사이트를 만든다고 가정해 봅시다.

1. GitHub에서 새 저장소 생성:
   - 저장소 이름: `project1`.

2. 로컬에서 Jekyll 사이트 생성:
    ```bash
    jekyll new project1
    cd project1
    ```

3. 사이트 테스트:
    ```bash
    bundle exec jekyll serve
    ```

4. 저장소에 사이트 파일 업로드:
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    git remote add origin https://github.com/사용자명/project1.git
    git push -u origin master
    ```

5. GitHub Pages 설정:
   - 저장소의 `Settings` > `Pages`에서 `main` 브랜치와 `/` 또는 `docs/` 디렉토리를 선택.

6. 사이트 확인:
   - `https://사용자명.github.io/project1`에서 사이트 확인.

