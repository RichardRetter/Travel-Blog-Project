<template>
  <div class="header">
    <TheHeader />
  </div>
  <div class="cities">
    <Cities />
  </div>
</template>

<script>
import Cities from '../components/Cities.vue';
import TheHeader from '../components/TheHeader.vue';
export default {
  components: {
    TheHeader,
    Cities
  }
};
</script>

<style scoped>
.header {
  height: 80px;
  width: 100vw;
  display: flex;
  margin: 0 auto;
  border-bottom: 3px solid white;
  border-top: 3px solid white;
}
.cities {
  margin: auto;
}
</style>
