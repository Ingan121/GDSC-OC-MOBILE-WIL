# What I Learned

## Container 여백
* margin: 바깥
* padding: 안

## 안드로이드 에뮬레이터 설정
* 안드로이드 스튜디오 -> Virtual Device Manager -> Create Image -> 이미지 다운로드 후 가상기기 생성
* 설치만 하면 VSCode에서도 인식됨
* 근데 ADB연결만 되면 인식되서 WSA나 블루스택 등 기타 에뮬레이터를 써도 무방할 것 같다.
* 밑에 저거 만들때는 WSA랑 안드10롬 올린 S7 공기계로 테스트했다.

## [갑자기 뭐 하나 떠올라서 만든 앱](https://github.com/Ingan121/PaymentRedirector) 만들면서 알게된거
* ```void initState()```: 앱 시작시 실행되는 코드 [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L128)
* ```setState(() {})``` 안에서 변수 변경해야 UI에 반영됨
* ```systemOverlayStyle```: 상하단바 커스텀 [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L87)
* 삼항연산자로 위젯 표시 여부 결정 가능. 숨기려면 그냥 Container() [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L115)
* Dart 구버전에서는 null 체크가 빡빡하지 않았는지 예전자료 갖다쓰면 null에서 에러나는경우 많음
* 모듈 설치: pubspec.yml dependencies 하위에 모듈명: 넣고 저장하면 알아서 설치됨
* uni_links: URL Scheme 처리 모듈
* qr_flutter: QR코드 쉽게 띄우는 위젯 [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L115)
* url_launcher: 브라우저 열어주는 모듈 [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L80)
* package_info_plus: 앱 정보에서 버전 가져오는 모듈 [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L130)
* flutter_svg: SVG 띄우는 모듈 [#](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/lib/main.dart#L77)
  * 로컬 svg 띄우기: 프로젝트 내부에 svg 넣고 pubspec.yml에 [이런식](https://github.com/Ingan121/PaymentRedirector/blob/934ea1f4a9a7758b84472dd2d523d870cf121971/pubspec.yaml#L66)으로 에셋 경로 등록해야함
