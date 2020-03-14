<template>
  <v-content>
      <div class="text-center">
        <v-pagination
          v-model="page"
          :length="6"
          @input="pageChange"
        ></v-pagination>
      </div>     
    </v-content>
</template>

<script>
export default {
  name: 'Pagenation',
  data () {
    return {
      page: 1,
      length:0,
      lists: [],
      displayLists: [],
      pageSize: 10,
    }
  },

  mounted: function(){
    this.lists = new Array(99).fill().map((v,i)=> {
      return { id : i,title : 'Title' + i };
    });
  },

  methods: {
    pageChange: function(pageChange) {
      this.displayLists = this.lists.slice(this.pageSize*(pageNumber -1), this.pageSize*(pageNumber));
    }
  }
}
</script>

<style>

</style>