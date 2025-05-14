<template>
  <div>
    <div class=" py-10  2xl:px-60  flex-container bg-white bg-auto lg:bg-cover bg-no-repeat">
      <div class="py-8">
        <Accordionlist :items="accordionItems" />
      </div>
      <!-- <div class=" bg-white text-black">
                <UAccordion type="multiple" :items="items" />
            </div> -->
    </div>

    <div class=""></div>
  </div>
</template>

<script setup lang="ts">

// import type { AccordionItem } from '@nuxt/ui'
import Accordionlist from '../Accordionlist.vue';

// const items = ref<AccordionItem[]>([
//   {
//     label: 'Icons',
//     icon: 'i-lucide-smile',
//     content: 'You have nothing to do, @nuxt/icon will handle it automatically.',
//   },
//   {
//     label: 'Icons',
//     icon: 'i-lucide-smile',
//     content: 'You have nothing to do, @nuxt/icon will handle it automatically.',
//   },
//   {
//     label: 'Icons',
//     icon: 'i-lucide-smile',
//     content: 'You have nothing to do, @nuxt/icon will handle it automatically.',
//   },
//   // {
//   //   label: 'Colors',
//   //   icon: 'i-lucide-swatch-book',
//   //   content: 'Choose a primary and a neutral color from your Tailwind CSS theme.'
//   // },
//   // {
//   //   label: 'Components',
//   //   icon: 'i-lucide-box',
//   //   content: 'You can customize components by using the `class` / `ui` props or in your app.config.ts.'
//   // }
// ])

const accordionItems = [
  {
    title: 'August 21 (Masterclass)',
    content: [
      '08.15-09.00              Registration',
      '09.00-09.15              Welcoming Notes',
      '09.15-10.15              Masterclass Session 1 - GRC Foundations for ESG and SDG Integration',
      '10.15-10.30              Coffee Break',
      '10.30-12.00              Masterclass Session 2 - Leveraging AI for GRC Excellence',
      '12.00-13.15              Lunch Break',
      '13.15-15.00              Practice Sharing, Q&A',
      '15.00-15.15              Closing Season'
    ]
  },
  {
    title: 'August 22 (Seminar)',
    content: [
      '07.45-08.15              Registration',
      '08.15-08.30              Welcoming Notes',
      '08.45-09.15              Keynote Speech 1, Resilience and Sustainability: GRC as a Strategic Enabler',
      '09.15-10.00              Lifetime Achievement Award Session',
      '10.00-10.15              Coffee Break',
      '10.15-11.30              Panel Discussion 1, Sustainability in Action: How GRC, ESG, and AI Support the SDGs',
      '11.30-13.15              Lunch Break',
      '13.15-13.55              Entertainment Performance and Inauguration',
      '13.55-14.25              Keynote Speakers 2: Achieving the SDGs through Governance and Innovation',
      '14.25-15.25              Panel Discussion 2, Collaborative Leadership for the Post-Digital Era: GRC, ESG, and Beyond',
      '15.25-15.30              Closing',
    ]
  }
]

</script>

<style lang="scss" scoped></style>