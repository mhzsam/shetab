<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="350px">
          <v-form ref="form" v-model="isValid" lazy-validation>
            <div v-if="!editeUserDetails">
              <v-card-title primary-title>
                <v-icon class="mx-4">mdi-account-circle</v-icon>
                مشخصات کاربری
              </v-card-title>
              <v-divider inset></v-divider>

              <v-card-text class="black--text" height="220px">
                <v-text-field
                  name="name"
                  label="نام"
                  id="id"
                  v-model="firstName"
                  clearable
                  outlined
                  rounded
                  dense
                  class="mb-n1"
                  :rules="nameRule"
                  required
                ></v-text-field>
                <v-text-field
                  name="family"
                  label="نام خانوادگی"
                  id="id"
                  v-model="lastName"
                  clearable
                  outlined
                  rounded
                  dense
                  :rules="nameRule"
                  class="my-n1"
                  required
                ></v-text-field>
                <v-select
                  required
                  name="gender"
                  label="جنسیت"
                  id="id"
                  :items="genderSelect"
                  v-model="gender"
                  outlined
                  rounded
                  dense
                  class="my-n1"
                ></v-select>
              </v-card-text>
              <v-flex d-flex justify-center>
                <v-btn
                  width="70%"
                  class="mx-2"
                  dark
                  elevation="2"
                  color="green"
                  @click="editeUserProfileValidate"
                >
                  ذخیره</v-btn
                >
              </v-flex>
            </div>
          </v-form>
          <div v-if="editeUserDetails">
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
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="350px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-face-man-profile</v-icon>
            عکس پروفایل
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
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="350px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-lock-reset</v-icon>
            تغییر رمز عبور
          </v-card-title>

          <v-divider inset></v-divider>

          <v-card-text class="inline black--text mx-5 mr-14" height="220px">
            برای تغییر رمز بر روی ایکون زیر کلیک نمایید
          </v-card-text>
          <v-flex d-flex justify-center>
            <v-btn
              justify-center
              width="70%"
              class=""
              dark
              elevation="2"
              color="red"
              href="/forgotPassword"
              >تغییر کلمه عبور</v-btn
            >
          </v-flex>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Dashboard-UserPanel",
  data() {
    return {
        files:"",
      isValid: true,
      esiteUserAvatar: false,
      genderSelect: ["زن", "مرد"],
      editeUserDetails: true,
      firstName: "محمد",
      lastName: "ضرابی",
      registerDate: "1400/11/01",
      email: "mhzsam@gmail.com",
      gender: "مرد",
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
    editeUserProfile() {
      var mmm = this.editeUserDetails;
      this.editeUserDetails = !mmm;
    },
    editeUserProfileValidate() {
      if (!this.isValid) {
      } else {
        var mmm = this.editeUserDetails;
        this.editeUserDetails = !mmm;
      }
    },
    uploadAvatar(){
        console.log(this.files)
         var mmm = this.esiteUserAvatar;
        this.esiteUserAvatar = !mmm;
    },
    changeAvatar(){
        var mmm = this.esiteUserAvatar;
        this.esiteUserAvatar = !mmm;
    }
  },
};
</script>

<style scoped></style>
