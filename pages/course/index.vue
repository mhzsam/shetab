<template >
  <div>
      <!-- {{mobileChecker}} -->
    <div v-if="! mobileChecker">
      <v-row no-gutters>
        <v-col cols="12" md="12">
          <v-card style="z-index: 999" color="#CCDCF2" class="mx-8 mb-n14 mt-5">
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-arrow-left-drop-circle</v-icon>
              دوره های شماره 1
            </v-card-title>
          </v-card>
          <v-card class="ma-5">
            <div class="pt-5">
              <v-carousel cycle height="auto" class="pb-5">
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/2.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 2
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="3" sm="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/3.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 3
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="3" sm="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/4.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 4
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>

                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/5.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 5
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-card>
        </v-col>
      </v-row>

      <v-row no-gutters>
        <v-col cols="12" md="12">
          <v-card style="z-index: 999" color="#CCDCF2" class="mx-8 mb-n14 mt-5">
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-arrow-left-drop-circle</v-icon>
              دوره های شماره 2
            </v-card-title>
          </v-card>
          <v-card class="ma-5">
            <div class="pt-5">
              <v-carousel cycle height="auto" class="pb-5">
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/2.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 2
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="3" sm="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/3.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 3
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="3" sm="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/4.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 4
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>

                    <v-col cols="3" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/5.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 5
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </div>

<!-- mobile -->


    <div v-if=" mobileChecker">
      <v-row no-gutters>
        <v-col cols="12" md="12">
          <v-card style="z-index: 999" color="#CCDCF2" class="mx-8 mb-n14 mt-5">
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-arrow-left-drop-circle</v-icon>
              دوره های شماره 1
            </v-card-title>
          </v-card>
          <v-card class="ma-5">
            <div class="pt-5">
              <v-carousel cycle height="auto" class="pb-5">
                

                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/2.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 2
                        </v-btn>
                      </a>
                    </v-col>
                  
                  </v-row>
                </v-carousel-item>




                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    
                    <v-col cols="6"  class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/3.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 3
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="6"  class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/4.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 4
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>

                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/5.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 5
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-card>
        </v-col>
      </v-row>

      <v-row no-gutters>
        <v-col cols="12" md="12">
          <v-card style="z-index: 999" color="#CCDCF2" class="mx-8 mb-n14 mt-5">
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-arrow-left-drop-circle</v-icon>
              دوره های شماره 2
            </v-card-title>
          </v-card>
          <v-card class="ma-5">
            <div class="pt-5">
              <v-carousel cycle height="auto" class="pb-5">
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                   
                    <v-col cols="6"  class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/4.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 4
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
                 <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/2.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 2
                        </v-btn>
                      </a>
                    </v-col>
                    <v-col cols="6"  class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/3.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 3
                        </v-btn>
                      </a>
                    </v-col>
                    
                  </v-row>
                </v-carousel-item>
                <v-carousel-item>
                  <v-row class="py-5 ma-5">
                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/1.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 1
                        </v-btn>
                      </a>
                    </v-col>

                    <v-col cols="6" class="on-hover">
                      <a style="text-decoration: none" href="">
                        <v-img src="/img/course/5.png"></v-img>
                        <v-btn color="#f4f6fc" class="py-5 active" block
                          >دوره شماره 5
                        </v-btn>
                      </a>
                    </v-col>
                  </v-row>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </div>
    
  </div>
</template>
<script>
export default {
  data() {
    return {
        
     
    };
  },
//   mounted(){
// return this.withofwindow=this.$vuetify.breakpoint.width
//   },
 computed:{
    mobileChecker(){
       if(this.$vuetify.breakpoint.width<600){
           return true
       }
       else{
           return false
       }
    }
 }

};
</script>
<style scoped >
</style>