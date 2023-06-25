<div class="mainups">
  <span class="home"><a href="$url('#')"><img src="/메뉴.PNG" width="61px"height="60px" alt="메뉴"></a></span>
  홈
  <span class="rig"><img src="/static/블렌더확대.png" width="60px" height="60px" alt="블렌더"></span>
</div>
<slot />
<style>
  .mainups{
    background-color: white;
    padding: 10px;
    padding-left: 13px;
    padding-top: 13px;
    margin: -8px;
    box-shadow: 3px 3px 3px 3px rgb(222, 234, 220);
  }
  .rig{
    margin-left: 1380px;
  }
  .rig:hover{
    cursor: pointer;
  }
  .rig:active{
    background-color: rgb(140, 140, 140);
    transform: scale(1);
    transition: 0.1s all;
  }
  .home:hover{
    cursor: pointer;
  }
  .mainups{
    transform-origin: right;
    transform: scale(1);
    transition: 0.1s all;
    transform-origin: right;
  }
</style>