<template>
  <div>
    <h1>oncli 事件</h1>
    <button v-on:click="greet" name="greet">Greet</button>
    <button @click="say('hi')">say hi</button>
    <button @click="say('hello')">say hello</button>
    <button v-on:click="sayHi('hello!', $event)">Submit</button>
  </div>
</template>

<script>
  export default{
    methods: {
      greet: function (event) {
        // 方法内 `this` 指向 vm
        console.log('Hello ' + this.name + '!')
        // `event` 是原生 DOM 事件
        console.log(event.target.tagName)
      },
      say: function (msg) {
        alert(msg)
      },
      sayHi: function (msg, event) {
        // 现在我们可以访问原生事件对象
        event.preventDefault()
      }
    }
  }
</script>
