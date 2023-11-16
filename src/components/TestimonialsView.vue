<template>
    <section id="testimonials">
        <div class="container">
            <h2 class="section-title">Testimonials</h2>
            <div class="row">
                <div class="col-md-4 mt-5" v-for="(TestimonialsArray, index) in TestimonialsArray"
                    :key="index">
                    <div class="testimonial-grid">
                        <div class="testimonial-item">
                            <div class="testimonial-content">
                                <p>
                                    {{ TestimonialsArray.text }}
                                </p>
                                <p class="testimonial-position">
                                    {{ TestimonialsArray.position }}
                                </p>
                                <p class="testimonial-author">{{ TestimonialsArray.name }}</p>
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
            TestimonialsArray: [
                {
                    id: 1,
                    position: "Lecturer and Front End Developer",
                    text:
                    "Marshalino is a very consistent developer. He gets quite excited when he sees an opportunity to participate and show off his abilities. He is always challenging himself to write complex ideas to improve his coding skills. I am certain Marshalino will continue to do well.",
                    name: "Jason Wandrag",
                },
                {
                    id: 2,
                    position: "Head of Curriculum and Learning",
                    text:
                    "Marshalino is a diligent student who pays particular attention to detail. His mastery of HTML, CSS and Bootsrap has proved him to be among the prospective top developers. His work ethics are above board. I highly recommend him for any opportunities within your organisation.",
                    name: "Godwin Dzvapatsva",
                },
                {
                    id: 3,
                    position: "Senior Coding Academy Lecturer",
                    text:
                    "Marshalino should be happy with his progress and understanding of the lesson content as he is doing very well. Marshalino has proven to have a detailed grasp of the HTML,CSS & Bootstrap material we have been studying. He is an expert at describing what he has done.",
                    name: "Joel Tshimanga Mukanya",
                },
                {
                    id: 4,
                    position: "Web Development Intern - Code Infinity",
                    text:
                    "Marshalino Jankowski is a great person to be around. He always lifts the mood which puts me in a better working mood thus increasing my work ethic and productivity. He is a team player and doing what must be done for the best of the team. He is extremely hard working. I can say Marshalino an amazing person and will be an asset to any company.",
                    name: "Ra'ees Benny",
                },
                {
                    id: 5,
                    position: "Technician - Spinnaker Software",
                    text:
                    "Marshalino Jankowski is a hardworking and dedicated person with a can-do attitude. In high-pressure circumstances, he leaps into action and assumes control. I have observed him working hard to advance both himself and his work. He is approachable and entertaining but also capable of taking charge when necessary",
                    name: "Saleem Ariefdien",
                },
                {
                    id: 6,
                    position: "Support Engineer - Itemate Solutions",
                    text:
                    "I would like to formally recommend Marshalino for his consistent work. He has the ability to complete tasks timelessly and effectively. His planning before taking action is always consistent and sharing ideas, steps for planning a website. I know that Marshalino has the ability and skills to be an excellent addition to the company",
                    name: "Emile Van Wyk",
                },
            ],
        };
    }
};
</script>
  
<style scoped>
#testimonials {
    background-color: #1c1c1c;
    color: #4af7ff;
    padding: 60px 0;
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
}

.testimonial-item {
    background-color: #1c1c1c;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(255, 102, 162, 0.5);
    padding: 20px;
    border: #4af7ff 3px solid;
}

.testimonial-content {
    font-size: 18px;
}

.testimonial-position {
    margin-top: 15px;
    font-size: 16px;
    color: #4af7ff;
}
.testimonial-author {
    margin-top: 15px;
    font-size: 16px;
}
</style>