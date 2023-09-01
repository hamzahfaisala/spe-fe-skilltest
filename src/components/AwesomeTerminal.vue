<template>
  <div>
    <div class="rectangle"></div>
    <div class="rainbow">
      <h1 class="title">helo</h1>
    </div>
  </div>
</template>
<style>
  .rectangle {
    height: 800px;
    width: 100;
    background-color: #111111;
    transform: rotate(-30deg);
    position: relative;
    margin-top: -500px;
    border-radius: 50px;
    border: 30px solid #EEEEEE;
  }

  .title{

  }

  .rainbow{
    margin-top: -300px;
    width: 100;
    height: 700px;
    background-image: linear-gradient(to right, #00DBDE , #FC00FF);
  }
</style>