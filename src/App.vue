<template>
  <div>
    <account-ui></account-ui>
    <login-screen></login-screen>
    <subscription-pricing></subscription-pricing>
    <double-registration></double-registration>
    <project-board></project-board>
    <language-learn></language-learn>
    <on-boarding></on-boarding>
    <pro-profile></pro-profile>
    <select-account></select-account>
  </div>

 </template>
<script>
import onBoarding from './components/onBoarding.vue'
import ProProfile from './components/ProProfile.vue'
import selectAccount from './components/selectAccount.vue';
import languageLearn from './components/languageLearn.vue';
import DoubleRegistration from './components/DoubleRegistration.vue';
import projectBoard from "./components/projectBoard.vue";
import subscriptionPricing from './components/subscriptionPricing.vue';
import AccountUi from './components/AccountUi.vue';
import LoginScreen from './components/LoginScreen.vue';



export default {
  name: 'App',
  components: {
  onBoarding,
    ProProfile,
    selectAccount,
    DoubleRegistration,
    languageLearn, projectBoard,
    subscriptionPricing,
    AccountUi,
    LoginScreen
 
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background:#EDEFF7;
  padding-top:50px;
 
}

*{
  margin: 0;
}
</style>
