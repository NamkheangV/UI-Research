<script setup lang="ts">
import { cn } from "@/libs/utils";

interface AccordionProps {
  title: string;
}

defineProps<AccordionProps>();

const openAccordion = ref(false);

const toggleAccordion = () => {
  openAccordion.value = !openAccordion.value;
};
</script>

<template>
  <div class="flex flex-col gap-y-5">
    <div
      :class="
        cn(
          'flex items-center gap-x-4 p-2 rounded-md transition-all duration-400 cursor-pointer',
          openAccordion ? 'bg-[#2E76C7]' : 'bg-[#F2F4F7]'
        )
      "
      @click="toggleAccordion">
      <div
        :class="
          cn(
            'ml-1 w-[16px] h-[16px] bg-[#2E76C7] rounded-full transition-all duration-400',
            openAccordion
              ? 'transform rotate-180 bg-white'
              : 'transform rotate-0 bg-[#2E76C7]'
          )
        "></div>

      <span
        :class="
          cn(
            'font-semibold transition-all duration-400 select-none',
            openAccordion ? 'text-white' : 'text-black'
          )
        ">
        {{ title }}
      </span>
    </div>

    <template
      v-if="openAccordion"
      class="grid transition-all duration-400 ease-in-out">
      <div class="flex flex-col">
        <!-- <SubTHTable /> -->
        <slot />
      </div>
    </template>
  </div>
</template>

<style scoped>
.th {
  padding: 20px;
}
</style>
