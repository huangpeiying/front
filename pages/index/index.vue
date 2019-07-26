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
<!--<label date-v-25adc6c0 class="vue-js-switch toggled" style="&#45;&#45;h:22px ;&#45;&#45;w:120px;&#45;&#45;d:101px;">-->
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
          url: '../../pages/monitor/main'})
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
    height:1000px;
    width: auto;


  }
  .Project_name{
    /*color: rgb(116,128,149);*/
    font-size: 24px;
    margin-left: 30px;
    margin-top: 20px;
    font-weight: bold;

  }
.Sloth_Technology{
  color: rgb(116,128,149);
  font-size: 12px;
  margin-left: 30px;
  margin-top: 14px;
}
.green{
  margin-top: 77px;
}
.yellow{
  margin-top: 20px;

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
  height: 78px;
  /*width: 96px;*/
  background-color: rgb(239,239,240);
  bottom:0;
  z-index: 999;

}
.first_pic{
  height: 48px;
  width: 96px;
  background-color: #FFFFFF;
  /*margin-top: 5px;*/
  margin-left: 30px;
  border-radius:4px;

}
  .set_up{
    margin-left: 39px;
    margin-top: 15px;
    width: 18px;
    height: 18px;

  }
  .second_pic{
    height: 48px;
    width: 96px;
    background-color: #FFFFFF;
    /*margin-top: 5px;*/
    margin-left: 14px;
    border-radius:4px;
  }
.service{
  margin-left: 39px;
  margin-top: 15px;
  width: 18px;
  height: 18px;
}
.third_pic{
  height: 48px;
  width: 96px;
  background-color: #FFFFFF;
  /*margin-top: 5px;*/
  margin-left: 14px;
  border-radius:4px;
}
.Personal{
  margin-left: 39px;
  margin-top: 15px;
  width: 18px;
  height: 18px;
}
  .black{
    margin-top: 20px;
  }
.red{
  margin-top: 20px;
}
</style>
