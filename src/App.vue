<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <br>

    <input class="input" v-model="user_name" placeholder="名前を入力してください。">
    <p>name: {{ user_name }}</p>

    <input type="radio" id="male" value="male" v-model="gender">
    <label for="male">male</label>
    <input type="radio" id="female" value="female" v-model="gender">
    <label for="female">female</label>
    <br>
    <span>gender: {{ gender }}</span>
    <br><br>

    <select v-model="years">
      <option disabled value="">Please select years</option>
      <option>10's</option>
      <option>20's</option>
      <option>30's</option>
      <option>40's</option>
      <option>50's</option>
    </select>
    <br>
    <span>select years: {{ years }}</span>
    <br><br>

    <textarea v-model="other_message" placeholder="その他入力欄"></textarea>
    <p style="white-space: pre-line;">message:{{ other_message }}</p>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Vuejs input form',
      user_name: '',
      gender: [],
      years: [],
      other_message: ''
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
