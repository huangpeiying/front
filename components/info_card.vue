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
  height: 328rpx;
  width: 630rpx;
  background-color: #0DB983;
  margin-left: 60rpx;
  border-radius:20rpx;
}
.English_Name{
  margin-top:120rpx ;
  margin-left: 40rpx;
  /*color: rgb(127,208,207);*/
  font-size: 24rpx;

}
.part1{
  display: flex;
  flex-direction: row;
}


.Chinese_name{
   margin-top:8rpx ;
   margin-left: 40rpx;
   color: #FFFFFF;
   font-size: 40rpx;
  font-weight: bold;
 }
  .number{
    margin-top:16rpx ;
    margin-left: 80rpx;
    color: #FFFFFF;
    font-size: 40rpx;
    font-weight: bold;
  }
.part2{
  display: flex;
  flex-direction: row;
  /*align-content: center;*/
  margin-top: 36rpx;
  width:630rpx;
  height:88rpx;
  background:rgb(255, 255, 255);
  z-index: 1;
  border-radius:0 0 20rpx 20rpx;

}
.normal{
  display: flex;
  flex-direction: row;
  margin-top: 20rpx;

}

.Nor{
  font-size: 28rpx;
  margin-left: 40rpx;
  color: rgb(85,97,117);
 }


.Num1{
  font-size: 28rpx;
  margin-left: 60rpx;
  text-align: center;
  font-weight: bold;
  color: #0DB983;
}
.Abnormal{
  display: flex;
  flex-direction: row;
  margin-left: 30rpx;
  width:210rpx;
  height:88rpx;
  border-style:none solid none solid;
  border-color:rgb(239, 239, 240);
  border-width: 2rpx 2rpx
}
  .abnormal{
    font-size: 28rpx;
    margin-left: 40rpx;
    color: rgb(85,97,117);
  }
  .Num2{
    font-size: 28rpx;
    margin-left: 60rpx;
    text-align: center;
    font-weight: bold;
    color: #ED7346;
  }

.Serious{
  display: flex;
  flex-direction: row;
}
.serious{
  font-size: 28rpx;
  margin-left: 40rpx;
  color: rgb(85,97,117);
}
.Num3{
  font-size: 28rpx;
  margin-left: 30rpx;
  text-align: center;
  font-weight: bold;
  color: #ED4646;
}

</style>
