<template>
    <section id="testimonials">
        <div class="container">
            <div class="row pt-5">
                <h3 class="heading">My Testimonials</h3>
                <div v-for="(TestimonialsArray, index) in TestimonialsArray" :key="index" class="col-md-4 pt-1 pb-1">
                    <div class="card mb-3 text-center" :style="{ boxShadow: cardShadow }">
                        <div class="card-body">
                            <p class="text">{{ TestimonialsArray.text }}</p>
                            <p class="position">{{ TestimonialsArray.position }}</p>
                            <p class="name">{{ TestimonialsArray.name }}</p>
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
                        "Marshalino is a diligent student who pays particular attention to detail. His mastery of web development has proved him to be among the prospective top developers. His work ethics are above board. I highly recommend him for any opportunities within your organisation.",
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
                        "Marshalino Jankowski is a great person to be around. He always lifts the mood which puts me in a better working mood thus increasing my work ethic and productivity. He is a team player and doing what must be done for the best of the team. He is extremely hard working and an amazing person and will be an asset to any company.",
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
            cardShadow: '0 4px 8px rgba(0, 0, 0, 0.1)',
        };
    }
};
</script>
  
<style scoped>
#testimonials {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #f6f8fa;
}
.text{
    color: black;
    font-size: 1rem;
    font-weight: 500;
}
.position{
    color: #009bdf;
    border-bottom: #758398 1px solid;
    font-size: 1.2rem;
    font-weight: bold;
}
.name{
    color: black;
    margin: 0;
    font-size: 1.1rem;
}
.card:hover {
    transform: scale(1.1);
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

.heading{
    color: #009bdf;
}

.card {
    border: none;
}
</style>