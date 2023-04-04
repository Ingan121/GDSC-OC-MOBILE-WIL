# What I Learned

## 플러터 위젯
* ```Widget build(BuildContext context) {}``` 안에 위젯들이 들어간다.
* Scaffold에는 appBar, body 등이 들어간다.
    * appBar: 상단 제목창
    * body: 메인 UI
    * floatingActionButton: 우하단 버튼
* 위젯 목록
    * Text: 그냥 텍스트
    * Container: 그냥 칸
    * Center: 가운데정렬
    * ListView: 스크롤 가능한 리스트 (width 무시하고 꽉채워짐)
    * Column: 세로 배열 (스크롤 불가)
    * Row: 가로 배열 (스크롤 불가)
    * SingleChildScrollView: Column 등을 스크롤 가능하게 해줌
    * Icon: 내장 [Material Icon](https://fonts.google.com/icons) 표시 (크기는 size 속성 이용해서 변경)
    * Image.network: 외부이미지 불러와서 표시
* Container 속성 목록
    * color: 색
    * width: 가로 길이
    * height: 세로 길이
    * style: 텍스트 스타일 (TextStyle)
    * decoration: 꾸미기 (BoxDecoration)
    * child: 하위 위젯
* TextStyle
    * fontSize: 글자 크기
    * fontWeight: 글자 굵기 (볼드체: ```FontWeight.bold```)
* BoxDecoration
    * color를 여기 넣을수도 있다.
    * boxShadow: 그림자 (BoxShadow)
    * border: 테두리 (모든곳에 테두리색 적용: ```Border.all(color: 색, width: 굵기)```)
    * borderRadius: 둥근 테두리 등 (```BorderRadius.circular(10)```)
    * shape: 동그랗게 만들기 등 (```BoxShape.circle```)
* BoxShadow
    * color: 그림자 색
    * blurRadius: 그림자 정도?

## 선언형 UI와 명령형 UI
* 선언형 UI: Flutter, SwiftUI 등
```
// Declarative style
return ViewB(
  color: red,
  child: ViewC(...),
)
```
* 명령형 UI: 기존의 것들
```
// Imperative style
b.setColor(red)
b.clearChildren()
ViewC c3 = new ViewC(...)
b.add(c3)
```
* 보다시피 선언형 UI의 코드가 훨씬 간결하다.
* 명령형 UI를 사용하는 일반 안드로이드 개발이나 C#, 웹개발 등에서는 명령형으로 UI를 전부 생성하기 골때려서 그런지 UI를 xml, html 등으로 따로 디자인하는 경우가 많던데 선언형 UI에서는 이럴 필요가 없는 모양이다.

[예시 출처](https://selfish-developer.com/entry/%EB%AA%85%EB%A0%B9%ED%98%95-UI-vs-%EC%84%A0%EC%96%B8%ED%98%95-UI)

## VSCode Flutter 개발 환경 설치
* Flutter는 이미 다 설치했으므로 그냥 Flutter 플러그인만 깔면 된다.
* 안드로이드 스튜디오와는 달리 SDK 경로도 자동으로 잡아준다.
* 명령 팔레트에 flutter 치면 여려 명령들이 나오는데, Select Device 들어가면 기기/플랫폼을 설정할 수 있다.
* 실행은 F5 누르면 된다.
* 그리고 VSCode가 안드로이드 스튜디오보다는 가벼운 것 같다.
* 또 VSCode에는 SSH로 원격 접속하여 로컬 환경처럼 쓰는 기능이 있다던데 나중에 이거갖고 가상머신 접속해서 iOS 빌드나 해봐야겠다.
<img width="1280" alt="4lSQGy813R" src="https://user-images.githubusercontent.com/34885971/229788514-82be913f-39e5-4f39-9191-75f5aff1b52c.png">
