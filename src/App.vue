<template>
  <PreLoader v-if="isLoading" />
  <MobileNavbar />
  <SearchModal />
  <router-view />
  <CartModal />
  <RTLBtn />
  <BackToUp />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PreLoader from "./components/Layouts/PreLoader.vue";
import MobileNavbar from "./components/Layouts/MobileNavbar.vue";
import SearchModal from "./components/Layouts/SearchModal.vue";
import CartModal from "./components/Layouts/CartModal.vue";
import RTLBtn from "./components/Layouts/RTLBtn.vue";
import BackToUp from "./components/Layouts/BackToUp.vue";

export default defineComponent({
  name: "App",
  components: {
    PreLoader,
    MobileNavbar,
    SearchModal,
    CartModal,
    RTLBtn,
    BackToUp,
  },
  data() {
    return {
      isLoading: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 1000);
  },
});
</script>
