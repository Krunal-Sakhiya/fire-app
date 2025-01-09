<template>
  <div>
    <div>
      <transition name="home" mode="out-in"></transition>
      <LargeCardSections
        v-for="cardSection of largeCardInfo.slice(0, 1)"
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
  transition: {
    name: "home",
    mode: "out-in",
  },
};
</script>

<style scoped>
.home-enter-active,
.home-leave-active {
  transition: opacity 0.5s;
}
.home-enter,
.home-leave-active {
  opacity: 0;
}
</style>
