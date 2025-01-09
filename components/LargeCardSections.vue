<template>
  <div class="container">
    <h4 class="header">
      {{ cardSectionInfo.title }}
    </h4>
    <p class="snippet">
      {{ cardSectionInfo.snippet }}
    </p>
    <div class="cards-container">
      <LargeCard
        v-for="card in cardSectionInfo.cards"
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
  margin-top: 2rem;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
  /* margin-top: 200px auto; */
}
.snippet {
  color: grey;
  margin-bottom: 1.5rem;
}
.cards-container {
  display: flex;
  justify-content: space-between;
}
</style>
