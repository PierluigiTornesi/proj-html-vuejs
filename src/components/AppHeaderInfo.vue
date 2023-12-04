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
                <p><i class="fa-solid fa-clock"></i> Open Hours: Mon - Sat - 9:00 - 18:00</p>
            </div>
            <div>
                <ul>
                    <li><a href=""><i class="fa-solid fa-phone"></i> +1 (305) 1234-5678</a></li>
                    <li><a href=""><i class="fa-solid fa-envelope"></i> hello@example.com</a></li>
                    <li><a href=""><i class="fa-brands fa-facebook-f"></i></a></li>
                    <li><a href=""><i class="fa-brands fa-twitter"></i></a></li>
                    <li><a href=""><i class="fa-brands fa-linkedin-in"></i></a></li>
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
    gap: 1rem;

    a{
        text-decoration: none;
        color: inherit;
    }
}

</style>