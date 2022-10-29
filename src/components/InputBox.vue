<script setup lang="ts">
    import { ref } from "vue";
    const ID = ref("");
    const changeText = (event: any) => {
        ID.value = event.target.value;
        alert("入力されたTwitter-IDは 「" + ID.value + "」 です。");
    }
    const jump = () => {
        window.location.href='https://twitter.com/'+ID.value+'/';
    }
</script>

<template>
    <input type="text" placeholder="Twitter-IDを入力" @change="changeText">
    <br><br>
    <a href="javascript:void(0)" @click="jump">「{{ ID }}」 のTwitterを開く</a>
</template>

<style scoped>
</style>
