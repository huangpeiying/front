<template>
  <div class="monitor">
    <div class="third_part" :style="{'background-color': third_par}">
      <div class="state" :style="{'color':state_C}">{{state}}</div>
      <div class="Number" :style="{'color':Num_C}">{{Number}}</div>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'monitor',
    props: [
      'state',
      'third_par',
      'state_C',
      'Number',
      'Num_C'
    ]
  }
</script>

<style scoped>
  .third_part{
    display: flex;
    flex-direction: row;
    width: 105px;
    height: 44px;
    background-color: #0DB983;
    margin-top: 30px;
  }
  .state{
    font-size: 14px;
    color: #FFFFFF;
    margin-left: 20px;
    margin-top: 15px;

  }
  .Number{
    font-size: 14px;
    color: #FFFFFF;
    margin-left: 20px;
    margin-top: 15px;
    font-weight: bold;
  }
</style>
