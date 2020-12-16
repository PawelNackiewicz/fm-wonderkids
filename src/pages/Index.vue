<template>
  <q-page class="row items-center justify-evenly">
    <player-list
      :players="players"
    ></player-list>
  </q-page>
</template>

<script lang="ts">
  import { Player } from 'components/models';
  import { defineComponent, ref } from '@vue/composition-api';
  import PlayerList from 'components/playerList/PlayerList.vue';

  export default defineComponent({
    name: 'PageIndex',
    components: { PlayerList },
    setup() {
      const players = ref<Player[]>([
        {
          id: '1',
          firstName: 'Michal',
          lastName: 'Karbownik',
          age: 21
        },
        {
          id: '2',
          firstName: 'Jakby',
          lastName: 'Moder',
          age: 22
        },
        {
          id: '3',
          firstName: 'Kacper',
          lastName: 'Kozłowski',
          age: 16
        },
        {
          id: '4',
          firstName: 'Tymoteusz',
          lastName: 'Puchacz',
          age: 21
        },
        {
          id: '5',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21
        }]);
      return { players };
    }
  });
</script>
