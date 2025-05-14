<template>
    <div>
        <div class=" p-5 lg:p-0 pt-[50px] lg:pt-[100px]  lg:pt-atas 2xl:px-60  flex-container bg-white bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-black">
                <div class="">
                    <h1 class=" font-bold text-[37px]">{{ title }}</h1>
                </div>
                <div class=" text-justify py-10 ">
                    <h2 class="text-[16px]"> {{ isi1 }} </h2>
                    <h2 class="text-[16px] py-7"> {{ isi2 }} </h2>
                </div>
            </div>
        </div>
        <img :src="bat" alt="GRC Summit" class="w-full h-auto object-cover" />

        <div class=""></div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import bat from '@/assets/image/bates.png';

const title = ref('About GRC Summit 2025');
const isi1 = ref(' The rapid digital transformation has reshaped the global business environment, presenting both unprecedented opportunities and complex challenges. In this post-digital era, organizations are required to adopt innovative Governance, Risk, and Compliance (GRC) frameworks that integrate Environmental, Social, and Governance (ESG) principles and align with the United Nations Sustainable Development Goals (SDGs) to create long-term value.');
const isi2 = ref(' The event will delve into how the integration of ESG can enhance GRC practices, supported by the rising capabilities of Artificial Intelligence (AI) to improve risk management, streamline compliance, and strengthen governance. It will also provide a platform for diverse stakeholders to exchange insights on building adaptability and innovation, ultimately driving significant economic, social, and environmental impact in a rapidly evolving global landscape.');
</script>

<style lang="scss" scoped>

</style>