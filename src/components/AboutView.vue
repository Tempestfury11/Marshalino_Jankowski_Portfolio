<template>
    <section id="about">
        <div class="/about">
            <div class="container">
                <div class="row">
                    <div class="col-md-6 pt-5 pb-5">
                        <div class="edgeRunnerCard">
                            <img src="https://i.postimg.cc/dt5L9rRg/me.jpg" alt="Edge Runner Image"
                                class="img-fluid rounded-circle shadow-1-strong">
                                <h2>Hi there, Im Marshalino Jankowski </h2>
                            <div class="buttons">
                                <a target="_blank" href="https://www.linkedin.com/in/marshalino-jankowski-385861247/">
                                    <button>LinkedIn</button>
                                </a>
                                <a target="_blank" href="https://github.com/Tempestfury11">
                                    <button>GitHub</button>
                                </a>
                                <button @click="downloadCV">Download CV</button>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6 pt-5 pb-5">
                        <p>
                            I am a Passionate Web Developer who has a AWS CCP and a
                            FullStack Web Development course. Proficient in HTML, CSS,
                            Bootstrap, JavaScript, MySQL, Node.js, Vue.js, React, WordPress,
                            and SEO. Adept at designing and implementing systems, I
                            excel as both a team player and lone wolf. Demonstrating
                            active listening, problem-solving, and conflict management, I
                            bring a goal-driven work ethic and openness to change.
                        </p>
                        <h2>Tech Stack</h2>
                        <p>
                            HTML
                            CSS
                            JAVASCRIPT
                            BOOTSTRAP
                            MYSQL
                            NODE
                            VUE.JS
                            React
                            WordPress
                            SEO
                        </p>
                        <h2>Soft Skills</h2>
                        <p>
                            ACTIVE LISTENING
                            PROBLEM SOLVING
                            CONFLICT MANAGEMENT
                            SELF-MANAGED
                            OPEN TO CHANGE
                            GOAL DRIVEN
                            SOUNDWORK ETHIC
                            OPEN TO FEEDBACK
                        </p>
                        <div class="container">
                            <div class="row">
                                <!-- left -->
                                <div class="col-sm-6">
                                    <p>City: Crawford, Cape Town</p>
                                    <p>Birth: 11/01/1998</p>
                                    <p>Criminal Record: None</p>
                                    <p>Gender: Male</p>
                                </div>
                                <!-- right -->
                                <div class="col-sm-6">
                                    <p>Email: swiftyblue11@gmail.com</p>
                                    <p>Cell: 061 844 5578</p>
                                    <p>Home language: English</p>
                                    <p>Second language: Afrikaans</p>
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
import cvFile from '../assets/CV.pdf';
export default {
    methods: {
        downloadCV() {
            const link = document.createElement('a');
            link.href = cvFile;
            link.download = 'Marshalino_Jankowski_CV.pdf';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        },
    },
};
</script>

<style scoped>
#about {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #1c1c1c;
}

.edgeRunnerCard {
    background-color: #1c1c1c;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(255, 102, 162, 0.5);
    padding: 30px;
    text-align: center;
    color: #4af7ff;
    border: #4af7ff 3px solid;
}

.edgeRunnerCard img {
    border-radius: 50%;
    margin-bottom: 10px;
    object-fit: cover;
    object-position: 0 0;
    border: #4af7ff 3px solid;
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