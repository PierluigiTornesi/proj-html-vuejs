<script>

  export default{
    data() {
        return {
            links:[
                "ALL","INSTITUTIONAL","SOCIAL","EVENTS","INNOVATION","ENVIRONMENT","TECHNOLOGY",
            ],
            projects:[
                {
                    imagePath:"project-1.jpg",
                    descImage:"Academic professional program in social media",
                },
                {
                    imagePath:"project-2.jpg",
                    descImage:"President's speech at the annual meeting",
                },
                {
                    imagePath:"project-3.jpg",
                    descImage:"International business trip in Shanghai",
                },
                {
                    imagePath:"project-4.jpg",
                    descImage:"Technology workshop with education theme",
                },
                {
                    imagePath:"project-5.jpg",
                    descImage:"Donation of clothes and food to the partner NGO",
                },
                {
                    imagePath:"project-6.jpg",
                    descImage:"Confraternization of the procurement team",
                },
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
                <span class="special">WE DO MORE FOR EVERYONE</span>
                <h3 class="title">Actions & <span class="back">Projects</span></h3>
            </div>
            <div>
                <ul>
                    <li v-for="link in links">
                        <a :class="link === 'ALL' ? 'back' : '' " href="">{{ link }}</a></li>
                </ul>
            </div>
            <div class="row">
                <div class="col-4" v-for="project in projects">
                    <a href="">
                        <img :src="(getImagePath(project.imagePath) )" alt="">
                    </a>
                    <h4>{{ project.descImage }}</h4>
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
        padding-bottom: 5rem;
    }

    ul{
        @include flex(row,center,center);
        list-style-type: none;
        gap: 4rem;
        margin-top: 1rem;

        a{
            text-decoration: none;
            color: inherit;
        }
    }

    .back{
        background-color: rgba($color: $BlueLagoon, $alpha: 0.6);
        padding: 0.3rem 0.5rem;
        border-radius: 5px;
    }

    .special{
        color: $FountainBlue;
    }

    .title{
        margin-top: 2rem;
        font-weight: bold;
        font-size: 3rem;
    }

    .col-4{
        position: relative;
        padding: 1rem;

        img{
            border-radius: 5px;
            filter: brightness(50%);
        }

        h4{
            width: 90%;
            position: absolute;
            top:70%;
            text-align: center;
            font-weight: bold;
        }
    }
</style>