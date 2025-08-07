<script setup lang="ts">
import { ref } from 'vue'

const email = ref('admin@admin.com')
const password = ref('admin')
const loading = ref(false)

const handleLogin = () => {
  loading.value = true
  setTimeout(() => {
    loading.value = false
    console.log('Login attempt:', { email: email.value, password: password.value })
  }, 1000)
}
</script>

<template>
  <v-container fluid class="login-page pa-0">
    <v-row no-gutters class="fill-height d-flex align-center justify-center">
      <v-col cols="12" class="d-flex align-center justify-center">
        <div class="login-container">
          <!-- Section gauche - Formulaire de connexion -->
          <div class="login-section">
            <!-- Header avec logo -->
            <div class="header">
              <div class="logo">
                <div class="logo-icon">
                  <svg width="35" height="35" viewBox="0 0 35 35" fill="none">
                    <path
                      d="M17.5 0C7.84 0 0 7.84 0 17.5S7.84 35 17.5 35 35 27.16 35 17.5 27.16 0 17.5 0zm0 32.5C9.28 32.5 2.5 25.72 2.5 17.5S9.28 2.5 17.5 2.5 32.5 9.28 32.5 17.5 25.72 32.5 17.5 32.5z"
                      fill="#0d9394"
                    />
                    <path
                      d="M17.5 8.75c-4.83 0-8.75 3.92-8.75 8.75s3.92 8.75 8.75 8.75 8.75-3.92 8.75-8.75-3.92-8.75-8.75-8.75zm0 15c-3.45 0-6.25-2.8-6.25-6.25s2.8-6.25 6.25-6.25 6.25 2.8 6.25 6.25-2.8 6.25-6.25 6.25z"
                      fill="#0d9394"
                    />
                  </svg>
                </div>
                <span class="logo-text">PrimeDash</span>
              </div>
            </div>

            <!-- Titre et sous-titre -->
            <div class="title-section">
              <h1 class="title">Sign in</h1>
              <p class="subtitle">To access template</p>
            </div>

            <!-- Alert avec credentials -->
            <div class="credentials-alert">
              <p class="alert-text">
                <strong>Email:</strong> admin@admin.com<br />
                <strong>Password:</strong> admin
              </p>
            </div>

            <!-- Formulaire -->
            <div class="form-section">
              <div class="input-field">
                <label class="input-label">Email</label>
                <input v-model="email" type="email" class="input" placeholder="admin@admin.com" />
              </div>

              <button @click="handleLogin" :disabled="loading" class="next-button">
                <span v-if="!loading">Next</span>
                <span v-else>Loading...</span>
              </button>
            </div>

            <!-- Séparateur -->
            <div class="separator">
              <div class="separator-line"></div>
              <span class="separator-text">OR</span>
              <div class="separator-line"></div>
            </div>

            <!-- Boutons sociaux -->
            <div class="social-buttons">
              <button class="social-btn google">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                  <path
                    d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"
                    fill="#4285F4"
                  />
                  <path
                    d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"
                    fill="#34A853"
                  />
                  <path
                    d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"
                    fill="#FBBC05"
                  />
                  <path
                    d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"
                    fill="#EA4335"
                  />
                </svg>
              </button>
              <button class="social-btn facebook">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                  <path
                    d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"
                    fill="#1877F2"
                  />
                </svg>
              </button>
              <button class="social-btn twitter">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                  <path
                    d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"
                    fill="#1DA1F2"
                  />
                </svg>
              </button>
              <button class="social-btn linkedin">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                  <path
                    d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"
                    fill="#0077B5"
                  />
                </svg>
              </button>
            </div>
          </div>

          <!-- Section droite - Inscription -->
          <div class="register-section">
            <div class="register-content">
              <div class="register-image">
                <img
                  src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80"
                  alt="Working desk with laptop"
                />
              </div>

              <h2 class="register-title">Not Register yet?</h2>
              <p class="register-description">
                Lost access to OneAuth? Worry not. Set up passphrase and backup number to recover
                OneAuth easily.
              </p>

              <button class="register-button">
                <span>Register</span>
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none">
                  <path
                    d="M9 0C4.03 0 0 4.03 0 9s4.03 9 9 9 9-4.03 9-9-4.03-9-9-9zm0 16.2C5.02 16.2 1.8 12.98 1.8 9S5.02 1.8 9 1.8 16.2 5.02 16.2 9 12.98 16.2 9 16.2z"
                    fill="#0d9394"
                  />
                  <path
                    d="M9 4.5c-2.48 0-4.5 2.02-4.5 4.5s2.02 4.5 4.5 4.5 4.5-2.02 4.5-4.5-2.02-4.5-4.5-4.5zm0 7.2c-1.49 0-2.7-1.21-2.7-2.7s1.21-2.7 2.7-2.7 2.7 1.21 2.7 2.7-1.21 2.7-2.7 2.7z"
                    fill="#0d9394"
                  />
                </svg>
              </button>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.login-page {
  min-height: 100vh;
  background: #f9fafb;
  width: 100%;
  display: flex;
  align-items: center; /* center vertically */
  justify-content: center; /* center horizontally */
  padding: 16px; /* mobile breathing space */
}

