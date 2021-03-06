---
id: getting-started
title: Getting Started
---


React native 환경설정

	0.	Homebrew 설치  (MacOS 만 설치 가능)
      - https://brew.sh/index_ko


	0.	Xcode 설치 (MacOS 만 설치 가능)
     - AppStore Xcode 설치


	0.	Java JDK8 설치 (Oracle 계정 필요)
     3.1 download URL : https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
     3.2 본인 PC OS에 맞는 버전 설치 할 것
     3.3 MacOS brew 설치 방법 (https://jojoldu.tistory.com/329)
       3.3.1 Homebrew 최신 업데이트(터미널 사용)
         - brew update && brew upgrade brew-cask && brew cleanup && brew cask cleanup
       3.3.2 Java 최신버전 brew를 통해 설치 (터미널 사용)
         - brew cask info java
         - brew cask install java
       3.3.3 Java의 버전을 관리해주는 jenv 패키지 설치 (터미널 사용)
         - brew install jenv
       3.3.4 .bash_profile에 코드를 추가하여 jenv 초기화 (터미널 사용)
         - 계정 홈 디렉토리에서 실행 -> vi $HOME/.bash_profile
         - 코드추가 : if which jenv > /dev/null; then eval "$(jenv init -)"; fi
         - 저장 -> :wq
          - 프로파일 실행 -> source $HOME/.bash_profile  

       3.3.5 Java8 설치 (터미널 사용)
         - brew tap cask room/versions
         - brew cask install java8
         - java 설치 디렉토리 확인         

         - 설치된 Java8 jenv 관리 항목에 추가 -> jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_202.jdk/Contents/Home/
         - 설치된 다른버전 java jenv 관리 항목에 추가 -> jenv add /Library/Java/JavaVirtualMachines/openjdk-12.jdk/Contents/Home/
       3.3.6 설치된 Java8 전역&로컬 버전 설정
         - jenv global oracle64-1.8.0.202
         - jenv 설정 확인 -> jenv version

	0.	 VSCODE 프로그램 설치
    - https://code.visualstudio.com/
    - 설치완료 후 프로그램 에서 cmd+shift+p 실행
    - 셸 명령: PATH에 ‘code’ 명령 설치 선택 실행  


	0.	React Native 설치
     5.1 가이드 
       - https://facebook.github.io/react-native/docs/getting-started
       - React Native CLI Quickstart 참고
       - PC MAC -> developmentOS : macOS / Target OS : IOS, AOS 모두 가이드별 설치
       - PC Windows ->  developmentOS : Windows / Target OS : AOS 가이드 설치 (IOS 지원안됨)    
     5.2 필수 설치
       5.2.1 node, watchman, yarn 설치
         - brew install node
         - brew install watchman
         - brew install yarn
       5.2.2 React native CLI 설치
         - npm install -g react-native-cli

	0.	Xcode  (MacOS 만 가능)
    - Xcode 환경설정 : https://facebook.github.io/react-native/docs/getting-started#command-line-tools

	0.	Android 설치
    7.1 Android Studio 설치 : https://facebook.github.io/react-native/docs/getting-started#1-install-android-studio
      - Android studio 설치 단계 Install Type은 반드시 Custom으로 선택 해야 됨. (Standard 선택 시 스튜디오 완전 삭제후 재 설치 필요)

    7.2 Android SDK 설치 : https://facebook.github.io/react-native/docs/getting-started#2-install-the-android-sdk
    7.3 ANDROID_HOME 환경변수 구성 : https://facebook.github.io/react-native/docs/getting-started#3-configure-the-android-home-environment-variable
 
	0.	프로젝트 다운로드 (Mac OS gitlab 계정 필요)   
    - maf client 다운로드 : https://gitlab.com/nullvana/maf-cli#installation / npm i -g git+https://gitlab+deploy-token-51357:WQcTK6oy7-6a1AymSw_c@gitlab.com/nullvana/maf-cli

    - maf client 전역 선언 : /usr/local/lib/node_modules/maf-cli>npm i -g .

    - maf client 실행 : /usr/local/lib/node_modules/maf-cli>nam run tsc

    - vscode로 소스 보기 : $HOME/work/maf-starter-default>code .

    - vscode에서 터미널 실행 : ctrl +` 
    - package.json 파일 내 명시된 Node.js 모듈 설치 : /usr/local/lib/node_modules/maf-cli>npm i
    - 설치된 Node.js 모듈 전역설정으로 설치 :/usr/local/lib/node_modules/maf-cli>npm i -g

    - maf-starter-default 설치 : $HOME/work>maf init
    - app 이름 입력


	0.	프로젝트 실행
    8.1 IOS : $HOME/work/maf-starter-default>yarn iOS
    8.2 AOS 
      - 안드로이드 스튜디오 실행 가상 디바이스 실행

      - $HOME/work/maf-starter-default>yarn android


##release. ## keystone 필요
 > yarn run android:release

Macintosh HD⁩ ▸ ⁨사용자⁩ ▸ ⁨stlee⁩ ▸ ⁨work⁩ ▸ ⁨maf-starter-default⁩ ▸ ⁨android⁩ ▸ ⁨app⁩ ▸ ⁨build⁩ ▸ ⁨outputs ▸ app ▸ ⁩release ▸ app-release.apk


## Generating Signed APK (keystone)
https://facebook.github.io/react-native/docs/signed-apk-android

# VSCode 확장 프로그램
ESLint - Dirk Baeumer
GitLens - Eric Amodio
TsLint - Microsoft
Prettier - Code from - Esben Petersen
Flow language support
@builtin TypeScript and JavaScript - 사용 안 함

