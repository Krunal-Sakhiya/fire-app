<template>
  <div class="container">
    <h4 class="header">{{ cardSectionInfo.title }}</h4>
    <div class="card-container">
      <SmallCard
        v-for="card of cardSectionInfo.cards"
        :key="card.image"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ["cardSectionInfo"],
};
</script>

<style scoped>
.container {
  padding: 2rem 0;
}

.header {
  font-weight: 700;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}

.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
