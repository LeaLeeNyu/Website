<template>
  <body class = "project">
    <div class="homepage">
      <div class = button><Button type="outline" text="Home" @click.native="goToHome" /></div>

      <div class="works">
        <div
          class="work"
          v-for="(work, i) of works"
          :key="i"
          @click="() => onClick(work.title)"
        >
          <!-- https://github.com/jooohyunpark/itp-wou-fall-2022/blob/main/Note.md#dyanmic-image-path-in-vue -->
          <img :src="require(`../assets/${work.src}`)" :alt="work.title" />
          <h2>{{ work.title }}</h2>
          <h3>{{work.description}}</h3>
        </div>
      </div>
    </div>
  </body>
  </template>
  
  <script>
  export default {
    data() {
      return {
        works: [
          { title: "Seed", description:"Organ Donation",src: "projects/1.png" },
          { title: "Re-design Equipment System of Death Stranding", description:"VR UX",src: "projects/Death.png" },
          { title: "X-Pace", description:"Exhibition Experience",src: "projects/3.png" },
        ],
      };
    },
    methods: {
      onClick(work) {
        console.log("clicked: ", work);
      },
      goToHome(){
   this.$router.push('/'); },
    },
  };
  </script>
  
  <style scoped>
  .project{
    background:#020287;
  }

  .homepage {
    max-width: 1280px;
    margin: 80px auto;
  }

  .works {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  
  .work {
    width: 33.33%;
    padding: 20px;
    box-sizing: border-box;
    position: relative;
    cursor: pointer;
  }
  
  .work img {
    width: 400px;
    height: 400px;
    transition: filter 0.2s linear;
  }
  
  .work h2 {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    margin: 0;
    color: white;
    opacity: 0;
    transition: opacity 0.2s linear;
 
  }
  .work h3 {
    margin: 0;
    color: white;
    opacity: 0;
    transition: opacity 0.2s linear;
 
  }
  
  
  .work:hover img {
    filter: brightness(0.2);
  }
  
  .work:hover h2 {
    opacity: 1;
    text-align: center;
  }
  .work:hover h3 {
    opacity: 1;
    text-align: center;
  }
  </style>