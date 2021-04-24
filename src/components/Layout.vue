<template>
  <div class="main_layout">
          <v-row align="center" justify="center" style="height: 100vh">
            <v-col cols="10">
                    <v-card style="padding: 0" color="white" height="100%" width="100%">
                        <v-card-text class="px-0 py-0">
                            <v-row justify="center" align="center">
                                <v-col cols="7">
                                    <Left />
                                </v-col>
                                <v-col cols="5">
                                    <Right />
                                </v-col>
                            </v-row>
                        </v-card-text>
                    </v-card>
            </v-col>
      </v-row>
  </div>
</template>

<script>
import Left from '@/components/Left.vue'
import Right from '@/components/Right.vue'
export default {
  components: { Left, Right }
}
</script>

<style scoped lang="less">
    .main_layout {
        background: #E5E5E5;
        height: 100vh;
        overflow: hidden;
    }
</style>
