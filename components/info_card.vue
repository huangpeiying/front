<template>
    <div class="info_card">
      <div class="second_framework" :style="{ 'background-color': c_par }">
        <div class="English_Name" :style="{ 'color':d_par}">{{English_Name}}</div>
        <div class="part1">
        <div class="Chinese_name">{{Chinese_name}}</div>
        <div class="number">{{number}}</div>
        </div>
        <div class="part2">
          <div class="normal">
            <div class="Nor">正常</div>
            <div class="Num1">18</div>
            <div class="Abnormal">
              <div class="abnormal">异常</div>
              <div class="Num2">2</div>
            </div>
            <div class="Serious">
              <div class="serious">严重</div>
              <div class="Num3">1</div>

            </div>
          </div>

        </div>

      </div>


    </div>
</template>

<script>
  export default {
    name: 'InfoCard',
    props: [
      'English_Name',
      'c_par',
      'Chinese_name',
      'number',
      'd_par'
    ]
  }
</script>


<style scoped>
.second_framework{
  display: flex;
  flex-direction: column;
  height: 164px;
  width: 315px;
  background-color: #0DB983;
  margin-left: 30px;
  border-radius:10px;
}
.English_Name{
  margin-top:60px ;
  margin-left: 20px;
  /*color: rgb(127,208,207);*/
  font-size: 12px;

}
.part1{
  display: flex;
  flex-direction: row;
}


.Chinese_name{
   margin-top:8px ;
   margin-left: 20px;
   color: #FFFFFF;
   font-size: 20px;
  font-weight: bold;
 }
  .number{
    margin-top:8px ;
    margin-left: 40px;
    color: #FFFFFF;
    font-size: 20px;
    font-weight: bold;
  }
.part2{
  display: flex;
  flex-direction: row;
  /*align-content: center;*/
  margin-top: 18px;
  width:315px;
  height:44px;
  background:rgb(255, 255, 255);
  z-index: 1;
  border-radius:0 0 10px 10px;

}
.normal{
  display: flex;
  flex-direction: row;
  margin-top: 10px;

}

.Nor{
  font-size: 14px;
  margin-left: 20px;
  color: rgb(85,97,117);
 }


.Num1{
  font-size: 14px;
  margin-left: 30px;
  text-align: center;
  font-weight: bold;
  color: #0DB983;
}
.Abnormal{
  display: flex;
  flex-direction: row;
  margin-left: 15px;
  width:105px;
  height:44px;
  border-style:none solid none solid;
  border-color:rgb(239, 239, 240);
  border-width: 1px 1px
}
  .abnormal{
    font-size: 14px;
    margin-left: 20px;
    color: rgb(85,97,117);
  }
  .Num2{
    font-size: 14px;
    margin-left: 30px;
    text-align: center;
    font-weight: bold;
    color: #ED7346;
  }

.Serious{
  display: flex;
  flex-direction: row;
}
.serious{
  font-size: 14px;
  margin-left: 20px;
  color: rgb(85,97,117);
}
.Num3{
  font-size: 14px;
  margin-left: 30px;
  text-align: center;
  font-weight: bold;
  color: #ED4646;
}

</style>
