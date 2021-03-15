<template>
  <div class="container HouseDTHeader" >
    <div class="extraBG" v-bind:style="{backgroundColor: NavBgColor}">
      <div class="row navBar" > 
        <div class="col-2">
          <router-link to="/"><span>Migratory Bird</span></router-link>
        </div>
        <div class="col-5"></div>
        <div class="col-1">
          <span class="find">Find</span>
        </div>
        <div class="col-1">
          <span>Need</span>
        </div>
        <div class="col-1">
          <span>Comunity</span>
        </div>
        <div class="col-1">
          <span>About</span>
        </div>
        <div class="col-1">
          <div class="profilepic" @click="show_hiddenNav"></div>
          <div class="infoDot" v-if="isShowInfoDot"></div>
        </div>
      </div>
    </div>
    <div class="hidden_nav" v-show="isShow_hiddenNav">
      <a href="http://" v-on:click="show_hiddenNav">Profile</a> <br />
      <a href="http://">My Nest</a> <br />
      <a href="http://">Like</a> <br />
      <a href="http://">LFR</a> <br />
      <a href="http://">In Box</a> <br />
      <div class="infoDot_inBox" v-if="isShowInfoDot"></div>
    </div>
  </div>
</template>

<script>
'use strict'
export default {
  name: "HouseDTHeaderer",

  data() {
    return {
      isShow_hiddenNav: false,
      isShowInfoDot: false,
      NavBgColor: '',
      navHeight: '',
    };
  },
  mounted () {//给window添加一个滚动滚动监听事件
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    show_hiddenNav: function() {
      this.isShow_hiddenNav = !this.isShow_hiddenNav;
    },
    handleScroll: function(){
      var scrollFromTop = window.pageYOffset|| document.documentElement.scrollTop || document.body.scrollTop;
      // console.log(scrollFromTop)
      if (scrollFromTop < 100){
        this.NavBgColor = 'transparent';
      }else{
        // this.NavBgColor = '#CFDDD6';
        this.NavBgColor = '#a6b6ae';
        this.navHeight = 70+'px';
      }
    },
  },
  beforedestroyed () { //离开该页面前需要移除这个监听的事件
    window.removeEventListener('scroll', this.handleScroll)
  },
}
</script>

<style lang="scss" scoped>
@mixin size($w, $h) {
  width: $w;
  height: $h;
}
$font_basic_size: 10px;
$color_white: #ffffff;
$color_black: #000;
$color_darkWhite: #e8e8e8;
$color_darkBrown: #75572e;
$color_darkGreen: #666b46;
$color_tagColor: #a6b6ae;

* {
  font-family: 微軟正黑體;
  position: relative;
  box-sizing: border-box;
}
// .HouseDTHeader{
//   border: 1px solid yellow;
// }
.extraBG{
  @include size($w: 100vw, $h: 50px);
  position: fixed;
  z-index: 1;
  left: 0px;
  display: flex;
  justify-content: center;
}
.navBar {
  @include size($w: 1140px, $h: 50px);
  // @include size($w: 100vw, $h: 50px);
  //to make navbar align to the left
  // left: 0px; 
  overflow: hidden;
  border-radius: 5px;
  position: fixed;
  // z-index: 1;
  transition-duration: 0.4s;
  div {
    display: flex;
    justify-content: center;
    align-items: center;
    .find {
      font-size: $font_basic_size * 2;
    }
    .profilepic {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      display: flex;
      background-color: $color_darkGreen;
      cursor: pointer;
      position: relative;
      z-index: 2;
    }
    .infoDot{
      @include size($w: 10px,$h: 10px);
      border-radius: 50%;
      background-color: #FA8937;
      z-index: 2;
      transform: translateX(-80%) translateY(-100%);
    }
  }
  span {
    color: $color_white;
  }
}
.hidden_nav {
  @include size($w: 100px, $h: auto);
  position: fixed;
  z-index: 1;
  background-color: $color_darkWhite;
  border: 1px solid #A6B6AE;
  border-radius: 10px;
  text-align: left;
  padding: 10px 10px 10px 17px;
  left: 100%;
  transform: translateX(-160%) translateY(25%);
  a {
    color: #7E7E7E;
  }
  .infoDot_inBox{
    @include size($w: 10px,$h: 10px);
    border-radius: 50%;
    background-color: #FA8937;
    position: absolute;
    left:60%;
    top: 77%
  }
}
</style>
