<template>
    <section id="about">
        <div class="/about">
            <div class="container">
                <div class="row pt-4 pb-5 mt-5">
                    <h3 class="heading-sub">About Me</h3>
                    <h4 class="heading">
                        I am a Passionate Web Developer who has a AWS CCP and a
                        FullStack Web Development course. Adept at designing and implementing systems, I
                        excel as both a team player and lone wolf.
                    </h4>
                    <div class="col-md-6 justify-content-center align-items-center text-center">
                        <div class="card">
                            <img src="https://i.postimg.cc/sD3NhC4H/Screenshot-186-removebg-preview.png"
                        class="img-fluid"
                        alt="Marshalino-Jankowski-Logo">
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
                    <div class="col-md-6">
                        <h3 class="heading-sub">Soft Skills</h3>
                        <p class="text">
                            Incorporating active listening, problem-solving, and conflict management, a successful
                            individual is self-managed, adaptable to change, goal-driven, and possesses a strong work ethic.
                            Openness to feedback completes this skill set, fostering continuous improvement and growth in
                            both personal and professional spheres.
                        </p>
                        <div class="container text">
                            <div class="row">
                                <div class="col-sm-6 details">
                                    <p>City: Crawford, Cape Town</p>
                                    <p>Birth: 11/01/1998</p>
                                    <p>Criminal Record: None</p>
                                    <p>Gender: Male</p>
                                </div>
                                <div class="col-sm-6 details">
                                    <p>Email: swiftyblue11@gmail.com</p>
                                    <p>Cell: 061 844 5578</p>
                                    <p>Home language: English</p>
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
import cvFile from '../assets/MarshalinoJankowskiCV.pdf';
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
.card{
    border: none;
    background-color: transparent;
}
.text{
    font-size: 1.2rem;
}
.heading{
    font-size: 2rem;
    font-weight: 600;
}
.heading-sub {
    color: #009bdf;
}
.details p{
    margin: 0;
}
.design{
    font-size: 3rem;
    font-weight: 900;
    color: #009bdf;
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