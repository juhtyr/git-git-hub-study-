깃 스터디 4장 정리
원격 저장소란?
- 검퓨터나 서버에서 만든 저장소
- 지역 저장소와 연결되어 있으면서 백업과 협업이라는 중요한 역할을 한다.

지역 저장소와 원격 저장소
지역 저장소- 사용자 컴퓨터에 있는 저장소
원격 저장소- 깃허브레 있는 저장소
푸시(psh) - 지역 저장소에서 원격 저장소로 커밋을 등록하는 것
풀(pull)- 원격 저장소의 변경 사항을 지역 저장소로 내려 받는 것

원격 저장소 만들기
-저장소에 접속할 때는 HTTPS방식이나 SHH방식 중 택1
-원격 저장소의 HTTPS주소
https://github.com/아이디/저장소명

지역 저장소 만들기
cd~
git init loc-git
cd loc-git 
vim f1.txt(f1.txt파일 열기)

-f1.txt파일을 스테이지에 올린 후 커밋
git add f1.txt
커밋(add a)- git commit -m "add a"
git log

원격 저장소에 연결하기
-HTTPS주소 복사-> 터미널에 추가
git remote add origin [복사한 주소]

git remote -v(연결 확인)

지역 저장소와 원격 저장소 동기화 하기
-지역 저장소의 커밋을 원격 저장소로 푸시
git branch -M mian
git push -u origin main(지역저장소의 브랜치를 원격 저장소의 main 브랜치로 푸시)

vim f1.txt(f1.txt 파일 열기)
git comit -am "add b"(스테이징과 커밋 한번에 실행)
git push(원격 저장소로 푸시)

깃허브에 ssh원격 접속하기
1. cd ~ (홈 디렉터리 이동)
2. ssh-keygen
3, enter키 입력-> SSH키가 저장되는 디렉터리가 홈 디렉터리 안에 있는 .ssh이라는 것을 확인
4.enter키 2번 누르기 -> SSH 접속을 위한 비밀번호 만들어짐
화면에 id_rsa는 파일 프라이빗 키, id_sra.pub파일은 퍼블릭 키
5. cd.ssh
6. ls -al(.ssh디렉터리로 이동 후 안에 내용 확인)

SSH 주소로 원격 저장소 연결하기
1. 깃버흐에 새 원격 저장소를 만든다.
2. SSH주소 복사
3. 홈 디렉터리로 이동 후, connect-ssh라는 디렉터리 저장소를 만들어 이동
4. git remote add origin [SSH주소]
5. 확인
6.vim으로 파일을 만든 후 글을 입력하고 저장
7. 스테이징과 커밋 진행
8. push를 사용해 원격 저장소로 푸시


======4장 문제======
1. git remote add
2. git remote -v
3. git push -u origin main
4. git push
5. git pull
6. ssh-keygen
