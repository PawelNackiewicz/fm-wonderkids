<template>
  <q-page class="row items-center justify-evenly">
    <player-list
      :players="players"
    ></player-list>
  </q-page>
</template>

<script lang="ts">
  import { Player } from 'src/model/models';
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
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '2',
          firstName: 'Jakby',
          lastName: 'Moder',
          age: 22,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '3',
          firstName: 'Kacper',
          lastName: 'Kozłowski',
          age: 16,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '4',
          firstName: 'Tymoteusz',
          lastName: 'Puchacz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '5',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '6',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '7',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '8',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '9',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        {
          id: '10',
          firstName: 'Bartosz',
          lastName: 'Ślisz',
          age: 21,
          club: 'Brighton',
          nation: 'Poland',
          position: 'MD',
          rating: 121,
          value: 1,
          wage: 1
        },
        ]);
      return { players };
    }
  });
</script>
