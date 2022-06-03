# React-Github
React 깃허브.io와 연결하기
## https://parkyongjun03.github.io/React-Github/

### 1. 깃허브에 레포지토리 만들기
### 2. VS code 켜서 Ctrl+Shigt+N(새창 열기) -> Github와 연결된 레포지토리 복제하기
  - ![image](https://user-images.githubusercontent.com/83456300/171770390-ef6bd0a9-46c6-483b-b93e-06f3972194be.png)
  -  레포지토리가 위치할 폴더 선택
  -  폴더 열기로 {해당 레포지토리} 열기
  -  작업 영역 만들기
### 3. 'npx create-react-app myreact'
  - 대문자 안 됨
  - 'myreact' 여기에 react 폴더 명 써넣기
### 4. 'cd myreact'
### 5. 'npm install gh-pages --save-dev'
  - 'myreact'폴더 안에서 써야 myreact 폴더 안에 있는 package.json에 입력이 된다.
  - 저거 쓰면   "devDependencies": {
                "gh-pages": "^4.0.0"
                }
                이게 추가 된다.
### 6. "homepage": "https://ParkYongJun03.github.io/React-Github",
{
  "name": "myreact",
  "version": "0.1.0",
+ "homepage": "https://{gitname}.github.io/{repository}",
  "private": true,
  }
### 7. 
  "scripts": {
+   "predeploy": "npm run build",
+   "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
### 8. $ git remote add origin https://github.com/ParkYongJun03/React-Github.git
  - 사용자에 따라  'git remote remove origin' 를 써야할 수도 있다.
  - 'git remote add origin https://github.com/{username}/{repo-name}.git'
  - ![image](https://user-images.githubusercontent.com/83456300/171771793-bb2da1f6-a8ce-4bee-975d-f868f7086533.png)
  - 분기를 정하고  Terminal에서 Enter 한 번 치면 저렇게 바뀐다
  - ![image](https://user-images.githubusercontent.com/83456300/171771893-49f3f76a-bed3-4bbe-8e2a-0996125a51a0.png)

### 9. 'npm run deploy'
  - ![image](https://user-images.githubusercontent.com/83456300/171772065-f5cd1095-2967-4fc8-80eb-7496429538ba.png)
  - deploy를 하고나면 위와 같이 branch에 gh-page가 생기게 된다.

### 10. 주의!
  - App.js 파일을 수정할때마다 'npm run deploy'를 해야 깃허브.io에 연동이 된다.

