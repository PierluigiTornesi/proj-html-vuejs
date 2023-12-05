<script>

  export default{
    data() {
        return {};
    },
    
}
</script>

<template>
    <section>
        <div class="container text-white">
            <div class="text-center">
                <span class="special">WE DO MORE FOR EVERYONE</span>
                <h3>Actions & <span class="back">Projects</span></h3>
            </div>
            <div>
                <ul>
                    <li><a class="back" href="">ALL</a></li>
                    <li><a href="">INSTITUTIONAL</a></li>
                    <li><a href="">SOCIAL</a></li>
                    <li><a href="">EVENTS</a></li>
                    <li><a href="">INNOVATION</a></li>
                    <li><a href="">ENVIRONMENT</a></li>
                    <li><a href="">TECHNOLOGY</a></li>
                </ul>
            </div>
            <div class="row">
                <div class="col-4">
                    <img src="../assets/img/project-1.jpg" alt="">
                    <h4>Academic professional program in social media</h4>
                </div>
                <div class="col-4">
                    <img src="../assets/img/project-2.jpg" alt="">
                    <h4>President's speech at the annual meeting</h4>
                </div>
                <div class="col-4">
                    <img src="../assets/img/project-3.jpg" alt="">
                    <h4>International business trip in Shanghai</h4>
                </div>
                <div class="col-4">
                    <img src="../assets/img/project-4.jpg" alt="">
                    <h4>Technology workshop with education theme</h4>
                </div>
                <div class="col-4">
                    <img src="../assets/img/project-5.jpg" alt="">
                    <h4>Donation of clothes and food to the partner NGO</h4>
                </div>
                <div class="col-4">
                    <img src="../assets/img/project-6.jpg" alt="">
                    <h4>Confraternization of the procurement team</h4>
                </div>
            </div>
        </div>
    </section>  
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section{
        background-color: $Woodsmoke;
        width: 100%;
    }

    ul{
        @include flex(row,center,center);
        list-style-type: none;
        gap: 2rem;

        a{
            text-decoration: none;
            color: inherit;
        }
    }

    .back{
        background-color: $EbonyClay;
        padding: 0.3rem 0.5rem;
        border-radius: 5px;
    }

    .special{
        color: $FountainBlue;
    }
</style>