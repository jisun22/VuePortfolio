<template>

<!-- <div class="black-bg" v-if="openModal == true">
  <div class="white-bg">
    <h4>{{oneroomData[0].title}}</h4>
    <p>{{oneroomData[0].content}}</p>
    <p>{{oneroomData[0].price}}</p>
    <button @click="openModal = false">닫기</button>
  </div>
</div> -->
  <div class="menu">
    <!-- 변수 작명 2개 까지 가능
    - 왼쪽 변수는 array 내의 데이터
    - 오른쪽 변수는 1씩 증가하는 정수 -->
    <!-- <a v-for="menus in menus" :key="menus">{{menus}}</a> -->
    <a href="">Home</a>
    <a href="">Products</a>
    <a href="">About</a>
  </div>
  <section id="headerSec">
  <div class="menulog">
      <a class="menulogin" style="font-size:10px">로그인</a> &nbsp;
      <a style="font-size:10px">|</a>&nbsp;
      <a class="menujoin" style="font-size:10px">회원가입&nbsp;&nbsp;&nbsp;</a>
  </div><br>
  <div>
    <img src="./assets/homeImg.png" class="logoImg">
    <p class="logoTxt">원룸샵</p>
  </div>
    <div class="mainTxt">
      <p>어떤 방을 찾으세요?</p>
    </div>
    <div class="search">
      <input class="searchInput" type="text" placeholder="검색어 입력">
      <button class="searchButton">검색</button>
    </div>
  </section>
</template>

<script>
import oneroomData from './oneroom';
// import Products from '/Products.vue';
// import App from '/App.vue';
// import About from '/About.vue';


export default {
  name: 'App',
  data(){
    //데이터 보관함
    return {
      // 데이터는 object 자료로 저장
      //{자료이름:자료내용}
      oneroomData : oneroomData,

      // style1 : 'color : blue',
    //   menus:['Home', 'Products', 'About'],
    }
  },
  // methods 는 함수 만드는 공간
  // method:{함수(){}} 안에 만들어야 한다.
  // methods: {
  //   increase(){
  //     this.신고수 += 1;
  //   },
  // },
  // components :{

  // }
}
</script>


<style>
body{
  margin: 0;
}
a {
  text-decoration: none;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#headerSec{
  background: #2e5695;
}
.menu {
  background: darkslateblue;
  padding: 15px;
}
.menu a{
  color: white;
  padding: 30px;
}
.menulog{
  color: #F7F7F7;
  float: right;
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
.logoImg{
  width: 100px;
  margin-top:20px ;
}
.logoTxt{
  font-weight: bolder;
  font-size: 20px;
  color: rgb(210, 210, 212);
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
.search{
  height: 40px;
  width: 100%;
  border: 2px solid #1b5ac2;
  background: #ffffff;
}
.searchInput{
  font-size: 16px;
  /* width: 100%; */
  padding: 10px;
  border: 0px;
  outline: none;
  float: left;
}
.searchButton{
  width: 50px;
  height: 100%;
  border: 0px;
  background: #1b5ac2;
  outline: none;
  float: right;
  color: #ffffff;
}
.searchButton:hover{
  background: #14418a;
  transition: 0.7s;
}
/* .mainTxt{
  float: left;
} */
.mainTxt p{
  color: #ffffff;
  font-size:30px;
  font-weight:bolder;
}
</style>
