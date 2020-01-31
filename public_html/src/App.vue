<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">{{ $t("homeLink") }}</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/trade-room">Trade Room</router-link>
      <router-link to="/registration">Registration</router-link>
      <router-link to="/education">Education</router-link>
      <router-link to="/quotes">Quotes</router-link>
      <a @click="setLocale('ua')" href="#">
      <flag class="locale" iso="ru"></flag>
      </a>
      <a @click="setLocale('ua')" href="#">
      <flag class="locale" iso="en"></flag>
      </a>
      {{$t("message")}}

    </div>
    <router-view />


  </div>
</template>

<script>
  import Vue from 'vue'
  import CountryFlag from 'vue-country-flag'

  Vue.component('country-flag', CountryFlag)
import "./less/app.less";
export default {
  name: "app",
  methods: {
    setLocale(locale) {
      this.$i18n.locale = locale;
    }
  }
};
</script>
