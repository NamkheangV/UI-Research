<script setup lang="ts">
interface TableProps {
  colspan?: number;
  rowspan?: number;

  class?: string;
}
</script>

<template>
  <table>
    <thead>
      <tr class="border-b border-gray-300 bg-blue-100">
        <th
          rowspan="2"
          class="">
          Object
        </th>
        <th
          rowspan="2"
          class="">
          Openings
        </th>
        <th
          colspan="3"
          class="border-l border-gray-300">
          Internal Dimensions
        </th>
        <th
          colspan="3"
          class="">
          Weight
        </th>
        <th class="">Volume</th>
      </tr>

      <tr class="bg-blue-100">
        <th class="border-l border-gray-300">sub header</th>
        <th class="border-l border-gray-300">sub header</th>
        <th class="border-l border-gray-300">sub header</th>
        <th class="border-l border-gray-300">sub header</th>
        <th class="border-l border-gray-300">sub header</th>
        <th class="border-l border-gray-300">sub header</th>
        <th class="border-l border-gray-300">sub header</th>
      </tr>
    </thead>
  </table>
</template>

<style scoped></style>
