<template>
  <div><h1>Bank</h1></div>
  <div>
    <div>Income: {{income}}€</div>
    <div>Outcome: {{outcome}}€</div>
    <div>Balance: {{balance}}€</div>
    <input type="text" class="border" v-model="name" placeholder="name">
    <input type="number" class="flex border" v-model="amount" placeholder="amount">
    <button @click="addItem" class="bg-rose-200 py-2 px-4 rounded-md">Add</button>
     <ul>
      <li v-for="(item, i) in items" :key="i">
        {{ item.name }} : {{ item.amount }}€
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      amount: 0,
      items: [],
    };
  },
  computed: {
    income() {
      return this.items
        .filter((item) => item.amount > 0)
        .reduce((acc, item) => acc + item.amount, 0);
    },
    outcome() {
      return this.items
        .filter((item) => item.amount < 0)
        .reduce((acc, item) => acc + item.amount, 0);
    },
    balance() {
      return this.income + this.outcome;
    },
  },
  methods: {
    addItem() {
      this.items.push({
        name: this.name,
        amount: this.amount,
      });
    },
  },
};
</script>
