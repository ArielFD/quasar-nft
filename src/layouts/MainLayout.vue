<template>
  <q-layout>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    
  },

  setup() {

    return {

    };
  },
});
</script>


<style lang="sass">
.q-layout
   background-color:  hsl(217, 54%, 11%)
</style>