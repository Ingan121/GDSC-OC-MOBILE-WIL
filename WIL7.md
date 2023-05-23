# What I Learned

## Wrap 위젯
* 화면 크기에 맞도록 크기가 고정된 자식 위젯들의 배치를 조절해주는 위젯
* direction: 나열 방향 (Axis.horizontal / Axis.vertical)
* alignment: 정렬
* spacing: 같은 줄 내 위젯 간 간격 (horizontal: 좌우, vertical: 상하)
* runSpacing: 줄 간격 (horizontal: 상하, vertical: 좌우)

## AspectRatio 위젯
* 이미지 비율 맞추는 위젯
* aspectRatio: 비율 (16 / 9, 4 / 3 등 가로 / 세로로 입력. 계산된 값 넣어도 되고 나눗셈 직접 넣어도 무방)

## AppBar 속성
* backgroundColor: AppBar 배경색
* bottom: AppBar 밑에 넣을 위젯 및 하단 영역 크기. PreferredSize 위젯을 이용하며 하단 영역 크기를 조절하며, 그 안에 child를 넣을 수 있음. 여기서는 구분선을 넣기 위해 사용
* elevation: 머티리얼 디자인 elevation 효과, 높을수록 그림자 세짐 (그만큼 떠있다는 디자인)
* centerTitle: 제목 중앙 정렬 여부
* iconTheme: leading 등 아이콘 색상 변경
* leading: AppBar 좌측 위젯
* title: AppBar 제목 영역 위젯

## GridView 위젯
* 그리드(바둑판식?) 배열 해주는 위젯. GridView.builder를 이용해 하나의 위젯 정의로 여러 위젯을 띄울 수 있다.
* gridDelegate 속성을 이용하여 각 위젯의 크기, 개수, 간격 등 조절
  * 위젯 내 width, height 등은 먹지 않는 듯 하다.
  * crossAxisCount: 하나의 행에 보여 줄 아이템의 개수
  * childAspectRatio: 아이템의 가로, 세로 비율. 위의 AspectRatio와 같은 형식으로 비율 입력
  * mainAxisSpacing: 수평 빈 공간
  * crossAxisSpacing: 수직 빈 공간
* itemBuilder: 위젯 정의, index를 이용하여 몇번째 위젯인지 알아내고 알맞은 정보 표시

## Navigator
* push: 페이지 열기
  * 페이지 소스 파일 임포트 하고 아래와 같은 방식으로 사용
  * 페이지명 함수 내에 인자 넣어서 데이터 전달 가능
```
Navigator.push(
    context,
    MaterialPageRoute(
        builder: (context) => PageName(
            property1: value1,
        ),
    ).
)
```
* pop(context): 뒤로가기

## GestureDetector 위젯
* 입력 감지하는 위젯
* onTap에 터치 시 작동할 함수 넣기
* 비슷한 것으로 머티리얼 물결효과 지원하는 InkWell이 있다. 그러나 배경색이 있으면 효과는 안보인다.

## 질문
![6SE1GdQrwj](https://github.com/Ingan121/GDSC-OC-MOBILE-WIL/assets/34885971/e526ac27-b78e-40a4-90d0-215af4689f89)
* 화면이 커지면 GridView 버튼이 지나치게 커지는 것 같은데 어떤 해결책이 좋을까요? Wrap을 쓰는게 좋을까요?
