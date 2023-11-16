<template>
  <section id="home">
    <div class="container">
      <div class="row">
        <div class="col-md-12 text-center">
          <div class="headingtext">
            <h1>{{ typedText }}</h1>
            <h2>Junior Web Developer</h2>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      originalText: "Hi, I'm Marshalino Jankowski",
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
    background:
    linear-gradient(rgba(0, 0, 0, 0),
    rgb(0, 0, 0)),
    url(https://i.postimg.cc/GtngTPD8/1330458.jpg);
    background-size: cover;
    background-attachment: fixed;
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
}
h1, h2{
  text-shadow: 0px 0px 10px #4af7ff;
}
</style>