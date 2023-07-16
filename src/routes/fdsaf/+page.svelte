<script>
  import biglocate from '$app/paths';
  import smalllocate from '$app/environment'
  let org = ['/Frame 13.png', '/Frame 12.png'];
  // 2차원 배열
  // 0. 공개/개인 1. 방 이름(지역) 2. 가장 최근에 내가 읽은 채팅 3. 최근채팅
  var arr = [[0,'공개'], [0, '공개'], [1, biglocate], [1, smalllocate], 
  [2, '인하대학교 병원 어떠세요? 그래도 가까워 보여요.'], 
  [2, '아이들이랑 같이 한 번 가 보시면 좋을 거 같아요!'], 
  [3, '웅진플레이도시는 저저번 달에 갔었는데, 다른 곳은 없으려나요...?'], 
  [3, '친구가 시흥시에 쇼핑하는 곳인데 볼거리도 많은 그런 곳이 있다는데, 아무리 검색해도 안나오네요 ㅠㅠ \n 혹시 아시는 분 계실까요?']]; 
</script>
<br>
<br>
<span class="img0"><img src="/새 채팅방.PNG" width="178px" height="71px" alt="블렌더"></span>
<div class="chatroom">
  <img src="/Rectangle 42.png" width="930px" height="120px" alt="블렌더">
  <img src="{org[0][0]}" width="300px" height="300px" alt="개인/단체 채팅방">
</div>
<div class="chatroom">
  <img src="/Rectangle 42.png" width="930px" height="120px" alt="블렌더">
</div>


<style>
  .img0{
    margin-left: 300px;
  }
  .chatroom{
    margin-left: 300px;
    margin-top: 20px;
  }
</style>
