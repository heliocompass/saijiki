<template>
    <v-app-bar color="grey-darken-2" density="compact">
        <v-app-bar-title>New Observation</v-app-bar-title>
    </v-app-bar>
    新規投稿
    <v-card class="pa-4">
        <v-form fast-fail method="get" action="/">
            <v-file-input accept="image/*" label="Select an image" outlined filled prepend-icon="mdi-camera"
                capture="camera"></v-file-input>
            <v-text-field label="タイトル"></v-text-field>
            <v-textarea label="メモ" variant="outlined"></v-textarea>
            <v-btn type="submit" color="primary" block class="mt-2">投稿</v-btn>
        </v-form>
    </v-card>
</template>
