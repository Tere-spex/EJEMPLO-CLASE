<template>
  <div>The count is: {{count}}</div>
  <button class="border px-4 py-2 rounded" @click="count++">+1</button>
  <button class="border px-4 py-2 rounded" @click="count--">-1</button>
</template>

<script>
export default {
    data() {
        return{
            count: 0,
        }
    }
};
</script>

<style>

</style>