<script>
export default {
  components: {},
  props: {
    infoList: {
      type: Object,
      required: true
    }
  },
  data: () => {
    return {
     
    };
  },
  methods: {
    showInfo(){
        
    }
  }
};
</script>

<template>
  <button class="btn-success" @click="showInfo()">Show</button>
</template>

<style scoped>
  button{
    border-radius: 10px;
  }
</style>