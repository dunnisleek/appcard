<template >
   
  <section :class="{dark:dark}">
    
    <button class="switcher" @click="toggleDark">Theme switcher</button>
   <HeaderCom/>
    <div class="wrapper">

   <svg xmlns="http://www.w3.org/2000/svg" class="box" display="flex" width="45" height="45" viewBox="0 0 24 24" stroke-width="2" stroke="white" fill="none" stroke-linecap="round" stroke-linejoin="round">
   <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
   <path d="M4 4m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2z"></path>
   <path d="M9 15v2"></path>
   <path d="M12 11v6"></path>
   <path d="M15 13v4"></path>
</svg>
   
 
    
    <h1>Untercom <span>APP</span></h1>
    <p>Convert your hottest leads</p>
   </div>
   <whiteSection :class="{light:dark}"/>
  
  <br />

  
  </section>
 
</template>
   
 <script setup>
import {ref} from 'vue';
//import HeaderCom from './components/HeaderCom'
import whiteSection from './components/whiteSection.vue'


      const dark = ref(true)
      const toggleDark = () =>{
        dark.value = !dark.value
      }
   
  



  // export default {
 
  //   name:'app',
  //   components:{whiteSection, HeaderCom},

  //   data(){
  //     return{
     
  //       mode:'dark',
       
      
  //     }
  //   },
    
  //   methods:{
  //     toggle(){
  //       if(this.mode === 'dark'){
  //         this.mode === 'light'
  //         console.log(this.mode)
  //       }else if(this.mode ==='light'){
  //         this.mode ='dark'
  //         console.log(this.mode)
  //       }else{
  //         this.mode ='dark'
  //       }
        
  //     },
    
      
  //   }
  // }

// </script>

<style>

p{
  color:#fff;
}
.box{
  margin: auto;
  display: flex;
}
body{
 
  margin: 0;
}
.switcher{
  position: absolute;
  right:72px;
  padding: 15px;
  border-radius: 5px ;
  border:1px solid blue;
  transition: all 0.3s linear;
  font-size:18px;
  
}
.switcher:hover{
  background: blue;
  color:#fff;
  transform: scaleX(1.2);
}


.dark{
  padding-top: 50px;
  background: #282828;
  position: absolute;
  left:0;
  right:0;
  top:0;
  bottom:0;
  
}
section{
  padding-top: 50px;
  position: absolute;
  left:0;
  right:0;
  top:0;
  bottom:0;
}
h1{
  color:#ffffff;
  text-align: center;
  font-size: 25px;
}
.wrapper{
  background: #3B81F6;
  width:350px;
  margin:0px auto 0px auto;
  height:30vh;
  padding-top: 20px;
 
}
h1 span{
  background: blue;
  padding: 10px;
  border-radius:5px ;
}
.wrapper p{
  color:#fff;
  text-align: center;
  padding-top: 15px;
}



</style>
