<template>
    <v-row>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Creating Impact</v-card-title>
                <v-card-subtitle class="pb-0">You show how you can create impact through your developed product and process towards a specific audience. This can start with only yourself but has to evolve to a broader spread of society.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon color="amber darken-3">mdi-account</v-icon>
                            The main impact of this project is on a personal level. 
                            The work I did was very close to my hobbies and studies, as I was working with vintage audio equipment and intertwined it with my programming skills.
                            I wanted to make this project for myself to show that I'm capable of being somewhat of a maker that follows his own passion and purpose instead of just following an assignment from school or a company.
                            Even though tape recording is long dead for any practical use, I like the feeling of recording on tape and I wanted to make it more approachable for myself and others.
                            <br><br>
                            <v-icon color="amber darken-2">mdi-account-group</v-icon>
                            My end product takes an old piece of audio equipment and brings it into the modern age by applying wireless technologies and simplifying the setup process.
                            This is why I decided to give the product a retro '70s/'80s look, to match the target audience of people who are interested in vintage audio equipment.
                            Although I love using vintage tape recorders, the hassle of just setting them up, connecting the right wires, and preparing for recording is an enourmous hassle.
                            With my product, you just plug it in to power, connect it to the cassette deck with the 11 pin connector and audio jacks, and you're ready to go.
                            This should make recording audio a lot more approachable to people who are not familiar with the process of recording audio. 
                            <br>
                            For example, I used it to record a tape with Stef for his escape room even tho he is not familiar with vintage audio recording at all.
                            Furthermore, I can see this being a neat product for people who want to record their own music on tape for personal use or as novelty gifts. 
                            I've contact a friend who's studying to become an audio engineer and he was very interested in the product.
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
        <v-col cols="5">
            <PictureCarousel :pictures="pictures"/>
        </v-col>
    </v-row>
    
</template>

<script>
import PictureCarousel from '@/components/PictureCarousel.vue';

export default {
    components: {
        PictureCarousel,
    },
    data: () => ({
        pictures: [
            {
                src: '/slides/2_creating_impact/cable_spaghetti.jpeg',
                description: 'The living hell that is cable management, especially with vintage audio equipment.',
            },
            {
                src: '/slides/2_creating_impact/final_product.jpeg',
                description: 'The final product, ready to be used with any Akai RC-17/RC-18 remote compatible cassette deck. I tried to embrace the retro look of the cassette deck to match my target audience.',
            },
            
            // {
            //     src: '/slides/2_creating_impact/ghoul.jpeg',
            //     description: "'What's the matter smoothskin? Never seen a ghoul before?'",
            // },   
        ],
    }),
}
</script>