<template>
  <div>
    <h1>{{ getTitle }}</h1>
    <button @click="setTitleViaApi">
      Set title via API
    </button>
    <button @click="resetTitle">
      Reset title
    </button>
  </div>
</template>

<script>

import { mapGetters, mapActions } from "vuex";

export default {
  components: {
  },
   computed: {
    ...mapGetters(["getTitle"])
  },
  methods: {
    ...mapActions([
      "setTitleViaApi",
      "resetTitle"
    ]),
  },
};
</script>

<style scope>

</style>
