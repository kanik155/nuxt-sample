<template>
  <div>
    <ex-header />
    <nuxt />
    <ex-footer />
  </div>
</template>

<script>
import ExHeader from "~/components/SampleHeader.vue";
import ExFooter from "~/components/SampleFooter.vue";

export default {
  name: "sample",
  components: {
    ExHeader,
    ExFooter
  }
};
</script>