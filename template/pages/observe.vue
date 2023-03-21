<template>
    <v-app-bar color="grey-darken-2" density="compact">
        <v-app-bar-title>New Observation</v-app-bar-title>
    </v-app-bar>

    新規投稿
    <div>
        <v-row align="center" justify="center">
            <v-col cols="12" sm="6" md="4">
                <v-file-input v-model="selectedFile" accept="image/*" label="Select an image" outlined filled
                    prepend-icon="mdi-camera" @change="uploadFile"></v-file-input>
            </v-col>
        </v-row>
    </div>
    <div class="d-flex align-center justify-center" style="height: 100vh">
        <v-card width="30rem" class="pa-4">
            <v-form fast-fail method="get" action="/">
                <v-text-field label="タイトル"></v-text-field>
                <v-textarea label="メモ" variant="outlined"></v-textarea>
                <v-btn type="submit" color="primary" block class="mt-2">投稿</v-btn>
            </v-form>
        </v-card>
    </div>
</template>

<script setup>
const items = [
    {
        prependAvatar: 'https://i0.wp.com/www.i879.com/hanablog/wp-content/uploads/2021/03/4459509_s.jpg?resize=618%2C464&ssl=1',
        title: '桜開花',
        subtitle: 'ちょうど卒業式の日でした。',
        place: '東京都世田谷区駒沢',
        path: '/my-observations/#',
        date: '2023/03/20',
        species: '桜',
    },

    {
        prependAvatar: "https://via.placeholder.com/350x200",
        title: 'title',
        subtitle: 'notes',
        path: '/my-observations',
        place: '(place)',
        date: 'YYYY/MM/DD',
        species: '(species)',
    },

    {
        prependAvatar: "https://via.placeholder.com/350x200",
        title: 'title',
        subtitle: 'notes',
        path: '/my-observations',
        place: '(place)',
        date: 'YYYY/MM/DD',
        species: '(species)',
    },

    {
        prependAvatar: "https://via.placeholder.com/350x200",
        title: 'title',
        subtitle: 'notes',
        path: '/my-observations',
        place: '(place)',
        date: 'YYYY/MM/DD',
        species: '(species)',
    },

    {
        prependAvatar: "https://via.placeholder.com/350x200",
        title: 'title',
        subtitle: 'notes',
        path: '/my-observations',
        place: '(place)',
        date: 'YYYY/MM/DD',
        species: '(species)',
    },
];
</script>