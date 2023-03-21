<template>
    <link href="https://cdn.jsdelivr.net/npm/@mdi/font@5.x/css/materialdesignicons.min.css" rel="stylesheet">
    <v-layout>
        <v-main>
            <slot></slot>
            <v-bottom-navigation grow>
                <v-btn to="/">
                    <v-icon>mdi-map</v-icon>
                    マップ</v-btn>
                <v-btn to="/observe">
                    <v-icon>mdi-camera</v-icon>
                    投稿</v-btn>
                <v-btn to="/my-observations">
                    <v-icon>mdi-account</v-icon>
                    マイ観測</v-btn>
            </v-bottom-navigation>
        </v-main>
    </v-layout>
</template>
