<template lang="html">
    <div>
      <heador></heador>
      <slider></slider>
      <welfare></welfare>
      <service></service>
      <hfooter></hfooter>
      <navbar></navbar>
    </div>
</template>

<script>
import Heador from "../public/header";
import Slider from "./islider";
import Welfare from "./welfare";
import Service from "./service";
import Hfooter from "../public/footer";
import Navbar from "../public/navbar";

export default {
  components: {
    Heador,
    Slider,
    Welfare,
    Service,
    Hfooter,
    Navbar
  }
};
</script>




