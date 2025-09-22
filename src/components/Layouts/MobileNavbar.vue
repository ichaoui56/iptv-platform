<template>
  <div
    :class="[
      'mobile-navbar offcanvas offcanvas-end border-0',
      { show: stateStoreInstance.navbar },
    ]"
  >
    <div class="offcanvas-header">
      <RouterLink to="/iptv-service" class="logo d-inline-block">
        <img src="@/assets/images/logo/nextplaytv-logo-w.png" width="190" height="50" alt="logo" />
      </RouterLink>
      <RouterLink to="/iptv-service" class="logo d-none">
        <img src="@/assets/images/logo/nextplaytv-logo.png" width="190" height="50" alt="logo" />
      </RouterLink>

      <button
        type="button"
        class="close-btn bg-transparent position-relative lh-1 p-0 border-0"
        @click="stateStoreInstance.responsiveNavbar"
      >
        <i class="ri-close-fill"></i>
      </button>
    </div>
    <div class="offcanvas-body">
      <ul class="mobile-menu">
        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/iptv-service"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            Home
          </RouterLink>
        </li>
        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/pricing-plan"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            Subscription
          </RouterLink>
        </li>
        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/channel-list"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            Channel List
          </RouterLink>
        </li>
        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/faq"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            FAQ
          </RouterLink>
        </li>
        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/about-us"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            About Us
          </RouterLink>
        </li>

        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/contact-us"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            Contact Us
          </RouterLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import stateStore from "@/utils/store";

export default defineComponent({
  name: "MobileNavbar",
  setup() {
    const stateStoreInstance = stateStore;

    const openMenu = ref<string | null>(null);

    const toggleMenu = (menu: string | null) => {
      openMenu.value = openMenu.value === menu ? null : menu;
    };

    const isActive = (menu: string | null) => {
      return openMenu.value === menu;
    };

    return {
      stateStoreInstance,
      toggleMenu,
      isActive,
    };
  },
});
</script>
