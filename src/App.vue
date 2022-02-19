<template>
  <!-- codevolution 1-15 -->
  <!-- <div>
  <h1>{{greet}} {{name}}</h1>
  <h1 v-text="channel"></h1>
  <button :disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined text</h2>
  <h2 class="underline" :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldOut ? 'sold-out' : 'new'">Sold out?</h2>
  <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 :class="[isPromoted  && 'promoted', isSoldOut ? 'sold-out' : 'new']">Array Conditional movie</h2>
  <h2 
    :class ="{
      promoted : isPromoted,
      new: !isSoldOut, 
      'sold-out' : isSoldOut, 
    }"
  >
    Object Conditional Movie
  </h2>
  <h2 :class="'promoted new'">testing</h2>
  </div>
  codevolution 10 - 15 -
  <div>
    <h2 v-if="num === 0">The number is zero</h2>
    <h2 v-else>the num is not zero</h2>
  </div>
  List rendering
  <div>
    <h2 v-for="(name, index) in names" :key="name">{{index}} {{name}}</h2>
  </div> -->
  <div>
  <h1> Normal method :  {{3 + 8 + 5}}</h1>
  <h1> Add method : {{add(5, 4, 3)}}</h1>
  <h1> Multiply method : {{multiply(10)}} </h1>
  <button v-on:click="changeName">Change name</button>
  <h1> {{name}} </h1>
  <!-- counter -->
  <h1> {{counter}} </h1>
  <div>
    <button v-on:click="increment($event)">increment</button>
  <!-- decrement -->
  <button v-on:click="decrement">decrement</button>
  </div>
  
  
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      name : "ishan",
      baseMultiplier : 5,
      counter : 0
      // codevolution 1-15
      // third code block
      // names : ['ishan','priyank', 'omeed', 'khs'],
      // second code block
      // num : 1,
      // first code block
      // greet: "hello",
      // name:"ishan",
      // channel:"spectro",
      // isDisabled : false,
      // status : "danger",
      // isPromoted : true,
      // isSoldOut : true,
    }
  }, 
  methods: {
    changeName(event){
      this.name = "Batman"
      console.log('Event', event);
    },
    add(a, b, c){
      return a + b + c
    },
    multiply(num){
      return num*this.baseMultiplier
    },
    increment(event){
      this.counter += 1;
      console.log('Event', event);
    },
    decrement(){
      this.counter -= 1;
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline{
  text-decoration: #2c3e50 underline;
}

.promoted{
  font-style: italic;
}

.new{
  color: green;
}

.sold-out{
  color: red;
}
</style>
