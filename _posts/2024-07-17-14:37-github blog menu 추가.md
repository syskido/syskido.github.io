---
layout: post
title: Blog menu 추가
date: 17-07-2024
categories: [GitHub]
tag: [like, comment, subscribe]
---

## 1. Jekyll 테마 선택 및 설정

먼저, Github 블로그는 주로 Jekyll이라는 정적 사이트 생성기를 사용합니다. 대부분의 Jekyll 테마는 메뉴를 쉽게 추가할 수 있도록 설정 파일을 제공합니다. 

## 2. `_config.yml` 파일 수정

블로그의 루트 디렉토리에 있는 `_config.yml` 파일을 열어야 합니다. 이 파일은 블로그의 기본 설정을 정의하는 파일입니다. 여기에서 메뉴를 추가할 수 있습니다.

### 예시:
```yaml
# _config.yml

title: My Blog
description: >- # this means to ignore newlines until "baseurl:"
  A simple blog
baseurl: "" # the subpath of your site, e.g. /blog
url: "https://username.github.io" # the base hostname & protocol for your site

# 추가할 메뉴 설정
nav:
  home:
    name: "Home"
    url: "/"
  about:
    name: "About"
    url: "/about"
  projects:
    name: "Projects"
    url: "/projects"
```

### 3. HTML 파일 수정

테마에 따라 `_layouts` 폴더나 `_includes` 폴더에 있는 파일들을 수정해야 할 수도 있습니다. 보통 헤더(header) 부분을 수정하여 메뉴를 추가합니다.

#### 예시:
```html
<!-- _includes/header.html 또는 _layouts/default.html -->

<nav>
  <ul>
    <li><a href="{{ site.baseurl }}/">{{ site.nav.home.name }}</a></li>
    <li><a href="{{ site.baseurl }}/about">{{ site.nav.about.name }}</a></li>
    <li><a href="{{ site.baseurl }}/projects">{{ site.nav.projects.name }}</a></li>
  </ul>
</nav>
```

### 4. 페이지 파일 생성

각 메뉴 항목에 해당하는 페이지를 만들어야 합니다. 예를 들어 `about` 페이지를 생성하려면 `about.md` 파일을 만듭니다.

#### 예시:
```markdown
---
layout: page
title: "About"
permalink: /about/
---

# About
이 페이지는 블로그에 대한 정보를 담고 있습니다.
```

### 5. 변경 사항 커밋 및 푸시

모든 수정이 완료되면 변경 사항을 커밋하고 푸시해야 합니다.

```bash
git add .
git commit -m "메뉴 추가"
git push origin main
```

