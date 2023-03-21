<template>
    <v-app-bar color="grey-darken-2" density="compact">
        <v-app-bar-title>My Observations</v-app-bar-title>
    </v-app-bar>
    <v-list lines="one">
        <template v-for="(item, index) in items" :key="index">
            <v-list-item :title="item.title" :prepend-avatar="item.prependAvatar" :subtitle="item.subtitle" ripple
                :to="'/my-observations/' + (index + 1)" nuxt>
                <template v-slot:title>
                    <div>
                        {{ item.title }}
                        <v-chip size="x-small">{{ item.species }}</v-chip>
                    </div>
                </template>
                <template v-slot:default>
                    <div>
                        <span class="text-caption"><v-icon size="x-small">mdi-calendar</v-icon>{{ item.date }}<v-icon
                                size="x-small">mdi-map-marker</v-icon>{{ item.place }}</span>
                    </div>
                </template>
                <template v-slot:append>
                    <v-icon>mdi-chevron-right</v-icon>
                </template>
            </v-list-item>
            <v-divider class="my-1 mx-4"></v-divider>
        </template>
    </v-list>
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