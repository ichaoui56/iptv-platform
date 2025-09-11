<template>
  <div
    :class="[
      'mobile-navbar offcanvas offcanvas-end border-0',
      { show: stateStoreInstance.navbar },
    ]"
  >
    <div class="offcanvas-header">
      <RouterLink to="/" class="logo d-inline-block">
        <img src="@/assets/images/logo.svg" alt="logo" />
      </RouterLink>
      <RouterLink to="/" class="logo d-none">
        <img src="@/assets/images/white-logo.svg" alt="logo" />
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
        <li :class="['mobile-menu-list', { active: isActive('home') }]">
          <a class="menu-link menu-toggle active" @click="toggleMenu('home')">
            Home
          </a>

          <ul class="mobile-menu-items" v-show="isActive('home')">
            <li>
              <RouterLink
                class="dropdown-item"
                to="/"
                @click="stateStoreInstance.responsiveNavbar"
              >
                ISP Provider
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/iptv-service"
                @click="stateStoreInstance.responsiveNavbar"
              >
                IPTV Service
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/isp-broadband"
                @click="stateStoreInstance.responsiveNavbar"
              >
                ISP Broadband
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/ott-platform"
                @click="stateStoreInstance.responsiveNavbar"
              >
                OTT Platform
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/movie-home"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Movie Home
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/satellite-internet"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Satellite Internet
              </RouterLink>
            </li>
          </ul>
        </li>

        <li :class="['mobile-menu-list', { active: isActive('services') }]">
          <a
            class="menu-link menu-toggle active"
            @click="toggleMenu('services')"
          >
            Services
          </a>

          <ul class="mobile-menu-items" v-show="isActive('services')">
            <li>
              <RouterLink
                class="dropdown-item"
                to="/services"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Services
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/services-details"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Services Details
              </RouterLink>
            </li>
          </ul>
        </li>

        <li :class="['mobile-menu-list', { active: isActive('pages') }]">
          <a class="menu-link menu-toggle active" @click="toggleMenu('pages')">
            Pages
          </a>

          <ul class="mobile-menu-items" v-show="isActive('pages')">
            <li>
              <RouterLink
                class="dropdown-item"
                to="/about-us"
                @click="stateStoreInstance.responsiveNavbar"
              >
                About Us
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/testimonials"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Testimonials
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/pricing-plan"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Pricing Plan
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/channel-list"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Channel List
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/faq"
                @click="stateStoreInstance.responsiveNavbar"
              >
                FAQ
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/privacy-policy"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Privacy Policy
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/terms-conditions"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Terms & Conditions
              </RouterLink>
            </li>
          </ul>
        </li>

        <li :class="['mobile-menu-list', { active: isActive('shop') }]">
          <a class="menu-link menu-toggle active" @click="toggleMenu('shop')">
            Shop
          </a>

          <ul class="mobile-menu-items" v-show="isActive('shop')">
            <li>
              <RouterLink
                class="dropdown-item"
                to="/products"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Products
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/product-details"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Product Details
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/cart"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Cart
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/checkout"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Checkout
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/pay-bill"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Pay Bill
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/pay-bill-pin"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Pay Bill PIN
              </RouterLink>
            </li>
          </ul>
        </li>

        <li :class="['mobile-menu-list', { active: isActive('blog') }]">
          <a class="menu-link menu-toggle active" @click="toggleMenu('blog')">
            Blog
          </a>

          <ul class="mobile-menu-items" v-show="isActive('blog')">
            <li>
              <RouterLink
                class="dropdown-item"
                to="/blog"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Blog
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/blog-details"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Blog Details
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/tags"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Tags
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/categories"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Categories
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/author"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Author
              </RouterLink>
            </li>
          </ul>
        </li>

        <li
          :class="['mobile-menu-list', { active: isActive('authentication') }]"
        >
          <a
            class="menu-link menu-toggle active"
            @click="toggleMenu('authentication')"
          >
            Authentication
          </a>

          <ul class="mobile-menu-items" v-show="isActive('authentication')">
            <li>
              <RouterLink
                class="dropdown-item"
                to="/login-register"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Login / Register
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/login"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Login
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/register"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Register
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/change-password"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Change Password
              </RouterLink>
            </li>
            <li>
              <RouterLink
                class="dropdown-item"
                to="/forgot-password"
                @click="stateStoreInstance.responsiveNavbar"
              >
                Forgot Password
              </RouterLink>
            </li>
          </ul>
        </li>

        <li class="mobile-menu-list without-icon">
          <RouterLink
            to="/pricing-plan"
            class="nav-link"
            @click="stateStoreInstance.responsiveNavbar"
          >
            Pricing Plan
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
