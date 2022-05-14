<template>
  <div class="">
    <div v-for="i in 5" :key="i">
    <a  class="link" :href="'/blog/'+(i++)">
           <div  class="pa-5 my-5">
        <v-card class="grey darken-4">
          <v-row>
            <v-col cols="8">
              <div>
                <v-card-title primary-title class="yellow--text">
                  مقاله شماره یک
                </v-card-title>
                <v-card-text class="text-justify white--text">
                  اگر شما یک طراح هستین و یا با طراحی های گرافیکی سروکار دارید
                  به متن های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند.
                  لورم ایپسوم یا طرح‌نما (به انگلیسی: Lorem ipsum) متنی ساختگی و
                  بدون معنی است که برای امتحان فونت و یا پر کردن فضا در یک طراحی
                  گرافیکی و یا صنعت چاپ استفاده میشود
                </v-card-text>
                <span class="text-justify red--text mb-5 mx-5">
                  نویسنده: ادمین    
                </span>
                 <span class="h6 text-justify yellow--text mb-5 mx-5 ">
                   تاریخ انتشار:1400/01/01
                </span>
              </div>
            </v-col>
            <v-col cols="4">
              <v-container fill-height fluid>
                <v-row align="center" justify="center">
                  <v-col>
                    
                    <v-img contain max-height="150" src="img/blog.jpeg"></v-img>
                  
                  </v-col>
                </v-row>
                
                  

                
              </v-container>

              <!-- <div class="d-flex justify-center align-center" >
                <v-img max-height="150" src="img/blog.jpeg"></v-img>
              </div> -->
            </v-col>
          </v-row>
        </v-card>
      </div>
       </a>
    </div>
  </div>
</template>
<script>
export default {
  name: "Blog",
  data() {
    return {};
  },
};
</script>
<style scoped>
.link{
  text-decoration: none;
}
.vert-text-btn {
  display: block;
  transform: rotate(90deg);
  margin: 50px;

  border-width: 5px;
}
</style>