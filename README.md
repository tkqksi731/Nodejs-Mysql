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
