
<template>
    <div class="d-flex align-center justify-center" style="height: 100vh">
        <v-card width="30rem" class="pa-4">
            <v-form fast-fail method="get" action="/">
                <v-text-field v-model="username" label="メールアドレス"></v-text-field>
                <v-text-field v-model="password" label="パスワード"></v-text-field>
                <v-btn type="submit" color="primary" block class="mt-2">ログイン</v-btn>
            </v-form>
            <div class="mt-2">
                <p class="text-body-2">アカウントをお持ちでない方は <a href="#">新規登録</a></p>
            </div>
            <a href="#" class="text-body-2 font-weight-regular">パスワードを忘れた方</a>
        </v-card>
    </div>
</template>
<script>
definePageMeta({ layout: 'noLogin' })
</script>