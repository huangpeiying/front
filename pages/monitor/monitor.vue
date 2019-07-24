<template>
  <div class="frame">
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
    height: 162px;
    background-color: #FFFFFF;

  }
  .Air_con{
    color: rgb(130,140,160);
    margin-left: 30px;
    font-size: 12px;
  }
  .part_two{
    display: flex;
    flex-direction: row;
    margin-top: 12px;

  }
  .part_two_left{
    display: flex;
    flex-direction: row;
    /*margin-top: 12px;*/
  }
  .C_name{
    font-size: 24px;

    margin-left: 30px;
    font-weight: bold;

  }
  .Num1{
    font-size: 24px;
    /*margin-top: 12px;*/
    margin-left: 30px;
    font-weight: bold;
    color: #0DB983;
  }

  .part_two_right{
    display: flex;
    flex-direction: row;
    margin-left: auto;
  }
  .Mon{
    height: 24px;
    width: 24px;
    margin-right: 30px;
  }
  .Control{
    margin-top: 3px;
    height: 18px;
    width: 24px;
    margin-right: 30px;
  }
  .first{
    display: flex;
    flex-direction: row;
    margin-left: 30px;
  }
  .part_three{
    display: flex;
    flex-direction: row;
  }
  .red_circle{
    height: 16px;
    width: 19px;
    border-radius:100px;
    background-color:red;
    margin-top: 22px;
    margin-left: -25px;
  }
  .circle_two{
    font-size: 12px;
    color: #FFFFFF;
    /*color:red;*/
    margin-left: 6px;
    align-content: center;
    font-weight: bold;
  }
  .line{
    margin-top: 30px;
    margin-left: 5px;
    height:44px ;
    border-style:none solid none none ;
    border-color:rgb(201,212,233);
    border-width: 1px
  }
  .gray_part{
    margin-top: 20px;
    margin-left: 30px;
    z-index: 1;
  }
  .second{
    display: flex;
    flex-direction: row;
  }
.gray_part_second{
  margin-top: 20px;
}
</style>
