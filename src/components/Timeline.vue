<template>
    <section id="timeline">
        <div class="container">
            <div class="row pt-5">
                <div class="col-md-12">
                    <h3>Timeline</h3>
                    <div class="accordion" id="accordionExample">
                        <div class="accordion-item">
                            <h2 class="accordion-header">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                                     12/2022 - 12/2023 CloudZA - Junior Web Developer
                                </button>
                            </h2>
                            <div id="collapseOne" class="accordion-collapse collapse show"
                                data-bs-parent="#accordionExample">
                                <div class="accordion-body">
                                    During my time at Cloudza, who are a South African cloud managed services provider. I was mentored and trained by a team of Certified AWS Professionals who helped me dive deeper into the cloud space. We worked and collaborated on multiple projects using AWS tools and services to design and refactor solutions for clients in various sectors such as education, healthcare as well as working with small to medium businesses
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                    09/2022 -12/2022 - LC Studio - Web Developer Intern
                                </button>
                            </h2>
                            <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                                <div class="accordion-body">
                                    During my time at LC Studio, I took part in a learning journey which covered various technologies such as HTML, CSS, Javascript, BOOTSTRAP, VUE.js, NODE.js, MYSQL, SEO and Wordpress. While be mentored and trained by a team of seasoned senior developers who gave me the right mentorship to equip me with the tools I needed to enter the web development industry and gain my AWS Certified Cloud Practitioner
                                </div>
                                <div class="buttons">
                                    <button @click="downloadCV('AWS Cloud Practitioner')">AWS Cloud Practitioner</button>
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                                    03/2022 - 09/2022 - LifeChoices Coding Academy - Student
                                </button>
                            </h2>
                            <div id="collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                                <div class="accordion-body">
                                    During my immersive journey at LifeChoices Coding Academy, I delved into the intricacies of web development, solidifying my passion for crafting digital experiences. Achieving a full-stack web development certification, I not only excelled academically but also thrived in hands-on experiences, particularly shining with a 99% pass in the MySQL module. LifeChoices became more than an academy—it became the forge where my coding skills were honed and where I discovered the thrill of transforming lines of code into dynamic, user-friendly websites.
                                </div>
                                <div class="buttons">
                                    <button @click="downloadCV('Fullstack Web Development')">Fullstack Web
                                        Development</button>
                                    <button @click="downloadCV('MySQL Certification')">MySQL Certification</button>
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                                    06/2021 - 03/2022 - CX INTERNATIONAL - CS Agent
                                </button>
                            </h2>
                            <div id="collapseFour" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                                <div class="accordion-body">
                                    In the role of Frontline Customer Advocate, I stood as the primary advocate for customer satisfaction, embodying the company's dedication to excellent customer service. Managing multichannel communication, I handled inbound and outbound calls, responded to emails, engaged in LiveChat sessions, and adeptly managed social media interactions. My goal was to provide comprehensive customer support across various channels, ensuring a seamless and positive experience for customers.
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
import awsCV from '../assets/AWSCertifiedCloudPractitionercertificate.pdf';
import fullstackCV from '../assets/fullstack_certification.pdf';
import mysqlCV from '../assets/mysql_certification.pdf';

export default {
    methods: {
        downloadCV(type) {
            let link;
            switch (type) {
                case 'AWS Cloud Practitioner':
                    link = awsCV;
                    break;
                case 'Fullstack Web Development':
                    link = fullstackCV;
                    break;
                case 'MySQL Certification':
                    link = mysqlCV;
                    break;
                default:
                    return;
            }

            const anchor = document.createElement('a');
            anchor.href = link;
            anchor.download = `Marshalino_Jankowski_${type.replace(/\s+/g, '_')}_Certification.pdf`;
            document.body.appendChild(anchor);
            anchor.click();
            document.body.removeChild(anchor);
        },
    },
};
</script>
  
<style scoped>
#timeline {
    display: flex;
    align-items: center;
    justify-content: center;
    background:
    linear-gradient(rgba(0, 0, 0, 0),
    rgb(255, 255, 255)),
    url(https://i.postimg.cc/qqj70ChP/christin-hume-Hcfwew744z4-unsplash.jpg);
    background-size: cover;
    background-attachment: fixed;
}
h3,
h4 {
    color: white;
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