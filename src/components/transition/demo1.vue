<template>
  <div>
    <div class="content" v-if="show" :transition="transitionName">hello</div>
    <button @click="showHide">show or hide</button>
  </div>
</template>

<script>
  export default{
    data () {
      return {
        show: true,
        transitionName: 'fade'
      }
    },
    methods: {
      showHide: function () {
        this.show = !this.show
      }
    }
  }
</script>

<style>
  .content {
    padding: 20px;
    background-color: #0b97c4;
    width: 30%;
  }
</style>
