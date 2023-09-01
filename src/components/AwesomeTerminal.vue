<template>
  <div>
    <div class="rectangle">
      <div class="date-container">
        <span style="width: 100;" class="date">{{timestamp}}</span>
      </div>
      <h1 class="title">&lt;SPE FRONTEND&gt</h1>
    </div>
    <div class="rainbow">
    </div>
  </div>
</template>
<script>
 
 export default {
  created() {
    setInterval(this.currentDate, 1000);
  },
  data() {
    return {
      timestamp:''
    }
  },
  methods: {
    currentDate() {
      const today = new Date();
      const date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
      const time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
      const dateTime = date +" "+ time;
      this.timestamp = dateTime;
    }
  },
 };
</script>
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
    display: flex;
  }

  .date-container{
    width: 100px;
    bottom: 0px;
    color: #00FF00;
    align-self: flex-end;
    font-size: 20px;
    margin-bottom: 200px;
    font-weight: 300; 
    transform: rotate(90deg);
  }

  .date{
    white-space: nowrap;
  }

  .title{
    bottom: 0px;
    color: #00FF00;
    align-self: flex-end;
    margin: 10px;
    margin-left: 100px;
    font-size: 80px;
    font-weight: 300;
  }

  .rainbow{
    margin-top: -300px;
    width: 100;
    height: 700px;
    background-image: linear-gradient(to right, #00DBDE , #FC00FF);
  }
</style>