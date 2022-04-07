<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="350px">
          
           
          <div >
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-account-circle</v-icon>
              مشخصات کاربری
            </v-card-title>
            <v-divider inset></v-divider>

            <v-card-text class="black--text mr-14" height="220px">
              <p>نام : {{ firstName }}</p>
              <p>نام خانوادگی : {{ lastName }}</p>
              <p>تاریخ عضویت : {{ registerDate }}</p>
              <p>جنسیت : {{ gender }}</p>
              <p>ایمیل : {{ email }}</p>
            </v-card-text>
            <v-flex d-flex justify-center>
              <v-btn
                width="70%"
                class=""
                dark
                elevation="2"
                color="orange"
                @click="editeUserProfile"
                >ویرایش</v-btn
              >
            </v-flex>
          </div>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card class="ma-5" height="350px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-face-man-profile</v-icon>
           ارسال تیکت
          </v-card-title>
          <v-divider inset></v-divider>
          <div v-if="esiteUserAvatar">
            <v-flex class="mt-5 pt-10" d-flex justify-center>
              <v-file-input
                class="ma-4"
                :rules="avatarRules"
                accept="image/png, image/jpeg, image/bmp"
                placeholder="بارگیری عکس"
                prepend-icon="mdi-paperclip"
                label="انتخاب عکس"
                outlined
                rounded
                v-model="files"
                
              ></v-file-input>
            </v-flex>
            <v-flex class="" d-flex justify-center>
              <v-btn width="70%" class="" dark elevation="2" color="green"
              @click="uploadAvatar"
                >ذخیره</v-btn
              >
            </v-flex>
          </div>
          <div v-if="!esiteUserAvatar">
            <v-flex class="mt-5" d-flex justify-center>
              <v-avatar max-width="180" size="180">
                <v-img src="img/avatar/avatar.png"></v-img>
              </v-avatar>
            </v-flex>
            <v-flex class="mt-5" d-flex justify-center>
              <v-btn width="70%" class="" dark elevation="2" color="orange"
              @click="changeAvatar"
                >ویرایش</v-btn
              >
            </v-flex>
          </div>
        </v-card>
      </v-col>
      
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Dashboard-Support",
  data() {
    return {
     
   
      avatarRules: [
        (value) => !value || value.size < 200000 || "کمتر از 2 مگابایت",
      ],
      nameRule: [
        (v) => !!v || " پر کردن اجباری می باشد ",
        (v) => (v && v.length >= 3) || "حداقل 3 کاراکتر",
      ],
    };
  },
  methods: {
    
    
  },
};
</script>

<style scoped></style>
