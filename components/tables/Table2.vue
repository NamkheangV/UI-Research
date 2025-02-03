<script setup lang="ts"></script>

<template>
  <table class="w-full">
    <thead class="border-b-2 border-blue-500">
      <tr class="bg-blue-100">
        <th class="p-2 text-start rounded-tl-md">จังหวัด</th>
        <th class="p-2 text-start">หน่วยงาน</th>
        <th class="p-2">กรมพินิจและคุ้มครองเด็กและเยาวชน</th>
        <th class="p-2">กรมคุมประพฤติ</th>
        <th class="p-2 rounded-tr-md">กรมราชทัณฑ์</th>
      </tr>
    </thead>

    <tbody v-for="(item, index) in 2">
      <tr class="">
        <td
          rowspan="4"
          class="p-2 text-start align-top border-b border-r">
          กรุงเทพมหานคร
        </td>
      </tr>

      <tr class="border-b">
        <td class="p-3">{{ "เรือนจำจังหวัดกระบี่" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
      </tr>

      <tr class="border-b">
        <td class="p-3">{{ "เรือนจำจังหวัดกระบี่" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
      </tr>

      <tr class="border-b">
        <td class="p-3">{{ "เรือนจำจังหวัดกระบี่" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
        <td class="p-3 text-center">{{ "89" }}</td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped></style>
