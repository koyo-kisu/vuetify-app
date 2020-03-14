<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="6" md="4" lg="3">
      <SaleGraph />
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3">
      <SaleGraph />
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3">
      <SaleGraph />
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3">
      <SaleGraph />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import SaleGraph from '../components/SaleGraph'

export default {
  components: {
    SaleGraph,
  },
  // breakpointの値を表示
  // 現在のサイズをtrueとして表示
  mounted(){
    console.log(this.$vuetify.breakpoint)
  }
};
</script>