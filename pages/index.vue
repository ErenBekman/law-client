<template>
  <div>
    <Banner />
    <AllCustomComponents />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Küpçük Hukuk Bürosu",
      meta: [
        {
          hid: "description",
          name: "Küpçük Hukuk Bürosu",
          content: "Küpçük Hukuk Bürosu"
        }
      ]
    };
  },
  data() {
    return {};
  },
  components: {
    Banner: () => import("@/components/shared/lp-banner/Banner"),
    AllCustomComponents: () => import("@/components/custom/AllCustomComponents")
  }
};
</script>
