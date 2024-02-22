<template>
    <section id="projects">
        <div class="container">
            <div class="row pt-5">
                <h3 class="heading pb-5">My Projects</h3>
                <div v-for="(project, index) in projects" 
                :key="index" class="col-md-4 pt-1 pb-1">
                    <div class="card mb-3 text-center" 
                    :style="{ boxShadow: cardShadow }">
                        <img :src="project.image" 
                        alt="Project Image" class="project-image" />
                        <div class="card-body">
                            <p class="name">{{ project.title }}</p>
                            <p class="text">{{ project.description }}</p>
                            <div class="buttons">
                                <a target="_blank" 
                                :href="project.liveLink">
                                    <button>View Live</button>
                                </a>
                            </div>
                        </div>
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
            projects: [
                // {
                //     id: 1,
                //     title: 'Ali-Express Fullstack Clone',
                //     image: 'https://i.postimg.cc/G2myy16F/aliexpress.png',
                //     description: 'Nuxt',
                //     liveLink: 'https://pearllemon.com/',
                // },
                {
                    id: 2,
                    title: 'Pearl Lemon',
                    image: 'https://i.postimg.cc/SKLYdBTM/Pearl-Lemon.png',
                    description: 'Wordpress',
                    liveLink: 'https://pearllemon.com/',
                },
                {
                    id: 3,
                    title: 'Pearl Lemon Catering',
                    image: 'https://i.postimg.cc/9FfPMQxN/Pearl-Lemon-Catering.png',
                    description: 'Wordpress',
                    liveLink: 'https://pearllemoncatering.com/',
                },
                {
                    id: 4,
                    title: 'Pearl Lemon Tattoos',
                    image: 'https://i.postimg.cc/kX71yCTx/Pearl-Lemon-Tattoos.png',
                    description: 'Wordpress',
                    liveLink: 'https://pearllemontattoos.com/',
                },
                {
                    id: 5,
                    title: 'Pets Lets Travel',
                    image: 'https://i.postimg.cc/NjmcrBFR/Pets-Lets-Travel.png',
                    description: 'Wordpress',
                    liveLink: 'https://petsletstravel.com/',
                },
                {
                    id: 6,
                    title: 'Pearl Lemon Visa',
                    image: 'https://i.postimg.cc/Vvf6K5ry/Pearl-Lemon-Visa.png',
                    description: 'Wordpress',
                    liveLink: 'https://pearllemonvisa.com/',
                },
                {
                    id: 7,
                    title: 'Pearl Lemon Leads',
                    image: 'https://i.postimg.cc/PxNVYQy0/Pearl-Lemon-Leads.png',
                    description: 'Wordpress',
                    liveLink: 'https://pearllemonleads.com/',
                },
                {
                    id: 8,
                    title: 'SoapYesterday Movie App',
                    image: 'https://i.postimg.cc/s2bLH4Yy/soaper.png',
                    description: 'Vue',
                    liveLink: 'https://soapyesterday.netlify.app/',
                },
                {
                    id: 9,
                    title: 'ToDo App',
                    image: 'https://i.postimg.cc/HnGHSgfq/To-Do-React.png',
                    description: 'React',
                    liveLink: 'https://legendary-toffee-42ad71.netlify.app/',
                },
                {
                    id: 10,
                    title: 'ToDo App',
                    image: 'https://i.postimg.cc/Jnwm48Pp/TodoVue.png',
                    description: 'HTML CSS JS',
                    liveLink: 'https://symphonious-cheesecake-7f5d05.netlify.app/',
                },
                {
                    id: 11,
                    title: 'Age Converter',
                    image: 'https://i.postimg.cc/XvbHJnrv/Age-Calculator.png',
                    description: 'HTML CSS JS',
                    liveLink: 'https://startling-parfait-d201e2.netlify.app/',
                },
                {
                    id: 12,
                    title: 'HEX To RGB',
                    image: 'https://i.postimg.cc/t4q3s7X7/HEX2RGB.png',
                    description: 'HTML CSS JS',
                    liveLink: 'https://eclectic-sunflower-2c3e9e.netlify.app/',
                },
            ],
            cardShadow: '0 4px 8px rgba(0, 0, 0, 0.1)',
        };
    },
};
</script>
  
<style scoped>
#projects {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #f6f8fa;
}

.text {
    color: black;
    font-size: 1rem;
    font-weight: 500;
}

.name {
    color: black;
    margin: 0;
    font-size: 1.1rem;
}

.heading {
    color: #009bdf;
}

.card {
    border: none;
}

.card:hover {
    transform: scale(1.1);
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}
.buttons button {
    margin: 5px;
    padding: 10px;
    border-top-left-radius: 10px;
    border-bottom-right-radius: 10px;
    border: #009bdf 3px solid;
    color: black;
    background-color: transparent;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

.buttons button:hover {
    margin: 5px;
    padding: 10px;
    background-color: #009bdf;
    text-shadow: 0px 0px 10px black;
    color: white;
    border-top-left-radius: 20px;
    border-bottom-right-radius: 20px;
    cursor: pointer;
}
</style>