<script>
  let locatee = 1;
  const clicked = () => {
    locatee = (locatee + 1) % 2 // locatee가 1이면 0, 0이면 1로 변환
  }
  function targeti() { 
    document.getElementsByClassName("mainups")[0].className = "deles"
  }
  </script>

<div class="mainups">
  <span class="home"><a href="#/"><img src="../../블렌더확대.png" width="61px"height="60px" alt="블렌더"></a></span>
  
  <span class="rig"><button on:click={targeti}><img src="../../메뉴.PNG" width="60px" height="60px" alt="메뉴"></button></span>
</div>
<div class="deles"></div>
<slot />

<style>
  .mainups{
    background-color: white;
    padding: 10px;
    padding-left: 13px;
    padding-top: 21px;
    margin: -8px;
    box-shadow: 3px 3px 3px 3px rgb(222, 234, 220);
    transform-origin: right;
    transform: scale(1);
    transition: 0.1s all;
  }
  .rig{
    margin-left: 1367px;
  }
  .rig:hover{
    cursor: pointer;
  }
  .rig:active{
    background-color: rgb(140, 140, 140);
    transform: scale(0.5);
    transition: 0.1s all; 
  }
  .home{
    padding: 12px;
  }
  .home:hover{
    cursor: pointer;
  }
  .deles{
    background-color: white;
    padding: 10px;
    padding-left: 13px;
    padding-top: 21px;
    margin: -8px;
    box-shadow: 3px 3px 3px 3px rgb(222, 234, 220);
    transform-origin: right;
    transform: scale(1);
    transition: 0.1s all;
  }
</style>

