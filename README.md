# InnoDB 8.0 Reference Manual

[MySQL 공식 레퍼런스 메뉴얼](https://dev.mysql.com/doc/refman/8.0/en/)에서 제공하는
내용 중, InnoDB 파트만을 분리하여 한글 번역본으로 제공합니다. InnoDB와 밀접히
연결된 경우에는 MySQL 파트에 대한 자료도 업로드 될 수 있습니다. 

MySQL/InnoDB와 관련된 추가적인 문서, 연구 자료나 논문 등도 업로드 될 수 있습니다. 

## Setup local server with Hexo

> 로컬 서버에서 테스트하기 위해서는 `npm`이 필요합니다. 

본 리포지토리를 clone 한 뒤 `yarn` 혹은 `npm i`를 실행하여 필요한 패키지들을 설치합니다.
`hexo`가 설치되어 있지 않은 경우 `npm i hexo-cli -g`를 통해 hexo 커맨드라인 툴을 설치합니다. 
모든 설치 작업이 정상적으로 완료된 경우 `hexo server`를 통해 로컬 서버를 실행하고,
웹 브라우저에서 `http://localhost:4000`을 통해 접속합니다. 

### Github page로 deploy 하기

작업이 완료된 이후 `hexo deploy -g` 를 통해 github로 deploy 한다.

## 문서 작성 요령

번역된 문서는 `source/blog` 안에 위치한다. 각각의 대주제에 맞도록 폴더를 구성하며, 현재까지는 InnoDB에 대한
번역만을 제공하므로 `source/blog/innodb` 폴더만 존재한다. 각 포스트의 이름은 주제가 뭔지 알 수 있도록
명확하게 명시한다. 마크다운을 이요하여 글을 작성할 때, 링크나 이미지의 주소는 본문에 바로 적지 않고,
아래의 예제처럼 참조연산을 사용한다.

```markdown
[이 링크의 주소를 본문에 바로 삽입하지 말고 참조를 사용하세요][use-reference]
[Direct reference]도 사용할 수 있습니다.
... 글의 다른 내용들....


.... 포스팅 마크다운 파일의 최 하단부 ....
[use-reference]: https://flashsql.github.io/innodb-doc-kr
[Direct reference]: https://flashsql.github.io/innodb-doc-kr
```