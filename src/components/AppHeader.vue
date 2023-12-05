<script>
import AppHeaderHero from './AppHeaderHero.vue';
import AppHeaderInfo from './AppHeaderInfo.vue';


  export default{
    data() {
        return {
          infos:[
            {
              classIcon:"fa-solid fa-phone",
              text:"+1 (305) 1234-5678",
            },
            {
              classIcon:"fa-solid fa-envelope",
              text:"hello@example.com",
            },
            {
              classIcon:"fa-brands fa-facebook-f",
              text:"",
            },
            {
              classIcon:"fa-brands fa-twitter",
              text:"",
            },
            {
              classIcon:"fa-brands fa-linkedin-in",
              text:"",
            }
          ],
          info:{
            dayStart:"Mon",
            dayOff:"Sat",
            hourStart:"9:00",
            hourOff:"18:00"
          }
        };
    },
    components: { AppHeaderInfo, AppHeaderHero }
}
</script>

<template>
  <section class="info">
    <AppHeaderInfo :links = infos  :info = info />
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