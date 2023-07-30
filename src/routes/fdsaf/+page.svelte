<script>
  import { locate } from "$lib/store";
  let org = ['/Frame 13.png', '/Frame 12.png', '/Ellipse 9.png', '/Ellipse 9 (1).png'];
  // 2차원 배열
  // 0. 공개/개인 1. 방 이름(지역) 2. 가장 최근에 내가 읽은 채팅 3. 최근채팅 4. 안읽음(2)/읽음(3) 5. 시간(최적화)
  // 공개 = 0, 개인 = 1
  let arr = [[0, `${$locate.big}`, 
  '인하대학교 병원 어떠세요? 그래도 가까워 보여요.', 
  `${$locate.bigchat[$locate.bigchat.length-1][1]}`, 2, '5월 23일'], 
  [0, `${$locate.big} ${$locate.small}`,  '아이들이랑 같이 한 번 가 보시면 좋을 거 같아요!', 
  '친구가 시흥시에 쇼핑하는 곳인데 볼거리도 많은 그런 곳이 있다는데, 아무리 검색해도 안나오네요 ㅠㅠ \n 혹시 아시는 분 계실까요?', 2, '7월 25일']];
  $: if (arr[0][2] === arr[0][3]){
    arr[0][4] = 3;
  }
  else {
    arr[0][4] = 2;
  } 
  // 305231340
  let sbc1 = Number($locate.bigchat[$locate.bigchat.length-1][2]);
  $: sbc1 = Number($locate.bigchat[$locate.bigchat.length-1][2]);
  let monthday = (Math.floor(sbc1/10000)) - (10000 * Math.floor((Math.floor(sbc1/10000))/10000));
  $: monthday = ((Math.floor(sbc1/10000)) - (10000 * Math.floor((Math.floor(sbc1/10000))/10000)));
  let today = new Date();
 /* $: if (sbc1 < 5){
    if (sbc1 == 0){
      console.log(0);
    }
    if (sbc1 == 1){
      console.log(1);
    }
  }
  */
  // 30523.134 -> 30523
  // 30523 -> 3.0523 -> 3 -> 30000
  window.alert(today);
</script>
<br>
<br>
<span class="img0"><img src="/새 채팅방.PNG" width="178px" height="71px" alt="블렌더"></span>
<div class="chatroom">
  <img class="rlt" src="/Rectangle 42.png" width="930px" height="120px" alt="블렌더">
  <div>
    <img style="position: absolute; top: 239px; left: 315px;" src={org[Number(arr[0][0])]} width="80px" height="80px" alt="개인/단체 채팅방">
    <span style="position: absolute; top: 247px; left: 423px; font-size: 26px;"> {arr[0][1]} </span>
    <img style="position: absolute; top: 253.5px; left: 540px;" src={org[Number(arr[0][4])]} width="20px" height="20px" alt="개인/단체 채팅방">
    <span style="position: absolute; top: 247px; left: 1123px; font-size: 16px; "> {arr[0][5]} </span>
  </div>
</div>
<div class="chatroom">
  <img class="rlt" src="/Rectangle 42.png" width="930px" height="120px" alt="블렌더">
  <div>
    <img style="position: absolute; top: 381px; left: 315px;" src="{org[Number(arr[1][0])]}" width="80px" height="80px" alt="개인/단체 채팅방">
    <span style="position: absolute; top: 389px; left: 423px; font-size: 26px;"> {arr[1][1]} </span>
  </div>
</div>

<style>
  .img0{
    margin-left: 300px;
  }
  .chatroom{
    margin-left: 300px;
    margin-top: 20px;
  }
  .rlt{
    position: relative;
    z-index: -3;
  }
</style>
