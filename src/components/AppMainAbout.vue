<script>


  export default{
    data() {
        return {};
    },
}
</script>

<template>
  <section>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-4"></div>
                <div class="col-8">
                    <span class="">ABOUT THE NETWORK</span>
                    <h2 class="fw-bold">
                        <span class="special">The</span> Company
                    </h2>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum exercitationem dolores quidem, eligendi suscipit ipsa! Ea, iusto suscipit! Et consequuntur nam harum voluptatum. Architecto quam earum error enim, obcaecati dolorum.</p>
                    <div class="d-flex">
                        <ul>
                            <li><span>0</span></li>
                            <li><h5>Employess</h5></li>
                            <li>Lorem, ipsum dolor sit amet.</li>
                        </ul>
                        <ul>
                            <li><span>0</span></li>
                            <li><h5>Employess</h5></li>
                            <li>Lorem, ipsum dolor sit amet.</li>
                        </ul>
                        <ul>
                            <li><span>0</span></li>
                            <li><h5>Employess</h5></li>
                            <li>Lorem, ipsum dolor sit amet.</li>
                        </ul>
                    </div>
                    <div class="d-flex gap-3">
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

span{
    color: $FountainBlue;
}

.special{
    background-color: rgba($color: $FountainBlue, $alpha: 0.3);
}
</style>