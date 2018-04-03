<template>
 <panel title="京东智投" :class="$style.panel">
     <section :class="$style.content">
         <img src="//img12.360buyimg.com/jrpmobile/jfs/t7162/219/4755741/18941/4e51a5aa/597b066dNf6c7a972.jpg?width=750&height=120" alt="">
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

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  margin-bottom: 0!important;
  > h4 {
    display: none;
  }
  .content {
    height: 102px;
    img {
      display: block;
      width: 100%;
      height: 102px;
    }
  }
}
</style>
