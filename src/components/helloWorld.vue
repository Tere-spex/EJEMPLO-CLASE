<template>
  <div>
    <h1>Hello</h1>
    <input type="text" v-model="message" class="border" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: "",
    };
  },
};
</script>
