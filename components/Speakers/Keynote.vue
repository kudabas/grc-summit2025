<template>
    <div>
        <div class=" py-[50px]  lg:pt-atas 2xl:px-60 flex-container bg-white bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-black w-full ">
                <div class="">
                    <h1 class=" font-normal text-justify text-[17px]"> <span class="font-bold">GRC Summit 2024 </span> {{ title }}</h1>
                </div>
            </div>
        </div>
        <div class=" text-justify w-full mx-auto">
            <div class=" text-black flex gap-10 py-10 pb-[100px] justify-center items-center">
                <div class="text-center font-bold">
                    <img :src="speak1" alt="GRC Summit" class="w-full h-auto object-cover mx-auto" />
                    
                </div>
                <div class="text-center font-bold">
                    <img :src="speak2" alt="GRC Summit" class=" w-full h-auto object-cover mx-auto" />
                </div>
            </div>
        </div>
        <!-- <div class=" bg-white h-[200px] "></div> -->

    </div>
</template>

<script setup>
import { ref } from 'vue';
import speak1 from '@/assets/image/speak/keynote1.png';
import speak2 from '@/assets/image/speak/keynote2.png';


const title = ref(' will assemble leading national and global experts in governance, risk, and compliance to offer attendees an extensive and diverse outlook on effective governance and management practices applicable across various organizations. Speakers at the GRC Summit 2024 hail from a broad spectrum of industries and possess a wealth of expertise. Among the featured speakers are:');

// const imageArray = ref([
//     '@/assets/image/image1.png',
//     '@/assets/image/image2.png',
//     '@/assets/image/image3.png',
//     '@/assets/image/image4.png',
//     '@/assets/image/image5.png',
//     '@/assets/image/image6.png'
// ]);

</script>

<style lang="scss" scoped></style>