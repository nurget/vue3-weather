<template>
    <div id="mapContainer">
        <div id="map">

        </div>
    </div>

</template>

<script>
export default {
    data() {
        return {};
    },
    mounted() {
        const API_KEY = import.meta.env.VITE_APP_KAKAO_KEY;
        if (window.kakao && window.kakao.maps) {
            this.initMap();
        } else {
            const script = document.createElement('script');
            /* global kakao */
            script.onload = () => kakao.maps.load(this.initMap);
            script.src =
                `http://dapi.kakao.com/v2/maps/sdk.js?autoload=false&appkey=${API_KEY}`;
            document.head.appendChild(script);
        }
    },
    methods: {
        initMap() {
            var mapContainer = document.getElementById('map'), // 지도를 표시할 div
                mapOption = {
                    center: new kakao.maps.LatLng(37.559906, 126.942906303), // 지도의 중심좌표
                    level: 7, // 지도의 확대 레벨
                };

            var map = new kakao.maps.Map(mapContainer, mapOption);
            var positions = [
                {
                    latlng: new kakao.maps.LatLng(37.559901686, 126.942906303),
                },
            ];

            // 마커 생성
            positions.forEach(function (pos) {
                var marker = new kakao.maps.Marker({
                    position: pos.latlng, // 마커의 위치
                });
                // 마커가 지도 위에 표시되도록 설정
                marker.setMap(map);
            });
        },
    },
};
</script>

<style lang="scss" scoped>
@import "@/scss/main.scss";

#mapContainer {
  @include center;
  width: 100%;
  height: 35%;

  #map {
    width: 80%;
    height: 90%;
    border-radius: 10px;
  }
}
</style>