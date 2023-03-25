<script setup lang="ts">
import { Loader } from '@googlemaps/js-api-loader'

const currentPosition = ref({ lat: 35.681236, lng: 139.767125 });

onMounted(async () => {
    getCurrentPosition();
    const loader = new Loader({
        apiKey: 'AIzaSyBWHhQO8dhd06rN8lZUckxaPv_VY9ZY30o',
        version: 'weekly',
    })

    const google = await loader.load()
    const map = new google.maps.Map(document.getElementById('google-map'), {
        center: currentPosition.value,
        zoom: 15,
        disableDefaultUI: true,
        styles: [
            {
                featureType: 'poi',
                stylers: [{ visibility: 'off' }],
            },
            {
                featureType: 'transit',
                stylers: [{ visibility: 'off' }],
            },
        ],
    })
},)

const getCurrentPosition = () => {
    navigator.geolocation.getCurrentPosition(
        (position) => {
            const latitude = position.coords.latitude;
            const longitude = position.coords.longitude;
            console.log(`現在位置: (${latitude}, ${longitude})`);
            currentPosition.value = { lat: latitude, lng: longitude };

        },
        (error) => {
            console.error(`現在位置の取得に失敗しました: ${error.message}`);
        }
    );
}

</script>
<template>
    <v-container class="ma-0 pa-0">

        <v-app-bar color="grey-darken-2" density="compact">
            <v-app-bar-title>Map</v-app-bar-title>
        </v-app-bar>

        <div id="google-map" flat>

        </div>
    </v-container>
</template>

<style scoped>
#google-map {
    position: abasolute;
    /* ヘッダーとボタンナビゲーションの高さをマイナス */
    height: calc(100vh - 48px - 56px);
    width: 100vw;
}
</style>