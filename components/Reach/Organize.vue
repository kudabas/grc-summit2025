<template>
    <div>
        <div class="py-[50px] lg:pt-atas 2xl:px-60 flex-container bg-white bg-cover bg-no-repeat">
            <div class="text-black w-full ">
                <div>
                    <h1 class="font-bold text-[32px] py-5">{{ title }}</h1>
                </div>
                <div class="py-10 w-full mx-auto">
                    <div class="text-black gap-10 grid grid-cols-1 lg:grid-cols-2 pb-10 justify-center items-center">
                        <div v-for="(data, index) in imageArray" :key="index" class="text-left font-bold flex gap-10">
                            <div class=" ">
                                <img :src="data.src" alt="GRC Summit" class="w-[131px] object-cover mx-auto" />
                            </div>
                            <div class=" font-normal ">
                                <h1 class=" font-bold pb-5"> {{ data.text }} </h1>
                                <h2> {{ data.addres }} </h2>
                                <h3> {{ data.phone }} </h3>
                                <h4> {{ data.link }} </h4>
                            </div>
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
    { src: pagi, text: 'Perkumpulan Profesional Governansi Indonesia (PaGI)', addres: 'Gedung Tifa lantai 3 , Ruang 304 Jl. Kuningan Barat No. 26  12710 Jakarta', phone: 'P.  0815-1625-670', link: 'www.governansi.org' },
    { src: grc, text: 'Perkumpulan Tatakelola Manajemen Risiko dan Kepatuhan (Asosiasi GRC)', addres: 'Gedung Tifa lantai 3 , Ruang 304 Jl. Kuningan Barat No. 26  12710 Jakarta ', phone: 'P. 0813-1101-0503', link: 'www.theigrca.org' },
    { src: irmapa, text: 'IRMAPA', addres: 'Gedung Tifa, Lt. 3, Suite 304 Jl. Kuningan Barat No. 26 Jakarta Selatan 12710 ', phone: 'P: 08111291253', link: 'E. sekretariat@irmapa.org' },
    { src: icopi, text: 'ICoPI', addres: 'STMA Trisakti, Kampus C Gedung B Jl. jend. A Yani Kav 85, Jakarta Timur 13210', phone: 'P. 081-11291-253', link: 'www.governansi.org' },
    { src: ipaca, text: 'IPACA', addres: 'Gedung Tifa lantai 3 , Ruang 304 Jl. Kuningan Barat No. 26  12710 Jakarta', phone: 'P.  0815-1625-670', link: 'www.governansi.org' },
]);
</script>

<style lang="scss" scoped></style>
