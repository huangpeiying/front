<template>
    <div class="monitor_card">
      <div class="first_frame">
        <div class="transverse">

         <div class="part_one">
          <div class="Name">{{Name}}</div>
          <div class="Explain">{{Explain}}</div>
         </div>

         <div v-on:click="green_switch" class="switch_a" >
          <div v-if="Green_switch" class="green_switch_1"></div>
          <div v-else class="green_switch_2"></div>
         </div>
        </div>

        <div class="part_two">
          <img class="refrigeration_green" src="../../static/images/refrigeration_green.png">


        </div>



      </div>


    </div>
</template>

<script>
  export default {
    data () {
      return {
        Green_switch: true
      }
    },
    name: 'monitor_card_one',
    props: [
      'Name',
      'Explain'
    ],
    methods: {
      green_switch () {
        if (this.Green_switch === true) {
          this.Green_switch = false
        } else {
          this.Green_switch = true
        }
      }
    }
  }
</script>

<style scoped>
 .first_frame{
  display: flex;
  flex-direction: column;
  margin-left: 60rpx;
  margin-top: 40rpx;
  height: 268rpx;
  width: 630rpx;
  background-color: #FFFFFF;
  border-radius: 36rpx;
 }
 .transverse{
   display: flex;
   flex-direction: row;
 }
 .part_one{
  display: flex;
  flex-direction: column;
   margin-left: 40rpx;
 }
  .Name{
    font-size: 32rpx;
    color: black;
    margin-top: 40rpx;
    font-weight: bold;
  }
  .Explain{
    font-size: 24rpx;
    color: rgb(172,172,172);
    margin-top: 20rpx;
  }
  .switch_a{
    display: flex;
    flex-direction: column;
    margin-left: auto;
  }
  .green_switch_1{
    height: 16rpx;
    width: 28rpx;
    border-radius: 8rpx;
    background-color: #0DB983;
    margin-top: 48rpx;
    margin-right: 40rpx;
  }
 .green_switch_2{
   height: 16rpx;
   width: 28rpx;
   border-radius: 8rpx;
   background-color: rgb(172,172,172);
   margin-top: 48rpx;
   margin-right: 40rpx;
 }
  .part_two{
    display: flex;
    flex-direction: row;
    margin-top: 40rpx;
    background-color: rgb(238,238,238);
    height:112rpx;
    width: 630rpx;
    border-radius: 0 0 36rpx 36rpx;
  }
  .refrigeration_green{
    height: 28rpx;
    width: 28rpx;
    margin-left: 40rpx;
    margin-top: 40rpx;

  }


</style>
