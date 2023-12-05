<script>

  export default{
    props:{
        linkHero: String,
    }
  }
</script>

<template>
    <a :class="linkHero === 'PROCESS' ? 'special' : '' " href="">{{linkHero}}</a>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.special{
    color:$BlueLagoon ;
}

</style>