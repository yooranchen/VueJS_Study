<template>
  <div id="forms">
    <demo1></demo1>
    <demo2></demo2>
  </div>
</template>

<script>
  import demo1 from 'components/form/form1.vue'
  import demo2 from 'components/form/form2.vue'

  export default{
    components: {
      demo1,
      demo2
    }
  }
</script>
