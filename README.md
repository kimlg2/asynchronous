# 동기 코드에서 비동기 코드로 변환

- 비동기 카운터 증가(_incrementCounter)
  1. 사용자가 화면의 버튼을 클릭하면 1초 동안 대기(Future.delayed)한 후에 _counter 값이 증가
  2. 비동기 처리를 통해 즉시 응답하지 않고,일정 시간이 지난 후에 상태를 변경하는 동작

- 데이터 로드(getData)
  1. 비동기 함수 getData()는 3초간 대기한 후 문자열 데이터를 반환

- FutureBuilder
  1. future 속성에 getData() 함수를 전달하여 데이터를 가져오고 비동기 작업이 진행 중일 때 로딩 인디케이터        (CircularProgressIndicator)를 표시
  2. snapshot.connectionState를 통해 비동기 작업의 상태 확인 후  작업 중일 경우 대기 상태를 나타내고 완       료 시 결과값 출력 
