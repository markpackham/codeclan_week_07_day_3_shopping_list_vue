<template>
<div>
  <h1>My Shopping List</h1>
  <ul>
  <shopping-list-item v-for="(item, index) in items" :key="index" :item="item"></shopping-list-item>
  </ul>
</div>
</template>

<script>
import ShoppingListItem from "./components/ShoppingListItem";

export default {
  name: "app",
  data() {
    return {
      items: [
        { name: "Milk", isPurchased: false },
        { name: "Cheese", isPurchased: true },
        { name: "Beans", isPurchased: false }
      ]
    };
  },
  components: {
    "shopping-list-item": ShoppingListItem
  }
};
</script>

<style>
</style>