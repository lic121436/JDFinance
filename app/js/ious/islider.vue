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
            "//img12.360buyimg.com/jrpmobile/jfs/t8491/303/504628479/60643/100648de/59a94358N92475fca.jpg?width=750&height=320"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t8437/321/1758527686/40952/f66d552f/59bf1f41N50d846f9.jpg?width=750&height=320"
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
