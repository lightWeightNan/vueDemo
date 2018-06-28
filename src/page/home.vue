<template>
  <div class="home-page">
    <v-header></v-header>
<!--     <ul class="nav">
       <li>
         <img src="../assets/page1.png">
         <span>前端开发</span>
       </li>
       <li>
         <img src="../assets/page2.png">
         <span>后端开发</span>
       </li>
       <li>
         <img src="../assets/page3.png">
         <span>移动开发</span>
       </li>
       <li>
         <img src="../assets/page4.png">
         <span>数据库</span>
       </li>
       <li>
         <img src="../assets/page5.png">
         <span>云计算</span>
       </li> 
    </ul> -->
        <ul class="nav">
           <li v-for="item in arrList">
             <img :src="item.imgUrl">
             <span>{{item.name}}</span>
           </li>
         </ul>
         <v-course :arrList="array"></v-course>
         <v-footer></v-footer>
  </div>
</template>

<script>
import Header from "@/components/header/"
import webImg from "@/assets/page1.png"
import webImg2 from "@/assets/page2.png"
import webImg3 from "@/assets/page3.png"
import webImg4 from "@/assets/page4.png"
import webImg5 from "@/assets/page5.png"
import course from "@/components/course/"

import course1 from "@/assets/course1.jpg"
import course2 from "@/assets/course2.jpg"
import course3 from "@/assets/course3.jpg"
import course4 from "@/assets/course4.jpg"
import course5 from "@/assets/course5.jpg"
import footer from "@/components/footer/"

export default {
  components:{
    'v-header':Header,
    'v-course':course,
    'v-footer':footer
  },
  data () {
    return {
        arrList:[],
        array:[]
    }
  },
  mounted(){
    this.arrList=[{
      imgUrl:webImg,
      name:'前端开发'
    },
     {
      imgUrl:webImg2,
      name:'后端开发'
     },
     {
      imgUrl:webImg3,
      name:'移动开发'
     },
     {
      imgUrl:webImg4,
      name:'数据库'
     },
     {
      imgUrl:webImg5,
      name:'云计算'
     }
    ];
    this.array=[
       {
         imgUrl:course1,
         title:'实例妙解Sed和Awk的秘密',
         msg:'中级.330在学'
       },
       {
         imgUrl:course2,
         title:'实例妙解Sed和Awk的秘密实例妙解Sed和Awk的秘密',
         msg:'中级.330在学'
       },
       {
         imgUrl:course3,
         title:'实例妙解Sed和Awk的秘密',
         msg:'中级.330在学'
       },
       {
         imgUrl:course4,
         title:'实例妙解Sed和Awk的秘密',
         msg:'中级.330在学'
       },
       {
         imgUrl:course5,
         title:'实例妙解Sed和Awk的秘密',
         msg:'中级.330在学'
       },
       {
         imgUrl:course1,
         title:'实例妙解Sed和Awk的秘密',
         msg:'中级.330在学'
       }     
    ]
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home-page .nav{
  height: 100PX;
  padding-top: 44PX;
  background: #f3f5f7;
  overflow-x: scroll;
  white-space: normal;
  font-size: 0;

}
.nav li{
  width: 88px;
  display: inline-block;
  text-align: center;
  font-size: 14px;
}
.nav li img{
  display: block;
  width: 32px;
  margin: 20px auto 12px;
}

</style>
