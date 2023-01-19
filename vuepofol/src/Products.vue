<template>

<div class="black-bg" v-if="openModal == true">
  <div class="white-bg">
    <h4>{{oneroomData[0].title}}</h4>
    <p>{{oneroomData[0].content}}</p>
    <p>{{oneroomData[0].price}}</p>
    <button @click="openModal = false">닫기</button>
  </div>
</div>
<div class="black-bg" v-if="openModal1 == true">
  <div class="white-bg">
    <h4>{{oneroomData[1].title}}</h4>
    <p>{{oneroomData[1].content}}</p>
    <p>{{oneroomData[1].price}}</p>
    <button @click="openModal1 = false">닫기</button>
  </div>
</div>
<div class="black-bg" v-if="openModal2 == true">
  <div class="white-bg">
    <h4>{{oneroomData[2].title}}</h4>
    <p>{{oneroomData[2].content}}</p>
    <p>{{oneroomData[2].price}}</p>
    <button @click="openModal2 = false">닫기</button>
  </div>
</div>
<div class="black-bg" v-if="openModal3 == true">
  <div class="white-bg">
    <h4>{{oneroomData[3].title}}</h4>
    <p>{{oneroomData[3].content}}</p>
    <p>{{oneroomData[3].price}}</p>
    <button @click="openModal3 = false">닫기</button>
  </div>
</div>
<div class="black-bg" v-if="openModal4 == true">
  <div class="white-bg">
    <h4>{{oneroomData[4].title}}</h4>
    <p>{{oneroomData[4].content}}</p>
    <p>{{oneroomData[4].price}}</p>
    <button @click="openModal4 = false">닫기</button>
  </div>
</div>
<div class="black-bg" v-if="openModal5 == true">
  <div class="white-bg">
    <h4>{{oneroomData[5].title}}</h4>
    <p>{{oneroomData[5].content}}</p>
    <p>{{oneroomData[5].price}}</p>
    <button @click="openModal5 = false">닫기</button>
  </div>
</div>

  
  <div class="menu">
    <!-- 변수 작명 2개 까지 가능
    - 왼쪽 변수는 array 내의 데이터
    - 오른쪽 변수는 1씩 증가하는 정수 -->
    <!-- <a v-for="menus in menus" :key="menus">{{menus}}</a> -->
    <a href="">Home</a>
    <a href="">Products</a>
    <a href="">About</a>
  </div>
  <div class="menulog">
      <a class="menulogin" style="font-size:10px">로그인</a> &nbsp;
      <a style="font-size:10px">|</a>&nbsp;
      <a class="menujoin" style="font-size:10px">회원가입</a>
  </div>

  <img src="./assets/homeImg.png" class="logoImg">
  <p class="logoTxt">원룸샵</p>
  <div>
  <!-- {{데이터바인딩}}
  -> JS 데이터를 HTML에 꽂아 넣는 문법  -->
  <!-- 1. HTML안 자체에 하드코딩을 해 놓으면 나중에 변경이 어렵다. -->
  <!-- 2. Vue의 실시간 자동 렌더링 기능 
          data를 변경하면 data와 관련된 HTML에도 실시간으로 반영됨 -->
    <img :src="oneroomData[0].image" class="room-img"><br><br>
    <button @click="openModal = true">{{oneroomData[0].title}}</button>
    <p>{{oneroomData[0].price}}</p>
    <!-- <button @click="신고수[0]++">허위매물신고</button> 
    <span>신고수 : {{신고수[0]}}</span> -->
  </div>
  <div>
    <img :src="oneroomData[1].image" class="room-img"><br><br>
    <button @click="openModal1 = true">{{oneroomData[1].title}}</button>
    <p>{{oneroomData[1].price}}</p>
  </div>
  <div>
    <img :src="oneroomData[2].image" class="room-img"><br><br>
    <button @click="openModal2 = true">{{oneroomData[2].title}}</button>
    <p>{{oneroomData[2].price}}</p>
  </div>
  <div>
    <img :src="oneroomData[3].image" class="room-img"><br><br>
    <button @click="openModal3 = true">{{oneroomData[3].title}}</button>
    <p>{{oneroomData[3].price}}</p>
  </div>
  <div>
    <img :src="oneroomData[4].image" class="room-img"><br><br>
    <button @click="openModal4 = true">{{oneroomData[4].title}}</button>
    <p>{{oneroomData[4].price}}</p>
  </div>
  <div>
    <img :src="oneroomData[5].image" class="room-img"><br><br>
    <button @click="openModal5 = true">{{oneroomData[5].title}}</button>
    <p>{{oneroomData[5].price}}</p>
  </div>
</template>

<script>
import oneroomData from './oneroom';


export default {
  name: 'App',
  data(){
    //데이터 보관함
    return {
      // 데이터는 object 자료로 저장
      //{자료이름:자료내용}
      oneroomData : oneroomData,
      openModal : false,
      openModal1 : false,
      openModal2 : false,
      openModal3 : false,
      openModal4 : false,
      openModal5 : false,
      price1 : 60,
      price2 : 70,
      price3 : 90,
      신고수: [0,0,0],
      // style1 : 'color : blue',
      products: ['역삼동원룸', '천호동원룸', '마포구원룸'],
    //   menus:['Home', 'Products', 'About'],
    }
  },
  // methods 는 함수 만드는 공간
  // method:{함수(){}} 안에 만들어야 한다.
  methods: {
    increase(){
      this.신고수 += 1;
    },
  },
  components :{

  }
}
</script>
<script src="/scripts/vue-router.js"></script>

<style>
body{
  margin: 0;
}
div{
  box-sizing: border-box;
}
.black-bg{
  width: 100%;
  /* height: 100%; */
  /* background: black; */
  position: fixed;
  padding: 20px;
}
.white-bg{
  width: 100%;
  background: rgb(255, 255, 255);
  border-radius: 8px;
  padding: 20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 30px;
}
.menulogin{
    font-weight: bold;

}
.menujoin{
    font-weight: bold;

}
.menulogin:hover{
  color: rgb(167, 167, 220);
  font-weight: bolder;
}
.menujoin:hover{
  color: rgb(167, 167, 220);
  font-weight: bolder;
}
.room-img{
  width: 100%;
  margin-top:40px ;
}
.logoImg{
  width: 100px;
  margin-top:20px ;
}
.logoTxt{
  font-weight: bolder;
  font-size: 20px;
  color: rgb(71, 71, 151);
}
.menu a:hover{
  color: rgb(167, 167, 220);
}

.aptTitlea:hover{
  color: rgb(29, 29, 232);
}

button {
    color: #444444;
    background: #F3F3F3;
    border: 1px #DADADA solid;
    padding: 5px 10px;
    border-radius: 2px;
    font-weight: bold;
    font-size: 9pt;
    outline: none;
}

button:hover {
    border: 1px #C6C6C6 solid;
    box-shadow: 1px 1px 1px #EAEAEA;
    color: #333333;
    background: #F7F7F7;
}

button:active {
    box-shadow: inset 1px 1px 1px #DFDFDF;   
}
</style>
