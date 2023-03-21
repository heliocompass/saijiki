<template>
    <v-app-bar color="grey-darken-2" density="compact">
        <v-app-bar-title>Observations Map</v-app-bar-title>
    </v-app-bar>
    <v-card id="google-map">
        <v-btn icon rounded elevation="2" id="add-btn" to="/observe">
            <v-icon size="x-large">mdi-camera</v-icon>
        </v-btn>
    </v-card>
</template>

<style scoped>
#google-map {
    height: 100vh;
    width: 100vw;
}

#add-btn {
    position: absolute;
    bottom: 8rem;
    right: 2rem;
}
</style>