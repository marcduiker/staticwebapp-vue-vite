<template>
  <div>
    <h1>{{ getTitle }}</h1>
    <button
      :disabled="!isDefaultTitle"
      @click="setTitleViaApi"
    >
      Set title via API
    </button>
    <button
      :disabled="isDefaultTitle"
      @click="resetTitle"
    >
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
    ...mapGetters([
        "getTitle",
        "isDefaultTitle"
      ])
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
