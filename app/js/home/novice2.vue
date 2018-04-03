<template>
    <panel :cname="$style.panel" title="理财精选">
        <section :class="$style.content">
            <ul>
                <li :class="$style.item">
                    <p :class="$style.title">
                        <span>定期理财</span>
                        <label>90天可质押</label>
                    </p>
                    <p :class="$style.value">5.50%</p>
                    <p :class="$style.desc">历史年化结算利率</p>
                </li>
                <li :class="$style.item">
                    <p :class="$style.title">
                        <span>固收理财</span>
                        <label>理财推荐</label>
                    </p>
                    <p :class="$style.value">5.80%</p>
                    <p :class="$style.desc">综合年化收益率</p>
                </li>
                <li :class="$style.item">
                    <p :class="$style.title">
                        <span>基智账户</span>
                        <label>组合投资</label>
                    </p>
                    <p :class="$style.value">8%-10%</p>
                    <p :class="$style.desc">止盈年化收益率</p>
                </li>
                <li :class="$style.item">
                    <p :class="$style.title">
                        <span>小白基金</span>
                        <label>超短期</label>
                    </p>
                    <p :class="$style.value">5.00%</p>
                    <p :class="$style.desc">7日年化收益率</p>
                </li>

            </ul>
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

<style scoped lang="scss" module>
@import "../../css/element.scss";
.panel {
  .content {
      ul{
          overflow: hidden;
      }
    .item {
      float: left;
      position: relative;
      width: 50%;
      height: 218px;
      padding-left: 32px;
      box-sizing: border-box;
      &::before {
        display: block;
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 1px;
        background: #eee;
        transform: scaleY(0.5);
        transform-origin: 0 0;
      }
      &:nth-child(odd)::after {
        content: "";
        position: absolute;
        right: 0;
        top: 40px;
        width: 2px;
        height: 136px;
        display: block;
        background: #eee;
        transform: scaleX(0.5);
        transform-origin: 0 0;
      }
      .title {
        height: 42px;
        margin: 34px 0 16px;
        line-height: 42px;
        font-family: PingFangSC-Medium;
        color: #333;
        box-sizing: border-box;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
        span {
          display: block;
          float: left;
          height: 42px;
          color: #333;
          font-weight: 700;
          font-size: 30px;
          line-height: 42px;
        }
        label {
          float: left;
          position: relative;
          top: 3px;
          left: 8px;
          height: 34px;
          padding: 0 8px;
          line-height: 34px;
          font-size: 24px;
          color: #ff5155;
          text-align: center;
          &::before {
            display: block;
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            min-width: 104px;
            width: 200%;
            height: 200%;
            line-height: 34px;
            border: 1px solid #ff5155;
            transform: scale(0.5, 0.5);
            transform-origin: 0 0;
            box-sizing: border-box;
          }
        }
      }
      .value {
        height: 58px;
        line-height: 58px;
        font-weight: 700;
        font-size: 44px;
        color: #ff5155;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
      }
      .desc {
        font-size: 24px;
        height: 34px;
        line-height: 34px;
        color: #999;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
      }
    }
  }
}
</style>
