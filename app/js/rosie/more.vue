<template>
 <panel title="更多福利" :class="$style.panel">
     <section :class="$style.content">
        <img v-for="(item, index) in items" :src="item.src" alt="" :v-key="index">
        <p>专享福利 > </p>
     </section>
 </panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../core/panel";

export default {
  data() {
    return {
        items:[
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t7456/56/1425209238/21928/f1fe492d/599cee57Naea99020.jpg?width=250&height=330"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t7894/126/1440046618/24763/5ce6a129/599cee04Ne77b3641.jpg?width=250&height=330"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t6385/103/1675552688/24265/91be4150/59549aedNa30670f7.jpg?width=250&height=330"
            }
        ]
    };
  },
  components: {
    Panel
  }
};
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  .content {
    position: relative;
    @include flex(row);
    padding-bottom: 40px;
    img {
      width: calc(100% / 3);
      height: 280px;
    }
    p {
      position: absolute;
      top: -112px;
      right: 20px;
      height: 112px;
      line-height: 112px;
      font-size: 28px;
      color: #999;
    }
  }
}
</style>
