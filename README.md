# Node.js & Mysql

```cmd
git init
```

git 초기화

```cmd
npm init
```

npm을 통한 초기화

```cmd
npm install
```

npm 설치

---

1. Node.js & Mysql Connection
   - node.js 설치 필요한 것
   ```cmd
   npm install mysql
   ```
2. Node.js & Mysql Mysql로 홈페이지 구현
   - 메인 페이지 변경 index.js
3. Node.js & Mysql 글 생성 기능 구현
   - create 부분 sql로 변경
4. Node.js & Mysql 글 수정 기능 구현
   - update 부분 sql로 변경
5. Node.js & Mysql 글 삭제 기능 구현
   - delete 부분 sql로 변경
6. Node.js & Mysql 작성자가 누군지 구현
   - 상세보기 부분에서 LEFT JOIN author On topic.author_id=author.id WHERE topic.id=? 삽입
   - 보기 위하여
   ```js
   <p>by ${topic[0].name}</p>
   ```
   작성
7. Node.js & Mysql JOIN 글 생성 구현
   - db 부분에서 author의 id, name를 넣어 create버튼을 누를 시 하단에 목록으로 egoing, duru, teaho가 나옴
   - template 부분에서 제일 하단 부분에 ,를 넣고 밑에 코드를 삽입
   ```js
   ,authorSelect:function(author){
    let tag = '';
    let i = 0;
    while(i < author.length){
      tag += `<option value="${author[i].id}">${author[i].name}</option>`;
      i++;
    }
    return `
    <select name="author">
    ${tag}
    </select>
    `
   ```
8. Node.js & Mysql JOIN 글 수정 구현
   - update 부분에 db.query(... author) 을 가져와 기존의 코드를 {}안으로 변경
   - template에서 while 부분(authorSelect:function(author){})에 밑에 코드를 삽입
   ```js
   let selected = "";
   if (authors[i].id === author_id) {
     selected = " selected";
   }
   ```
