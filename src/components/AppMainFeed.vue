<script>



  export default{
    data() {
        return {
            feedbacks:[
                {
                    imagePath:"logo-1.png",
                    desc1:"Dolor obcaecati sapiente blanditiis distinctio optio deleniti quam dolore culpa voluptate ad consectetur porro architecto nisi reiciendis impedit veniam maxime, numquam expedita.",
                    desc2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. ",
                },
                {
                    imagePath:"logo-2.png",
                    desc1:"Dolor obcaecati sapiente blanditiis distinctio optio deleniti quam dolore culpa voluptate ad consectetur porro architecto nisi reiciendis impedit veniam maxime, numquam expedita.",
                    desc2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. ",
                },
                {
                    imagePath:"logo-3.png",
                    desc1:"Dolor obcaecati sapiente blanditiis distinctio optio deleniti quam dolore culpa voluptate ad consectetur porro architecto nisi reiciendis impedit veniam maxime, numquam expedita.",
                    desc2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. ",
                }
            ]
        };
    },
    methods:{
        getImagePath(path){
            return new URL(`../assets/img/${path}`, import.meta.url).href;
        },
    }
    
}
</script>

<template>
  <section>
    <div class="container text-white">
        <div class="text-center p-3">
            <span class="special fw-bold">CUSTOMER TESTIMONIALS</span>
            <h3 class="title">
                Trusted <span class="back">Feedback</span> 
            </h3>
        </div>
        <div class="desc">
            <p>We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for the recognition.
            </p>
        </div>
    </div>
    <div class="container">
        <div class="row">
            <div class="col-3" v-for="feedback in feedbacks">
                <div class="logo">
                    <img :src="getImagePath(feedback.imagePath)" alt="">
                </div>
                <p>{{ feedback.desc1 }}</p>
                <p>{{ feedback.desc2 }}</p>
            </div>
        </div>
    </div>
</section>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section{
        background-color: $GrayNurse;
    }

    .special{
        color: $FountainBlue;
    }

    .desc{
        margin: 0 auto;
        width: 55%;
        text-align: center;
        padding-bottom: 2rem;
        color: $ShuttleGray;
    }

    .back{
        background-color: rgba($color:$Bermuda, $alpha: 0.4);
        padding: 0.3rem 0.5rem;
        border-radius: 5px;
        color: $BlueLagoon;
    }

    .title{
        margin-top: 2rem;
        font-weight: bold;
        font-size: 3rem;
        color: black;
    }

    .logo{
        width: 50%;
    }
    .row{
        @include flex(row,center,center);
        gap: 2rem;
        padding-bottom: 4rem;
    }
    .col-3{
        border-radius: 10px;
        padding: 2rem;
        background-color: $White;

        p{
            margin-top: 1rem;
            color: $ShuttleGray;
        }
    }
</style>