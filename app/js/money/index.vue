<template lang="html">
    <div>
      <heador></heador>
      <slider></slider>
      <one-banner></one-banner>
      <money></money>
      <two-banner></two-banner>
      <finance></finance>
      <three-banner></three-banner>
      <hfooter cname="mfooter"></hfooter>
      <navbar></navbar>
    </div>
</template>

<script>
import Heador from "../public/header";
import Slider from "./mslider";
import OneBanner from "./onebanner";
import TwoBanner from "./twobanner";
import Money from "./money";
import Finance from "./finance";
import ThreeBanner from "./threebanner";
import Hfooter from "../public/footer";
import Navbar from "../public/navbar";

export default {
  components: {
    Heador,
    Slider,
    OneBanner,
    Money,
    TwoBanner,
    Finance,
    ThreeBanner,
    Hfooter,
    Navbar
  }
};
</script>

<style lang="scss">
    .mfooter{
        ul{
            li:first-child{
                display: none;
            }
        }
    }
</style>



