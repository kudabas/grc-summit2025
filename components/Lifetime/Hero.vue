<template>
    <div>
        <div
            class=" w-full 2xl:px-60 flex-container bg-[url('@/assets/image/curve.png')] bg-cover bg-center bg-gray-950 bg-no-repeat">
            <div class="text-left w-full pr-10 py-40 font-bold">
                <div class=" w-full mx-auto">
                    <div class=" text-black flex gap-10 py-10 pb-[100px] justify-center items-center">
                        <div class="text-center font-bold">
                            <img :src="achiev" alt="GRC Summit" class="w-full h-auto object-cover mx-auto" />
                        </div>
                    </div>
                    <div class=" text-[21px] text-center font-normal ">
                        <h2 class=" py-10">{{ content1 }}</h2>
                        <h2 class="">{{ content2 }}</h2>
                    </div>
                    <div class=" text-center font-bold text-[37px] py-10 pt-[100px]">
                        <h1>{{ tittle }}</h1>
                        <div class=" border-1 border-gray-400 w-[1000px] flex mx-auto"></div>
                    </div>
                    <div class=" text-black flex gap-10 py-10 pb-[100px] justify-center items-center">
                        <div class="text-center font-bold">
                            <img :src="list" alt="GRC Summit" class="w-full h-auto object-cover mx-auto" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import achiev from '@/assets/image/lifetime/achievment.png';
import list from '@/assets/image/lifetime/list-lifetime.png';

const content1 = ref('As part of GRC Summit events, the GRC Association giving awards to practitioners and academicians in the GRC field who have consistently practiced, socialized, and developed the implementation of GRC in organizations. ');
const content2 = ref('This event is the 5th year of awarding Lifetime Achievement to individuals who deserve the GRC award. After going through selection and judging, this year, two awards will be given to individuals who deserve them this year.');
const tittle = ref('List of The Previous Lifetime Achievement Awardees ')
</script>

<style lang="scss" scoped></style>v