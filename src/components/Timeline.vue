<template>
    <section id="timeline-sec">
        <div class="container">
            <div class="row">
                <h1>Timeline</h1>
                <div class="col-md-12">
                    <div class="timeline">
                        <div class="timeline-item">
                            <div class="timeline-content">
                                <h3>December 2022</h3>
                                <h4>CloudZA - Junior Web Developer</h4>
                                <p>
                                    During my time at Cloudza, who are a South African
                                    cloud managed services provider. I was mentored and
                                    trained by a team of Certified AWS Professionals who
                                    helped me dive deeper into the cloud space. We
                                    worked and collaborated on multiple projects using
                                    AWS tools and services to design and refactor solutions
                                    for clients in various sectors such as education,
                                    healthcare as well as working with small to medium
                                    businesses
                                </p>
                            </div>
                        </div>
                        <div class="timeline-item">
                            <div class="timeline-content">
                                <h3>September 2022 - December 2022</h3>
                                <h4>LC Studio - Web Developer Intern</h4>
                                <p>
                                    During my time at LC Studio, I took part in a learning
                                    journey which covered various technologies such as
                                    HTML, CSS, Javascript, BOOTSTRAP, VUE.js, NODE.js,
                                    MYSQL, SEO and Wordpress. While be mentored and
                                    trained by a team of seasoned senior developers who
                                    gave me the right mentorship to equip me with the
                                    tools I needed to enter the web development industry
                                    and gain my AWS Certified Cloud Practitioner
                                </p>
                                <button @click="downloadCV('AWS Cloud Practitioner')">AWS Cloud Practitioner</button>
                            </div>
                        </div>
                        <div class="timeline-item">
                            <div class="timeline-content">
                                <h3>March 2022 - September 2022</h3>
                                <h4>LifeChoices Coding Academy - Student</h4>
                                <p>
                                    During my immersive journey at LifeChoices Coding Academy, I delved into the intricacies
                                    of web development, solidifying my passion for crafting digital experiences. Achieving a
                                    full-stack web development certification, I not only excelled academically but also
                                    thrived in hands-on experiences, particularly shining with a 99% pass in the MySQL
                                    module. LifeChoices became more than an academy—it became the forge where my coding
                                    skills were honed and where I discovered the thrill of transforming lines of code into
                                    dynamic, user-friendly websites.
                                </p>
                                <div class="buttons">
                                    <button @click="downloadCV('Fullstack Web Development')">Fullstack Web
                                        Development</button>
                                    <button @click="downloadCV('MySQL Certification')">MySQL Certification</button>
                                </div>
                            </div>
                        </div>
                        <div class="timeline-item">
                            <div class="timeline-content">
                                <h3>June 2021 to March 2022</h3>
                                <h4>CX INTERNATIONAL - CS Agent</h4>
                                <p>
                                    In the role of Frontline Customer Advocate, I stood as
                                    the primary advocate for customer satisfaction,
                                    embodying the company's dedication to excellent
                                    customer service. Managing multichannel
                                    communication, I handled inbound and outbound calls,
                                    responded to emails, engaged in LiveChat sessions,
                                    and adeptly managed social media interactions. My
                                    goal was to provide comprehensive customer support
                                    across various channels, ensuring a seamless and
                                    positive experience for customers.
                                </p>
                            </div>
                        </div>
                        <!-- Add more timeline items as needed -->
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
#timeline-sec {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    background-color: #1c1c1c;
}

.timeline {
    position: relative;
    max-width: 800px;
    margin: 20px auto;
}

.timeline-item {
    position: relative;
    padding: 20px;
    margin: 20px;
    background: #1c1c1c;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(255, 102, 162, 0.5);
    overflow: hidden;
    border: #4af7ff 4px solid;
    display: flex;
    text-align: center;
}

.timeline h3 {
    margin-top: 0;
}

.timeline p {
    margin-bottom: 0;
}

button {
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

button:hover {
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