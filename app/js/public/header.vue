<template>
 <div :class="$style.header">
     <span :class="$style.left">
         <em>注册</em>&nbsp;|&nbsp;<em>登陆</em>
     </span>
     <btn :class="$style.btnDownload">APP下载</btn>
 </div>
</template>

<script type="text/ecmascript-6">
import btn from "../core/btn";

export default {
  data() {
    return {};
  },
  components: {
    btn
  }
};
</script>

<style scoped lang="scss" module>
.header {
  z-index: 100;
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  height: 100px;
  line-height: 100px;
  color: #666;
  font-size: 32px;
  background: url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) #fff center center no-repeat;
  background-size: auto 50%;
  .left{
      height: 30px;
      margin: 17px 0 0 18px;
      font-size: 28px;
      line-height: 30px;
  }
  .btnDownload{
      float: right;
      min-width: 120px;
      height: 56px;
      padding: 0;
      margin: 28px 24px 0 0;
      line-height: 56px;
      font-size: 24px;
      border-width: 0;
      border-radius: 4px;
  }
}
</style>
