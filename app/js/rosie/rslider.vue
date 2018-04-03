<template>
    <panel title="金融头条" :class="$style.panel">
        <section :class="$style.content">
          <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="(item, index) in items" :key="index">{{item.title}}<em>></em></swiper-slide>
          </swiper>
        </section>
    </panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../core/panel";
import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  data() {
    return {
      options: {
        direction: "vertical",
        autoplay: true,
        loop: true,
        notNextTick: false
      },
      items: [
        {
          title: "签到领流量，1元500M！"
        },
        {
          title: "百万白条券免费送，速来领取！！ "
        },
        {
          title: "签到领流量，1元500M！ "
        },
        {
          title: "百万白条券免费送，速来领取！！ "
        }
      ]
    };
  },
  components: {
    Panel,
    swiper,
    swiperSlide
  }
};
</script>

<style lang="scss">
.swiper-container-vertical {
  height: 72px;
  .swiper-slide {
    font-family: PingFangSC-Medium;
    font-size: 28px;
    color: #333;
    em {
      float: right;
      margin-right: 20px;
      color: #ddd;
    }
  }
}
</style>


<style  lang="scss" module>
@import "~swiper/dist/css/swiper.css";
@import "../../css/element.scss";
.panel {
  @include panel;
  margin-top: 120px !important;
  > h4 {
    display: none;
  }
  .content {
    height: 72px;
    padding-left:178px;
    line-height: 72px;
    background:url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) no-repeat left top;
    background-size: contain;
    overflow: hidden;
  }
}
</style>
