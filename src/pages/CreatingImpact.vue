<template>
    <v-row>
        <v-col cols="5">
            <PictureCarousel :pictures="pictures"/>
        </v-col>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Creating Impact</v-card-title>
                <v-card-subtitle class="pb-0">You show how you can create impact through your developed product and process towards a specific audience. This can start with only yourself but has to evolve to a broader spread of society.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon>mdi-account</v-icon>
                            The main impact of this project is on a personal level. 
                            The work I did was very close to my hobbies and studies, as I was working with vintage audio equipment and intertwined it with my programming skills.
                            I wanted to make this project for myself to show that I'm capable of being somewhat of a maker that follows his own passion and purpose instead of following an assignment from school or a company.
                            Even though tape recording is long dead for any practical use, I like the feeling of recording on tape and I wanted to make it more approachable for myself and others.
                            <br><br>
                            <v-icon>mdi-account-group</v-icon>
                            My end product takes an old piece of audio equipment and brings it into the modern age by applying wireless technologies and simplifying the setup process.
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
                src: 'https://picsum.photos/seed/1/300/300',
                description: 'Image 1',
            },
            {
                src: 'https://picsum.photos/seed/2/300/300',
                description: 'Image 2',
            },
            {
                src: 'https://picsum.photos/seed/3/300/300',
                description: 'Image 3',
            },
            {
                src: 'https://picsum.photos/seed/4/300/300',
                description: 'Image 4',
            },
            {
                src: 'https://picsum.photos/seed/5/300/300',
                description: 'Image 5',
            },
            {
                src: 'https://picsum.photos/seed/6/300/300',
                description: 'Image 6',
            },
            {
                src: 'https://picsum.photos/seed/7/300/300',
                description: 'Image 7',
            },
            {
                src: 'https://picsum.photos/seed/8/300/300',
                description: 'Image 8',
            },
            {
                src: 'https://picsum.photos/seed/9/300/300',
                description: 'Image 9',
            },
            {
                src: 'https://picsum.photos/seed/10/300/300',
                description: 'Image 10',
            },
            {
                src: 'https://picsum.photos/seed/11/300/300',
                description: 'Image 11',
            },
            {
                src: 'https://picsum.photos/seed/12/300/300',
                description: 'Image 12',
            },
            {
                src: 'https://picsum.photos/seed/13/300/300',
                description: 'Image 13',
            },
            {
                src: 'https://picsum.photos/seed/14/300/300',
                description: 'Image 14',
            },
            {
                src: 'https://picsum.photos/seed/15/300/300',
                description: 'Image 15',
            },
            {
                src: 'https://picsum.photos/seed/16/300/300',
                description: 'Image 16',
            },
            {
                src: 'https://picsum.photos/seed/17/300/300',
                description: 'Image 17',
            }      
        ],
    }),
}
</script>