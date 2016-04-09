<template>
  <div>
    <h1>v-if demo</h1>
    <div v-if="Math.random() >  0.5">
      数值大于0.5啦
    </div>
    <div v-else>
      数值小于0.5啦
    </div>
  </div>
</template>
