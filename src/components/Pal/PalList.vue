<template>
  <div class="list">
    <breadcrumb></breadcrumb>
    <search></search>
    <pal-item></pal-item>
  </div>
</template>

<script>
import Search from "./Search";
import PalItem from "./PalItem";
import Breadcrumb from "~/components/Breadcrumb";

export default {
  name: 'PalList',
  components: {
    Breadcrumb,
    Search,
    PalItem,
  },
  beforeRouteLeave(to, form, next) {
    this.$store.state.palSearchName = ""
    this.$store.state.attributeId = 0
    next()
  }
}
</script>
