깃 5장 정리

05-1 서로 다른 컴퓨터에서 원격 저장소 함꼐 사용하기

-원격 저장소 복제하기
- 깃 허브에 있는 원격 저장소(test-1)를 두 컴퓨터에 각각 git clone 명령으로 복제
- 복제 시 디렉터리는 자동 생성

-커밋 로그 확인
- git log 명령으로 각 디렉터리의 커밋 내역을 확인
- 복제한 저장소는 동일한 커밋 히스토리를 가짐

<집 컴퓨터에서 작업할 때>
-git_home 디렉터리에서 f1.txt 파일에 'C' 추가
-git commit- am "add C" 로 커밋 후 git push로 우너격 저장소에 업로드

<회사 컴퓨터에서 작업할 때>
-git_office 디렉터리에서 git pull로 최신 커밋을 받아옴
-f1.txt에 'd'추가 후 git commit -am "add d" 후 git push로 업로드

-git_home에서 git pull로 'add d'커밋을 받아 최신 상태 유지

05-2 원격 브랜치 정보 가져오기

- 원격 저장소 정보 가져오기
- git_office 디렉터리 git fetch 명령을 실행하면 원격 저장소의 최신 커밋 정보만 가져옴
- vim f3.txt로 f3.txt 새로운 파일 추가하기
- git add f3.txt
- git commit -m "create f3.txt"
- 이때 git log --online으로 확인하면 HEAD->main이 create f3.txt를 가리킴

- 커밋 차이 확인
- git diff HEAD origin/main 명령으로 원격 저장소의 최신 커밋을 지역 저장소에 병합
- git log --online으로 확인하면 HEAD, main, origin/main, origin/HEAD 모두 create f3.txt 커밋을 가리킴


05-3 협업의 기본 알아보기

- 원격 저장소 만들기
- github에서 새 저장소 생성(manials)
- 기본 브랜치로 main이 자동 생성됨
- README 파일 선택적으로 추가 가능

-브랜치 생성 및 관리
- 협업 시 충돌 방지를 위해 사용자별 브랜치를 만드는 것이 좋음
ex) [main] → apple 입력 → [Create branch apple from 'main'] 클릭
- 브랜치 목록 main,apple,ms 브랜치 확인 가능
- 각 사용자는 자신의 브랜치에 커밋하고, 팀장이 main 브랜치로 병합

-공동 작업자 추가하기
- 저장소의 [setting]탭 클릭-> Collaborators선택
- [Add people]버튼 클릭 후 이메일 또는 github 사용자명 입력
- 자동완성된 사용자 선택 -> [Add to this repository] 클릭
- 보안 강화된 계쩡은 비밀번호 입력 필요

-초대 수락 과정
- 초대받은 사용자는 github 알림 또는 이메일로 초대 메시지 수신

05-4 원격 저장소에서 협업하기

- 원격 저장소 생성
-github에서 저장소 생성
-README.md 파일 추가 -> main브랜치 자동 생성

-저장소 복제
-  git clone https://github.com/jjlaon/manuals.git manuals

- 브랜치 전환
- git switch apple

- 파일 생성 및 커밋
- vim apple.txt
-git add apple.txt
-git commit -m "초안 작성"

-원격 저장소에 푸시
-git push -u origin apple

-병합 확인
- PR이 병합되면 상태가 Merge로 변경된다.
-main 브랜치로 전환하면 apple.txt와 초안작성 커밋이 반영된 것을 확인 가능


=====문제 풀이=====
1. git clone
2. git fetch
3. git pull
4. git diff
5. git config user.name
6. git config user.email
7. git push




