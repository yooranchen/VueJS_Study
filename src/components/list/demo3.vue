<template>
  <div>
    <h1>v-for 在template中,并动态添加</h1>
    <ul>
      <template v-for="item in items">
        <li>{{ item.msg }}</li>
      </template>
    </ul>
    <button class="btnPush" @click="btnPush"> 添加啦</button>
  </div>

</template>

<script>
  export default{
    data  () {
      return {
        items: [
          {msg: '哈哈'},
          {msg: '哈哈'},
          {msg: '哈哈'},
          {msg: '哈哈'}
        ]
      }
    },
    methods: {
      btnPush: function () {
        this.items.push({msg: '你好我..我是添加的'})
      }
    }
  }
</script>
