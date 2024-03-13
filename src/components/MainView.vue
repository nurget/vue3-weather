<template>
  <div class="leftContainer">
      <div id="cityNameBox">
          <div class="cityName">
              <p>San Fransisco</p>
              <p>May 28, 2024</p>
          </div>
      </div>
      <div id="contentBox">
          <div class="buttonBox">
              <div class="buttonBackground">
                  <button class="forecast">Forecast</button>
                  <button class="airquality">Air Quality</button>
              </div>
          </div>
          <div class="weatherBox">
              <div class="weatherDegree">
                  <p>10&deg;</p>
              </div>
              <div class="weatherIcon">
                  <img src="@/assets/images/01d.png" alt="MainLogo" />
              </div>
              <div class="weatherData">
                  <div>
                      <p></p>
                      <p></p>
                  </div>
              </div>
          </div>
      </div>
      <div id="todayWeather">
          <div class="textBox">
              <p>시간대별 날씨 정보</p>
              <p>이번주 날씨 보기</p>
          </div>
          <div class="timelyWeatherBox">
              <div class="timelyWeather">
                  <div class="icon">
                      <img src="@/assets/images/02d.png" alt="" />
                  </div>
                  <div class="data">
                      <p class="time">2pm</p>
                      <p class="currentDegree">32&deg;</p>
                      <div>
                          <img src="@/assets/images/drop.png" alt="" />
                          <p class="fall">15%</p>
                      </div>
                  </div>
              </div>
          </div>
      </div>
      <nav>
          <i class=""></i>
          <i class=""></i>
          <i class=""></i>
          <i class=""></i>
      </nav>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/scss/main";

.leftContainer {
    width: 324px;
    height: 700px;
    border-radius: 50px;
    background: linear-gradient(#16455f, #0e1239);
    box-shadow: 5px 5px 10px gray;

    #cityNameBox {
        width: 100%;
        height: 10%;

        .cityName {
            @include c-center;
            width: 100%;
            height: 100%;

            p {
                color: white;
                font-family: "Poppins", sans-serif;
                line-height: 2.5;
                text-align: center;

                &:first-child {
                    width: 241px;
                    height: 33px;
                    font-size: 1.35rem;
                }
                &:last-child {
                    width: 160px;
                    height: 19px;
                    font-size: 0.9rem;
                    font-weight: 100;
                }
            }
        }
    }

    #contentBox {
        width: 100%;
        height: 62.5%;

        .buttonBox {
            @include center;
            width: 100%;
            height: 20%;

            .buttonBackground {
                width: 224px;
                height: 35px;
                background-color: #052137;
                border-radius: 10px;
                display: flex;

                button {
                    width: 112px;
                    height: 35px;
                    border: 0;
                    border-radius: 7.5px;
                    outline: 0;
                    cursor: pointer;

                    &.forecast {
                        background-color: #0889ff;
                        color: white;
                    }
                    &.airquality {
                        background-color: transparent;
                        color: #467599;
                    }
                }
            }
        }
    }
}
</style>