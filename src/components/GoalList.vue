<template>
  <div>
  <h1>GOALSLIST</h1>
    <ul>
      <Goal v-for="goal in goals"
        :key="goal.id"
        :goal="goal"
        :onUpdate="handlePut"
      />
    </ul>
  </div>
</template>

<script>
import { putGoal } from '../services/api';

import Goal from './Goal';
export default {
  props: ['goals'],
  components: {
    Goal
  },
  methods: {
    handlePut(goal) {
      putGoal(goal);
    }
  }
};
</script>

<style>

</style>
