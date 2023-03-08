# TIL
----------------------------------------------------------------------------------------------------------------------
					버전관리의 본질
----------------------------------------------------------------------------------------------------------------------
<버전 만들기>

git config --global user.name "자신의 닉네임" (버전에 포함될 버전 만들때 사용, 한번만 하면 됨 -> 이제 안함)
git config --global user.email "자신의 이메일"

git init (현재 디렉토리 버전관리)

vim 파일명.형식자 (파일 만들기)

git status (폴더의 상태 확인, 빨간색)

git add 파일명.형식자 (깃에게 파일을 추적하도록 명령, 수정할 때마다 해야함, 커밋 대기로 바뀜)

git status (폴더의 상태 확인, 초록색)

git commit (깃에 최종적으로 버전저장)

git log (지금까지 올린 버전 확인 가능 저자, 시기 확인 가능)

----------------------------------------------------------------------------------------------------------------------
<버전 효용 -> 과거와 차이점 알기, 과거로 돌아가기 가능>

git log -p (차이점 알 수 있음)  -> q 눌러서 화면 닫기

git diff commit주소1..commit주소2 (commit주소1와 commit주소2의 차이점 보여줌)

git diff (git add 전후 비교) 

git reset commit주소 --hard (commit주소 다음 log 삭제됨)   (더 찾아보고 할 것)
git revert "commit주소" (commit주소만 없어짐)

----------------------------------------------------------------------------------------------------------------------
					git의 원리
----------------------------------------------------------------------------------------------------------------------
 파이썬 설치 후 Gistory 설치

sha1 online

----------------------------------------------------------------------------------------------------------------------
					git의 혁신 - branch
----------------------------------------------------------------------------------------------------------------------
git commit -m "메시지" (커밋 메시지 저장)

git branch (현재 사용중인 브랜치 확인)

git branch 브랜치명 (브랜치명으로 브랜치 생성)

git checkout 브랜치명 (브랜치명으로 브랜치 전환)

git log 브랜치명1 .. 브랜치명2 (브랜치명1과 브랜치명2를 비교)

git diff 브랜치명1 .. 브랜치명2 (브랜치 간의 코드 비교)

git log --branches --graph --decorate --oneline (로그의 모든 브랜치, 그래프, 브랜치 명, 한줄로 표시)

git checkout A	(A 브랜치로 B 브랜치를 병합 A <- B)
git merge B

git branch -d 브랜치명 (브랜치 강제로 지우기)

git stash (실행 중인 일, 인덱스 내용 저장)

git reset --hard HEAD (가장 최근 커밋상태로 돌림, 리셋)

git stash apply (제일 최신 스태시 사용, 삭제안됨, stash {0}을 적용)

git stash list (스태시 리스트, 남아있는게 보임 -> 명시적으로 삭제하지 않는 이상 살아있음,	{0} 방금 처리 {1} 아까 처리)

git stash drop (스태시 삭제)

git stash pop (apply하고 drop하는 것을 동시에 실행)

----------------------------------------------------------------------------------------------------------------------
					원격저장소
----------------------------------------------------------------------------------------------------------------------
부모 디렉토리로 이동 후
git init --bare 디렉토리이름 (작업수행은 안되는 저장소 'bare' 만들기)

git remote add orgin /주소 (주소의 별명이 orgin으로 설정)

git push (원격저장소로 업로드 됨)

git log (commit 전달 내용 확인 가능)
