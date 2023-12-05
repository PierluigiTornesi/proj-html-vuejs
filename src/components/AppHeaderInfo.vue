<script>

  export default{
    props:{
        links:Array,
        info:Array
    }
  }
</script>

<template>
    <section>
        <div class="container text-white">
            <div>
                <p><i class="fa-solid fa-clock"></i> Open Hours: {{info.dayStart}} - {{info.dayOff}} - {{info.hourStart}} - {{info.hourOff}}</p>
            </div>
            <div>
                <ul>
                    <li v-for="link in links">
                        <a href="">
                            <i :class="link.classIcon"></i> {{ link.text }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.container{
    @include flex(row,space-between,center);
    height: 50px;
    padding-top: 0.6rem;
}

ul{
    @include flex(row,space-between,center);
    list-style: none;
    gap: 2rem;

    a{
        text-decoration: none;
        color: inherit;
    }
}

</style>