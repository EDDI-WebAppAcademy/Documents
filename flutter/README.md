## Flutter 설치

1. Android Studio 설치  
2. SDK 위치로 이동 -> Flutter SDK 설치(OS에 맞게 다운로드)  
   https://docs.flutter.dev/development/tools/sdk/releases?tab=windows  
   되도록이면 각종 side effect 를 피하기 위해 2.10.3 버전으로 통일한다.  
   https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_2.10.3-stable.zip  
4. 설치시 설치 경로를 c 혹은 d 드라이브에 flutter 로 배치하도록 한다.  
5. 자동 등록이 안된다면 윈도우 환경 변수 등록  
6. 터미널에서 flutter --version 을 통해 버전이 나오는지 확인한다.  

## 가장 무난한 방법

1. Android Studio 설치  
2. 안드로이드 스튜디오 실행 후 Ctrl + Alt + S 누름  
3. Plugins 에서 Flutter 찾아서 설치  
4. 설치 완료후 Android Studio 재실행  
5. File -> New Flutter Project 로 플러터 프로젝트 생성  

* 만약 이때 Flutter 를 못 찾는다는 메시지가 나타난다면 아래 위치에서 flutter 를 직접 다운로드 받도록 한다.  

SDK 위치로 이동 -> Flutter SDK 설치(OS에 맞게 다운로드)  
https://docs.flutter.dev/development/tools/sdk/releases?tab=windows  
되도록이면 각종 side effect 를 피하기 위해 2.10.3 버전으로 통일한다.  
https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_2.10.3-stable.zip  

추가적으로 압축을 풀어다 C 드라이브에 배치한다.  
그리고 환경 설정에 해당 경로를 배차하여 터미널에서 flutter --version 정보가 나오도록 설정한다.  

MaC 혹은 Linux 의 경우엔 아래와 같은 스크립트를 배치해야 한다.  
vi ~/.bash_profile 에 export PATH=$PATH:/home/계정/flutter/bin  
이후 source ~/.bash_profile 하면 적용 완료  
실제 Android Studio 터미널에서 구동 안될 경우 .zshrc 에 위의 작업을 동일하게 해줌  

7. Flutter App 선택하고 Next 신공  
8. 프로젝트 생성 이후 Android Stduio 자체 터미널에서 flutter doctor 입력  
9. Android Toolchain 문제가 거론된다면 flutter doctor --android-licenses  
10. 클래스를 못찾는다고 말한다면 SDK Manager -> SDK Tools -> Android SDK Command-line Tools 체크 후 설치  
