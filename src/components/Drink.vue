<template>
    <div>
        <h2>ドリンクの設定をして下さい</h2>
        <p>
            <span>値段</span></br>
            <input type="text" v-model="price" number></br>
            <span>{{ price }}</span>
        </p>
        <p>
            <span>名前</span></br>
            <input type="text" v-model="name"></br>
            <span>{{ name }}</span>
        </p>
        <button @click="submit">決定</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                price: 100,
                name: 'コーラ'
            }
        },
        methods: {
            submit () {

            }
        }
    }
</script>