<template>
  <div>
    <v-card>
      <v-card-title class="text-center title-page py-3">
        <v-icon class="mx-2" color="black">mdi-arrow-left-bold-circle</v-icon>

        <span class="">ناحیه کاربری </span>
      </v-card-title>

      <v-tabs
        background-color="#555"
        active-class="active-class"
        color="yellow "
        show-arrows
      >
        <v-tab class="white--text" style="title-tab"> داشبورد</v-tab>
        <v-tab-item> 
          <Dashboard />
        </v-tab-item>

        <v-tab class="white--text" style="title-tab">ویرایش حساب</v-tab>
        <v-tab-item>
          <Dashboard-UserPanel />
        </v-tab-item>
        <v-tab class="white--text" style="title-tab">آخرین دوره های خرید شده </v-tab>
        <v-tab-item>
          <v-card flat>
            <Dashboard-Course />
          </v-card>
        </v-tab-item>
        <v-tab class="white--text" style="title-tab">مالی</v-tab>
        <v-tab-item>
          <v-card flat>
           <Dashboard-Financial />
          </v-card>
        </v-tab-item>
        <v-tab class="white--text" style="title-tab">پشتیبانی</v-tab>
        <v-tab-item>
          <Dashboard-Support />
        </v-tab-item>
      </v-tabs>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tab: null,

      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
    };
  },
};
</script>

<style scoped>
.active-class {
  background-color: black;
  color: yellow !important;
}
.title-page {
  background-color: #f4f6fc;
  font-weight: bold;
}
.basil {
  background-color: #ffffff !important;
}
.basil--text {
  color: #356859 !important;
}
</style>
