<template>
  <div class="frame">
    <navigate ul="../page/control.vue" >
      <button type="Jump" v-on:click="btn">跳转</button>
    </navigate>
    <div class="part_one">
      <div class="Air_con">{{Eng_name}}</div>
      <div class="part_two">
        <div class="part_two_left">
          <div class="C_name">{{chinese_name}}</div>
          <div class="Num1">{{Num}}</div>
        </div>
        <div class="part_two_right">
          <img class="Mon" src="../../../static/images/gray.png" alt="监控模式">
          <img class="Control" src="../../../static/images/green.png" alt="控制模式">
        </div>
      </div>
      <div class="part_three">
        <div class="first">
          <monitor state="正常"  Number="12" ></monitor>
        </div>
        <div class="second">
          <monitor state="异常" third_par="#EFEFF0"  state_C="#333333" Num_C="#ED7346" Number="4" >
          </monitor>
        </div>
        <div class="red_circle">
          <div class="circle_two">2</div>
        </div>
        <div class="line"></div>
        <div class="third">
          <monitor state="严重" third_par="#EFEFF0"  state_C="#333333" Num_C="#ED4646" Number="0" ></monitor>
        </div>
      </div>
    </div>
    <div class="gray_part">
      <Master Name="银河SOHO - B1" Explain="正在运行"  temperature="23"></Master>
       <div class="gray_part_second">
      <Master Name="银河SOHO - B1" Explain="正在运行"  temperature="23"></Master>
       </div>
    </div>

  </div>
</template>

<script>
  import monitor from '../../components/monitor'
  import Master from '../../components/Master'
  export default {
    components: {monitor,
      Master
    },
    data () {
      return {
        Eng_name: 'Air condition',
        chinese_name: '空调',
        Num: '16'
      }
    },
    methods: {
      btn () {
        console.log('test')
        wx.navigateTo({
          url: '../../pages/control/main'})
      }
    }
  }
</script>
<style>
  page{
    background-color: rgb(228,228,228);
  }
</style>

<style scoped>

  .frame{
    display: flex;
    flex-direction: column;
    width: auto;
  }
  .part_one{
    width: auto;
    height: 324rpx;
    background-color: #FFFFFF;

  }
  .Air_con{
    color: rgb(130,140,160);
    margin-left: 60rpx;
    font-size: 24rpx;
  }
  .part_two{
    display: flex;
    flex-direction: row;
    margin-top: 24rpx;

  }
  .part_two_left{
    display: flex;
    flex-direction: row;
    /*margin-top: 12rpx;*/
  }
  .C_name{
    font-size: 48rpx;
    margin-left: 60rpx;
    font-weight: bold;

  }
  .Num1{
    font-size: 48rpx;
    /*margin-top: 12rpx;*/
    margin-left: 60rpx;
    font-weight: bold;
    color: #0DB983;
  }

  .part_two_right{
    display: flex;
    flex-direction: row;
    margin-left: auto;
  }
  .Mon{
    height: 48rpx;
    width: 48rpx;
    margin-right: 60rpx;
  }
  .Control{
    margin-top: 6rpx;
    height: 36rpx;
    width: 48rpx;
    margin-right: 60rpx;
  }
  .first{
    display: flex;
    flex-direction: row;
    margin-left: 60rpx;
  }
  .part_three{
    display: flex;
    flex-direction: row;
  }
  .red_circle{
    height: 32rpx;
    width: 38rpx;
    border-radius:200rpx;
    background-color:red;
    margin-top: 44rpx;
    margin-left: -50rpx;
  }
  .circle_two{
    font-size: 24rpx;
    color: #FFFFFF;
    /*color:red;*/
    margin-left: 12rpx;
    align-content: center;
    font-weight: bold;
  }
  .line{
    margin-top: 60rpx;
    margin-left: 10rpx;
    height:88rpx ;
    border-style:none solid none none ;
    border-color:rgb(201,212,233);
    border-width: 2rpx
  }
  .gray_part{
    margin-top: 40rpx;
    margin-left: 60rpx;
    z-index: 1;
  }
  .second{
    display: flex;
    flex-direction: row;
  }
.gray_part_second{
  margin-top: 40rpx;
}
</style>
