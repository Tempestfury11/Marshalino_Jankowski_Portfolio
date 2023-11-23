<template>
    <section id="about">
        <div class="/about">
            <div class="container">
                <div class="row pt-5 pb-5 mt-5">
                    <h3>About Me</h3>
                    <h4>
                        I am a Passionate Web Developer who has a AWS CCP and a
                        FullStack Web Development course. Proficient in HTML, CSS,
                        Bootstrap, JavaScript, MySQL, Node.js, Vue.js, React, WordPress,
                        and SEO. Adept at designing and implementing systems, I
                        excel as both a team player and lone wolf. Demonstrating
                        active listening, problem-solving, and conflict management, I
                        bring a goal-driven work ethic and openness to change.
                    </h4>
                    <div class="col-md-6 pt-5 pb-5">
                        <h3>
                            I design professional & beautiful websites
                        </h3>
                    </div>
                    <div class="col-md-6 pt-5 pb-5">
                        <h3>Soft Skills</h3>
                        <p>
                            Incorporating active listening, problem-solving, and conflict management, a successful
                            individual is self-managed, adaptable to change, goal-driven, and possesses a strong work ethic.
                            Openness to feedback completes this skill set, fostering continuous improvement and growth in
                            both personal and professional spheres.
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
    background-color: #f6f8fa;
}

h3 {
    color: #758398;
}

.buttons button {
    margin: 5px;
    padding: 10px;
    border-top-left-radius: 10px;
    border-bottom-right-radius: 10px;
    border: #4af7ff 3px solid;
    color: black;
    background-color: transparent;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

.buttons button:hover {
    margin: 5px;
    padding: 10px;
    background-color: #4af7ff;
    text-shadow: 0px 0px 10px black;
    border: black 3px solid;
    color: white;
    border-top-left-radius: 20px;
    border-bottom-right-radius: 20px;
    cursor: pointer;
}
</style>