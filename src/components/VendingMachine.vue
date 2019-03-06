<template>
    <div>
        <h2>自販機の画像を貼って下さい</h2>
        <input type="file" @change="onFileChange" v-if="showVendingButton">
        <img v-show="uploadImage" :src="uploadImage" id="vendingImage">
    </div>
</template>

<script>
    export default {
        data() {
            return {
                uploadImage: '',
                showVendingButton: true
            }
        },
        methods: {
            onFileChange(e) {
                let files = e.target.files || e.dataTransfer.files;
                this.createImage(files[0])
            },
            createImage(file) {
                let reader = new FileReader();
                reader.onload = (e) => {
                    this.uploadImage = e.target.result;
                }
                reader.readAsDataURL(file)
                document.getElementById('vendingImage').with = 400;
                document.getElementById('vendingImage').height = 300;
                this.showVendingButton = false
            }
        }
    }
</script>