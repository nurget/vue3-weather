<template>
  <div class="rightContainer">
      <div id="cityNameBox">
          <div class="cityName">
              <p>Seoul</p>
              <p>March 28, 2024</p>
          </div>
      </div>
      <div id="contentsBox">
          <div class="buttonBox">
              <div class="buttonBackground">
                  <button class="forecast">Forecast</button>
                  <button class="airquality">Air Quality</button>
              </div>
          </div>
          <div class="weatherBox">
              <div class="airCondition">
                  <p>너무 더웡</p>
              </div>
              <div class="detail">
                  <div class="title">
                      <p>Detail Temperatires</p>
                  </div>
                  <div class="data">
                      <div class="dataName">
                          <p></p>
                          <p></p>
                      </div>
                      <div class="dataValue">
                          <p>
                              <span></span> &deg;
                          </p>
                      </div>
                  </div>
              </div>
          </div>
      </div>
      <Map />
      <nav>
          <i class="material-symbols-outlined">home</i>
          <i class="material-symbols-outlined">location_on</i>
          <i class="material-symbols-outlined">chart_data</i>
          <i class="material-symbols-outlined">settings</i>
      </nav>
  </div>
</template>

<script>
import Map from "@/components/Map.vue";

export default {
    components: {
        Map,
    }
}
</script>

<style lang="scss" scoped>
@import "@/scss/main";
@import "@/scss/subview";
</style>