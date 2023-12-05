<script>


  export default{
    data() {
        return {
            process:[
                {
                    number:"01",
                    title: "Collection of information",
                    desc: "Lorem ipsum dolor sit amet consectetur.",
                },
                {
                    number:"02",
                    title: "Strategic planning",
                    desc: "Lorem ipsum dolor sit amet consectetur.",
                },
                {
                    number:"03",
                    title: "Assignment of responsibilities",
                    desc: "Lorem ipsum dolor sit amet consectetur.",
                },
                {
                    number:"04",
                    title: "Formatting process",
                    desc: "Lorem ipsum dolor sit amet consectetur.",
                },
                {
                    number:"05",
                    title: "Continuity formalization",
                    desc: "Lorem ipsum dolor sit amet consectetur.",
                }
            ]
        };
    },
    
}
</script>

<template>
<section>
    <div class="container text-white">
        <div class="text-center p-3">
            <span class="special fw-bold">HOW IT WORKS IN PRACTICE</span>
            <h3 class="title">
                <span class="back">Process</span> Management
            </h3>
        </div>
        <div class="desc">
            <p class="text-black">We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planned.
            </p>
        </div>
    </div>
    <hr>
    <div class="moved">
        <ul>
            <li v-for="proces in process">
                <p class="circle">
                    <span class="special">{{ proces.number }}</span>
                </p>
                <h3>{{proces.title}}</h3>
                <p>{{proces.desc}}</p>
            </li>
        </ul>
    </div>
</section>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section{
        position: relative;
        height: 500px;
    }

    .container{
        margin-top: 4rem;
    }

    .desc{
        margin: 0 auto;
        width: 55%;
        text-align: center;
        padding-bottom: 2rem;
    }

    .title{
        margin-top: 2rem;
        font-weight: bold;
        font-size: 3rem;
        color: black;
    }

    .special{
        color: $FountainBlue;
    }

    .back{
        background-color: rgba($color:$Bermuda, $alpha: 0.4);
        padding: 0.3rem 0.5rem;
        border-radius: 5px;
        color: $BlueLagoon;
    }

    .circle{
        background-color: rgba($color: $Bermuda, $alpha: 0.4);
        height: 40px;
        width: 40px;
        border-radius: 50%;
        aspect-ratio: 1;
        @include flex(row,center,center);
        
        .special{
            color: $BlueLagoon;
            font-size: 1.5rem;
            font-weight: bold;
        }
    }

ul{
    @include flex(row,center,center);
    list-style: none;
    gap: 1rem;

    li{
        @include flex(column,center,center); 

        p{
            margin-top: 1rem;
            text-align: center;
            width: 70%;
        }
    }

}
hr{
    height: 10px;
    color:$Bermuda;
    background-color: $Bermuda;
    bottom: 0;
    left: 0;
}

.moved{
    width: 100%;
    position: absolute;
    margin: 0 auto;
    top: 47%;
}
</style>