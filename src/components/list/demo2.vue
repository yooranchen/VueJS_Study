<template>
  <div>
    <h1>v-for demo</h1>
    <ul id="example-1">
      <li v-for="item of items">
        {{ item.message}} {{$index + 1 }} 个
      </li>
    </ul>
  </div>
</template>

<script>
  export default{
    data () {
      return {
        items: [
          {message: '这是第'},
          {message: '这是第'},
          {message: '这是第'},
          {message: '这是第'}
        ]
      }
    }
  }
</script>
