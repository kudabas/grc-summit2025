<template>
    <div>
        <div class="py-[50px] lg:pt-atas 2xl:px-60 flex-container bg-white bg-auto lg:bg-cover bg-no-repeat">
            <div class="text-black w-full">
                <div>
                    <h1 class="font-bold text-[32px] py-5">{{ title }}</h1>
                </div>
                <div class="py-10 w-full mx-auto">
                    <div class="text-black gap-10 grid grid-cols-2 pb-10 justify-center items-center">
                        <div v-for="(data, index) in imageArray" :key="index" class="text-left font-bold gap-10 grid grid-cols-3">
                            <div class="  ">
                                <img :src="data.src" alt="GRC Summit" class=" object-cover mx-auto"" />
                            </div>
                            <div class=" col-span-2 font-normal text-justify ">
                                <h1 class=" font-bold pb-5"> {{ data.text }} </h1>
                                <h2> {{ data.addres }} </h2>
                                <h3> {{ data.phone }} </h3>
                                <h4> {{ data.link }} </h4>
                                <h3> {{ data.mobile }} </h3>
                                <h4> {{ data.mail }} </h4>
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

import mks from '@/assets/image/support/mks.png';
import grk from '@/assets/image/support/grk.png';
import crms from '@/assets/image/support/crms.png';
import way from '@/assets/image/support/way.png';
import erma from '@/assets/image/support/erma.png';
import wim from '@/assets/image/support/wim.png';

const title = ref('Supported by:');

const imageArray = ref([
    { src: crms, text: 'CRMS Indonesia', addres: 'Jalan Batununggal Asri No.18, Kel. Mengger, Kec. Bandung Kidul, Kota Bandung, Provinsi Jawa Barat, 40267', phone: 'P   : (+62-22) 8730 1035', mobile: 'M  : (+62) 811  22 333 075', mail: 'E   : secretariat@crmsindonesia.org' },
    { src: mks, text: 'LSP MKS', addres: 'Gedung Tifa, Lt. 3, Ruang 304 Jl. Kuningan Barat 1 No. 26 Jakarta 12710', phone: 'P   : (+62 –22) 8730 4033',  mobile: 'M  : (+62) 812 2054 0542', mail: 'E   : sekretariat@lspmks.id' },
    { src: grk, text: 'LSP GRK', addres: 'Gedung Tifa, Lt. 3, Ruang 304 Jl. Kuningan Barat 1 No. 26 Jakarta 12710', phone: 'P   :(+62) 21 – 2751 – 4461', mobile: 'M : (+62) 822-9565-1817', mail: 'E   : sekretariat@lspgrc.co.id' },
    { src: way, text: 'Way Academy', addres: 'Jl. Batununggal Asri No.18, Kel. Mengger, Kec. Bandung Kidul, Kota Bandung, Provinsi Jawa Barat, 40267', phone: 'M  : (+62) 858-8266-1827', mobile: 'E   : sekretariat@wayacademy.id', mail: '' },
    { src: erma, text: 'ERMA', addres: '16 Raffles Quay #33-03, Hong Leong Building, Singapore 048581', phone: 'Office 8-SCBD, Level 18-A Jl. Jend. Sudirman Kav 52-53  Jakarta Selatan, Indonesia', mobile: 'P: (+62) 878 2100 6401', mail: '' },
    { src: wim, text: 'Wimconsult', addres: 'Gedung Tifa, Lt. 3, Ruang 304 Jl. Kuningan Barat 1 No. 26 Jakarta 12710', phone: 'P   : (+62 –22) 22323899', mobile: 'M  : (+62) 813-9883-0433', mail: 'E   : info@myriskresolution.com' },
])
</script>
