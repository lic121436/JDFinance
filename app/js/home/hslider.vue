<template>
    <article>
        <slider :items="items" :cname="$style.slider"></slider>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name: item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script type="text/ecmascript-6">
import Slider from '../core/slider';

export default {
  data() {
    return {
      items: [
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t17215/109/1091647092/48863/61fc1fd6/5abb622cNc932a685.jpg?width=750&height=320"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t18595/119/1080925611/26405/263b9103/5abb6265N6fe84326.jpg?width=750&height=320"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t16933/223/1054856242/49211/28f2dd23/5abb628dN30aa1258.jpg?width=750&height=320"
        },
        {
          href: "home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t17800/105/1127304192/49668/a783398/5abb62a8Nbbf3147e.jpg?width=750&height=320"
        }
      ],
      enters: [
        {
          href: "download",
          img:
            "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
          title: "优惠券"
        },
        {
          href: "download",
          img:
            "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
          title: "领红包"
        },
        {
          href: "home",
          img:
            "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
          title: "抢钢镚"
        },
        {
          href: "home",
          img:
            "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
          title: "白条提额"
        }
      ]
    };
  },
  components: {
    Slider
  }
};
</script>

<style  lang="scss" module>
@import "../../css/element.scss";
.slider {
  margin-top: 120px;
  img{
      width: 100%;
  }
}
.list {
  padding-top: 40px;
  padding-bottom: 20px;
  @include list(row);
  background: #fff;
  justify-content: space-around;
  a {
    text-decoration: none;
  }
  .item {
    text-align: center;
    img {
      display: inline-block;
      width: 90px;
      height: 90px;
    }
    h4 {
      margin-top: 12px;
      font-size: 26px;
      color: #666;
    }
  }
}
</style>
