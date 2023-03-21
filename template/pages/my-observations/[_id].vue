<template>
    <v-app-bar color="grey-darken-2" density="compact">
        <v-btn icon to="/my-observations">
            <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
        <v-app-bar-title>{{ item.title }}</v-app-bar-title>
    </v-app-bar>
    <v-img src="https://i0.wp.com/www.i879.com/hanablog/wp-content/uploads/2021/03/4459509_s.jpg?resize=618%2C464&ssl=1">
        <v-chip>桜</v-chip>
    </v-img>
    <v-card>
        <v-card-text>
            <div>
                <span class="text-caption"><v-icon size="x-small">mdi-calendar</v-icon>{{ item.date }}<v-icon
                        size="x-small">mdi-map-marker</v-icon>{{ item.place }}</span>
            </div>
            ちょうど卒業式の日でした。
        </v-card-text>
    </v-card>
</template>

<script setup>

const item =
{
    prependAvatar: 'https://i0.wp.com/www.i879.com/hanablog/wp-content/uploads/2021/03/4459509_s.jpg?resize=618%2C464&ssl=1',
    title: '桜開花',
    subtitle: 'ちょうど卒業式の日でした。',
    place: '東京都世田谷区駒沢',
    path: '/my-observations/#',
    date: '2023/03/20',
    species: '桜',
}

</script>