.login-container {
  display: flex;
  width: 90%;
  max-width: 900px;
  background: white;
  border-radius: 10px;
  box-shadow:
    0px 3px 1px -2px rgba(145, 158, 171, 0.2),
    0px 2px 2px 0px rgba(145, 158, 171, 0.14),
    0px 1px 5px 0px rgba(145, 158, 171, 0.12);
  overflow: hidden;
  min-height: 528px;
}

/* Section gauche */
.login-section {
  flex: 1;
  padding: 32px;
  max-width: 400px;
  display: flex;
  flex-direction: column;
}

.header {
  margin-bottom: 24px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 8px;
}

.logo-icon {
  width: 35px;
  height: 35px;
}

.logo-text {
  font-family: 'Public Sans', sans-serif;
  font-weight: 700;
  font-size: 24px;
  line-height: 36px;
  color: #0d9394;
}

.title-section {
  margin-bottom: 24px;
}

.title {
  font-family: 'Public Sans', sans-serif;
  font-weight: 500;
  font-size: 18px;
  line-height: 28px;
  color: rgba(33, 43, 54, 0.87);
  margin: 0 0 4px 0;
}

.subtitle {
  font-family: 'Public Sans', sans-serif;
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  color: rgba(33, 43, 54, 0.87);
  opacity: 0.6;
  margin: 0;
}

.credentials-alert {
  background: rgba(0, 184, 217, 0.12);
  border-radius: 8px;
  padding: 14px 16px;
  margin-bottom: 24px;
}

.alert-text {
  font-family: 'Public Sans', sans-serif;
  font-size: 14px;
  line-height: 22px;
  color: #00b8d9;
  margin: 0;
}

.alert-text strong {
  font-weight: 700;
}

.form-section {
  margin-bottom: 24px;
}

.input-field {
  margin-bottom: 24px;
}

.input-label {
  display: block;
  font-family: 'Public Sans', sans-serif;
  font-weight: 400;
  font-size: 12px;
  line-height: 18px;
  color: rgba(33, 43, 54, 0.87);
  margin-bottom: 8px;
}

.input {
  width: 100%;
  height: 40px;
  padding: 8px 16px;
  border: 1px solid rgba(33, 43, 54, 0.22);
  border-radius: 8px;
  font-family: 'Public Sans', sans-serif;
  font-size: 16px;
  line-height: 24px;
  color: rgba(33, 43, 54, 0.87);
  background: white;
  outline: none;
  transition: border-color 0.3s;
}

.input:focus {
  border-color: #0d9394;
}

.next-button {
  width: 100%;
  height: 36px;
  background: #0d9394;
  color: white;
  border: none;
  border-radius: 8px;
  font-family: 'Public Sans', sans-serif;
  font-weight: 500;
  font-size: 14px;
  cursor: pointer;
  transition: background-color 0.3s;
  box-shadow:
    0px 3px 1px -2px rgba(145, 158, 171, 0.2),
    0px 2px 2px 0px rgba(145, 158, 171, 0.14),
    0px 1px 5px 0px rgba(145, 158, 171, 0.12);
}

.next-button:hover {
  background: #0a7a7b;
}

.next-button:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}

.separator {
  display: flex;
  align-items: center;
  margin: 24px 0;
  gap: 12px;
}

.separator-line {
  flex: 1;
  height: 1px;
  background: rgba(145, 158, 171, 0.24);
}

.separator-text {
  font-family: 'Public Sans', sans-serif;
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  color: rgba(33, 43, 54, 0.87);
  white-space: nowrap;
}

.social-buttons {
  display: flex;
  justify-content: center;
  gap: 16px;
}

.social-btn {
  width: 40px;
  height: 40px;
  border-radius: 20px;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition:
    transform 0.3s,
    box-shadow 0.3s;
}

.social-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.google {
  background: #0d9394;
}

.facebook {
  background: #00b8d9;
}

.twitter {
  background: rgba(33, 43, 54, 0.87);
}

.linkedin {
  background: #ff5630;
}

/* Section droite */
.register-section {
  flex: 1;
  background: white;
  padding: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-left: 1px solid rgba(145, 158, 171, 0.06);
  max-width: 400px;
}

.register-content {
  text-align: center;
  width: 100%;
  max-width: 200px;
}

.register-image {
  margin-bottom: 24px;
}

.register-image img {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 8px;
}

.register-title {
  font-family: 'Public Sans', sans-serif;
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  color: rgba(33, 43, 54, 0.87);
  margin: 0 0 12px 0;
}

.register-description {
  font-family: 'Public Sans', sans-serif;
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  color: rgba(33, 43, 54, 0.87);
  margin: 0 0 16px 0;
}

.register-button {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 9px 19px;
  background: white;
  border: 1px solid #0d9394;
  border-radius: 8px;
  color: #0d9394;
  font-family: 'Public Sans', sans-serif;
  font-weight: 500;
  font-size: 14px;
  cursor: pointer;
  transition: all 0.3s;
}

.register-button:hover {
  background: #0d9394;
  color: white;
}

/* Responsive */
@media (max-width: 768px) {
  .login-container {
    width: 90%;
    max-width: 500px;
    flex-direction: column;
  }

  .login-section,
  .register-section {
    max-width: none;
    padding: 24px;
  }

  .register-image img {
    width: 100%;
    max-width: 200px;
  }
}
</style>
