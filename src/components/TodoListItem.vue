<template>
  <li>
    {{ todo.text }} <button @click="$emit('remove', todo.id);">X</button>
    <div v-html="1">aaba</div>
  </li>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true
    }
  }
};
</script>
