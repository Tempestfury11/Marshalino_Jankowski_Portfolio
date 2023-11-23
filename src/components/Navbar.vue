<template>
    <nav class="navbar navbar-expand-lg fixed-top cyberpunk-navbar" :class="{ 'sticky': isSticky }">
        <div class="container-fluid">
            <a class="navbar-brand" href="/">
                <img src="https://i.postimg.cc/25wNNFHx/Screenshot-2023-11-15-121925-removebg-preview.png" 
                alt="Logo" width="30" height="24"
                class="d-inline-block align-text-top">
              </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" aria-current="page" href="/">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#testimonials">Testimonials</a>
                    </li>
                    <!-- <li class="nav-item">
                        <a class="nav-link" href="#projects">Projects</a>
                    </li> -->
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
  data() {
    return {
      isSticky: false,
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const scrollTop = window.scrollY;

      // You can adjust the scroll threshold as needed
      const scrollThreshold = 50;

      this.isSticky = scrollTop > scrollThreshold;
    },
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
};
</script>
  
<style scoped>
.cyberpunk-navbar {
  background-color: transparent;
  padding: 10px 30px;
  transition: 0.3s ease-in-out;
}
.cyberpunk-navbar.sticky {
  background-color: white;
}
.navbar-brand,
.nav-link {
    color: black;
    transition: all 0.3s ease-in-out;
    font-weight: 600;
}

.nav-link:hover {
    color: #009bdf;
    border-bottom:#009bdf 1px solid;
    font-weight: 600;
}

.nav-item {
    margin-right: 15px;
}

.navbar-nav {
    display: flex;
    align-items: center;
}
</style>