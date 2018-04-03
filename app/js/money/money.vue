<template>
 <panel :class="$style.panel" title="理财精选">
     <section :class="$style.content">
        <dl :class="$style.item" v-for="item in items" :key="item.title">
            <dt>{{item.title}}<span>{{item.sub}}</span></dt>
            <dd>{{item.rate}}</dd>
            <dd>{{item.text}}</dd>
        </dl>
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
          title: "定期理财",
          sub: "理财首选",
          rate: "5.60%",
          text: "历史年化回报率"
        },
        {
          title: "小白理财",
          sub: "理财首选",
          rate: "4.22%",
          text: "7日年化收益率"
        },
        {
          title: "月月盈",
          sub: "养老保障",
          rate: "5%",
          text: "7日年化收益率"
        },
        {
          title: "小白基金",
          sub: "天天赚钱",
          rate: "4.27%",
          text: "7日年化收益率"
        }
      ]
    };
  },
  components: {
    Panel
  }
};
</script>

<style  lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  .content {
    @include flex(row);
    justify-content: space-around;
    box-sizing: border-box;
    &::after{
        display: block;
        content: "";
        position: relative;
        top: -208px;
        width: 100%;
        height: 0;
        border-bottom: 1px solid #ddd;
        box-sizing: border-box;
    }
    .item {
      position: relative;
      width: 50%;
      font-weight: bold;
      box-sizing: border-box;
      &::after {
        display: block;
        position: absolute;
        top: 50%;
        right: 0;
        content: "";
        width: 1px;
        height: 136px;
        margin-top: -68px;
        border-right: 1px solid #eee;
      }
      &:nth-child(2n) {
        &::after {
          display: none;
        }
      }
      padding: 34px 16px;
      dt {
        font-size: 30px;
        line-height: 42px;
        counter-reset: #333;
        span {
          padding: 0 8px;
          margin-left: 2px;
          font-size: 22px;
          color: #ff5155;
          border: 1px solid #ff5155;
          vertical-align: 1;
        }
      }
      dd {
        &:nth-child(2) {
          height: 58px;
          font-weight: 700;
          font-size: 44px;
          line-height: 58px;
          color: #ff5155;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
        &:nth-child(3){
            height: 34px;
            font-size: 24px;
            line-height: 34px;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
        }
      }
    }
  }
}
</style>
