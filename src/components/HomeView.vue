<template>
  <section id="home">
    
    <div class="container bg-con">
      <div class="row">
        <div class="col-sm-12 col-md-6 hometext">
          <div class="col-header">
            <h3 class="hello">Hello, my name is</h3>
          </div>
          <div class="col-main">
            <h1 class="name">{{ typedText }}</h1>
            <h2 class="position">Junior Web Developer</h2>
          </div>
        </div>
        
        <div class="col-sm-12 col-md-6">
          <img class="img pt-3" 
          src="https://i.postimg.cc/W1NYT0V1/red-removebg-preview.png" alt="Marshalino-Jankowski">
        </div>
      </div>
    </div>


    <div class="container sm-con">
      <div class="row">
        <div class="col-sm-12 col-md-6">
          <img class="img" 
          src="https://i.postimg.cc/W1NYT0V1/red-removebg-preview.png" alt="Marshalino-Jankowski">
        </div>
        <div class="col-sm-12 col-md-6">
          <h3 class="hello">Hello, my name is</h3>
            <h1 class="smallname">{{ typedText }}</h1>
            <h2 class="position">Junior Web Developer</h2>
        </div>
      </div>
    </div> 
  </section>
</template>

<script>
export default {
  data() {
    return {
      originalText: "Marshalino Jankowski",
      typedText: "",
      currentIndex: 0,
    };
  },
  methods: {
    startTyping() {
      const intervalId = setInterval(() => {
        this.typedText += this.originalText[this.currentIndex];
        this.currentIndex++;

        if (this.currentIndex === this.originalText.length) {
          clearInterval(intervalId);
        }
      }, 100);
    },
  },
  mounted() {
    this.startTyping();
  },
};
</script>


<style scoped>
#home {
    background-color:#f6f8fa;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: right;
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url('https://i.postimg.cc/MpkmjY7D/pngegg-7.png');
}
.name{
  font-size: 4rem;
  font-weight: bold;
}
.smallname{
  font-size: 3rem;
}
.position{
  color: #009bdf;
  text-transform: capitalize;
}
.hello{
  color: #758398;
  text-transform: uppercase;
  font-size:large;
}
.img{
border-radius: 50%;
width: 100%;
}
.hometext{
  display: flex;
  justify-content: center;
  align-content: center;
  flex-direction: column;
  text-align: start;
}
.col-main{
  margin-top: 50px;
  margin-bottom:50px ;
}
.bg-con{
  display: block;
}

.sm-con{
  display: none;
}

@media only screen and (max-width: 767.5px){
  .bg-con{
  display: none;
}

.sm-con{
  display: block;
}
}
</style>