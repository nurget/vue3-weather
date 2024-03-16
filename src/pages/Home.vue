<template>
  <div class="wrap">
      <div class="container">
          <MainView />
          <SubView />
      </div>
  </div>
</template>

<script>
import MainView from "@/components/MainView.vue";
import SubView from "@/components/SubView.vue";

export default {
    components: {MainView, SubView}
};
</script>

<!-- scoped는 현재 내가 작업하는 페이지에서만 스타일이 적용됨 -->
<style lang="scss" scoped>
@import "@/scss/main";

.wrap {
  @include center;
  width: 100%;
  height: 100vh;
  font-size: 16px;

  .container {
    @include center-sb;
    width: 55%;
    height: 90%;
    max-width: 1920px;
    max-height: 1354px;
  }
}

</style>