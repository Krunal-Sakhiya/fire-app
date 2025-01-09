<template>
  <div>
    <div>
      <Hero />
      <LargeCardSections
        v-for="cardSection of largeCardInfo"
        :key="cardSection.id"
        :cardSectionInfo="cardSection"
      />
      <SmallCardSection
        v-for="cardSection of smallCardInfo"
        :key="cardSection.id"
        :cardSectionInfo="cardSection"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    };
  },
};
</script>

<style></style>
