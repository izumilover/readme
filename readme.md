gitHub 연동법


1. gitHub 가입
	-https://github.com

2. git 설치
	
	-https://git-scm.com/
	에서 윈도우버전을 다운받아 설치한다.

3. 에디터 설치 및 셋팅
	
	1. PHPStrom, WEBStrom
		- https://www.jetbrains.com/phpstorm/
		- https://www.jetbrains.com/webstorm/
			에서 다운로드 후 설치한다.
		- 30일 동안 사용가능.
		- 에디터 자체에서 git 연동을 제공

	2. editplus
		
		- SourceTree 또는 GitHub Desktop 설치 후 연동
		- SourceTree 설치
			http://hackersstudy.tistory.com/41 참조

	3. Atom
		
4. PHPStrom, WEBStrom gitHub 연동
	
	1. 기본 설정
		
		- 에디터실행
		- ctrl + alt + s 로 settings 열기
		- settings > Version Control > git 클릭
			Path to Git executable 에 git.exe 경로를 셋팅한다.
		- settings > Version Control > GitHub 클릭
			Host : github.com
			Auth Type : Password
			Login : github 본인 계정
			password : github 본인 계정 비번
			입력 후 test 로 확인 성공이 뜨면 완료
		- 설정완료

	2. gitHub clone 하기
		
		- VCS > checkout from version control > gitHub 클릭
			
			Git Repository Url : git@github.com:XXXXX/XXXXXXXX.git (GitHub 에 저장된 저장소 경로)
			Parent Directory : 작업폴더
			Directory Name : 작업폴더명
			입력 후 Clone 클릭


	3. branch 생성
		- master branch 에서 별개의 저장소를 생성한다.
		- 이 후 작업은 생성된 branch 에서 한다.

		- VCS > Git > Branches 클릭
		- New Branch
		- branch 명 입력 후 OK


	4. commit
		- 변경사항을 임시 저장한다.

		- Ctrl + k
		- Commit Message 필히 입력 (간략하게 수정내용을 입력)
		
		- After Commit 부분에 업로드 서버를 지정 (Always use selected server 체크)
		  커밋 후 서버에 자동 업로드 함.

		- Commit or Commit and Push 클릭

	5. push
		- 커밋된 변경사항을 저장소에 적용한다.	
		- ctrl + shift + k
		- Push 클릭

	6. update project
		- 변경된 파일이 있는지 체크 한 후 변경사항이 있으면 가져온다.

		- VCS > update project (ctrl + t)
		- Merge
		- OK 클릭
		
	7. Merge
		- 로컬파일과 저장소의 파일이 틀릴 경우 Merge 한다.

	8. Pull
		- 변경된 파일이 있는지 체크 한후 변경사항이 있으면 가져온다.

		- VCS > Git > Pull
		- 가져올 branch 를 선택한다. ( 본인의 branch 와 master branch 를 체크)
		- Pull 클릭

5. 파일색상에 따른 구분
	
	1. 파란색
		- 작업자가 변경한 후 커밋전 파일
	
	2. 녹색
		- 신규로 생성된 파일 중 커밋전 파일

	3. 회색
		- 커밋이 불가능한 파일
		- .gitignore 파일에 설정
		- 공유하면 안되는 파일 등에 적용한다. (config 파일 등)

	4. 빨간색
		- 오류파일

	5. 하얀색
		- 변경점이 없거나 커밋이 완료된 파일

6. Pull request
	
	- github 사이트에서 처리
	- 해당 프로젝트의 저장소로 이동
	- 상단의 branches 클릭
	- New pull request 가 존재할 경우 클릭
	- 하단의 상세정보에서 변경사항을 확인
	- 정상이라면 코멘트 작성 후 Create pull request 클릭
	- Merge pull request 클릭 
	- Confirm merge 클릭
	- master branch 적용확인


7. 용어설명
	1. git
		- 버전관리 툴, 비슷한걸로 subversion 이 있다.
	2. github
		- git에 기반한 소셜저장소
	3. clone
		- master branch 저장소에서 소스를 받아온다.
	4. commit
		- 변경사항을 저장한다.(임시저장)
	5. push
		- 변경사항을 저장소에 업데이트 한다.
	6. pull
		- 변경된 소스를 가져온다.
	7. branch
		- 저장소
