# git_cancel
Git Commit Cancel Test

##  작업 취소하기
	- HEAD 를 이전 식별자로 옮기고 상태를 Staging 으로 변경하기 ( 최신 commit 취소 )
	  git reset --soft HEAD~
	  git restore <file path>
	- HEAD 를 이전 식별자로 옮기고 상태를 working directory 작업내용으로 변경하기( 최신 add 취소 )
	  git reset --mixed HEAD~
	  git restore <file path>
	- HEAD 를 이전 식별자로 옮기고 상태를 working directory 작업내용 마저 취소
	  git reset --hard HEAD~
	  git restore <file path>	  
	- 최신 commit 나 add 에서 해당 파일을 삭제하고 해당 파일을 working directory 작업내용으로 복귀시킴
	  git rm --cached <파일명>
	- working directory 의 변경사항까지도 모두 취소하고 그 이전의 commit 으로 복귀
	  git checkout --<파일명>
	- Local 저장소의 모든 변경내용을 취소하고 원격저장소의 내용으로 복귀
	  git fetch origin
	  git fetch --hard origin/master
	- 최신 commit 나 add 에서 물리적인 파일삭제
	  git rm -f <파일명>	
	- 특정식별자 상태의 소스내용 확인하기
	  git checkout <식별자>
	  
	( 기타 : 차이점 확인하기 )
	- working directory 의 현재 파일과 최신 commit 파일간의 차이점 비교하기
	  git diff
	- working directory 의 현재 파일과 staging 파일과의 차이점 비교하기
     git diff --cached/staged
