<template>
  <div>
    <q-img src="src/assets/madeira-verde-background.png" style="width: 1620px">
      <div class="absolute-bottom-right text-subtitle2">
        AGENCIAMENTO E TRADING DE MADEIRA
      </div>
    </q-img>
  </div>
  <div>
    <img src="src/assets/fibra-logo.png" />
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';
import { Todo, Meta } from '../models';

interface Props {
  title: string;
  todos?: Todo[];
  meta: Meta;
  active: boolean;
}
// const props = withDefaults(defineProps<Props>(), {
//   todos: () => [],
// });

// const clickCount = ref(0);
// function increment() {
//   clickCount.value += 1;
//   return clickCount.value;
// }

// const todoCount = computed(() => props.todos.length);
</script>
