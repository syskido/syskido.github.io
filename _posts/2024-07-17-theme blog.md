---
layout: post
title: theme blog
date: 17-07-2024
categories: [github]
tag: [like, comment, subscribe]
---

# Jekyll 테마를 사용해 블로그를 만드는 방법

Jekyll은 정적 사이트 생성기로, GitHub Pages와 잘 통합되어 개인 블로그나 프로젝트 사이트를 쉽게 만들 수 있습니다.

## 1. Jekyll 설치
먼저 Jekyll을 설치해야 합니다. Ruby와 RubyGems가 필요합니다. 아래 명령어를 통해 설치할 수 있습니다.

```sh
# Ruby 및 RubyGems 설치 (macOS의 경우)
brew install ruby

# Jekyll 및 Bundler 설치
gem install jekyll bundler
```

## 2. 새로운 Jekyll 사이트 생성
Jekyll 명령어를 사용하여 새로운 사이트를 생성합니다.

```sh
jekyll new myblog
cd myblog
```

## 3. 사이트 빌드 및 로컬 서버 실행
아래 명령어를 통해 사이트를 빌드하고 로컬 서버를 실행할 수 있습니다.

```sh
bundle exec jekyll serve
```

이제 `http://localhost:4000`에서 로컬 서버를 확인할 수 있습니다.


예를 들어, "minima" 테마를 적용하려면 `_config.yml` 파일에 다음 줄을 추가합니다.

```yaml
theme: minima
```

## 5. Gemfile 수정
선택한 테마를 Gemfile에 추가해야 합니다.

```ruby
gem "minima"
```

그리고 번들을 업데이트 합니다.

```sh
bundle install
```

## 6. GitHub Pages에 배포
GitHub에 새로운 저장소를 만들고 코드를 푸시합니다.

```sh
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/yourrepository.git
git push -u origin master
```

GitHub Pages 설정에서 브랜치를 `master` 또는 `gh-pages`로 설정합니다.

## 7. 추가 설정 및 커스터마이징
Jekyll 테마를 추가적으로 커스터마이징하고 `_config.yml` 파일을 통해 사이트 제목, 설명, 기타 설정을 변경할 수 있습니다.



# Jekyll 플러그인

은 사이트 기능을 확장하고 커스터마이즈할 수 있는 중요한 도구입니다. Jekyll에는 여러 가지 유용한 플러그인이 있으며, 이를 통해 다양한 기능을 추가할 수 있습니다. 여기서는 플러그인의 설치 방법, 구성, 그리고 유용한 플러그인 몇 가지를 소개하겠습니다.

## 1. 플러그인 설치

Jekyll 플러그인은 Gem을 통해 설치할 수 있습니다. 플러그인을 설치하려면 `Gemfile`에 해당 플러그인을 추가하고 `bundle install`을 실행하면 됩니다.

예를 들어, `jekyll-seo-tag` 플러그인을 설치하려면 `Gemfile`에 다음 줄을 추가합니다.

```ruby
gem "jekyll-seo-tag"
```

그런 다음, 다음 명령어를 실행합니다.

```sh
bundle install
```

## 2. 플러그인 구성

플러그인을 설치한 후, `_config.yml` 파일에 플러그인을 등록해야 합니다. 예를 들어, `jekyll-seo-tag` 플러그인을 등록하려면 `_config.yml` 파일에 다음과 같이 추가합니다.

```yaml
plugins:
  - jekyll-seo-tag
```

# 유용한 플러그인 예시

## 1. `jekyll-seo-tag`
SEO 관련 메타 태그를 자동으로 생성해주는 플러그인입니다.

설치:
```ruby
gem "jekyll-seo-tag"
```

구성:
```yaml
plugins:
  - jekyll-seo-tag
```

사용:
```html
<head>
  {% seo %}
</head>
```

## 2. `jekyll-sitemap`
사이트맵을 자동으로 생성해주는 플러그인입니다.

설치:
```ruby
gem "jekyll-sitemap"
```

구성:
```yaml
plugins:
  - jekyll-sitemap
```

## 3. `jekyll-paginate`
페이지네이션 기능을 추가해주는 플러그인입니다.

설치:
```ruby
gem "jekyll-paginate"
```

구성:
```yaml
plugins:
  - jekyll-paginate

paginate: 5
paginate_path: "/page:num/"
```

## 4. `jekyll-feed`
RSS 피드를 생성해주는 플러그인입니다.

설치:
```ruby
gem "jekyll-feed"
```

구성:
```yaml
plugins:
  - jekyll-feed
```

## 5. `jekyll-assets`
사이트의 CSS와 JavaScript 자산을 관리해주는 플러그인입니다.

설치:
```ruby
gem "jekyll-assets"
```

구성:
```yaml
plugins:
  - jekyll-assets
```

# 커스텀 플러그인 작성

필요한 기능이 존재하지 않는 경우, 커스텀 플러그인을 작성할 수 있습니다. Jekyll 프로젝트의 `_plugins` 폴더에 Ruby 파일을 추가하면 됩니다.

예를 들어, 간단한 필터 플러그인을 작성해보겠습니다. `_plugins` 폴더에 `reverse_filter.rb` 파일을 추가하고 다음 코드를 작성합니다.

```ruby
module Jekyll
  module ReverseFilter
    def reverse(input)
      input.reverse
    end
  end
end

Liquid::Template.register_filter(Jekyll::ReverseFilter)
```

이제 이 필터를 Liquid 템플릿에서 사용할 수 있습니다.

```html
{{ "Hello, World!" | reverse }}
```

위 코드는 "Hello, World!" 문자열을 뒤집어서 출력합니다.

## 마무리

커스텀 플러그인은 Jekyll의 기능을 확장하거나 맞춤화할 수 있는 강력한 방법입니다. 여기서는 커스텀 플러그인을 작성하는 과정을 자세히 설명하겠습니다.




## 예시: 현재 날짜를 출력하는 태그

```ruby
module Jekyll
  class CurrentDateTag < Liquid::Tag
    def render(context)
      Time.now.strftime("%Y-%m-%d")
    end
  end
end

Liquid::Template.register_tag('current_date', Jekyll::CurrentDateTag)
```

이제 이 태그를 Liquid 템플릿에서 사용할 수 있습니다.

```html
{% current_date %}
```


## 4. 제너레이터 플러그인 작성

제너레이터 플러그인은 Jekyll 사이트를 빌드할 때 새로운 페이지를 생성하거나 기존 페이지를 변형합니다. `_plugins` 폴더에 새로운 Ruby 파일을 생성하고 제너레이터를 정의할 수 있습니다.


```ruby
module Jekyll
  class PageListGenerator < Generator
    safe true

    def generate(site)
      site.pages.each do |page|
        puts "Page: #{page.url}"
      end
    end
  end
end
```

이 제너레이터는 Jekyll 사이트를 빌드할 때 모든 페이지의 URL을 콘솔에 출력합니다. 물론 실제로는 파일을 생성하거나 페이지를 수정하는 등의 작업을 수행할 수 있습니다.

## 5. 플러그인 테스트

플러그인을 작성한 후, Jekyll 서버를 재시작하여 플러그인이 제대로 작동하는지 확인합니다.

```sh
bundle exec jekyll serve
```





