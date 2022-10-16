# 깃 연습장
깃을 연습하는 저장소입니다. 불필요한 커밋은 삭제합니다.

Git을 공부하기에 좋은 서적은 **팀 개발을 위한 Git, GitHub 시작하기(한빛미디어)** 입니다.
설명이 매우 쉽고 구체적입니다. 차근차근 읽고 실습하다 보면 현업에서 깃을 사용하기에 부족함이 없는 수준에 도달할 것입니다.

# 깃 명령어

자주 쓰이는 명령어를 위주로 목록화합니다. 지속적으로 업데이트 중입니다.

깃에 숙달해지면 작업 속도를 높이거나 세세하게 제어하기 위해 CLI를 사용하는 편이 좋습니다.
dsf
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

- 커밋에 대한 상세설명 추가하여 커밋하기
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

- 추가 예정

# 소스트리

사실 소스트리는 GUI라서 굳이 메모가 필요할까? 사용법이 간단해서 음. 일단 고민해보도록 하겠습니다. 소스트리 설치 방법은 유튜브를 참고하시기 바니다. 별도의 계정 가입 절차 없이 깃허브 계정만으로 바로 사용할 수 있습니다.
