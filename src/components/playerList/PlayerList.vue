<template>
  <div>
    <h2>
      Player list
    </h2>
    <q-option-group
      v-model="separator"
      inline
      class="q-mb-md"
    />
    <q-table
      :data="players"
      row-key="name"
      :columns="columns"
      :pagination="initialPagination"
    >
      <template v-slot:header-cell-firstName="props">
        <q-th :props="props">
          <q-icon name="face" size="1.5em" />
          {{ props.col.label }}
        </q-th>
      </template>
      <template v-slot:header-cell-lastName="props">
        <q-th :props="props">
          <q-icon name="face" size="1.5em" />
          {{ props.col.label }}
        </q-th>
      </template>
    </q-table>
  </div>
</template>

<script lang="ts">
  import { PropType } from '@vue/composition-api';
  import { Player } from 'components/models';

  export default {
    name: 'PlayerList',
    props: {
      players: {
        type: (Array as unknown) as PropType<Player[]>,
        required: true
      }
    },
    data() {
      return {
        initialPagination: {
          rowsPerPage: 30
        },
        columns: [
          {
            name: 'firstName',
            required: true,
            label: 'First name',
            align: 'left',
            sortable: true,
            field: row => row.firstName,
            classes: 'bg-grey-2 ellipsis',
            headerClasses: 'bg-primary text-white'
          },
          {
            name: 'lastName',
            align: 'center',
            label: 'Last name',
            sortable: true,
            field: row => row.lastName,
            classes: 'bg-grey-2 ellipsis',
            headerClasses: 'bg-primary text-white'
          },
          {
            name: 'rating',
            align: 'center',
            label: 'Rating',
            sortable: true,
            field: row => row.rating,
            classes: 'bg-grey-2 ellipsis',
            headerClasses: 'bg-secondary text-white'
          },
        ],
      }
    }
  };
</script>

<style scoped>

</style>
