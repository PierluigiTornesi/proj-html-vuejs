<script>

  export default{
    props:{
        info: Object,
    }
  }
</script>

<template>
    <span class="circle">
        <i class="fa-solid" :class="info.classIcon" ></i>
    </span>
    <a href="">
     {{ info.text }}
    </a>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.circle{
        background-color: rgba($color: $BlueLagoon, $alpha: 0.4);
        margin-right: 1rem;
        height: 40px;
        width: 40px;
        border-radius: 50%;
        color: $BlueLagoon;
        aspect-ratio: 1;
        @include flex(row,center,center);
    }
a{
    text-decoration: none;
    color: $BlueLagoon;
}


</style>