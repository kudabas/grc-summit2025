<template>
    <div>
        <div class=" py-[50px] lg:py-[50px] p-5 lg:p-0 lg:pt-atas 2xl:px-60 h-[300px] flex-container bg-gray-100 bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-black w-full ">
                <div class="">
                    <h1 class=" font-bold text-[37px]">{{ title }}</h1>
                </div>
            </div>
            <div class=" bg-white "></div>
        </div>
        <div class=" h-[500px] lg:h-[400px] relative bottom-[200px] text-justify py-10 w-full lg:w-[800px] mx-auto">
            <div class=" text-black flex gap-2 lg:gap-10 py-10 justify-center items-center">
                <div class="text-center font-bold">
                    <img :src="speak1" alt="GRC Summit" class=" lg:pt-0 pt-2 w-[200px] h-auto object-cover mx-auto" />
                    <h1 class="text-[26px] mt-4">Prof. Peter Verhezen</h1>
                    <h2 v-for="(item, index) in dataSpeak1" :key="index" class="py-2">
                        • {{ item }}
                    </h2>
                </div>
                <div class="text-center font-bold">
                    <img :src="speak2" alt="GRC Summit" class=" w-[200px] h-auto object-cover mx-auto" />
                    <h1 class="text-[26px] mt-4">Dr. Antonius Alijoyo</h1>
                    <h2 v-for="(item, index) in dataSpeak2" :key="index" class="py-2">
                        • {{ item }}
                    </h2>
                    <img :src="world" alt="GRC Summit" class="w-[50px] h-auto object-cover mx-auto" />
                </div>
            </div>
        </div>
        <!-- <div class=" bg-white h-[200px] "></div> -->

    </div>
</template>

<script setup>
import { ref } from 'vue';
import speak1 from '@/assets/image/speak/peter.png';
import speak2 from '@/assets/image/speak/Dr.AntoniusAlijoyo.png';
import world from '@/assets/image/speak/wef.png';


const title = ref('Speakers');

const dataSpeak1 = ref([
    'IFC - International Finance Corporation (World Bank Group) – Senior Advisor Corporate Governance',
    ' The Boardroom Partnership Think Tank – Senior Partner & Co-founder',
]);

const dataSpeak2 = ref([
    'Supervisory Board of the GRC Association',
    'Member of The World Economic Forum\'s (WEF) Global Future Council On Complex Risks 2023−2024',
]);

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