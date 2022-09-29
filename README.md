# 깃 연습장
깃을 연습하는 저장소입니다. 불필요한 커밋은 삭제합니다.

# 깃 명령어

자주 쓰이는 명령어를 위주로 목록화합니다. 지속적으로 업데이트 중입니다.

- 폴더에서 버전 관리 시작하기
```
git init
```

- 깃에 계정 연동하기
```
git config --global user.email "메일주소"
git config --global user.name "계정명"
```

- 커밋에 추가할 파일 선택하기
```
git add 파일명
```

- 커밋에 대한 상세설명 추가하기
```
# `m`은 massage의 약자입니다. 
git commit -m "설명"
```

- 커밋 목록 확인하기
```
git log
```

- 이전 커밋으로 돌아가기
```
git checkout 커밋 코드 앞 부분 7자리
```

- 최신 커밋으로 돌아가기
```
git checkout -
```

- 로컬 저장소의 커밋을 원격 저장소에 올리기
```
git push origin master
```

- 원격 저장소의 커밋을 로컬 저장소에 내려받기
```
git pull origin master
```

- 깃허브 원격 저장소에 연동하기
```
git remote add origin 원격 저장소 주소
```

- 원격 저장소의 커밋을 로컬 저장소에 복제(clone)하기
```
# 원격 저장소 주소 뒤에 ' .'을 붙이면 폴더 안에 있는 파일만 복사합니다.
# 예컨대 https://github.com/LeeSeungwon89/Git_Test.git .형태입니다.
git clone 원격 저장소 주소
```

- 추가 

# 소스트리

사실 소스트리는 GUI라 굳이 메모할 필요한가? 일단 고민해보도록 하지
