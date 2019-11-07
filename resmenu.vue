<template>
   <div class="potato-voting">
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" class="bg1">
          <u class="text">This is a page for potato voting.</u>
        </b-col>
        <b-col sm="6" class="bg2">
         
          <p class="text">Made by with Love By [Name]</p>
        </b-col>
      </b-row>
    </b-container>


 <b-container class="bg3">
    <b-row>
        <b-col sm="6" offset="4" class="img">
          <b-nav>
            <b-nav-item>
              <img src="https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/mashedPotato.jpg"  width="150" height="90" >
            </b-nav-item>
            <b-nav-item >
             <b-button variant="success" @click="likefnc+=1">Like</b-button>
            </b-nav-item>
            <b-nav-item disabled> <span class="text">  likes:{{likefnc}}</span></b-nav-item>
          </b-nav>
        </b-col>
      </b-row> 



      <b-row>
        <b-col sm="6" offset="4" class="img">
          <b-nav>
            <b-nav-item>
              <img src="https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/bakedPotato.jpeg"  width="150" height="90" >
            </b-nav-item>
            <b-nav-item >
             <b-button variant="danger" @click="dislikefun+=1">Dislike</b-button>
            </b-nav-item>
            <b-nav-item disabled> <span class="text">  Dislikes:{{dislikefun}}</span></b-nav-item>
          </b-nav>
        </b-col>
      </b-row> 


      <b-row> 
         <b-col sm="6" offset="5" class="potato-banner1">
          <b-nav>
           
            <b-nav-item >
             <b-button @click="reset" variant="warning">Reset</b-button>
            </b-nav-item>
            <b-nav-item disabled> <span class="text"> TotalClickes : {{likefnc + dislikefun}} </span> </b-nav-item>
          </b-nav>
        </b-col>
      </b-row> 

</b-container>

   </div>
    
</template>
<script>
export default {
    data(){
        return{
          likefnc:0,
            dislikefun:0,
        }
    },
    methods:{
        reset(){
            this.likefnc = 0,
            this.dislikefun=0
        }
    }
}
</script>

<style  scoped>
.bg1{
    background-image: url('http://www.gsfdcy.com/data/img/11/1232442-blue-wallpaper.png');
    height: 50vh;
    background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.bg2{
  background-image: url('https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/thumbs.png');  
height: 50vh;
    background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.bg3{
    background-image: url('https://wallpaperaccess.com/full/307203.jpg');
    height: 60vh;
}
.text{
    position: absolute;
    top: 100px;
    left: 60px;
    font-size: 30px;
    
    font-size: 25px;
}
.img{
    padding: 20px;
}
</style>
