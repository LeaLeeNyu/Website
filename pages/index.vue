
<template>
  <body class ="index">
  <div class = "main">

    <h1>👋Hello! This is Lea.</h1>
    <h1>👩‍💻An Interactive Designer &</h1>
    <h1>👩‍🎤A Creative Technologist</h1>

    <div class = "button">
    <div><Button type="outline" text="Game" @click.native="goToGame" /></div>
    <div><Button type="outline" text="UX" @click.native="goToUX" /></div>
    <div><Button type="outline" text="Side Work" @click.native="goToSidework" /></div>
    <div><Button type="outline" text="Contect Me :)" @click.native="btnClick"/></div>
  </div>
  </div>
  </body>
</template>


<script>

export default {
  
  name: "components",
  methods: {
   goToGame(){
   this.$router.push('/projects'); },
   goToUX(){
   this.$router.push('/UX'); },
   goToSidework(){
   this.$router.push('/Sidework'); },
   btnClick: function(event) {
   window.open("https://www.instagram.com/lea_artworks/");
  },
  },

};
</script>

<style scoped lang="scss">
$blue:#2828cd;
$white:#ffff;
$black:#000000;
$yellow:#ffd900;

.index{
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top:80px;
  background-color: #020287;
}

.main{
  h1{
    color:$white;
    line-height:28px;
   
  }
  h3{
    color:white;
    font-family:'Courier New', Courier, monospace;
  }
  .button{
  display: flex;
  justify-content: center;
  align-items: center;
  }
}


</style>>



