# git_cancel
Git Commit Cancel Test

##  Git 작업 취소하기
###	< commit 작업 취소 >
	- HEAD 를 이전 식별자로 옮기고 상태를 Staging 으로 변경하기 ( 최신 commit 취소 )
	  git reset --soft HEAD~   ( HEAD 만 이동된 상태 )
	  git restore <file path>  ( 파일까지 복원된 상태 )
	- HEAD 를 이전 식별자로 옮기고 상태를 working directory 작업내용으로 변경하기( 최신 add 취소 )
	  git reset --mixed HEAD~
	  git restore <file path>
	- HEAD 를 이전 식별자로 옮기고 상태를 working directory 작업내용 마저 취소
	  git reset --hard HEAD~
	  git restore <file path>
	- Local 저장소의 모든 변경내용을 취소하고 원격저장소의 내용으로 복귀
	  git fetch origin
	  git fetch --hard origin/master
	
###	< file 작업 취소>
	- 최신 commit 나 add 에서 해당 파일을 삭제하고 해당 파일을 working directory 작업내용으로 복귀시킴
	  git rm --cached <file path>
	- 해당 파일 식별자의 Staging 상태( add 된 상태 )로 복원
	  git checkout <식별자> -- <file path>
	- 최신 commit 나 add 에서 물리적인 파일삭제
	  git rm -f <file path>		  
	  
	- 특정식별자 상태의 소스내용 확인하기
	  git checkout <식별자>

	  
###	( 기타 : 차이점 확인하기 )
	- 최신 commit 과 working 영역의 차이점 확인하기
	  git diff
	- 최신 Staging 영역과 working 영역의 차이점 확인하기
     	  git diff --staged	
	- 특정 파일의 변경사항 이력확인
	  git log -- <file path>
	- 원격 저장소 변경여부 확인하기
	  git fetch origin
