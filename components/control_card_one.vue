<template>
  <div class="control_card_one">
    <div class="third_part" :style="{'background-color': third_par}">
      <div class="state" :style="{'color':state_C}">{{state}}</div>
      <div class="Number" :style="{'color':Num_C}">{{Number}}</div>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'control_card_one',
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
    width: 210rpx;
    height: 88rpx;
    background-color: #0DB983;
    /*background-color:red;*/
    margin-top: 60rpx;
  }
  .state{
    font-size: 28rpx;
    color: #FFFFFF;
    margin-left: 40rpx;
    margin-top: 30rpx;

  }
  .Number{
    font-size: 28rpx;
    color: #FFFFFF;
    margin-left: 40rpx;
    margin-top: 30rpx;
    font-weight: bold;
  }
</style>
