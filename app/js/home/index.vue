<template lang="html">
    <div>
      <heador></heador>
      <hslider></hslider>
      <novice></novice>
      <borrow></borrow>
      <money></money>
      <product></product>
      <life></life>
      <hfooter></hfooter>
      <navbar></navbar>
    </div>
</template>

<script>
import Heador from "../public/header";
import Hslider from "./hslider";
import Novice from "./novice";
import Borrow from "./borrow";
import Money from "./money";
import Product from "./product";
import Life from "./life";
import Hfooter from "../public/footer";
import Navbar from "../public/navbar";

export default {
  components: {
    Heador,
    Hslider,
    Novice,
    Borrow,
    Money,
    Product,
    Life,
    Hfooter,
    Navbar
  }
};
</script>

<style>
body {
  background: #f5f5f5;
}
</style>

