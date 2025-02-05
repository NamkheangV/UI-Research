<script setup lang="ts">
interface TableCell {
  content: string;
  colspan?: number;
  rowspan?: number;
  class?: string;
}

interface TableRow {
  cells: TableCell[];
}

interface TableSection {
  rows: TableRow[];
  isHeader?: boolean;
}

interface Props {
  sections: TableSection[];
  tableClass?: string;
}

const props = withDefaults(defineProps<Props>(), {
  tableClass: "w-full",
});
</script>

<template>
  <table :class="tableClass">
    <template
      v-for="(section, sectionIndex) in sections"
      :key="`section-${sectionIndex}`">
      <thead
        v-if="section.isHeader"
        class="border-b-2 border-blue-500">
        <tr
          v-for="(row, rowIndex) in section.rows"
          :key="`header-row-${rowIndex}`"
          class="border-blue-600 bg-blue-100">
          <th
            v-for="(cell, cellIndex) in row.cells"
            :key="`header-cell-${cellIndex}`"
            :colspan="cell.colspan"
            :rowspan="cell.rowspan"
            :class="[
              'p-2',
              cell.class,
              {
                'rounded-tl-md':
                  sectionIndex === 0 && rowIndex === 0 && cellIndex === 0,
                'rounded-tr-md':
                  sectionIndex === 0 &&
                  rowIndex === 0 &&
                  cellIndex === row.cells.length - 1,
              },
            ]">
            {{ cell.content }}
          </th>
        </tr>
      </thead>

      <tbody v-else>
        <tr
          v-for="(row, rowIndex) in section.rows"
          :key="`body-row-${rowIndex}`"
          class="">
          <td
            v-for="(cell, cellIndex) in row.cells"
            :key="`body-cell-${cellIndex}`"
            :colspan="cell.colspan"
            :rowspan="cell.rowspan"
            :class="[
              'p-2',
              cell.class,
              {
                'border-x border-y border-blue-200': true,
                'text-center': !cell.class?.includes('text-'),
              },
            ]">
            {{ cell.content }}
          </td>
        </tr>
      </tbody>
    </template>
  </table>
</template>
