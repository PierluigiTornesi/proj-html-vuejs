<script>
import AppFooterForm from './AppFooterForm.vue';


  export default{
    data() {
        return {};
    },
    components: { AppFooterForm }
}
</script>

<template>
  <AppFooterForm />
  <section>
    <div class="container text-white">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <p>@ 2020 NEXGEN is Proudly Powered by <span>Codinac</span></p>
  </div>
  </section>

</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section{
      background-color: $Shark;
      
      .container{
        @include flex(row,space-between,center);
        

        span{
          color: $FountainBlue;
        }
      }
    }
</style>