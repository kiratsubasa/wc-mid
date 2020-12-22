<template lang="pug">
  #app
    el-button(type="primary") 我是按鈕!!!!
    .pageContainer
      .boxFlex
        .box
        .box
      .innerContainer
        img.pageName(alt="page name" src="./assets/pageName.png")
        .menu.drop-down-menu
          //-   router-link(to="/") Home |
          //-   router-link(to="/about") About
          //- router-view
          ul.menuItem(v-for="items in menuList") {{items.menuTitle}}
            li.menuOption(v-for="option in items.menu") {{option}}
          .scholarship {{scholarship}}
        router-view
      .boxFlex
        .box
        .box
</template>
<script>
export default {
  data(){
    return{
      menuList:[
        {menuTitle: '清大藝術學院'},
        {menuTitle: 'HOME'},
        {menuTitle: 'NEWS'},
        {menuTitle: '招生',menu: ['〝春之清華〞卓越獎學金 5名','學士班 FB粉絲頁']},
        {menuTitle: '學士班',menu:['學士班簡介','學士班課程']},
        {menuTitle: '師資',menu: ['學士班師資','藝設系師資']},
        {menuTitle: '科藝賞析' ,menu: ['數位文創作品','互動藝術作品']},
        {menuTitle: 'CON.'}
      ],
      scholarship: '〝春之清華〞卓越獎學金',
    }
  }
}
</script>
<style lang="sass">
html
  width: 1920px
  padding: 0px
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: left
  color: #C7A10D
  background-color: #801313
  width: 1920px
  // height: 1000px
  padding: 15px
.pageContainer
  border: 1px solid #C7A10D
  padding: 15px
.boxFlex
  width: 100%
  height: 50px
  display: flex
  flex-direction: row
  justify-content: space-between
.box
  width: 50px
  height: 50px
  background-color: #C7A10D
.innerContainer
  width: 1790px
  // height: 200px
  border: 1px solid #C7A10D
  margin: auto
.pageName
  margin: 30px
.menu 
  // padding: 30px
  display: flex
  flex-direction: row
  flex-wrap: wrap
  justify-content: space-between
  padding: 0px 65px
.menuItem
  padding: 10px 20px
  border: 3px solid #C7A10D
  font-size: 40px
.scholarship
  padding: 10px 20px
  border: 3px solid #C7A10D
  font-size: 60px
  margin: auto
  margin-top: 40px
  margin-bottom: 40px
ul.drop-down-menu ul 
  border: #ccc 1px solid
  position: absolute
  z-index: 99
  left: -1px
  top: 100%
  min-width: 180px
    

ul.drop-down-menu ul li 
    border-bottom: #ccc 1px solid


ul.drop-down-menu ul li:last-child 
  border-bottom: none
  

ul.drop-down-menu ul ul  /*第三層以後的選單出現位置與第二層不同*/
  z-index: 999
  top: 10px
  left: 90%

ul.drop-down-menu ul  /*隱藏次選單*/
    display: none


ul.drop-down-menu li:hover > ul  /* 滑鼠滑入展開次選單*/
    display: block
  
    
#nav a 
  font-weight: bold
  color: #2c3e50


#nav a.router-link-exact-active 
  color: #42b983

</style>
