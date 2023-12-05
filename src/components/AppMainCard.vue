<script>

  export default{
    props:{
        infoCard: Object,
    }
  }
</script>

<template>
    <div class="card" style="width: 20rem;">
         <div class="card-body">
            <p class="circle">
                <span class="special">
                    <i class="fa-solid" :class="infoCard.iconClass"></i>
                </span>
            </p>
            <h5 class="card-title">{{infoCard.titleCard}}</h5>
            <p class="card-subtitle mb-2 text-muted">{{ infoCard.textCard }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;



    .card{
        margin: 6rem 0;
        padding: 1rem 1rem;
    }
    .circle{
        background-color: rgba($color: $FountainBlue, $alpha: 0.3);
        height: 60px;
        width: 60px;
        border-radius: 50%;
        aspect-ratio: 1;
        @include flex(row,center,center);
        
        .special{
            color: $BlueLagoon;
            font-size: 1.5rem;
        }
    }
</style>