<template>
  <div>
       <v-card tile flat color="white" height="100%" width="100%">
           <v-card-text>
             <v-row>
               <v-col cols="auto">
                 <hooper :vertical="true" style="height: 700px" :itemsToShow="7" :centerMode="false">
                    <slide style="cursor: pointer" class="px-0" v-for="(item, i) in images" :key="i">
                      <v-card @click="selected = item.link" outlined flat style="border-radius: 4px" width="65" height="65">
                        <v-img class="fill-height" :src="item.link" >
                      </v-img></v-card>
                    </slide>
                  </hooper>
               </v-col>
               <v-col cols="10">
                 <v-card flat style="border-radius: 8px" outlined height="100%" width="100%">
                   <v-card-text>
                     <v-row justify="center" align="center">
                       <v-col cols="auto">
                         <v-img width="300" height="500" contain :src="selected"></v-img>
                       </v-col>
                     </v-row>
                   </v-card-text>
                 </v-card>
               </v-col>
             </v-row>
           </v-card-text>
        </v-card>
  </div>
</template>

<script>
import { Hooper, Slide } from 'hooper'
import 'hooper/dist/hooper.css'

export default {
  components: {
    Hooper,
    Slide
  },
  data () {
    return {
      selected: require('../assets/images/product1.png'),
      images: [
        {
          link: 'https://static-01.daraz.pk/p/cf508a4902f6d34e304c7b8ced614776.jpg'
        },
        {
          link: 'https://androidnik.ru/wp-content/uploads/2016/03/stilus-v-smartfone-chto-eto-takoe3.jpg'
        },
        {
          link: 'https://aquamarket.ua/53875-large_default/head-shoulders-gift-set-for-men-men-ultra-shampoo-comprehensive-care-360ml-deodorant-old-spice-150ml.jpg'
        },
        {
          link: 'https://www.fivestartrading-holland.eu/images/product_images/original_images/Lays%20Chips%20Bolognese.png'
        },
        {
          link: 'https://static-01.daraz.pk/p/cf508a4902f6d34e304c7b8ced614776.jpg'
        },
        {
          link: 'https://aquamarket.ua/53875-large_default/head-shoulders-gift-set-for-men-men-ultra-shampoo-comprehensive-care-360ml-deodorant-old-spice-150ml.jpg'
        },
        {
          link: 'https://androidnik.ru/wp-content/uploads/2016/03/stilus-v-smartfone-chto-eto-takoe3.jpg'
        },
        {
          link: 'https://www.fivestartrading-holland.eu/images/product_images/original_images/Lays%20Chips%20Bolognese.png'
        }
      ]
    }
  }
}
</script>

<style>
.hooper-track {
  padding: 0px !important
}
.hooper {
  outline: 0 !important;
}
</style>
