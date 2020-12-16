<template>
  <div>
    <h2>
      Player list
    </h2>
    <q-list bordered>
      <PlayerItem
        v-for="(player) in players"
        :key="player.id"
        :player="player"
      />
    </q-list>
  </div>
</template>

<script lang="ts">
  import { PropType } from '@vue/composition-api';
  import { Player } from 'components/models';
  import PlayerItem from 'components/playerList/PlayerItem.vue';

  export default {
    name: 'PlayerList',
    components: { PlayerItem },
    props: {
      players: {
        type: (Array as unknown) as PropType<Player[]>,
        required: true
      }
    }
  };
</script>

<style scoped>

</style>
