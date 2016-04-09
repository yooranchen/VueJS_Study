<template>
  <div>
    <h1>对象 v-for</h1>
    <ul id="repeat-object" class="demo">
      <li v-for="(key, val) in object">
        {{ key }} : {{ val }}
      </li>
    </ul>
  </div>
</template>

<script>
  export default{
    data () {
      return {
        object: {
          FirstName: 'John',
          LastName: 'Doe',
          Age: 30
        }
      }
    }
  }
</script>
