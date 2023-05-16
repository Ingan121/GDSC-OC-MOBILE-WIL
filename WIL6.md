# What I Learned

https://github.com/Ingan121/GDSC-OC-MOBILE-WEEK6
<img src="https://github.com/Ingan121/GDSC-OC-MOBILE-WEEK6/raw/main/screenshot.png" />

## 위젯
* SizedBox: 빈 간격 만드는 위젯, 인자: height, width
* SingleChildScrollView: 내부 위젯을 스크롤 가능하게 해주는 위젯
  * scrollDirection: Axis.horizontal (가로) / Axis.vertical (세로)
* ClipRRect: 이미지 둥글게 할 수 있는 위젯

## 속성
* margin: 바깥쪽 빈공간, padding: 안쪽 빈공간
  * EdgeInsets를 값으로 가짐. EdgeInsets: symmetric (가로 or 세로 양쪽), all (4면 다), only (각각), fromLTRB (순서대로 왼쪽 위 오른쪽 아래)
* crossAxisAlignment: 위젯의 주축과 반대되는 방향의 정렬 (Row: 가로정렬, Column: 세로정렬)
* mainAxisAlignment: 위젯의 주축과 같은 방향의 정렬 (Row: 세로정렬, Column: 가로정렬)

## 기능
* Ctrl+Shift+R: 선택된 위젯을 다른 위젯으로 감싸거나 메소드로 추출할 수 있다.
* 메소드 추출: 위젯 덩어리를 하나의 위젯으로 만들기
  * 변하는 부분만 변수로 만들고 인자로 받아와 사용할 수 있다.
