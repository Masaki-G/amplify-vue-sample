<script setup>
import { Authenticator } from "@aws-amplify/ui-vue";
import "@aws-amplify/ui-vue/styles.css";
import { I18n } from "aws-amplify";
import { translations } from "@aws-amplify/ui-vue";
I18n.putVocabularies(translations);
I18n.setLanguage("ja");

const formFields = {

};
</script>
<template>
  <authenticator
    :form-fields="formFields"
    :sign-up-attributes="signUpAttributes"
  >
    <template v-slot="{ user, signOut }">
      <h1>Hello {{ user.username }}!</h1>
      <button @click="signOut">Sign Out</button>
    </template>
  </authenticator>
</template>
