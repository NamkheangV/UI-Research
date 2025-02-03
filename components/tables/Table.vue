<script setup lang="ts">
// if it's a first & last column of the table then add rounded corners
// first column of the table then add rounded left corner
// last column of the table then add rounded right corner

</script>

<template>
  <table class="w-full">
    <thead class="border-b-2 border-blue-500">
      <tr class="border-blue-600 bg-blue-100">
        <th
          rowspan="2"
          class="p-2 rounded-tl-md">
          ลำดับ
        </th>

        <th rowspan="2" class="p-2 text-start">ฐานความผิด</th>
        <th rowspan="2">จำนวนผู้ที่กระทำผิด (คน)</th>

        <th
          colspan="3"
          class="p-2 text-start border-l border-blue-200 rounded-tr-md">
          จำนวนผู้ที่อาจจะกระทำความผิด(คน)
        </th>
      </tr>

      <tr class="bg-blue-100">
        <th class="p-2 border-x border-y border-blue-200">1 ปี</th>
        <th class="p-2 border-t border-blue-200">3 ปี</th>
      </tr>
    </thead>

    <tbody>
      <tr v-for="(item, index) in 6">
        <td class="p-2">{{ index + 1 }}</td>
        <td class="p-2">
          {{
            "การกระทำที่ก่อให้เกิดภัยภัยอันตรายหรือเจตนาให้เกิดอันตรายต่อผู้อื่น"
          }}
        </td>
        <td class="text-center">{{ "2" }}</td>
        <td class="text-center">{{ "6" }}</td>
        <td class="text-center">{{ "6" }}</td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped></style>
