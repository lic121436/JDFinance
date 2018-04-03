<template>
 <panel title="下载APP" :class="$style.panel">
     <section :class="$style.content">
         <div></div>
         <p>立即下载</p>
         <span>copyright</span>
     </section>
 </panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../core/panel";
export default {
  data() {
    return {};
  },
  components: {
    Panel
  }
};
</script>

<style  lang="scss" module>
@import "../../css/element.scss";
html,
body {
  background: #fff;
}
.panel {
  @include panel;
  margin: 0 !important;
  > h4 {
    display: none;
  }
  .content {
    @include flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 1136px;
    > div {
      width: 600px;
      height: 800px;
      background: url(//img12.360buyimg.com/jrpmobile/jfs/t8956/285/1249806938/50853/8cd3c8f0/59b65f36N05367075.png)
        no-repeat;
      background-size: 100% auto;
    }
    > p {
      position: fixed;
      bottom: 130px;
      height: 50px;
      width: 471px;
      @include btn($size:28px,$bgcolor:#f1443e);
      line-height: 50px;
    }
    >span{
       position: fixed;
       bottom: 16px;
       font-size: 24px;
       color: #666; 
    }
  }
}
</style>
