<template>
  <section id="home">
    <div class="container">
      <div class="row">
        <div class="col-md-6 pt-5 pb-5">
          <h3>Hello, my name is</h3>
            <h1>{{ typedText }}</h1>
            <h2>Junior Web Developer</h2>
        </div>
        <div class="col-md-6 pt-5 pb-5">
          <img class="img img-fluid" 
          src="https://i.postimg.cc/DwzFG9rr/Mashalinoresized-removebg-preview.png" alt="Marshalino-Jankowski">
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
    background-size: cover;
    background-attachment: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
}
h1{
  font-weight: bold;
}
h2{
  color: #758398;
  text-transform: capitalize;
}
h3{
  color: #758398;
  text-transform: uppercase;
  font-size:large;
}
.img{
border-radius: 50%;
}
</style>