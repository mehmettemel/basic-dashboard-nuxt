<template>
  <div class="container">
    <AppNav />
    <AppMain />
    <AppAside />
  </div>
</template>

<script>
import AppAside from "../components/AppAside";
import AppMain from "../components/AppMain";
import AppNav from "../components/AppNav";
export default {
  components: {
    AppMain,
    AppAside,
    AppNav
  }
};
</script>

<style lang="scss">
.container {
  position: relative;
  width: 100%;
  height: 100vh;
  display: grid;
  grid-template-columns: 10% 1fr 400px;
  grid-template-rows: 1fr 1fr 1fr;

  @include large {
    height: 105vh;
    grid-template-columns: 1fr;
    grid-template-rows: 400px 1fr;
    padding-bottom: 4em;
  }
}
</style>
