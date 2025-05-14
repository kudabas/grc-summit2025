<template>
    <div>
        <div class=" pt-[100px] h-[350px] lg:pt-atas 2xl:px-60 lg:h-[600px] flex-container bg-[url('@/assets/image/reach-bg.png')] bg-cover bg-no-repeat">
            <div class="text-left w-1/2 pr-10 py-40 font-bold">
                <h1 class="text-[62px]">{{ title }}</h1>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const title = ref('Reach Us');
</script>

<style lang="scss" scoped>

</style>