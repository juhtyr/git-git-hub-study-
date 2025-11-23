2장 정리

 02-1 깃 저장소 만들기
1.mkdir을 이용하여 새로운 디렉터리를 만들고, cd 명령어를 이용하여 디렉터리로 이동한다.
2.ls -a를 이용해 현재 디렉터리 안의 내용을 살펴본다. (-a라는 옵션은 숨김 파일이나 디렉터리까지 포함해서 보여달라는 의미)
3.ls -a를 하게되면 현재 디렉터리는.으로 표시되고, 상위 디렉터리는 ..으로 표시된다.
4.git init을 사용해 깃을 초기화 한다.
5. Initalized empty Git repository ~ 라는 메세지가 나타나면 깃을 사용할 수 있음.

02-2 버전 만들기
깃에서 버전이란 문서를 수정하고 저장할 떄마다 생기는 것
먼저 작업 트리에서 문서를 수정하고 수정한 파일 가운데 버전으로 만들고 싶은 파일을 스테이에 저장을 한다. 그릭 그 파일을 저장로소 커밋하면 버전이 만들어 진다.

git add:스테이징 명령어
git status: 무엇이 바뀌었는지 확인
git commit:깃에서 파일을 커밋
git log:저장소에 저장된 버전 확인

02-3

git diff:수정한 뒤 저장소에 있는 최근 버전과 비교

02-4
trackes파일: 최소 한번 커밋한 파일, 계속 수정사항이 있는지 추적
untracked 파일: 한번도 커밋하지 않았으며, 수정 내용을 추적하지 않는다.
git log --stat:커밋과 관련된 여러 통계를 보여준다.
git commit --amend:방금 커밋한 메세지 수정하기

02-5
git restore --stages ; 스테이지 모든 파일은 한번에 되돌리기
git restore --staged 파일명: 해당 파일만 골라서 되돌리기

<연습문제>

 user.name easys
 user,email doit@easys.co.kr
 init
 status
 add
 commit -m "ch01"
 commit -am "ch02"
 log
 diff
 restore work.txt
 restore --staged work.txt
 reset HEAD^
 reset 커밋 해시
 revert 커밋 해시
