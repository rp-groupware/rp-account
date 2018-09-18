# 계정 레파지토리 생성 가이드
##### openldap(https://www.openldap.org/)을 계정 레파지토리로 한다.
##### linux 계열을 우선 지원


## openldap 설치
```
Mac의 경우 HomeBrew가 설치되어 있지 않으면, 먼저 설치하자!
(https://brew.sh/index_ko)

#터미널에 붙여넣기(HomeBrew설치)
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# openldap 설치 완료
brew install openldap

# 설치된 경로 (설치 시점에 따라 버전은 상이할 수 있다.)
# /usr/local/Cellar/openldap/2.4.46

```
* version : 2.4.46 (https://www.openldap.org/software/download/)
* 설치 가이드 참고 (https://www.openldap.org/doc/admin24/quickstart.html)
1. download
   * wget ftp://ftp.openldap.org/pub/OpenLDAP/openldap-release/openldap-2.4.46.tgz
2. 압축풀기
   * gunzip -c ./openldap-2.4.46.tgz | tar xvfB - 
   * cd ./openldap-2.4.46
3. build
   * ./configure
   * make depend
   * make
   * make test
   * su root -c 'make install'
