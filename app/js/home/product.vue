<template>
 <panel :class="$style.panel" title="精品推荐">
     <section :class="$style.content">
         <div :class="$style.arrow">更多尖货&gt;</div>
        <slider :options="options" :items="items" cname="product-slider"></slider>
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
            "//img12.360buyimg.com/jrpmobile/jfs/t13963/267/2355123229/48850/254f797a/5a3c59aeN9cb550f6.jpg?width=335&height=421"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t13021/306/1996997425/21953/bda69db3/5a2f6a17N9da099b1.jpg?width=335&height=421"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t14125/310/1997192193/46667/3c910f8b/5a2f6a36Nad95b650.jpg?width=335&height=421"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t15784/188/381232069/39444/8878571d/5a2f6a4aNbd5a574c.jpg?width=335&height=421"
        }
      ],
      options: {
        slidesPerView: 2.3,
        spaceBetween: 30,
        freeMode: true
        // pagination: {
        //   el: ".swiper-pagination",
        //   clickable: true
        // }
      }
    };
  },
  components: {
    Panel,
    Slider
  }
};
</script>

<style  lang="scss">
.product-slider {
  .swiper-container {
    padding: 0 24px;
    box-sizing: border-box;
    .swiper-slide {
      display: inline-block;
      width: 100%;
      img {
        display: block;
        width: 100%;
        border: 1px solid #fafafa;
      }
    }
  }
}
</style>

<style  lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  .content {
    position: relative;
    padding-bottom: 40px;
    .arrow {
      position: absolute;
      right: 20px;
      top: -70px;
      font-size: 28px;
      color: #999;
    }
  }
}
</style>
