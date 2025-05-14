<template>
    <div>
        <div class=" p-5 lg:p-0 pt-[0px] lg:pt-[100px] h-[350px] lg:pt-atas 2xl:px-60 lg:h-[850px] flex-container bg-[url('@/assets/image/home-bg.png')] bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-left pr-0 lg:pr-[500px] py-40">
                <h1 class=" text-[20px] lg:text-[60px]">{{ title }} <span class=" font-[1000] ">Leading Through GRC In The Post-Digital Era</span></h1>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const title = ref('Resilience To Sustainability : ');
</script>

<style lang="scss" scoped>

</style>