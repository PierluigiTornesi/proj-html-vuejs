<script>
import AppMainAbout from './AppMainAbout.vue';
import AppMainListCard from './AppMainListCard.vue';


  export default{
    data() {
        return {};
    },
    components: { AppMainListCard, AppMainAbout }
}
</script>

<template>
  <main>
    <AppMainListCard />
    <AppMainAbout />
  </main>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;
</style>