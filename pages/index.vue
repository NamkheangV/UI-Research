<script setup lang="ts">
const tableData = {
  sections: [
    {
      isHeader: true,
      rows: [
        {
          cells: [
            {
              content: "ลำดับ",
              rowspan: 2,
              class: "rounded-tl-md",
            },
            {
              content: "ฐานความผิด",
              rowspan: 2,
              class: "text-start",
            },
            {
              content: "จำนวนผู้กระทำผิด (คน)",
              rowspan: 2,
            },
            {
              content: "จำนวนผู้ที่อาจจะกระทำความผิด(คน)",
              colspan: 3,
              class: "text-start border-1 border-blue-200 rounded-tr-md",
            },
          ],
        },
        {
          cells: [
            {
              content: "1 ปี",
              class: "p-2 border-x border-y border-blue-200",
            },
            {
              content: "3 ปี",
              class: "p-2 border-t border-blue-200",
            },
          ],
        },
      ],
    },
    {
      isHeader: false,
      rows: [
        {
          cells: [
            { content: "1" },
            {
              content:
                "การกระทำที่ก่อให้เกิดอันตรายที่อาจเฉียบพลันหรือเรื้อรังต่อสุขภาพ",
            },
            { content: "2" },
            { content: "6" },
            { content: "6" },
          ],
        },
        {
          cells: [
            { content: "2" },
            {
              content:
                "การกระทำที่ก่อให้เกิดอันตรายที่อาจเฉียบพลันหรือเรื้อรังต่อสุขภาพ",
            },
            { content: "2" },
            { content: "6" },
            { content: "6" },
          ],
        },
      ],
    },
  ],
};
</script>

<template>
  <div class="w-full h-screen flex flex-col space-y-6 p-6">
    <SubTHTable />

    <SubTDTable />

    <TestTable :sections="tableData.sections" />

    <Table />

    <div class="flex flex-col gap-y-4">
      <h2 class="text-lg font-bold">ข้อมูลความผิด</h2>

      <!-- <div class="flex flex-col gap-y-4">
        <div v-for="(item, index) in 2"> -->
      <Accordion
        :title="`ฐานความผิดที่อาจจะกระทำผิดตามมาตรฐานระหว่างประเทศว่าด้วยการจำแนกประเภทอาชญากรรมเพื่อประโยชน์ทางสถิติ (ICCS)`">
        <SubTHTable />
      </Accordion>

      <Accordion
        :title="`ฐานความผิดที่อาจจะกระทำผิดตามมาตรฐานระหว่างประเทศว่าด้วยการจำแนกประเภทอาชญากรรมเพื่อประโยชน์ทางสถิติ (ICCS)`">
        <SubTHTable />
      </Accordion>
      <!-- </div>
      </div> -->
    </div>
  </div>
</template>

<style scoped></style>
