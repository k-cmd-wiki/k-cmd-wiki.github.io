# k-cmd-wiki.github.io

https://k-cmd-wiki.github.io/

## 페이지 구조

.html 파일 하나만으로 구성된 SPA(싱글 페이지 애플리케이션) 웹사이트이며, 사용자의 컴퓨터에서 여기 깃허브 리포지토리의 데이터를 불러오는 식으로 동작합니다.

홈화면은 클라이언트가 chapters.txt 파일을 불러와서 그에 맞게 버튼과 부제목을 생성하며, 하위 페이지는 pages 폴더의 .md 파일을 불러와서 html 코드로 변환하는 식으로 동작합니다.

### chapters.txt

chapters.txt 파일은 줄단위로 파싱되며, 맨 오른쪽과 맨 왼쪽에 있는 공백을 무시합니다.

비어있는 줄이나, 하이픈(`-`) 기호로만 이루어져 있는 줄이나, 공백으로만 이루어져 있는 줄 또한 무시됩니다.

세미콜론(`:`) 기호가 정확히 1개 배치되어 있는 텍스트는 버튼으로 인식됩니다. 세미콜론의 왼쪽이 버튼의 이름이며, 세미콜론의 오른쪽은 연결할 하위 페이지의 파일명입니다. 하위 페이지는 pages 폴더 내부에 있는 .md 파일만 인식하며, chapters.txt 파일에는 확장자 없이 작성하세요.
```
버튼 이름 : test
```

그 외의 텍스트는 부제목으로 인식됩니다. 맨 오른쪽과 맨 왼쪽에 있는 공백을 무시한 해당 줄 전체가 제목으로 판정됩니다.
```
이건 제목입니다. 예. 이게 제목이라고요.
```

제목 밑에 버튼을 나열하는 식으로 페이지가 구성됩니다. 이건 뜯어보시는게 이해가 더 빠릅니다.
```
이건 제목입니다. 예. 이게 제목이라고요.
    버튼 이름 : test
    다른 버튼 이름 : asdf
    버튼 이름을 뭐로 하지 : QWERSDAFASDGREBHRSEG
```
