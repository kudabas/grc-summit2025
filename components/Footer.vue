<template>
    <div>
        <img :src="bat" alt="GRC Summit" class="w-full h-auto object-cover" />
        <div class=" py-[30px]  lg:pt-atas 2xl:px-60  flex-container bg-gray-950 bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-white">
                <div class=" text-center ">
                    <h1 class=" font-normal text-[10px]">{{ title }}</h1>
                    <h2 class=" font-normal text-[13px] "> {{ title2 }} </h2>
                </div>
            </div>
        </div>

        <div class=""></div>
    </div>
</template>

<script setup>
import bat from '@/assets/image/bates.png';
const title = ref('For further inquiries, please reach us through:');
const title2 = ref('info@grcsummit.co.id');
</script>

<style lang="scss" scoped>

</style>