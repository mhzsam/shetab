<template>
  <div>
    <v-row class="pt-3 ">
      <v-carousel cycle height="auto">
        <v-carousel-item>
          <v-img src="/img/wallpaper/1.png"> </v-img>
        </v-carousel-item>
      </v-carousel>
      
    </v-row>
    
    <v-row>
      <v-col class="mt-10" cols="12">
        <h2 class="d-flex justify-center">خدمات ویژه استارتاپ ها</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col center cols="12" md="6">
        <div class="d-flex justify-center ma-n6 pa-0" justify-center>
          <v-img max-width="300" src="/img/wallpaper/acc.png"> </v-img>
        </div>
      </v-col>
      <v-col cols="12" md="6">
        <div class="mt-12 px-8 mb-3">
          <ul>
            <li>دسترسی به پنل های اختصاصی (پیش شتابدهی و شتابدهی)</li>
            <li>
              امکان دسترسی به بستری کاملا کاربردی برای ایجاد و توسعه استارتاپ
            </li>
            <li>امکان بهره مندی از منتورهای با تجربه و متخصص</li>
            <li>امکان جذب سرمایه از سرمایه گذاران عضو وینوهاب</li>
            <li>امکان استفاده از خدمات آموزشی استاندارد و به روز</li>
            <li>امکان مدیریت تیم در پنل</li>
          </ul>
        </div>
      </v-col>
    </v-row>

    <v-parallax
      gradient="to top right, rgba(252,255,0,.7), rgba(2,0,36,.7)"
      dark
      src="/img/wallpaper/para.jpg"
      height="350"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="text-h4 yellow--text font-weight-thin mb-4">هم اکنون</h1>
          <h4 class="subheading yellow--text">با هم پیشرفت کنیم</h4>
          <v-btn href="/login" color="yellow" width="200" class="mt-8"
            >ثبت نام</v-btn
          >
        </v-col>
      </v-row>
    </v-parallax>

    <v-row class="" >
      <v-col class="mt-10" cols="12">
        <h2 class="d-flex justify-center">خدمات ویژه سرمایه‌گذاران</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col center cols="12" md="6">
        <div class="d-flex justify-center ma-n6 pa-0" justify-center>
          <v-img max-width="300" src="/img/wallpaper/investt.png"> </v-img>
        </div>
      </v-col>
      <v-col class="pb-10 mb-16" cols="12" md="6">
        <div class="mt-12 px-8 mb-3">
          <ul>
            <li>
              امکان مشاهده تمامی استارتاپ های عضو وینوهاب که آماده جذب سرمایه
              هستند.
            </li>
            <li>امکان سرمایه گذاری بر روی استارتاپ های عضو وینوهاب</li>
            <li>امکان رصد فعالیت استارتاپ های سرمایه گذاری شده</li>
            <li>امکان جذب سرمایه از سرمایه گذاران عضو وینوهاب</li>
            <li>امکان دریافت محتواهای آموزشی مرتبط با حوزه سرمایه گذاری</li>
            <li>
              امکان دسترسی به پنل اختصاصی جهت سرمایه گذاری و مدیریت تیم ها
            </li>
          </ul>
        </div>
      </v-col>
    </v-row>

    <v-parallax dark src="/img/wallpaper/para2.jpg" height="350">
      <v-row align="center" justify="center"> </v-row>
    </v-parallax>

    <v-row>
      <v-col class="mt-10" cols="12">
        <h2 class="d-flex justify-center">خدمات ویژه منتورها</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col center cols="12" md="6">
        <div class="d-flex justify-center ma-n6 pa-0" justify-center>
          <v-img max-width="300" src="/img/wallpaper/meeting.png"> </v-img>
        </div>
      </v-col>
      <v-col cols="12" md="6">
        <div class="mt-12 px-8 mb-3">
          <ul>
            <li>امکان دسترسی به پنل اختصاصی جهت مدیریت خدمات منتورینگ</li>
            <li>امکان مدیریت درخواست های مشاوره</li>
            <li>امکان تنظیم جلسات مشاوره در پنل</li>
            <li>امکان دریافت و ارسال گزارشات مرتبط با استارتاپ ها</li>
            <li>
              مکان دسترسی به بخش اعظمی از محتواهای آموزشی و ابزارهای کاربردی جهت
              استفاده در جلسات منتورینگ
            </li>
          </ul>
        </div>
      </v-col>
    </v-row>
    <v-parallax class="mt-10" dark src="/img/wallpaper/para.jpg" height="50">
      <v-row align="center" justify="center"> </v-row>
    </v-parallax>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "/img/wallpaper/2.png",
        },
        {
          src: "/img/wallpaper/1.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
.graybackground {
  background-color: #333;
}
</style>>

