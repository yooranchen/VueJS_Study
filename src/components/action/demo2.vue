<template>
  <div>
    <h1>事件修饰符</h1>
    <!-- 阻止单击事件冒泡 -->
    <a v-on:click.stop="doThis">连接1</a>
    <!-- 提交事件不再重载页面 -->
    <form v-on:submit.prevent="onSubmit">
    </form>
    <!-- 修饰符可以串联 -->
    <a v-on:click.stop.prevent="doThat">连接2</a>
    <!-- 只有修饰符 -->
    <form v-on:submit.prevent></form>
    <!-- 添加事件侦听器时使用 capture 模式 -->
    <div v-on:click.capture="doThis">...</div>

    <!-- 只当事件在该元素本身（而不是子元素）触发时触发回调 -->
    <div v-on:click.self="doThat">...</div>
  </div>
</template>
