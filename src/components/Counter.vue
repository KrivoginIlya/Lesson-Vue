<template>
  <button @click="onClick">Clicked {{ counter }}</button>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    onClick() {
      this.counter++;
    },
  },
};
</script>
