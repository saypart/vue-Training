<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  
  <div class="menu">
     <a v-for=" a in 메뉴들" :key="a">{{a}}</a>
  </div>


  <div>
     <h4 v-for=" a,i in products" :key="a">{{a}}<br>
     <img src ="require(`@/assets/images/${image}`)">
     <img src = "./assets/room1.jpg"/>
     <p style="스타일">{{price[i]}} 만원</p>
     <button v-on:click="신고수[i]++">허위매물 신고</button>
     <span>신고수 : {{신고수[i]}}</span>
    </h4>
    </div>


  <!-- <div>
    <h4> {{products[0]}}</h4>
    <p style="스타일">{{price[0]}} 만원</p>  </div>
  <div>
    <h4> {{products[1]}}</h4>
    <p style="스타일">{{price[1]}} 만원</p>
  </div>
  <div>
    <h4> {{products[2]}}</h4>
    <p style="스타일">{{price[2]}} 만원</p>
  </div> -->

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'


export default {
  name: 'App',
  data(){
    return {
        image : ['room0.jpg','room1.jpg','room2.jpg'],
        신고수 : [0,0,0],
        메뉴들 : ['Home', 'Shop','About'],
        스타일 : 'color : blue',
        price : [50, 60, 40],
        products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸']
    }
  },
  methods: {
        increase(){
            this.신고수[0] += 1;
        }
    }
//   components: {
//     HelloWorld
//   }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
.menu{
    background: darkslateblue;
    padding: 15px;
    border-radius: 5px;
}

.menu a{
    color: white;
    padding: 10px;
}

</style>
