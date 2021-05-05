<template>
  <div>
    <!-- <h1>Hello {{animal}}</h1>
    <h2>원숭이는 {{food}}를 좋아합니다</h2>
    <input type="text" v-model="food" />
    <div v-html="alertMessage"></div> 
    <img v-bind:src="imageSource" alt="random"/>
    <a :href="naverUrl">{{food}}</a>
    <hr />
    <h2 v-bind:class="{ red: food==='apple','not-good':food==='rice'}">원숭이는 {{food}}를 좋아합니다</h2> -->
    <!-- <h2> 당신의 나이는 {{age}}입니다.</h2>
    <h3 v-if="age > 18">당신은 어른입니다.</h3>
    <h3 v-else-if="age > 13 && age <=18">당신은 청소년입니다.</h3>
    <h3 v-else>당신은 어린이입니다</h3>
  </div> -->
    <!-- <h2 v-if="display">(if)보입니다!!!</h2>
    <h2 v-show="display">(show)보입니다!!</h2>
    <h2 v-for="(animal, index) in animals" :key="index">{{animals}} -->
    <!-- <ul>
      <li v-for="(user,index) in users" :key="index">
        이름은 {{user.name}}이고 직업은 {{user.job}}
        <p v-for="item in user.skill" :key="item">{{user.skill}} </p>
      </li>
    </ul> -->
    <template v-for="(animal,index) in animals" :key="index">
      <h2 v-if="animal !=='monkey'">{{animal}} 인덱스는 :: {{index}}</h2>
    </template>
  </div>
    
</template>

<script>
export default {
  name: 'App',
  data() {
    return{
      age:10,
      display:false,
      animals:["monkey","rat","dog","lion","monkey"],
      users:[
        {name:'scalper',job:'developer',gender:'male'},
        {name:'john',job:'designer',gender:'male'},
        {name:'철수',job:'pm',gender:'female'}
      ]
    };
  }
  //   return {
  //     animal: "Monkey",
  //     food: "banana",
  //     imageSource:"https://placeimg.com/100/100/any",
  //     naverUrl:"https://naver.com",
  //   };
  // }
};
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
input{
  font-size:20;
}
.orange{
  color:orange;
}
.salmon{
  color:salmon
}
.not-good{
  text-decoration:line-through
}
.red{
  color:red
}
</style>
