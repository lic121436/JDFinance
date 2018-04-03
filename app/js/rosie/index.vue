<template lang="html">
    <div>
      <heador></heador>
      <slider></slider>
      <daily></daily>
      <in></in>
      <more></more>
      <hfooter cname="mfooter"></hfooter>
      <navbar></navbar>
    </div>
</template>

<script>
import Heador from "../public/header";
import Slider from "./rslider";
import Daily from "./daily";
import In from "./in";
import More from "./more";
import Hfooter from "../public/footer";
import Navbar from "../public/navbar";

export default {
  components: {
    Heador,
    Slider,
    Daily,
    In,
    More,
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



