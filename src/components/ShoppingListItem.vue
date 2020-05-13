<template>
  <li :class="purchasedClass">{{item.name}}</li>
</template>

<script>
export default {
  name: "shopping-list-item",
  props: ["item"],
  computed: {
    purchasedClass: function(item) {
        // if (this.item.isPurchased) {
        //     return "purchased"
        // } else {
        //     return "not-purchased"
        // }
        return this.item.isPurchased ? "purchased" : "not-purchased";
    }
  }
};
</script>

<style>
.not-purchased {
  background-color: cyan;
}
.purchased {
  background-color: burlywood;
  text-decoration: line-through;
}
</style>