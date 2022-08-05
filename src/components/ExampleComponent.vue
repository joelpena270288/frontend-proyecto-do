<template>
  <div>

    <h6>Primer texto</h6>
    <h6>Segundo texto</h6>
    <p>Rercer Texto</p>
  </div>
</template>

<script lang="ts">
import {
  defineComponent,
  PropType,
} from 'vue';
import { Todo, Meta } from './models';





export default defineComponent({
  name: 'InicioComponent',
  props: {
    title: {
      type: String,
      required: true
    },
    todos: {
      type: Array as PropType<Todo[]>,
      default: () => []
    },
    meta: {
      type: Object as PropType<Meta>,
      required: true
    },
    active: {
      type: Boolean
    }
  },

});
</script>
