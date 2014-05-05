윈도우즈 + GNU C Compiler + Code::Blocks
======================================= 
----  

CygWin 설치하기
--------------

*윈도우 7 64bit 에서 Cygwin을 설치하는 방법*  

* Cygwin홈페이지<http://www.cygwin.com>에서 설치파일<http://cygwin.com/setup-x86_64.exe>을 d:\cygwin_pkg에 다운로드

* setup-x86_64.exe 실행
	* Choose A Download Source 에서 Install from Internet 선택
    * Select Root Install Directory 에서 기본값인 C:\cygwin64 사용
    * Select Local Package Directory 에 d:\cygwin_pkg 입력
        * 설치할 패키지를 다운로드할 디렉토리이며, 설치후 삭제해도 됨
    * Select Your Internet Connection 에서 Direct Connection 선택
    * Choose A Download Site 에서 **http://ftp.jaist.ac.jp** 선택
        * apt-cyg(우분투의 apt-get 과 유사한 프로그램)에서 레포지토리로 사용됨
    * Select Packages 에서 curl, wget, patch 선택
	    * search 해서 선택하는 것이 쉬움.
	    * curl은 net 그룹에, wget은 web 그룹에, patch는 devel 그룹에 있음.
	* → 설치완료

* 환경변수 수정
	* PATH 에 C:\cygwin64;C:\cygwin\bin64 추가
	* 환경변수 CYGWIN_HOME을 만들고 C:\cygwin64로 설정

* apt-cyg 설치
	* 바탕화면의 Cygwin64 Terminal을 실행하여 다음 명령 실행
	> $ curl http://apt-cyg.googlecode.com/svn/trunk/apt-cyg \> /usr/local/bin/apt-cyg  
	> $ chmod +x /usr/local/bin/apt-cyg  
	> $ apt-cyg update -m http://ftp.jaist.ac.jp/pub/cygwin  

* 개발에 필요한 프로그램 설치
    > $ apt-cyg install autoconf make gcc-g++ flex bison gdb 



Code::Blocks 설치하기
--------------------
*MinGW를 사용하지 않고 Cygwin을 사용하도록 Code::Blocks 설정*


#### 기타

* Cygwin terminal에서 폰트 바꾸기
    > echo 'Font=NanumGothicCoding' >> ~/.minttyrc  
    > echo 'FontHeight=10' >> ~/.minttyrc  
    > echo 'CursorType=Block' >> ~/.minttyrc  
