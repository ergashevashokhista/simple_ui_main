<template>
  <div>
    <v-card tile  flat color="white" height="100%" width="100%">
      <v-card-text>
        <v-row :gutters="[5, 5]">
          <v-col cols="12">
            <h2 class="title_product">
              100% органический 10 лет корень корейского <br />
              женьшеня красный Panax улучшить иммунную
            </h2>
            <v-row align="center" class="my-2 mx-1" :gutters="[4, 4]">
              <v-col cols="auto" class="px-1">
                <v-rating
                  :value="4.5"
                  color="#DAD873"
                  dense
                  half-increments
                  readonly
                  size="18"
                ></v-rating>
              </v-col>
              <v-col cols="auto" class="px-0"
                ><div class="grey--text ml-1">243</div></v-col
              >
              <v-col cols="auto">
                <div class="grey--text ml-7">
                  <small>Количество заказов: 1</small>
                </div>
              </v-col>
            </v-row>
            <v-divider class="mr-5"></v-divider>
          </v-col>
          <v-col cols="12">
            <div class="price_view">15 000 000 <small>сум</small></div>
            <v-row align="center" class="my-1" :gutters="[4, 4]">
              <v-col cols="auto" class="ml-1">
                <span class="text-decoration-line-through">20 000 000 сум</span>
              </v-col>
              <v-col cols="auto" class="px-0"
                ><v-chip class="px-1" small label color="#FF5530" dark>
                  -25%
                </v-chip>
              </v-col>
            </v-row>
            <v-row :gutters="[12, 12]" align="center">
              <v-col cols="auto"
                ><span class="font_13">Методы оплаты:</span></v-col
              >
              <v-col cols="auto"
                ><img :src="require('../assets/images/payme.png')" alt="payme"
              /></v-col>
              <v-col cols="auto"
                ><img :src="require('../assets/images/humo.png')" alt="humo"
              /></v-col>
              <v-col cols="auto"
                ><img :src="require('../assets/images/click.png')" alt="click"
              /></v-col>
            </v-row>
            <v-row :gutters="[12, 12]" align="center">
              <v-col cols="auto"
                ><span class="font_13">Методы доставки:</span></v-col
              >
              <v-col cols="auto" class="ml-4">
                <v-row align="center">
                  <v-col cols="auto " class="px-1"
                    ><img
                      :src="require('../assets/icons/delivery.svg')"
                      alt="delevery"
                  /></v-col>
                  <v-col cols="auto " class="px-0 pb-4">
                    <span style="color: black">Доставка продавца</span></v-col
                  >
                </v-row>
              </v-col>
              <v-col cols="auto" class="ml-4">
                <v-row align="center">
                  <v-col cols="auto " class="px-1"
                    ><img :src="require('../assets/icons/box.svg')" alt="box"
                  /></v-col>
                  <v-col cols="auto " class="px-0 pb-4"
                    ><span style="color: black">Самовывоз</span></v-col
                  >
                </v-row>
              </v-col>
            </v-row>
            <v-divider class="mr-5 my-2"></v-divider>
          </v-col>
          <v-col cols="12">
            <span class="font_13 my-1">Количество</span>
            <v-row align="center">
              <v-col class="py-0" cols="auto">
                <button type="button" @click="counter--" class="btn_style">
                  <v-icon> mdi-minus </v-icon>
                </button>
              </v-col>
              <v-col class="py-0 px-1" cols="auto"
                ><v-sheet
                    style="border-radius: 4px; border: 1px solid #E0E0E0"
                  height="42"
                  class="text-center align-center pa-2"
                  rounded
                  outlined
                  width="50"
                  color="#F6F6F6"
                >
                  <span class="">{{ counter }}</span>
                </v-sheet></v-col
              >
              <v-col cols="auto">
                <button type="button" @click="counter++" class="btn_style">
                  <v-icon> mdi-plus-thick </v-icon>
                </button>
              </v-col>
              <v-col class="py-0" cols="auto">
                <v-chip
                  class="ma-2"
                  style="font-size: 11px"
                  color="#EFEEB4"
                  label
                >
                  <v-icon left color="green"> mdi-check </v-icon>
                  в наличии 1 245 шт.
                </v-chip>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="auto"
                ><v-btn elevation="0" dark color="#309975"
                  >Купить в один клик</v-btn
                ></v-col
              >
              <v-col cols="auto"
                ><v-btn dark color="grey" outlined
                  ><span class="black--text">Связаться с продавцом</span></v-btn
                ></v-col
              >
            </v-row>
            <v-divider class="mr-5 my-4"></v-divider>
          </v-col>
          <v-col cols="12" class="protocol my-1 py-0">
            <span>* Стоимость доставки заказов до 40 000 сум - договорная</span
            ><br />
            <span>** Бесплатная доставка при заказе от 40 000 сум</span>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    counter: 123
  })
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap");
.title_product {
  font-family: "Rubik";
  font-size: 20px;
  font-weight: 500;
  color: black;
}
.price_view {
  font-family: "Rubik";
  color: black;
  font-size: 24px;
  font-weight: 500;
}
.font_13 {
  font-size: 13px;
  color: #596178;
}
.protocol {
  font-size: 15px;
  color: #596178;
}
.btn_style {
    padding: 2px;
    margin: 0px;
    height: 42px;
    width: 42px;
    border-radius: 4px;
    border: 1px solid #E0E0E0;
    color:#E0E0E0;
    background: white;
    width: 42px
}
</style>
