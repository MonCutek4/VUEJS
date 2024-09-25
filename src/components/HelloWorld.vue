<template>
  <div class="hello">
    <div>
      <label> Goal</label><br>
      <input type="text" id="goal" v-model="goal2"/><br>
      <button @click="showGoal">Add Goal</button>
    </div>
    <ul>
    <li v-for="(goal) in goal :key"></li>
      <li>
      {{ goal.desc }}
      <button>Done</button>
      <button>Delete</button>
      </li>
    </ul>
  </div>
  
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  setup() {
    const goal = ref('qua mon +');
    const goal2 = ref('');

    const showGoal = () => {
      // Xử lý khi nút "Show Goal" được click
    };

    return {
      goal,
      goal2,
      showGoal
    };
  }
}
</script>

