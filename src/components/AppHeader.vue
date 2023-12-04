<script>
import AppHeaderHero from './AppHeaderHero.vue';
import AppHeaderInfo from './AppHeaderInfo.vue';


  export default{
    data() {
        return {};
    },
    components: { AppHeaderInfo, AppHeaderHero }
}
</script>

<template>
  <section class="info">
    <AppHeaderInfo />
  </section>
  <section class="hero">
    <AppHeaderHero />
  </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.info{
  background-color: $EbonyClay;
}

.hero{
  background-image: url(../assets/img/bg-4.jpg);
}

</style>