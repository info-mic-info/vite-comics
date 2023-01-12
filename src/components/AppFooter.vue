<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'DIGITAL COMICS',
                    url: '#',
                    active: false,
                    image: 'buy-comics-digital-comics.png'
                },
                {
                    label: 'DC MERCHANDISE',
                    url: '#',
                    active: true,
                    image: 'buy-comics-merchandise.png'
                },
                {
                    label: 'SUBSCRIPTION',
                    url: '#',
                    active: false,
                    image: 'buy-comics-subscriptions.png'
                },
                {
                    label: 'COMIC SHOP LOCATOR',
                    url: '#',
                    active: false,
                    image: 'buy-comics-shop-locator.png'
                },
                {
                    label: 'DC POWER VISA',
                    url: '#',
                    active: false,
                    image: 'buy-dc-power-visa.svg'
                }
            ],

            info: [
                {
                    Title: 'DC COMICS',
                    paragraf: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    Title: 'SHOP',
                    paragraf: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    Title: 'DC',
                    paragraf: ['Term of use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contacts Us']
                },
                {
                    Title: 'SITES',
                    paragraf: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                },
            ],

            social: [
                {
                    logo: 'facebook'
                },
                {
                    logo: 'twitter'
                },
                {
                    logo: 'youtube'
                },
                {
                    logo: 'pinterest'
                },
                {
                    logo: 'periscope'
                },
            ]



        }
    }
}
</script>

<template lang="">
<footer>
<!-- PARTE ALTA -->
<section class="up">
    <nav>
        <ul>
            <li v-for="(elem, index) in menu" :key="index">

               <div class="image">
                   <img :src="'/src/assets/images/' + elem.image" alt="">
               </div>
     
                <a :href="elem.url" :class="elem.active ? 'active' : ''">{{elem.label}}</a>

            </li>
        </ul> 
    </nav>
</section>


<!-- PARTE CENTRALE -->
<section class="middle">


<div class="info">
 <nav>
        <ul>
            <li v-for="(elem, index) in info" :key="index">

              <h4 :class="elem.active ? 'active' : ''">{{elem.Title}}</h4>
              <p v-for="(elem2, index2) in elem.paragraf" :key="index2" :class="elem.active ? 'active' : ''">{{elem2}}</p>

            </li>
        </ul> 

         
    </nav>
</div>
<div class="logo_rotate">
    <img src="../assets/images/dc-logo-bg.png" alt="">
 </div>
</section>


<!-- PARTE BASSA -->
<section class="down">

<h3>SIGN-UP NOW!</h3>

    <nav class="follow">
        
        <h4>FOLLOW US</h4>
      
        <ul>
            <li v-for="(elem, index) in social" :key="index">

                <div class="image">
                      <img :src="'/src/assets/images/' + 'footer-' + elem.logo + '.png'" alt="">
              </div>

            </li>
        </ul> 
    </nav>
</section>
</footer>

</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;





.up,
.middle,
.down {
    padding: $universalPadding;
    padding: $paddingSemantic;
}


.up {
    background-color: $primary;

    a {
        color: $ligth;
        margin: auto 0
    }
}


.up {

    ul,
    li {
        @include flex-beetween;
    }
}

.middle {
    background-image: url("../assets/images/footer-bg.jpg");
    color: $ligth;
    @include flex-beetween;

    .info {
        display: flex;

        ul {
            display: flex;
        }

        li {
            margin: 0 10px
        }

        p {
            margin: 5px 0
        }
    }
}

.down {
    background-color: #303030;
    @include flex-beetween;


    .image img {
        width: 20px;
    }

    ul {
        @include flex-beetween;
    }

    .follow {
        display: flex;
    }

    h3 {
        border: solid 3px $primary;
        padding: 5px;
    }

    h4 {
        color: $primary
    }


}
</style>