<template>
  <!-- p3 - padding , 3 is 1 rem -->
  <!-- p-lg-5   padding at breakpoint large is 5 or 3 rem -->
  <section id="about" class="resume-section p-3 p-lg-5 d-flex align-items-center">
    <!-- width -->
    <div class="w-100">
      <!-- mb - margin bottom -->
      <h1 class="mb-0">
        {{ name.first }}
        <span class="text-primary">{{ name.last }}</span>
      </h1>

      <div class="subheading mb-5">
        {{ address.street }} &middot; {{ address.town }}, {{ address.postCode }} &middot; {{ telephone }} &middot;
        <a :href="'mailto:' + email">{{ email }}</a>
      </div>
      <p
        class="lead mb-5"
      >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      <div class="social-icons">
        <a :href="social.url" v-for="(social, index) in socialList" :key="index">
          <font-awesome-icon :icon="['fab', social.icon]"></font-awesome-icon>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
  props: {
    name: Array
  },
  data() {
    return {
      address: {
        street: "3/4 82 Barrland Street",
        town: "Glasgow",
        postCode: "G41 1AJ"
      },
      telephone: "07426803506",
      email: "augusto.pasaulis@gmail.com",
      socialList: [
        {
          name: "LinkedIn",
          url: "#",
          icon: "linkedin"
        },
        {
          name: "GitHub",
          url: "#",
          icon: "github"
        }
      ]
    };
  }
};
</script>
