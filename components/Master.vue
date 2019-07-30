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

          <div v-on:click="cool" class="cooling">
          <div v-if="ac_cooling" class="green_square">
            <div class="green_square_num">制冷</div>
          </div>
            <img v-else class="refrigeration_2" src="../../static/images/refrigeration_2.png" alt="制冷">
          </div>

          <div  v-on:click="drying_switch"  class="dry_switch">
          <img v-if="ac_drying" class="drying" src="../../static/images/dehumidification.png" alt="除湿">
          <div v-else class="drying_2">
            <div class="green_drying_square">除湿</div>
          </div>
          </div>

          <div  v-on:click="Heating_switch"  class="Heating">
          <img  v-if="ac_Heating" class="second_Heating" src="../../static/images/Heating1.png" alt="制热">
            <div v-else class="Heating_2">
              <div class="green_heating_square">制热</div>
            </div>
          </div>

          <div  v-on:click="aeration_switch"  class="Aeration">
          <img v-if="ac_aeration" class="aeration" src="../../static/images/aeration.png" alt="通风">
            <div v-else class="aeration_2">
              <div class="green_aeration_square">通风</div>
            </div>
          </div>

          <div  v-on:click="automatic_switch"  class="Automatic">
          <img v-if="ac_automatic" class="automatic" src="../../static/images/automatic.png" alt="自动">
            <div v-else class="automatic_2">
              <div class="green_automatic_square">自动</div>
            </div>
          </div>
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
        ac_condition: true,
        ac_drying: true,
        ac_cooling: true,
        ac_Heating: true,
        ac_aeration: true,
        ac_automatic: true
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
      },
      drying_switch () {
        if (this.ac_drying === true) {
          this.ac_drying = false
        } else {
          this.ac_drying = true
        }
      },
      cool () {
        if (this.ac_cooling === true) {
          this.ac_cooling = false
        } else {
          this.ac_cooling = true
        }
      },
      Heating_switch () {
        if (this.ac_Heating === true) {
          this.ac_Heating = false
        } else {
          this.ac_Heating = true
        }
      },
      aeration_switch () {
        if (this.ac_aeration === true) {
          this.ac_aeration = false
        } else {
          this.ac_aeration = true
        }
      },
      automatic_switch () {
        if (this.ac_automatic === true) {
          this.ac_automatic = false
        } else {
          this.ac_automatic = true
        }
      }
    }
  }
</script>

<style scoped>
  .Function{
    height:570rpx;
    width: 630rpx;
    background-color: rgb(238,238,238);
    border-radius:20rpx;
  }
  .white_part{
    display: flex;
    flex-direction: column;
    height:240rpx;
    width: 630rpx;
    background-color: #FFFFFF;
    border-radius:10px 10px 0 0;
  }
  .white_part_one{
    display: flex;
    flex-direction: row;
    margin-top: 40rpx;
  }
  .switch{
    display: flex;
    flex-direction: row;
  }
  .switch_line{
    /*border-style:none none none solid;*/
    /*border-color:#0DB983;*/
    /*border-width: 50rpx;*/
    width: 60rpx;
    height: 4rpx;
    background-color: #0DB983;
    margin-top: 20rpx;
    margin-left: 246rpx;
  }

  .switch_line_2{
    width: 60rpx;
    height: 4rpx;
    border-color:rgb(239, 239, 239);
    margin-top: 20rpx;
    margin-left: 246rpx;
  }
  .switch_circle{
    width: 20rpx;
    height: 20rpx;
    background-color: white;
    text-align: center;
    border-radius: 200rpx;
    border: 3px #0DB983 solid;
    margin-top: 6rpx;
    margin-left: -20rpx;
  }

  .switch_circle_2{
    width: 20rpx;
    height: 20rpx;
    background-color: white;
    text-align: center;
    border-radius: 100rpx;
    border: 3px rgb(228, 228, 228) solid;
    margin-top: 6rpx;
    margin-left: -50rpx;
  }

  .name{
    margin-left: 40rpx;
    font-size: 32rpx;

  }
  .explain{
    margin-top: 20rpx;
    margin-left: 40rpx;
    font-size: 28rpx;
    color: rgb(172,172,172);
  }
  .white_part_two{
    display: flex;
    flex-direction: row;
    margin-top: 40rpx;
  }
  .refrigeration{
   height:40rpx;
    width: 40rpx;
    margin-left: 40rpx;
     }
