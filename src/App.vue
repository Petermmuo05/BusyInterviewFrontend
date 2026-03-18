<script setup>
import { ref } from 'vue'
import heroImage from './assets/hero.png'

const showPassword = ref(false)
</script>

<template>
  <div class="page">
    <div class="card">
      <aside class="promo">
        <div class="brand">
          <img class="desktop-logo" src="/logoimg.png" alt="Team Achieve logo" />
        </div>

        <img class="promo-image" src="/loginimage.png" alt="Team Achieve community" />

        <div class="promo-caption">
          <div class="caption-title">Team Achieve</div>
          <div class="caption-sub">Your perfect solution for funding your desires</div>
        </div>
      </aside>

      <main class="form-area">
        <div class="form-shell">
          <div class="brand mobile-brand">
            <img class="logo-img" src="/logoimg.png" alt="Team Achieve logo" />
            <span class="brand-name">Team Achieve</span>
          </div>

          <h1>Welcome Back</h1>
          <p class="subtitle">Enter your email address and password to access your account.</p>

          <form class="login-form">
            <label class="field">
              <span class="label">Email Address <span class="req">*</span></span>
              <input type="email" placeholder="Enter your email" autocomplete="email" required />
            </label>

            <label class="field">
              <span class="label">Password <span class="req">*</span></span>
              <div class="input-wrap">
                <input
                  :type="showPassword ? 'text' : 'password'"
                  placeholder="Enter your password"
                  autocomplete="current-password"
                  required
                />
                <button
                  class="icon-btn"
                  type="button"
                  :aria-label="showPassword ? 'Hide password' : 'Show password'"
                  @click="showPassword = !showPassword"
                >
                  <svg v-if="showPassword" viewBox="0 0 24 24" aria-hidden="true">
                    <path
                      d="M3 3l18 18M10.58 10.58a3 3 0 004.24 4.24M9.88 5.1A10.94 10.94 0 0112 5c4.42 0 8.06 2.97 10 7-1 2.14-2.58 3.94-4.54 5.1M6.1 6.1C4.15 7.26 2.55 9.24 2 12c.76 2.06 2.17 3.87 4.06 5.12"
                    />
                  </svg>
                  <svg v-else viewBox="0 0 24 24" aria-hidden="true">
                    <path
                      d="M12 5c4.42 0 8.06 2.97 10 7-1.94 4.03-5.58 7-10 7S3.94 16.03 2 12c1.94-4.03 5.58-7 10-7zm0 3.5A3.5 3.5 0 1015.5 12 3.5 3.5 0 0012 8.5z"
                    />
                  </svg>
                </button>
              </div>
            </label>

            <div class="row">
              <label class="checkbox">
                <input type="checkbox" />
                <span>Remember me</span>
              </label>
              <a class="link" href="#">Forgot Password?</a>
            </div>

            <button class="primary" type="submit">Sign in</button>

            <p class="foot">
              Don't have an account? <a class="link" href="#">Sign up</a>
            </p>
          </form>
        </div>
      </main>
    </div>
  </div>
</template>
