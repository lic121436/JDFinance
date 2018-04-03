<template>
 <panel title="理财精选" :class="$style.panel">
     <section :class="$style.content">
         <div :class="$style.item" v-for="item in items" :v-key="item.title">
             <img :src="item.src" :alt="item.title">
             <div>
                 <h4>{{item.title}}</h4>
                 <p>{{item.desc}}</p>
             </div>
             <em>去赚钱 &gt;</em>
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
          title: "月度理财",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76",
          desc: "预期年化收益率4.50%"
        },
        {
          title: "季度理财",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76",
          desc: "历史年化回报率5.50%"
        },
        {
          title: "一年理财",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76",
          desc: "历史年化回报率5.80%"
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
          line-height: 1.1;
          color: #ff3232;
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
