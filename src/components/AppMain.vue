<script>
import AppMainAbout from './AppMainAbout.vue';
import AppMainAeP from './AppMainAeP.vue';
import AppMainFeed from './AppMainFeed.vue';
import AppMainListCard from './AppMainListCard.vue';
import AppMainPM from './AppMainPM.vue';


  export default{
    data() {
        return {};
    },
    components: { AppMainListCard, AppMainAbout, AppMainAeP, AppMainPM, AppMainFeed }
}
</script>

<template>
  <main>
    <AppMainListCard />
    <AppMainAbout />
    <AppMainAeP />
    <AppMainPM />
    <AppMainFeed />
  </main>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;
</style>