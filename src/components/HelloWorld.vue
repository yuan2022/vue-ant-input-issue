<template>
  <ul class="hello">
    <li><a-input v-model:value.trim="filed1"></a-input></li>
    <li><input v-model.trim="filed2" /></li>
  </ul>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from "vue";

export default defineComponent({
  setup() {
    const state = reactive({
      filed1: "",
      filed2: "",
    });
    return {
      ...toRefs(state),
    };
  },
});
</script>
