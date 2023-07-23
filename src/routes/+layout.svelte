<script>
  let locatee = 1;
  let deles = false;
  const clicked = () => {
    locatee = (locatee + 1) % 2; // locatee가 1이면 0, 0이면 1로 변환
  };
</script>
<div class="main">
<div class="mainups" class:deles>
  <span class="home">
    <a href="#/">
      <img
        src="../../Group 1.png"
        width="75px"
        height="75px"
        alt="블렌더"
      />
    </a>
  </span>

  <span class="rig"></span>
</div>
<div class="mainbu" class:deles>
<button on:click={() => (deles = !deles)}
  ><img
    src="../../메뉴 버튼.png"
    width="70px"
    height="70px"
    alt="메뉴"
  /></button>
<span class="deles" />
</div>
</div>
<slot />

<style>
  .mainups {
    background-color: white;
    padding: 5px;
    padding-left: 4px;
    padding-top: 4px;
    box-shadow: 0px 3px 3px 3px rgb(222, 234, 220);
    transform-origin: right;
    transform: translateX(120%);
    transition: 0.5s all;
  }
  .rig {
    margin-left: 1367px;
  }
  .rig:hover {
    cursor: pointer;
  }
  .rig:active {
    background-color: rgb(140, 140, 140);
    transform: scale(0.5);
    transition: 0.1s all;
  }
  .home {
    margin-right: -25px;
    padding: 12px;
  }
  .home:hover {
    cursor: pointer;
  }
  .mainups.deles {
    transform: translateY(0);
  }
  .main{
    display: flex;
  }
  .mainbu{
    padding-top: 10px;
    padding-left: 10px;
    padding-right: 10px;
    z-index: 1;
  }
  .mainbu.deles{
    background-color: white;
    box-shadow: 3px 3px 0px 3px rgb(222, 234, 220);
  }
  .mainbu > button{
    all: unset;
  }
</style>
