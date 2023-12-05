<script>
import AppFooterInfo from "../components/AppFooterInfo.vue"

  export default{
    data(){
      return{
        infos:[
            {
                classIcon:"fa-phone",
                text:"+1 (305) 1234-5678",
            },
            {
                classIcon:"fa-envelope",
                text:"hello@example.com",
            },
            {
                classIcon:"fa-location-dot",
                text:"Main Avenue, 987",
            }
        ]
      }
    },
    components: {AppFooterInfo}
  }
</script>

<template>
    <div class="bc-back">
        <div class="container">
            <div class="row">
                <div class="col-8">
                    <div class="text-form text-white">
                        <div class="special">
                            <span>SEND A MESSAGE</span>
                        </div>
                        <div>
                            <h2 class="fw-bold">Get in <span class="back">Touch</span></h2>
                        </div>
                        <div class="descform">
                            <p>We will respond to your message as soon as possible.</p>
                        </div>
                    </div> 
                    <div class="row">
                        <div class="col-6">
                            <div class="mb-3">
                                <label for="nameInput" class="form-label"></label>
                                <input type="text" class="form-control colored" id="nameInput" placeholder="Name" required>
                            </div>
                        </div>
                        <div class="col-6">
                            <div class="mb-3">
                                <label for="emailInput" class="form-label"></label>
                                <input type="email" class="form-control colored" id="emailInput" placeholder="Email" required>
                            </div>
                        </div>
                        <div class="col-6">
                            <div class="mb-3">
                                <label for="numberInput" class="form-label"></label>
                                <input type="text" class="form-control colored" id="numberInput" placeholder="Phone" required>
                            </div>
                        </div>
                        <div class="col-6">
                            <div class="mb-3">
                                <label for="moreInfoInput" class="form-label"></label>
                                <select class="form-select colored" id="moreInfoInput" required>
                                    <option selected disabled value="">More Info </option>
                                    <option value="1">Info 1</option>
                                    <option value="2">Info 2</option>
                                    <option value="3">Info 3</option>
                                </select>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="mb-3">
                                <label for="exampleFormControlTextarea1" class="form-label"></label>
                                <textarea class="form-control colored" id="exampleFormControlTextarea1" rows="5" placeholder="Message"></textarea>
                            </div>
                        </div>
                    </div>
                    <div>
                        <a class="colored-button text-white" href="">SEND</a>
                    </div>
                </div>
                <div class="col-4 text-white">
                    <h4>Example Inc.</h4>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. </p>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
                    <ul>
                        <li v-for="infoTaken in infos">
                            <AppFooterInfo :info = infoTaken />
                        </li>
                    </ul>
                    <a class="nocolor-button" href="">VIEW MAP</a>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

    .bc-back{
        background-color: $Woodsmoke;
    }

    .container{
        padding-top: 4rem;
        padding-bottom: 4rem;
    }

    ul{
        padding: 1rem;
        @include flex(column,space-between,left);
        list-style: none;
        gap: 2rem;

        li{
            @include flex(row,none,center);
        }
    }

    .nocolor-button{
    border: 1px solid $FountainBlue;
    color: $White;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
    }
    
    .col-4{
        p{
            width: 70%;
            color: $GrayNurse;
        }
    }


.text-form{

    .special{
        color: $FountainBlue;
        padding-bottom: 1rem;
    }

    .back{
        background-color: rgba($color: $BlueLagoon, $alpha: 0.4);
        padding: 0.3rem 0.6rem;
        border-radius: 5px;
        
    }

    .descform{
        color: $GrayNurse;
        margin-top: 1rem;
        padding-bottom: 2rem;
    }
}

.colored{
    background-color: $Shark;
    color: $ShuttleGray;
    border-color: $Shark;
}


.colored-button{
    background-color: $FountainBlue;
    border-color: $FountainBlue;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
}
</style>