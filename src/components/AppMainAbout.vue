<script>
import AppMainAboutCard from "./AppMainAboutCard.vue";

  export default{
    data() {
        return {
            infoAbouts:[
                {
                    number: 0,
                    title:"Employees",
                    desc:"Lorem, ipsum dolor sit amet."
                },
                {
                    number: 0,
                    title:"Partners",
                    desc:"Lorem, ipsum dolor sit amet."
                },
                {
                    number: 0,
                    title:"Customers",
                    desc:"Lorem, ipsum dolor sit amet."
                }
            ]
        };
    },
    components: { AppMainAboutCard }
}
</script>

<template>
  <section >
    <div>
        <div class="container">
            <div class="row">
                <div class="col-5"></div>
                <div class="col-6">
                    <span class="fw-bolder">ABOUT THE NETWORK</span>
                    <h2 class="fw-bold mt-4 ">
                        <span class="special">The</span> Company
                    </h2>
                    <p class="mt-4">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum exercitationem dolores quidem, eligendi suscipit ipsa! Ea, iusto suscipit! Et consequuntur nam harum voluptatum. Architecto quam earum error enim, obcaecati dolorum.</p>
                    <div class="d-flex">
                        <AppMainAboutCard v-for="infoTaken in infoAbouts" :info = infoTaken />
                    </div>
                    <div class="d-flex gap-3 mt-4">
                        <a class="colored-button text-white" href="">GET IN TOUCH</a>
                        <a class="nocolor-button" href="">READ MORE</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div>
        <img src="../assets/img/about-5.jpg" alt="">
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section{
        @include flex(row,center,center);
        
        img{
            max-width: 100%;
        }
    }

.colored-button{
    background-color: $BlueLagoon;
    border-color: $BlueLagoon;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
}

.nocolor-button{
    border: 1px solid $BlueLagoon;
    color: $BlueLagoon;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
}

span{
    color: $BlueLagoon;
}

.special{
    background-color: rgba($color: $FountainBlue, $alpha: 0.2);
    padding: 0.5rem 1rem;
    border-radius: 5px;
}

h2{
    font-size: 3rem;
}

</style>