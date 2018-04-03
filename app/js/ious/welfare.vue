<template>
 <panel title="白条福利" :class="$style.panel">
     <section :class="$style.content">
         <div :class="$style.item" v-for="item in items" :v-key="item.title">
             <img :src="item.src" :alt="item.title">
             <div>
                 <h4>{{item.title}}</h4>
                 <p>{{item.desc}}</p>
             </div>
             <em>{{item.linkTitle}} &gt;</em>
         </div>
     </section>
 </panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../core/panel";

export default {
  data() {
    return {
      items: [
        {
          title: "开通白条",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t4378/62/155957680/9017/16463551/58affd58Nb5c9198e.jpg?width=120&height=120",
          desc: "送188元礼包",
          linkTitle: "立即开通"
        },
        {
          title: "白条闪付",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t4150/330/141981421/9147/604e3e04/58affc3bNbfa8f9d7.jpg?width=120&height=120",
          desc: "新手享158元礼包",
          linkTitle: "随机立减"
        },
        {
          title: "白条提额",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t4270/96/1102370053/8651/58b7fa5a/58bd2e10N453e9464.jpg?width=120&height=120",
          desc: "金融app专享提额礼包",
          linkTitle: "去提额"
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
  > h4{
      border-bottom: 1px solid #ddd;
  }
  .content {
    @include flex;
    .item {
      @include flex(row);
      align-items: center;
      height: 140px;
      &::after{
          content: "";
          height: 0;
          width: 100%;
          margin-left: 136px;
          border-bottom: 1px solid #ddd;
          box-sizing: border-box;
      }
      &:last-child:after{
          border-color: #fff;
      }
      > img {
        display: inline-block;
        width: 88px;
        height: 88px;
        margin: 0 32px;
      }
      > div {
        width: 344px;
        line-height: 1.8;
        font-size: 32px;
        color: #333;
        p {
          color: #999;
          line-height: 1.1;
          font-size: 24px;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
      }
      > em {
        font-size: 28px;
        color: #ff8014;
      }
    }
  }
}
</style>
