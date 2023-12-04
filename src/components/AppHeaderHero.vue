<script>

  export default{
    data(){
      return{
        
      }
    }
  }
</script>

<template>
    <section>
        <div class="hero-up container text-white">
            <div class=" mt-3">
                <button class="btn half-button">NEX 
                    <span class="text-white ">GEN</span> </button>
            </div>
            <div class="links mt-3">
            <ul>
                <li><a href="">HOME</a></li>
                <li><a href="">ABOUT</a></li>
                <li><a href="">PROJECTS</a></li>
                <li><a href="" class="special">PROCESS</a></li>
                <li><a href="">TESTIMONIALS</a></li>
                <li><a href=""><i class="fa-regular fa-user"></i></a></li>
                <li>
                    <button class="btn colored-button text-white">GET IN TOUCH</button>
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
            <button class="btn colored-button text-white">GET IN TOUCH</button>
            <button class="btn nocolor-button text-white">READ MORE</button>
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
}

.nocolor-button{
    border: 1px solid $FountainBlue;
}

.half-button{
    padding: 0.5rem 1.5rem;
    border-radius: 20px;
    color: $FountainBlue;
    background-color: rgba($color: $BlueLagoon, $alpha: 0.2);
}

</style>