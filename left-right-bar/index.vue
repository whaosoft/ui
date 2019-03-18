<template>
<div>
  <div class="chart-wrap" style="float: left">
    <div class="title">主标题</div>
    <div class="item-wrap">
      <div class="bar-title">&nbsp;</div>
      <div class="bar-gap"></div>
      <div style="text-align: right;width: 22%;margin-right: 5px;">系统上线前</div>
      <div style="text-align: left;width: 22%">系统上线后</div>
    </div>
    <div style="padding-top: 5px;"></div>

    <div class="item-wrap"  v-for="o in 5 " :key="o" >
      <div class="bar-title">你好大你好大 你好大你好大 你好大你好大 你好大你好大</div>
      <div class="bar-gap" :style="o"></div>
      <div class="bar-wrap-left">
        <div class="bar" style="width: 40%;">&nbsp;</div><span>40%&nbsp;</span></div>
      <div class="bar-wrap-right">
        <div class="bar" style="width: 20%;">&nbsp;</div><span>&nbsp;20%</span></div>
    </div>
  </div>

  <div style="width: 40%;font-size: x-small;float: left">
    <div class="title">主标题</div>
    <div class="item-wrap">
          <div class="bar-title">&nbsp;</div>
          <div class="bar-gap"></div>
          <div style="text-align: right;width: 22%;margin-right: 5px;">系统上线前</div>
          <div style="text-align: left;width: 22%">系统上线后</div>
    </div>
    <div style="padding-top: 5px;"></div>

    <div class="item-wrap"  v-for="o in 5 " :key="o" >
      <div class="bar-title">你好大你好大 </div>
      <div class="bar-gap" :style="o"></div>
      <div class="bar-wrap-left">
        <div class="bar" style="width: 60%;">&nbsp;</div><span>40%&nbsp;</span></div>
      <div class="bar-wrap-right">
        <div class="bar" style="width: 20%;">&nbsp;</div><span>&nbsp;20%</span></div>
    </div>
  </div>
</div>
</template>

<script>
export default {

}
</script>

<style >
  .chart-wrap {
    width: 50%;
    font-size: x-small;
  }
    .title {}
    .item-wrap {
      margin-top: 10px;
      display: flex;
      flex-direction: row;
      align-items: flex-start;
      justify-content: space-between;
      flex-wrap: nowrap;
      }
      .bar-title {
        flex: none;
        width: 54%;
      }
      .bar-wrap-left {
        width: 22%;
        margin-right: 5px;
      }
      .bar-wrap-right {
        width: 22%;
      }
      .bar-wrap-left span {
        float: right;
      }
      .bar-wrap-left div {
        overflow: hidden;
        float: right;
        width: 0%;
        background: #00FFFF;
        animation: 1s toline linear;
        border-radius: 4px;
      }
      .bar-wrap-right span {
        float: left;
      }
      .bar-wrap-right div {
        overflow: hidden;
        float: left;
        width: 0%;
        background: #00FFFF;
        animation: 1s toline linear;
        border-radius: 4px;
      }
      .bar{
        height: 7px;
        margin-top: 3px;
      }
      .bar-gap{
        width: 10px;
      }

    @keyframes toline {
    0% {
      width: 0%;
    }/*
    50% {
      width: 10%;
    }*/
    100% {
      width: 20%;
    }
  }
</style>
