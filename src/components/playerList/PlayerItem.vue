<template>
  <q-item clickable>
    <q-item-section avatar>
      <q-avatar>
        <img src="https://cdn.quasar.dev/img/boy-avatar.png" :alt="player.firstName">
      </q-avatar>
    </q-item-section>
    <q-item-section>
      {{ player.firstName }} {{ player.lastName }}
    </q-item-section>
    <q-item-section>
      {{ player.age }}
    </q-item-section>
  </q-item>
</template>

<script lang="ts">
  import { PropType } from '@vue/composition-api';
  import { Player } from 'components/models';

  export default {
    name: 'PlayerItem',
    props: {
      player: {
        type: (Object as unknown) as PropType<Player>,
        required: true
      }
    }
  };
</script>

<style scoped>

</style>
