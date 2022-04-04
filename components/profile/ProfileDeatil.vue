<template lang="">
  <div>
    <v-container fluid class="mt-n10 px-6">
      <v-row>
        <v-col xs="12" sm="4" md="4" lg="4">
          <v-card height="220px" >
            <v-card-text>
              <p>نام : {{ firstName }}</p>
              <p>نام خانوادگی : {{ lastName }}</p>
              <p>تاریخ عضویت : {{ registerDate }}</p>
              <p>جنسیت : {{ gender }}</p>
              <p>ایمیل : {{ email }}</p>
            </v-card-text>

            




 <v-row justify="center pt-5">
    <v-dialog
      v-model="dialog"
      persistent
      max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
          class=""
        >
         ویرایش حساب کاربری
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">ویرایش حساب کاربری</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col
                cols="12"
                sm="6"
                md="6"
              >
                <v-text-field
                  label="نام"
                  required
                  :value=firstName
                ></v-text-field>
              </v-col>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <v-text-field
                  label="نام خانوادگی"
                  required
                  :value=lastName
                ></v-text-field>
              </v-col>
          
              <v-col cols="12">
                <v-text-field
                  label="ایمیل*"
                  required
                  :value=email
                ></v-text-field>
              </v-col>
             
              
            </v-row>
          </v-container>
        
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="blue darken-1"
            text
            @click="dialog = false"
          >
            بستن
          </v-btn>
          <v-btn
            color="blue darken-1"
            text
            @click=changeProfileDetails()
          >
            ذخیره
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>










            
          </v-card>
        </v-col>
        <v-col xs="12" sm="4" md="4" lg="4">
          <v-card height="220px" align="center">
            <v-avatar class="profile mt-5 " color="" size="120px" tile>
              <v-img src="img/avatar.png"></v-img>
            </v-avatar>
            
            <v-card-actions class="justify-center mt-3">
              <v-btn elevation="2" color="">ویرایش عکس پروفایل</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col xs="12" sm="4" md="4" lg="4">
          <v-card height="220px">
            <v-card-title primary-title> کیف پول </v-card-title>
            <v-card-text>
              <p>موجودی : {{ balance }}</p>
            </v-card-text>

            <v-card-actions class="justify-center mt-12">
              <v-btn elevation="2" color="">تاریخچه تراکنش </v-btn>
              <v-btn elevation="2" color="">افزایش موجودی</v-btn>
            </v-card-actions>
            
          </v-card>
        </v-col>
        <v-col xs="12" sm="8" md="8" lg="8">
          <v-card height="250px">
            <v-card-title primary-title> میزان فعالیت </v-card-title>

       <v-sparkline
      
    :value="value"
    :gradient="gradient"
    :smooth="radius || false"
    :padding="padding"
    :line-width="width"
    :stroke-linecap="lineCap"
    :gradient-direction="gradientDirection"
    :fill="fill"
    :type="type"
    :auto-line-width="autoLineWidth"
    auto-draw
  ></v-sparkline>
  
      </v-card>
    </v-card>

            
          </v-card>
        </v-col>
        </v-col>
        <v-col xs="12" sm="4" md="4" lg="4">
          <v-card height="250px"  >
           
                  
            <div class="gauge">
              
              
                         <VueSvgGauge
  :start-angle="-110"
  :end-angle="110"
  :value="75"
  :separator-step="25"
  :min="0"
  :max="100"
  :gauge-color="[{ offset: 0, color: '#5C6BC0'}, { offset: 100, color: '#8CDFAD'}]"
  :scale-interval="2"
  
/>

            </div>
            <div class="svgtext" >
              <h3>میزان پیشرفت</h3>
              <h3>75%</h3>
              </div>


           
          </v-card>
        </v-col>

      </v-row>
      <v-row>
        <v-col >
          <v-card height="420px" >
            <v-card-title primary-title>
              آخرین دوره های خرید
            </v-card-title>
           <v-row >
             <v-col
        v-for="n in 4"
        :key="n"
        cols="12"
        sm="3"
         class="pa-5"
      >
        <v-card
          class="pa-5"
          flat
         
        >
             <v-card class="justify-center" to="123">
              <v-img
                          
                src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
              >
              </v-img>
             <v-card-title class="justify-center">
               شتاب دهنده امین
             </v-card-title>

              
            </v-card>
          
        </v-card>
        
      </v-col>
    </v-row>
           </v-content>

             <v-card-actions class="justify-center">
              <v-btn elevation="2" color="">دیدن همه دوره ها</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

      </v-row>
      
    </v-container>
  </div>
  
</template>
<script>
const gradients = [
  // ['#222'],
  // ['#42b3f4'],
  // ['red', 'orange', 'yellow'],
  // ['purple', 'violet'],
  // ['#00c6ff', '#F0F', '#FF0'],
  // ['#f72047', '#ffd200', '#1feaea'],
];
export default {
  name: "ProfileDeatil",
  data() {
    return {
 dialog: false,

      width: 1,
      radius: 10,
      padding: 8,
      lineCap: "round",
      gradient: gradients[5],
      value: [0, 2, 5, 9, 2, 9, 0],
      gradientDirection: "top",
      gradients,
      fill: false,
      type: "trend",
      autoLineWidth: false,

      firstName: "mohammad",
      lastName: "zarrabi",
      registerDate: "1400/11/01",
      gender: "male",
      email: "mhzsam@gmail.com",
      balance: 3500,
    };
  },
  methods:{
changeProfileDetails(){
this.dialog=false
}
  },
};
</script>
<style scoped>
p {
  margin: 2px;
}
.gauge {
  margin: auto;

  width: 90%;
}
.svgtext {
  margin-top: -100px;
  color: #5c6bc0;
  text-align: center;
}
</style>
