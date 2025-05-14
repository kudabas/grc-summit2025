<template>
    <div>
        <div class=" p-5 lg:p-0 py-[50px] lg:py-[50px] lg:pt-atas 2xl:px-60  flex-container bg-gray-950 bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-white ">
                <div class="">
                    <h1 class=" font-bold text-[37px]">{{ title }}</h1>
                </div>
                <div class=" text-justify py-10 ">
                    <div class=" lg:flex gap-10 py-10">
                        <div class="  ">
                            <img :src="master" alt="GRC Summit" class=" w-[500px] h-auto object-cover" />
                        </div>
                        <div class=" py-5 lg:py-0 ">
                            <h2 class=" text-center lg:text-left text-[28px] font-bold ">Day 1, August 21 (Masterclass) </h2>
                            <h3 class=" py-5">
                                <ul>
                                    <li v-for="(item, index) in dataMaster" :key="index"
                                        class="flex items-center gap-2">
                                        <span class="text-[25px]">•</span>
                                        {{ item }}
                                    </li>
                                </ul>
                            </h3>
                        </div>
                    </div>
                    <div class=" lg:flex gap-10 py-10">
                        <div class="  ">
                            <img :src="sem" alt="GRC Summit" class=" w-[500px] h-auto object-cover" />
                        </div>
                        <div class=" py-5 lg:py-0  ">
                            <h2 class=" text-center lg:text-left text-[28px] font-bold ">Day 2, August 22 (Seminar)  </h2>
                            <h3 class=" py-5">
                                <ul>
                                    <li v-for="(item, index) in dataSeminar" :key="index"
                                        class="flex items-center gap-2">
                                        <span class="text-[25px]">•</span>
                                        {{ item }}
                                    </li>
                                </ul>
                            </h3>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class=""></div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import master from '@/assets/image/masterclass.png';
import sem from '@/assets/image/seminar.png';


const title = ref('Session');

const dataMaster = ref([
    'Masterclass Session 1, GRC Foundations for ESG and SDG Integration',
    'Masterclass Session 2, Leveraging AI for GRC Excellence',
    'Practice Sharing, Q&A',
]);

const dataSeminar = ref([
    'Keynote Speech 1, Resilience and Sustainability: GRC as a Strategic Enabler',
    'Panel Discussion 1, Sustainability in Action: How GRC, ESG, and AI Support the SDGs',
    'Keynote Speakers 2, Achieving the SDGs through Governance and Innovation',
    'Panel Discussion 2, Collaborative Leadership for the Post-Digital Era: GRC, ESG, and Beyond'
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