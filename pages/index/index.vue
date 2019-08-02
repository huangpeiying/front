<template>
  <div class="General_framework">
    <navigate ul="../page/monitor.vue" >
      <button type="Jump" v-on:click="btn">跳转</button>
    </navigate>
    <div class="Project_name">{{company_name}}</div>
    <div class="Sloth_Technology">{{Sloth_Technology}}</div>
    <div class="info_card_list">
      <div class="green">
      <InfoCard  c_par="#0DB983" d_par="rgb(127,208,207)"English_Name="Air condition" Chinese_name="空调" number="21"></InfoCard>
      </div>
      <div class="yellow">
        <InfoCard c_par="#FFAF27" d_par="rgb(223,216,168)" English_Name="Elevator" Chinese_name="电梯" number="21"></InfoCard>
      </div>
      <div class="black">
        <InfoCard c_par="#000022"  d_par="rgb(223,216,168)" English_Name="Elevator" Chinese_name="电梯" number="21"></InfoCard>
      </div>
      <div class="red">
        <InfoCard c_par="#ED4646"  d_par="rgb(223,216,168)" English_Name="Elevator" Chinese_name="电梯" number="21"></InfoCard>
      </div>
    </div>
    <div class="three_pic">
      <div class="first_pic">
      <img class="set_up" src="../../../static/images/Set_up.png" alt="设置" >
      </div>
      <div class="second_pic">
        <img class="service" src="../../../static/images/service.png" alt="客服">
      </div>

      <div class="third_pic">
        <img class="Personal" src="../../../static/images/Personal.png" alt="个人用户">
      </div>


    </div>
    </div>
<!--    <button v-on:click="bt" v-bind:class ="{'c1': isActive, 'c2': hasError }">button</button>-->
<!--<label date-v-25adc6c0 class="vue-js-switch toggled" style="&#45;&#45;h:22px ;&#45;&#45;w:120rpx;&#45;&#45;d:101rpx;">-->
<!--  <input data-v-25adc6c0 type="checkbox" class="v-switch-input">-->
<!--  <span data-v-25adc6c0 class="v-switch-core" style="background-color: rgb(187,153,205)">-->
<!--    ::before-->
<!--  </span>-->
<!--  <div data-v-25adc6c0>-->
<!--    <span data-v-25adc6c0 class="v-switch-label v-left"></span>-->
<!--  </div>-->
<!--</label>-->

</template>

<script>
  import InfoCard from '../../components/info_card'
  export default {
    data () {
      return {
        company_name: '树懒科技',
        Sloth_Technology: 'Sloth Technology Co., Ltd.',
        hasError: true,
        isActive: false

      }
    },
    components: {
      InfoCard
    },
    methods: {
      btn () {
        console.log('test')
        wx.navigateTo({
          url: '../../pages/control/main'})
      },
      bt () {
        if (this.isActive === false) {
          this.isActive = true
          this.hasError = false
        } else {
          this.isActive = false
          this.hasError = true
        }
      }
    }
  }
</script>

<style>
  page{
    background: rgb(239,239,240);
    height: 100%;
  }

</style>


<style scoped>

  .General_framework{
    display: flex;
    flex-direction: column;
    height:1000rpx;
    width: auto;


  }
  .Project_name{
    /*color: rgb(116,128,149);*/
    font-size: 48rpx;
    margin-left: 60rpx;
    margin-top: 40rpx;
    font-weight: bold;

  }
.Sloth_Technology{
  color: rgb(116,128,149);
  font-size: 24rpx;
  margin-left: 60rpx;
  margin-top: 28rpx;
}
.green{
  margin-top: 144rpx;
}
.yellow{
  margin-top: 40rpx;

}
  .c1{
    background-color: blueviolet;
  }
  .c2{
    background-color: red;
  }
.three_pic{
  display: flex;
  flex-direction:row;
  position: fixed;
  height: 156rpx;
  width: 750rpx;
  background-color: rgb(239,239,240);
  bottom:0;
  z-index: 999;

}
.first_pic{
  height: 96rpx;
  width: 192rpx;
  background-color: #FFFFFF;
  /*margin-top: 5rpx;*/
  margin-left: 60rpx;
  border-radius:8rpx;

}
  .set_up{
    margin-left: 78rpx;
    margin-top: 30rpx;
    width: 36rpx;
    height: 36rpx;

  }
  .second_pic{
    height: 96rpx;
    width: 192rpx;
    background-color: #FFFFFF;
    /*margin-top: 5rpx;*/
    margin-left: 28rpx;
    border-radius:8rpx;
  }
.service{
  margin-left: 78rpx;
  margin-top: 30rpx;
  width: 36rpx;
  height: 36rpx;
}
.third_pic{
  height: 96rpx;
  width: 192rpx;
  background-color: #FFFFFF;
  /*margin-top: 5rpx;*/
  margin-left: 28rpx;
  border-radius:8rpx;
}
.Personal{
  margin-left: 78rpx;
  margin-top: 30rpx;
  width: 36rpx;
  height: 36rpx;
}
  .black{
    margin-top: 40rpx;
  }
.red{
  margin-top: 40rpx;
}
</style>
