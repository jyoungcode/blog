# blog
make a blog

## key point
- server 구동 : jekyll serve --watch --baseurl ""

- config.yml 한칸 무조껀 띄어야 한다.

- 주석 달면 에러 생긴다.

- _posts 에서 날짜가 나중에 것이 최근이 되서 1번이 된다.

### data 폴더
- data 폴더 있으면 더이상 
_posts 에 planet-types md 파일 따로 없어도 되고
markdownify 를 통해서 원래 html 코드를 똑같이 입힐 수 있다.

### cli
- `ctrl + l` 새로 사용

### 기능 순서
- `{% for layout in site.categories.category limit:1 %} {% endfor %}`
- limit으로 게시글 개수 제한

### md 파일에 갖다 붙이기 
- permelink: /blog/:title

{% for planet in site.data.planet-types %} -->
		<li><a href="{{site.baseurl}}/planets/{{planet.folder}}/">{{planet.title}}</a>
		{{planet.content | markdownify}}