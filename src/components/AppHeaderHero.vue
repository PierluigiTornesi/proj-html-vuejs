<script>
import AppHeaderHeroLink from './AppHeaderHeroLink.vue';


  export default{
    data() {
        return {
            links: [
                "HOME",
                "ABOUT",
                "PROJECTS",
                "PROCESS",
                "TESTIMONIALS"
            ]
        };
    },
    components: { AppHeaderHeroLink }
}
</script>

<template>
    <section>
        <div class="hero-up container text-white">
            <div class=" mt-3">
                <a class="text-white half-button" href="">
                    <span >N E X</span> G E N
                </a>
            </div>
            <div class="links mt-3">
            <ul>
                <li v-for="link in links">
                    <AppHeaderHeroLink :linkHero = link />
                </li>
                <li><a href=""><i class="fa-regular fa-user"></i></a></li>
                <li>
                    <a class=" colored-button text-white" href="">GET IN TOUCH</a>
                </li>
            </ul>
        </div>
    </div>
    <div class="container hero-down">
        <div>
            <span class="special">HUMAN REROURCES</span>
            <h2 class="title text-white">Get More</h2>
            <h2 class="title text-white">
                <span>Productivity</span>
            </h2>
        </div>
        <div>
            <p>Planning,recruitment and selection process and performance evaluation of employess.</p>
        </div>
        <div class="d-flex gap-3">
            <a class="colored-button text-white" href="">GET IN TOUCH</a>
            <a class="nocolor-button text-white" href="">READ MORE</a>
        </div>
    </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

section{
    height: 860px;
}
.hero-up{
    @include flex(row,space-between,none)
}

.hero-down{
    height: 60%;
    margin-top: 5rem;
    @include flex(column,space-evenly,left);
}

ul{
    @include flex(row,space-between,center);
    list-style: none;
    gap: 3rem;

    a{
        text-decoration: none;
        color: inherit;
    }
}

.special{
    color:$BlueLagoon ;
}

.title{
    font-size: 5rem;
    font-weight: bolder;
}

p{
    color: $SilverSand;
    width: 40%;
    font-size: 1.5rem;
}

.colored-button{
    background-color: $FountainBlue;
    border-color: $FountainBlue;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
}

.nocolor-button{
    border: 1px solid $FountainBlue;
    color: $FountainBlue;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
}

.half-button{
    border-radius: 20px;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: bold;
    
    span{
        color: $FountainBlue;
        background-color: rgba($color: $BlueLagoon, $alpha: 0.2);
        padding-left: 1.5rem;
        padding-top: 0.6rem;
        padding-bottom: 0.6rem;
        border-top-left-radius: 20px;
        border-bottom-left-radius: 20px;
    }
}

</style>