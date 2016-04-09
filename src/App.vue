<template>

  <div id="app">
    <demo1></demo1>
    <demo2></demo2>
    <demo3></demo3>
    <demo4></demo4>
    <demo5></demo5>
  </div>
</template>

<script>
  import demo1 from 'components/list/demo1'
  import demo2 from 'components/list/demo2'
  import demo3 from 'components/list/demo3'
  import demo4 from 'components/list/demo4'
  import demo5 from 'components/list/demo5'

  export default{
    components: {
      demo1,
      demo2,
      demo3,
      demo4,
      demo5
    }
  }

</script>

