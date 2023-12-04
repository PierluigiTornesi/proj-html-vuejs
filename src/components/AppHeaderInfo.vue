<script>

  export default{
    data(){
      return{
        
      }
    }
  }
</script>

<template>
    <section>
        <div class="container text-white">
            <div>
                <p>Open Hours: Mon - Sat - 9:00 - 18:00</p>
            </div>
            <div>
                <ul>
                    <li><a href="">+1 (305) 1234-5678</a></li>
                    <li><a href="">hello@example.com</a></li>
                    <li><a href="">facebook</a></li>
                    <li><a href="">twitter</a></li>
                    <li><a href="">in</a></li>
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
}

ul{
    @include flex(row,space-between,center);
    list-style: none;
    gap: 0.5rem;

    a{
        text-decoration: none;
        color: inherit;
    }
}

</style>