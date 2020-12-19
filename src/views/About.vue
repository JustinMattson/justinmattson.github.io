<template>
  <div class="about container-fluid bg-image">
    <div class="row">
      <div class="col-12">
        <!-- Because the top of the display slides under the fixed Navbar -->
        <div class style="height:75px;"></div>
        <h1
          class="text-dark-vue text-shadow-light p-2 rounded-lg"
          style="background-color:#ffffffcc"
        >...More about Justin Mattson</h1>
      </div>
    </div>

    <!-- Clock Component -->
    <div class="row m-3 d-flex">
      <clock />
    </div>

    <!-- Fun little personality profile -->
    <div class="row m-3 d-flex justify-content-center py-2 my-2">
      <div
        class="col-12 text-light-vue text-shadow-dark valign bg-white rounded-lg"
        style="min-width:320px;max-width:450px;"
      >
        <a
          href="https://drive.google.com/file/d/1wr6A3HvVw2nHFLzWRMOftcsuuIi1bPSK/view?usp=sharing"
        >
          <h4 class="p-2 m-0">My Emergenetics Profile</h4>
        </a>
      </div>
      <div
        class="col-12 col-md-6 text-light-vue text-shadow-dark valign bg-white rounded-lg"
        style="min-width:320px;max-width:450px;"
      >
        <a href="https://www.emergenetics.com/">
          <img
            class="py-2"
            :src="require('@/assets/img/emergenetics_logo.png')"
            style="height:75px;"
            alt="Emergenetics Logo"
          />
          <!-- <br />
          <small class="text-muted">https://www.emergenetics.com</small>-->
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Clock from "@/components/Clock.vue";
export default {
  name: "about",
  components: {
    Clock,
  },
};
</script>

<style scoped>
a {
  color: #800080;
}
.bg-image {
  background: url("../assets/img/RRcanyon.jpg") no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  background-attachment: fixed;
  min-height: 100vh;
}
</style>