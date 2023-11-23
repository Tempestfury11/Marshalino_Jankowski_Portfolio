<template>
    <section id="timeline">
        <div class="timeline">
            <div class="container">
                <div class="row pt-5 pb-5">
                    <div class="col-md-6 timeline-card">
                        <h3 class="heading-sub">My Experience</h3>
                        <div class="card" v-for="(experience, index) in experiences" :key="index">
                            <h6><span class="date">{{ experience.date }}</span></h6>
                            <p class="role">{{ experience.role }}</p>
                            <p class="text">{{ experience.description }}</p>
                        </div>
                    </div>
                    <div class="col-md-6 timeline-card">
                        <h3 class="heading-sub">What I do</h3>
                        <p class="text">
                            From understanding your requirements, designing a blueprint and delivering the final product, I do everything that falls in between these lines.
                        </p>
                        <div class="card" v-for="(roles, index) in roles" :key="index">
                            <span class="icon" v-html="roles.img"></span>
                            <p class="role">{{ roles.role }}</p>
                            <p class="text">{{ roles.description }}</p>
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
            experiences: [
                {
                    date: "12/2022 - 12/2023",
                    role: "Junior Web Developer @ CloudZA",
                    description:
                        "Worked and collaborated with team of Certified AWS Professionals on multiple projects using AWS tools and services to design and create solutions for clients in various sectors such as education, healthcare across small to medium businesses",
                },
                {
                    date: "09/2022 - 12/2022",
                    role: "Web Developer Intern @ LC Studio",
                    description:
                        "I took part in a learning journey which covered various technologies while be mentored and trained by a team of seasoned senior developers providing me with the tools I needed to enter the web development industry and gain my AWS Certified Cloud Practitioner",
                },
                {
                    date: "03/2022 - 09/2022",
                    role: "Student @ LifeChoices Coding Academy",
                    description:
                        "During my time at LifeChoices Coding Academy, I delved into the intricacies of web development, achieving a full-stack web development certification. My coding skills were honed and I discovered the thrill of transforming lines of code into dynamic, user-friendly websites.",
                },
            ],
            roles: [
                {
                    img: '<i class="fa-solid fa-pen-ruler" style="font-size: 32px;"></i>',
                    role: "UI/UX DESIGN",
                    description:
                        "An effective UI/UX is what captures attention and spreads a clear message. I make sure the design is innovative and neat with all of this",
                },
                {
                    img: '<i class="fa-solid fa-laptop-code" style="font-size: 32px;"></i>',
                    role: "WEB DEVELOPMENT",
                    description:
                        "If you are looking for a developer who’ll take over the research and development of your website, I am a well-established professional to help you with this.",
                },
                {
                    img: '<i class="fa-solid fa-mobile-screen" style="font-size: 32px;"></i>',
                    role: "APP DEVELOPMENT",
                    description:
                        "If you are looking for a user-friendly app that will attract more mobile users, I can help you design and build a platform with the latest and trendiest look and feel.",
                },
            ],
        };
    },
};
</script>
  
<style scoped>
.timeline {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f6f8fa;
}

.timeline-card {
    align-content: center;
    flex-direction: column;
    text-align: start;
    display: flex;
    background-color: #f6f8fa;
}

.card {
    padding: 20px;
    border: none;
    background-color: #f6f8fa;
}

.date {
    border-bottom: #758398 1px solid;
    color: black;
    font-size: 1rem;
    font-weight: 500;
    margin: 0;
}

.role {
    color: #009bdf;
    font-size: 1.2rem;
    font-weight: bold;
    margin: 0;
}
.text {
    color: black;
    margin: 0;
    font-size: 1.1rem;
}

.heading-sub {
    color: #009bdf;
}
</style>