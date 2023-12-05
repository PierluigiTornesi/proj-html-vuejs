<script>
import AppMainAbout from './AppMainAbout.vue';
import AppMainAeP from './AppMainAeP.vue';
import AppMainListCard from './AppMainListCard.vue';


  export default{
    data() {
        return {};
    },
    components: { AppMainListCard, AppMainAbout, AppMainAeP }
}
</script>

<template>
  <main>
    <AppMainListCard />
    <AppMainAbout />
    <AppMainAeP />
  </main>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;
</style>