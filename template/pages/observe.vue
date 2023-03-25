<script setup lang="ts">
import species from '~~/data/species';
import VueDatePicker from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css'

const date = ref(new Date())
const format = (date: Date) => {
    const day = date.getDate();
    const month = date.getMonth() + 1;
    const year = date.getFullYear();

    return `${year}/${month}/${day}`;
}
</script>


<template>
    <v-app-bar color="grey-darken-2" density="compact">
        <v-app-bar-title>New Observation</v-app-bar-title>
    </v-app-bar>
    新規投稿
    <v-card class="pa-4">
        <v-form fast-fail method="get" action="/">
            <v-file-input accept="image/*" label="Select an image" outlined filled prepend-icon="mdi-camera"
                capture="camera"></v-file-input>
            <v-autocomplete variant="outlined" density="compact" label="観測種目" item-value="id" item-title="species"
                :items="species"></v-autocomplete>
            <VueDatePicker :format="format" :enable-time-picker="false" disable-month-year-select :max-date="new Date()"
                :clearable="false" text-input auto-apply locale="jp" v-model="date" class="mb-4">
            </VueDatePicker>
            <v-text-field label="タイトル"></v-text-field>
            <v-textarea label="メモ" variant="outlined"></v-textarea>
            <v-btn type="submit" color="primary" block class="mt-2">投稿</v-btn>
        </v-form>
    </v-card>
</template>
