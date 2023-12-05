<script>
import AppMainCard from './AppMainCard.vue';


  export default{
    data() {
        return {
            info:[
                {
                    iconClass:"fa-user-group",
                    titleCard:"Human Capital",
                    textCard:"Humanizing business: Harness the power of technology to improve the way people work.",
                },
                {
                    iconClass:"fa-chart-pie",
                    titleCard:"Core Business",
                    textCard:"It takes innovative approaches to transform, modernize, and run existing platforms.",
                },
                {
                    iconClass:"fa-chart-simple",
                    titleCard:"Performance",
                    textCard:"Achieving maximum impact and value from investments in finance and supply chain.",
                }
            ]
        };
    },
    components: { AppMainCard }
}
</script>

<template>
    <section>
        <div class="container">
            <AppMainCard v-for="infoTaken in info" :infoCard =infoTaken />
        </div>
    </section>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section{
        background-color: $GrayNurse;
    }

    .container{
        @include flex(row,space-between,center)
    }
</style>