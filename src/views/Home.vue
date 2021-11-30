<template>
  <v-col cols="10" lg="4" class="mx-auto">
    <v-card>
      <v-app-bar dark color="blue darken-3">
        <v-toolbar-title>Login Form</v-toolbar-title>
      </v-app-bar>

      <v-form ref="form" @submit.prevent="submit">
        <v-card-text>
          <v-text-field
            v-model="email"
            :rules="emailRules"
            type="email"
            label="Email"
            placeholder="Email"
            prepend-inner-icon="mdi-account"
            required
          />
          <v-text-field
            type="password"
            label="Password"
            placeholder="Password"
            prepend-inner-icon="mdi-key"
            required
          />
        </v-card-text>
        <v-card-actions class="justify-end">
          <v-btn type="submit" color="blue darken-3" @click="validate">
            <span class="white--text px-8">Login</span>
          </v-btn>
        </v-card-actions>
      </v-form>
    </v-card>
  </v-col>
</template>
