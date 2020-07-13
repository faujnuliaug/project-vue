<template>
  <div id="box">
    <h3>div默认是垂直方向排列的</h3>
    <div style="background-color: #d0d0d0;height: 250px;">
      <div style="background-color: #D9006C;height: 50px;width: 50px;">1</div>
      <div style="background-color: #FF8F59;height: 50px;width: 50px;">2</div>
      <div style="background-color: rgb(82, 76, 76);height: 50px;width: 50px;">3</div>
      <div style="background-color: #AD5A5A;height: 50px;width: 50px;">4</div>
    </div>
    <h3>盒子模型默认是水平方向排列</h3>
    <div style="background-color: #d0d0d0;height: 250px;display: flex;">
      <div style="background-color: #D9006C;height: 50px;width: 50px;">1</div>
      <div style="background-color: #FF8F59;height: 50px;width: 50px;">2</div>
      <div style="background-color: rgb(82, 76, 76);height: 50px;width: 50px;">3</div>
      <div style="background-color: #AD5A5A;height: 50px;width: 50px;">4</div>
    </div>
  </div>
</template>

<style lang="scss">
</style>
