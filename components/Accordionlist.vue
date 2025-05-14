<template>
    <div class="w-full mx-auto space-y-4">
        <div v-for="(item, index) in items" :key="index" class="text-black rounded-xl overflow-hidden">
            <button @click="toggle(index)"
                class="w-full text-left px-6 py-4 bg-gray-100 hover:bg-gray-200 flex justify-between items-center">
                <span class="font-extrabold text-[25px]">{{ item.title }}</span>
                <svg class="w-5 h-5 transition-transform duration-300"
                    :class="{ 'rotate-180': openIndexes.includes(index) }" fill="none" stroke="currentColor"
                    viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
            </button>

            <div v-show="openIndexes.includes(index)" class="px-6 py-4 bg-white border-t border-gray-200 space-y-2">
                <div v-for="(paragraph, i) in item.content" :key="i" class="text-black font-bold">
                    <h1 class=" text-[20px] border-b border-gray-400 py-5 whitespace-break-spaces"> 
                        {{ paragraph }}
                    </h1>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
    items: {
        type: Array,
        required: true
    }
})

const openIndexes = ref([])

const toggle = (index) => {
    if (openIndexes.value.includes(index)) {
        openIndexes.value = openIndexes.value.filter(i => i !== index)
    } else {
        openIndexes.value.push(index)
    }
}
</script>