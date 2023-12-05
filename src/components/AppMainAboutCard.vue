<script>

  export default{
    props:{
        info: Object,
    }
  }
</script>

<template>
    <ul>
        <li><span class="fw-bold">{{ info.number }}</span></li>
        <li><h5 class="fw-bold">{{ info.title }}</h5></li>
        <li><p>{{ info.desc }}</p></li>
    </ul>
</template>

<style lang="scss" scoped>
  @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    ul{
    list-style-type: none;

    span{
        font-size: 2.5rem;
        color: $BlueLagoon;
    }
}

</style>