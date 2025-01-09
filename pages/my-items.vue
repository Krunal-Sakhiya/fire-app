<template>
  <div class="container">
    <MyItems v-for="item in myItems" :key="item.id" :item="item" />
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  layout: "no-nav",
  computed: {
    ...mapState(["myItems"]),
  },
};
</script>

<style scoped>
.container {
  padding: 5rem 0;
}
</style>
