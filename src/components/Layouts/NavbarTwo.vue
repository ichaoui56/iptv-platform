<template>
  <nav
    :class="[
      'navbar navbar-expand-lg bg-transparent p-0 fixed-top mt-20',
      { sticky: isSticky },
    ]"
  >
    <div class="container mw-1720 bg-opacity px-50 position-relative">
      <RouterLink class="navbar-brand" to="/">
        <img
          src="@/assets/images/logo/nextplaytv-logo.png"
          class="main-logo"
          width="190"
          height="50"
          alt="white-logo"
        />
        <img
          src="@/assets/images/white-logo.svg"
          class="white-logo d-none"
          width="190"
          height="50"
          alt="white-logo"
        />
      </RouterLink>
      <a class="navbar-toggler" @click="stateStoreInstance.responsiveNavbar">
        <span class="burger-menu">
          <span class="top-bar"></span>
          <span class="middle-bar"></span>
          <span class="bottom-bar"></span>
        </span>
      </a>

      <div class="collapse navbar-collapse">
        <ul class="navbar-nav" style="margin-left: 120px">
          <li class="nav-item dropdown">
            <RouterLink class="nav-link" to="/"> Home </RouterLink>
          </li>

          <li class="nav-item dropdown">
            <RouterLink class="nav-link" to="/pricing-plan">
              Subscription
            </RouterLink>
          </li>

          <li class="nav-item dropdown">
            <RouterLink class="nav-link" to="/channel-list">
              Channel List
            </RouterLink>
          </li>

          <li class="nav-item dropdown">
            <RouterLink class="nav-link" to="/faq"> FAQ </RouterLink>
          </li>

          <li class="nav-item dropdown">
            <RouterLink class="nav-link" to="/about-us"> About Us </RouterLink>
          </li>
          <li class="nav-item dropdown">
            <RouterLink class="nav-link" to="/contact-us"> Contact </RouterLink>
          </li>
        </ul>
      </div>

      <ul
        class="d-flex ps-0 mb-0 list-unstyled justify-content-end align-items-center others-options"
      >
        <li class="d-none d-sm-inline-block">
          <a href="tel:125487568" class="call icon">
            <i class="ti ti-phone-incoming"></i>
          </a>
        </li>
        <li class="d-none d-xl-block">
          <RouterLink to="/pricing-plan" class="btn">
            <span class="border-style">Get Started</span>
          </RouterLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script lang="ts">
import { defineComponent, onMounted, ref } from "vue";
import stateStore from "@/utils/store";
import { useCartStore } from "@/store/index";

export default defineComponent({
  name: "NavbarTwo",
  setup() {
    const isSticky = ref(false);
    const stateStoreInstance = stateStore;
    const cartStore = useCartStore();

    onMounted(() => {
      window.addEventListener("scroll", () => {
        let scrollPos = window.scrollY;
        isSticky.value = scrollPos >= 100;
      });
    });

    return {
      isSticky,
      stateStoreInstance,
      cartStore,
    };
  },
});
</script>
