<template>
  <div>
    <h2>1. Text</h2>
    <div class="content">
      <span>Message is: {{ message }}</span>
      <br>
      <input type="text" v-model="message" placeholder="edit me">

    </div>
    <h2>2. CheckBox</h2>
    <div class="content">
      <label>做出选择吧</label>
      <input type="checkbox" v-model="checked" id="checkbox">
      <label for="checkbox">{{checked}}</label>
    </div>
    <h2>3. 多个勾选框，绑定到同一个数组：</h2>
    <div class="content">
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
      <label for="jack">Jack</label>
      <input type="checkbox" id="john" value="John" v-model="checkedNames">
      <label for="john">John</label>
      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
      <label for="mike">Mike</label>
      <br>
      <span>Checked names: {{ checkedNames | json }}</span>
    </div>
    <h2>4. 单选框</h2>
    <div class="content">
      <input type="radio" id="one" value="one" v-model="picked" checked>
      <label for="one">one</label>
      <input type="radio" id="two" value="two" v-model="picked">
      <label for="two">two</label>
      <br>
      <span>Picked:{{picked}}</span>
    </div>

    <h2>5. select 单选</h2>
    <div class="content">
      <select v-model="selected">
        <option selected id="A" value="A">A</option>
        <option id="B" value="V">B</option>
        <option id="C" value="C">C</option>
      </select>
      <span>Selected: {{ selected }}</span>
    </div>
    <h2>6. select 多选</h2>
    <div class="content">
      <select v-model="selected1" multiple>
        <option selected>A</option>
        <option>B</option>
        <option>C</option>
      </select>
      <span>Selected:{{selected1 | json}}</span>
    </div>
    <h2>动态选项，用 v-for 渲染：</h2>
    <div class="content">
      <select v-model="selected2">
        <option v-for="option in options" v-bind:value="option.value">
          {{option.text}}
        </option>
      </select>
      <span>Selected:{{selected2}}</span>
    </div>
  </div>
</template>

<script>
  export default{
    data () {
      return {
        checked: true,
        checkedNames: [],
        picked: 'one',
        selected: 'A',
        options: [
          {text: 'one', value: 'one'},
          {text: 'two', value: 'two'},
          {text: 'three', value: 'three'}
        ],
        selected2: 'two'
      }
    }
  }
</script>
<style>
  h2 {
    margin: 10px;
  }

  .content {
    padding: 10px;
  }
</style>

