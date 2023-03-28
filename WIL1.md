# What I Learned

## Flutter 3.7.7 설치 (윈도우)
* https://docs.flutter.dev/development/tools/sdk/releases?tab=windows 들어가서 3.7.7 다운받고 대충 압축풀고 ```systempropertiesadvanced.exe``` 들어가서 flutter\bin폴더 PATH 환경변수에 등록
* 안드로이드 스튜디오 설치
  * SDK Manager에서 Android SDK Command-line Tools 설치
  * Flutter 플러그인 설치
* cmd에서 flutter doctor 실행
```
C:\Users\User>flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[√] Flutter (Channel stable, 3.7.7, on Microsoft Windows [Version 10.0.22621.1413], locale ko-KR)
[X] Windows Version (Unable to confirm if installed Windows version is 10 or greater)
[√] Android toolchain - develop for Android devices (Android SDK version 33.0.2)
[√] Chrome - develop for the web
[√] Visual Studio - develop for Windows (Visual Studio Community 2022 17.5.0)
[√] Android Studio (version 2022.1)
[√] VS Code (version 1.76.2)
[√] Connected device (3 available)
[√] HTTP Host Availability

! Doctor found issues in 1 category.
```
* 윈도우 버전 오류 - [여기](https://ssscool.tistory.com/643) 보면 master 채널로 바꾸라던데 이러면 최신버전으로 올라가버려서 3.7.7로 재설치함
  * 윈도우11 깔려있는데 인식 못하는 것뿐이므로 그냥 무시
## 프로젝트 생성
* 안드로이드 스튜디오 메인 -> New Flutter Project -> Flutter 압축푼 폴더 선택 -> 프로젝트 정보 입력
* main.dart 파일이 메인 코드 파일
* 빌드: 초록 재생버튼, 그 옆에있는 드롭다운으로 기기/플랫폼 설정 가능
* WSA 에뮬레이터 연결: 그냥 adb connect localhost:(WSA 설정에 뜨는 포트번호) 하면 저 목록에 뜸
![55ern5YlVE](https://user-images.githubusercontent.com/34885971/228249697-5e97359e-fe21-459e-9ecf-10a4362bea36.jpg)
* 좌: 안드로이드 (Windows Subsystem for Android)
* 우: 윈도우 앱
* 뒤: 웹버전 (크롬)
* 안드로이드 빌드하는데 SDK 33인가가 없다고 오류나길래 SDK Manager에서 SDK 32버전이던거 34로 업뎃했더니 해결됨

## Flutter 3.7.7 설치 (맥)
* 맥북 없는 앱등이라 가상머신에 벤투라 깔고 Xcode 깔음
  * VMware WorkStation에 macOS 설치: [Unlocker](https://github.com/DrDonk/unlocker/releases) 설치 후 iso 구해서 설치 
* 그래픽 가속이 안돼서 GUI로 작업하기에는 속터지므로 SSH 접속해서 작업함
```
curl -O https://storage.googleapis.com/flutter_infra_release/releases/stable/macos/flutter_macos_3.7.7-stable.zip
unzip flutter_macos_3.7.7-stable.zip
rm flutter_macos_3.7.7-stable.zip
vi ~/.zshrc
export PATH="$PATH:~/flutter"
```

## 질문
* 윈도우 IDE에서 SSH 등으로 맥 연결해서 iOS 빌드하는 방법이 있나요?
