<template>
    <section id="skills">
        <div class="/skills">
            <div class="container">
                <div class="row">
                    <h3 class="heading">My Skills</h3>
                    <div v-for="(skill, index) in skills" :key="index" class="col-md-4">
                        <div class="card mb-3 text-center" :style="{ boxShadow: cardShadow }">
                            <div class="card-body">
                                <i :class="['fab', getIconClass(skill.name), 'fa-3x', 'mb-3', 'skill-icon']"></i>
                                <h5 class="card-title">{{ skill.name }}</h5>
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
            skills: [
                { name: 'HTML' },
                { name: 'CSS' },
                { name: 'Bootstrap' },
                { name: 'JavaScript' },
                { name: 'Node.js' },
                { name: 'Vue.js' },
                { name: 'React' },
                { name: 'WordPress' },
                { name: 'SEO' },
            ],
            cardShadow: '0 4px 8px rgba(0, 0, 0, 0.1)',
        };
    },
    methods: {
        getIconClass(skillName) {
            switch (skillName) {
                case 'HTML':
                    return 'fa-html5';
                case 'CSS':
                    return 'fa-css3';
                case 'Bootstrap':
                    return 'fa-bootstrap';
                case 'JavaScript':
                    return 'fa-js';
                case 'Node.js':
                    return 'fa-node-js';
                case 'Vue.js':
                    return 'fa-vuejs';
                case 'React':
                    return 'fa-react';
                case 'WordPress':
                    return 'fa-wordpress';
                case 'SEO':
                    return 'fa-searchengin';
                default:
                    return 'fa-question';
            }
        },
    },
};
</script>
  
<style scoped>
#skills {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #f6f8fa;
}
.heading {
    color: #009bdf;
}
.card:hover {
    transform: scale(1.1);
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

.card {
    border: none;
}
</style>