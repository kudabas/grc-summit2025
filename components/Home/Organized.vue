<template>
    <div>
        <div
            class=" p-5 py-[50px] lg:pt-atas 2xl:px-60 flex-container bg-white bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-gray-300 w-full text-center">
                <div>
                    <h1 class="font-bold text-[23px]">{{ title }}</h1>
                </div>
                <div class="py-10 w-full mx-auto">
                    <div class="text-black flex gap-10 pb-10 justify-center items-center">
                        <div v-for="(image, index) in imageArray" :key="index" class="text-center font-bold">
                            <img :src="image" alt="GRC Summit" class=" h-[70px] object-cover mx-auto" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="bg-white"></div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';


import grc from '@/assets/image/organized/grc.png';
import pagi from '@/assets/image/organized/pagi.png';
import irmapa from '@/assets/image/organized/irmapa.png';
import icopi from '@/assets/image/organized/icopi.png';
import ipaca from '@/assets/image/organized/ipaca.png';

const title = ref('Organized by:');

const imageArray = ref([
    grc,
    pagi,
    irmapa,
    icopi,
    ipaca,
]);

</script>

<style lang="scss" scoped></style>script