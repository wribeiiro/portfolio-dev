<template>
  <v-footer app absolute class="footer">
    <v-col class="text-center" cols="12">
      <span>
        © {{ new Date().getFullYear() }} feito com <v-icon size="18" color="red">mdi-heart</v-icon> Wellisson Ribeiro
      </span>
    </v-col>
  </v-footer>
</template>

<script>
  export default {};
</script>

<style lang="scss">
  .footer {
    background-color: #7159c1 !important;

    span {
      color: #fff;
    }
  }
</style>