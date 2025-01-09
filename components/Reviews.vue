<template>
  <div v-if="!$fetchState.pending">
    <h3>Customer Reviews</h3>
    <ReviewCard
      v-for="review in reviews.results"
      :key="review.login.uuid"
      :review="review"
    />
  </div>
  <div v-else>
    <h3 class="loading">Loading data</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviews: [],
    };
  },
  async fetch() {
    this.reviews = await fetch("https://randomuser.me/api/?results=5").then(
      (res) => res.json()
    );
  },
};
</script>

<style scoped></style>
