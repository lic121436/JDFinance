<template>
    <panel title="轮播图" :class="$style.panel">
        <section :class="$style.content">
        <slider :items="items" :cname="$style.slider"></slider>
        </section>
    </panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../core/panel";
import Slider from "../core/slider";

export default {
  data() {
    return {
      items: [
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t11149/181/856008463/68797/dc303e9/59f97baeN3cdae084.jpg?width=750&height=400"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t9994/205/2575467053/189117/125e7b05/59f97c36N7599be57.png?width=750&height=400"
        }
      ]
    };
  },
  components: {
    Panel,
    Slider
  }
};
</script>

<style  lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  margin-top: 120px;
  >h4{
      display: none;
  }
  .content {
    .slider {
      img{
        width: 100%;
      }
    }
  }
}
</style>
