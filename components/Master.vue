<template>
  <div class="Master">
    <div class="Function">
      <div class="white_part">
        <div class="white_part_one">
        <div class="name">{{Name}}</div>


          <div  v-on:click="ac_switch"  class="switch">
          <div v-if="ac_condition" class="switch_line"></div>
          <div v-else class="switch_line_2"></div>
          <div v-if="ac_condition" class="switch_circle"></div>
          <div v-else class="switch_circle_2"></div>
        </div>

        </div>
        <div class="explain">{{Explain}}</div>
        <div class="white_part_two">
        <img class="refrigeration" src="../../static/images/refrigeration.png" alt="制冷">
          <div class="temperature">{{temperature}}</div>
          <div class="little_c">。</div>
          <img class="first_Heating" src="../../static/images/Heating.png" alt="制热">
        </div>
      </div>
      <div class="gray_part">
        <div class="gray_part_one">
          <div class="green_square">
            <div class="green_square_num">制冷</div>
          </div>
          <img class="dehumidification" src="../../static/images/dehumidification.png" alt="除湿">
          <img class="second_Heating" src="../../static/images/Heating1.png" alt="制热">
          <img class="aeration" src="../../static/images/aeration.png" alt="通风">
          <img class="automatic" src="../../static/images/automatic.png" alt="自动">
        </div>
      </div>
      <div class="gray_part_two">
        <div class="first_square">
          <div class="reduce"></div>
          <img class="wind_speed_2" src="../../static/images/wind_speed_2.png" alt="风速">
          <div class="increase">+</div>
        </div>
        <div class="second_square">
          <div class="reduce"></div>
          <img class="wind_direction2" src="../../static/images/wind_direction2.png" alt="风向">
          <div class="increase">+</div>
        </div>

      </div>


    </div>


  </div>
</template>

<script>
  export default {
    data () {
      return {
        ac_condition: true
      }
    },
    name: 'Master',
    props: [
      'Name',
      'Explain',
      'temperature'
    ],

    methods: {
      ac_switch () {
        if (this.ac_condition === true) {
          this.ac_condition = false
        } else {
          this.ac_condition = true
        }
      }
    }
  }
</script>

<style scoped>
  .Function{
    height:285px;
    width: 315px;
    background-color: rgb(238,238,238);
    border-radius:10px;
  }
  .white_part{
    display: flex;
    flex-direction: column;
    height:120px;
    width: 315px;
    background-color: #FFFFFF;
    border-radius:10px 10px 0 0;
  }
  .white_part_one{
    display: flex;
    flex-direction: row;
    margin-top: 20px;
  }
  .switch{
    display: flex;
    flex-direction: row;
  }
  .switch_line{
    border-style:none none none solid;
    border-color:#0DB983;
    border-width: 25px;
    height: 2px;
    margin-top: 10px;
    margin-left: 123px;
  }

  .switch_line_2{
    border-style:none none none solid;
    border-color:rgb(239, 239, 239);
    border-width: 25px;
    height: 2px;
    margin-top: 10px;
    margin-left: 123px;
  }
  .switch_circle{
    width: 10px;
    height: 10px;
    background-color: white;
    text-align: center;
    border-radius: 100px;
    border: 3px #0DB983 solid;
    margin-top: 3px;
    margin-left: -10px;
  }

  .switch_circle_2{
    width: 10px;
    height: 10px;
    background-color: white;
    text-align: center;
    border-radius: 100px;
    border: 3px rgb(228, 228, 228) solid;
    margin-top: 3px;
    margin-left: -25px;
  }

  .name{
    margin-left: 20px;
    font-size: 16px;

  }
  .explain{
    margin-top: 10px;
    margin-left: 20px;
    font-size: 14px;
    color: rgb(172,172,172);
  }
  .white_part_two{
    display: flex;
    flex-direction: row;
    margin-top: 20px;
  }
  .refrigeration{
   height:20px;
    width: 20px;
    margin-left: 20px;
     }
.temperature{
  font-size: 20px;
  color:#0DB983;
  margin-left: 54px;
  font-weight: bold;
  z-index: 22;
}
  .little_c{
    color:#0DB983;
    font-size: 20px;
    font-weight: bold;
    margin-top: -15px;
  }
  .first_Heating{
    height: 20px;
    width: 20px;
    margin-left: auto;
    margin-right: 20px;
  }
.gray_part{
  display: flex;
  flex-direction: column;
}
  .gray_part_one{
    display: flex;
    flex-direction: row;
    align-content: center;
    margin-top: 31px;


  }
  .green_square{
    height: 42px;
    width: 48px;
    background-color: #0DB983;
    margin-left: 20px;
    border-radius:9px
  }
  .green_square_num{
    color: #FFFFFF;
    text-align: center;
    margin-top: 10px;
    font-size: 14px;
    font-weight: bold;
  }
  .dehumidification{
    height: 20px;
    width: 20px;
    margin-left: 23px;
    margin-top: 10px;
  }
.second_Heating{
  height: 20px;
  width: 20px;
  margin-top: 10px;
  margin-left: 39px;
}

  .aeration{
    height: 20px;
    width: 20px;
    margin-top: 10px;
    margin-left: 36px;
  }
  .automatic{
    height: 20px;
    width: 20px;
    margin-left: 38px;
    margin-top: 10px;
  }
  .gray_part_two{
    display: flex;
    flex-direction: row;
  }
  .first_square{
    display: flex;
    flex-direction: row;
    align-content: center;
    margin-left: 20px;
    margin-top: 20px;
    height: 52px;
    width: 133px;
    background-color: rgb(230,230,230);
    border-radius:18px

  }
  .reduce{
    border-style:none none none solid;
    /*border-color:#0DB983;*/
    border-width: 10px;
    height: 2px;
    margin-left: 20px;
    margin-top: 25px;
  }
 .wind_speed_2{
  height:20px;
   width: 20px;
   margin-left: 25px;
   margin-top: 16px;
}
  .increase{
    font-size: 30px;
    margin-top: 5px;
    /*font-weight: bold;*/
    margin-left: 20px;
  }
.second_square{
  display: flex;
  flex-direction: row;
  align-content: center;
  margin-left: 20px;
  margin-top: 20px;
  height: 52px;
  width: 133px;
  background-color: rgb(230,230,230);
  border-radius:18px
}
  .wind_direction2{
    width: 24px;
    height: 18px;
    margin-left: 25px;
    margin-top: 16px;
  }

</style>
