<template>
  <v-ons-navigator :page-stack="pageStack">
    <component :is="page" v-for="page in pageStack" :page-stack="pageStack"></component>
  </v-ons-navigator>
</template>

<script>
  import signin from './signin';
  import signup from './signup';

  export default {
    data() {
      return {
        pageStack: [signin]
      }
    }
  }
</script>
