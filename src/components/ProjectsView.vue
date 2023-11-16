<template>
    <section id="projects" class="projects">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <h2 class="section-title">Projects</h2>
                    <div class="project-filter">
                        <button @click="filterProjects('all')" :class="{ 'active': activeFilter === 'all' }">All</button>
                        <button @click="filterProjects('next')"
                            :class="{ 'active': activeFilter === 'next' }">Next.js</button>
                        <button @click="filterProjects('nuxt')"
                            :class="{ 'active': activeFilter === 'nuxt' }">Nuxt.js</button>
                    </div>
                    <div class="project-list">
                        <div v-for="project in filteredProjects" :key="project.id" class="project-item">
                            <img :src="project.image" alt="Project Image" class="project-image" />
                            <div class="project-details">
                                <h3>{{ project.title }}</h3>
                                <p>{{ project.description }}</p>
                                <div class="buttons">
                                    <a target="_blank" :href="project.liveLink">
                                        <button>View Live</button>
                                    </a>
                                    <a target="_blank" :href="project.githubLink">
                                        <button>View GitHub</button>
                                    </a>
                                </div>
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
                {
                    id: 1,
                    title: 'Ali-Express',
                    type: 'nuxt',
                    image: 'https://i.postimg.cc/G2myy16F/aliexpress.png',
                    description: 'Full Stack Ecommerce',
                    liveLink: 'https://harmonious-caramel-8a4644.netlify.app/',
                    githubLink: 'https://github.com/Tempestfury11/AliExpressClone',
                },
            ],
            activeFilter: 'all',
        };
    },
    computed: {
        filteredProjects() {
            if (this.activeFilter === 'all') {
                return this.projects;
            } else {
                return this.projects.filter(project => project.type === this.activeFilter);
            }
        },
    },
    methods: {
        filterProjects(filter) {
            this.activeFilter = filter;
        },
    },
};
</script>
  
<style scoped>
.projects {
    background-color: #1c1c1c;
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
}

.project-filter {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
    transition: transform 0.3s ease-in-out;
}

.project-filter button {
    background-color: transparent;
    border: none;
    margin: 0 10px;
    padding: 10px 15px;
    cursor: pointer;
    transition: color 0.3s ease-in-out;
}

.project-filter button.active {
    color: #4af7ff;
}

.project-filter button:hover {
    color: #ff66a2;
}

.project-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    transition: transform 0.3s ease-in-out;
}

.project-item {
    width: 300px;
    margin: 20px;
    overflow: hidden;
    border: 3px solid #4af7ff;
    box-shadow: 0 4px 8px rgba(255, 102, 162, 0.5);
    border-radius: 5px;
    transition: transform 0.3s ease-in-out;
}

.project-item:hover {
    transform: scale(1.05);
}

.project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.project-details {
    padding: 15px;
}

.buttons button {
    margin: 5px;
    padding: 10px;
    border-top-left-radius: 10px;
    border-bottom-right-radius: 10px;
    border: #4af7ff 3px solid;
    color: #4af7ff;
    background-color: transparent;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

.buttons button:hover {
    margin: 5px;
    padding: 10px;
    background-color: #4af7ff;
    text-shadow: 0px 0px 10px black;
    border: #ffffff 3px solid;
    color: white;
    border-top-left-radius: 20px;
    border-bottom-right-radius: 20px;
    cursor: pointer;
}
</style>