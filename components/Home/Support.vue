<template>
    <div>
        <div
            class="pb-[50px] 2xl:px-60 flex-container bg-white bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-gray-300 w-full text-center">
                <div>
                    <h1 class="font-bold text-[23px]">{{ title }}</h1>
                </div>
                <div class="py-10 w-full mx-auto">
                    <div class="text-black flex gap-10 pb-10 justify-center items-center">
                        <div v-for="(image, index) in imageArray" :key="index" class="text-center font-bold">
                            <img :src="image" alt="GRC Summit" class=" h-[40px] object-cover mx-auto" />
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


import mks from '@/assets/image/support/mks.png';
import grk from '@/assets/image/support/grk.png';
import crms from '@/assets/image/support/crms.png';
import way from '@/assets/image/support/way.png';
import erma from '@/assets/image/support/erma.png';
import wim from '@/assets/image/support/wim.png';
import top from '@/assets/image/support/top.png';


const title = ref('Supported by:');

const imageArray = ref([
    mks,
    grk,
    crms,
    way,
    erma,
    wim,
    top,
]);

</script>

<style lang="scss" scoped></style>script