.temperature{
  font-size:40rpx;
  color:#0DB983;
  margin-left: 108rpx;
  font-weight: bold;
  z-index: 22;
}
  .little_c{
    color:#0DB983;
    font-size: 40rpx;
    font-weight: bold;
    margin-top: -30rpx;
  }
  .first_Heating{
    height: 40rpx;
    width: 40rpx;
    margin-left: auto;
    margin-right: 40rpx;
  }
.gray_part{
  display: flex;
  flex-direction: column;
}
  .gray_part_one{
    display: flex;
    flex-direction: row;
    align-content: center;
    margin-top: 62rpx;
  }
  .green_square{
    height: 84rpx;
    width: 96rpx;
    background-color: #0DB983;
    margin-left: 40rpx;
    border-radius:9px
  }
  .green_square_num{
    color: #FFFFFF;
    text-align: center;
    padding-top: 20rpx;
    /*margin-top: 10rpx;*/
    font-size: 28rpx;
    font-weight: bold;
  }
  .refrigeration_2{
    height: 40rpx;
    width: 40rpx;
    margin-left: 40rpx;
    margin-top: 20rpx;
  }
  .drying{
    height: 40rpx;
    width: 40rpx;
    margin-left: 46rpx;
    margin-top: 20rpx;
  }
  .drying_2{
    height: 84rpx;
    width: 96rpx;
    background-color: #0DB983;
    margin-left: 40rpx;
    border-radius:9px
  }
  .green_drying_square{
    color: #FFFFFF;
    font-size: 28rpx;
    text-align: center;
    padding-top: 20rpx;
    font-weight: bold;
  }

  .second_Heating{
  height: 40rpx;
  width: 40rpx;
  margin-top: 20rpx;
  margin-left: 78rpx;
}
 .Heating_2{
   height: 84rpx;
   width: 96rpx;
   background-color: #0DB983;
   margin-left: 40rpx;
   border-radius:9px
 }

 .green_heating_square{
   color: #FFFFFF;
   font-size: 28rpx;
   text-align: center;
   padding-top: 20rpx;
   font-weight: bold;
 }
  .aeration_2{
    height: 84rpx;
    width: 96rpx;
    background-color: #0DB983;
    margin-left: 40rpx;
    border-radius:9px
  }
  .green_aeration_square{
    color: #FFFFFF;
    font-size: 28rpx;
    text-align: center;
    padding-top: 20rpx;
    font-weight: bold;
  }
  .aeration{
    height: 40rpx;
    width: 40rpx;
    margin-top: 20rpx;
    margin-left: 72rpx;
  }
  .automatic{
    height: 40rpx;
    width: 40rpx;
    margin-left: 76rpx;
    margin-top: 20rpx;
  }
  .automatic_2{
    height: 84rpx;
    width: 96rpx;
    background-color: #0DB983;
    margin-left: 40rpx;
    border-radius:9px
  }
  .green_automatic_square{
    color: #FFFFFF;
    font-size: 28rpx;
    text-align: center;
    padding-top: 20rpx;
    font-weight: bold;
  }
  .gray_part_two{
    display: flex;
    flex-direction: row;
  }
  .first_square{
    display: flex;
    flex-direction: row;
    align-content: center;
    margin-left: 40rpx;
    margin-top: 40rpx;
    height: 104rpx;
    width: 266rpx;
    background-color: rgb(230,230,230);
    border-radius:18px

  }
  .reduce{
    border-style:none none none solid;
    /*border-color:#0DB983;*/
    border-width: 20rpx;
    height: 4rpx;
    margin-left: 40rpx;
    margin-top: 50rpx;
  }
 .wind_speed_2{
  height:40rpx;
   width: 40rpx;
   margin-left: 50rpx;
   margin-top: 32rpx;
}
  .increase{
    font-size: 60rpx;
    margin-top: 10rpx;
    /*font-weight: bold;*/
    margin-left: 40rpx;
  }
.second_square{
  display: flex;
  flex-direction: row;
  align-content: center;
  margin-left: 40rpx;
  margin-top: 40rpx;
  height: 104rpx;
  width: 266rpx;
  background-color: rgb(230,230,230);
  border-radius:18px
}
  .wind_direction2{
    width: 48rpx;
    height: 36rpx;
    margin-left: 50rpx;
    margin-top: 32rpx;
  }

</style>
