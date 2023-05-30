# What I Learned

## async / await
* 비동기 처리
* 서버에 요청하거나 기타 시간이 오래걸리는 작업 할 때 쓰는 것
* 안쓰고 그냥 하면 다른 모든 작업이 중단되고 화면도 멈춘다(아마)
* Future: 대충 JS의 Promise랑 비슷한 것인 듯 하다.
* FutureBuilder: 위의 Future 끝나면 알아서 결과 보여주는 위젯
  * future: 사용할 Future
  * builder: 표시할 위젯, 함수 두번째 인자가 future 반환값

## http/https 요청
* GET 요청: http.get(URL)
* 응답을 반환
* 응답 body: (반환값).body

## 기타
* CircularProgressIndicator: 원형 로딩 표시기
* jsonDecode: JSON 파싱 함수
* Image.network: 웹 이미지 불러오기
