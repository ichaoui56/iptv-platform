<template>
  <div class="authentication-area">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7">
          <div class="authentication-form">
            <h2>Login</h2>

            <form>
              <div class="form-floating mb-4">
                <input
                  type="email"
                  class="form-control"
                  id="floatingInput2"
                  placeholder="Email"
                />
                <label for="floatingInput2" class="floating">Email</label>
              </div>
              <div class="form-floating mb-4">
                <input
                  type="password"
                  class="form-control"
                  id="floatingInput1"
                  placeholder="Password"
                />
                <label for="floatingInput1" class="floating">Password</label>
              </div>
              <div
                class="d-flex justify-content-between align-items-center mb-4 flex-wrap"
              >
                <div class="form-check mb-0">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                  />
                  <label
                    class="form-check-label position-relative tops-2"
                    for="flexCheckDefault"
                  >
                    Remember Me
                  </label>
                </div>
                <RouterLink to="/forgot-password" class="forgot mt-2 mt-sm-0">
                  FORGOT PASSWORD?
                </RouterLink>
              </div>
              <div class="text-center">
                <button type="submit" class="btn px-275">
                  <span class="border-style">Login Now</span>
                </button>
              </div>
              <div class="py-4 text-center">or</div>
              <div class="text-center">
                <button type="submit" class="btn active px-275">
                  <span class="border-style">Login With Phone Number</span>
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Login",
});
</script>
