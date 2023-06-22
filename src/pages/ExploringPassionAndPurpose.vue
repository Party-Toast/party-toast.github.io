<template>
    <v-row>
        <v-col cols="5">
            <PictureCarousel :pictures="pictures"/>
        </v-col>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Exploring Passion and Purpose</v-card-title>
                <v-card-subtitle class="pb-0">You can powerfully communicate your passion and indicate how it guided you to your personal purpose. Demonstrating valuable evidence is necessary to support this narrative and see the connection towards the developed product.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon>mdi-cassette</v-icon>
                            My passion that inspired this project is my love for vintage audio equipment, especially old reel-to-reel recorders, turn tables, and cassette decks.
                            I've already had some experience with repairing and restoring these devices, but I wanted to take it a step further and create something new.
                            When I was cleaning out my grandfather's house, I found this old cassette deck with a weird remote control port that I had never seen before.
                            After I did some Googling, I found out that it was a proprietary remote control port which are quite rare and expensive.
                            I decided to try and reverse engineer the remote and build my own remote control for the cassette deck.
                            After asking for and receiving help on a <a href="https://www.tapeheads.net/threads/diy-akai-remote-version-2-0.99205/#post-775683806">forum about analog tape</a>, 
                            I made a first simple paper prototype which worked surprisingly well.
                            <br><br>
                            <v-icon>mdi-tools</v-icon>
                            Since there are a lot of tools at Pulsed that I don't have at home, I decided to service the cassette deck a little.
                            I cleaned the heads and tape path with isopropyl alcohol and replaced some of the broken lights behind the control buttons.
                            After doing some tests and calibration, the cassette deck was ready for the rest of my project.
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
    </v-row>
    
</template>

<script>
import PictureCarousel from '../components/PictureCarousel.vue';

export default {
    components: {
        PictureCarousel,
    },
    data: () => ({
        pictures: [
            {
                src: "/slides/1_exploring_passion_and_purpose/reel_to_reel_1.jpeg",
                description: 'My Sony TC-377 reel-to-reel recorder, which I restored in the past.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/reel_to_reel_2.jpeg",
                description: 'A picture of the Akai GX-4400D reel-to-reel recorder, of which I am currently restoring a model.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/cassette_deck_rear.jpeg",
                description: 'The rear of my Akai GXC-760D cassette deck which inspired me to start this project.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/diagram.jpeg",
                description: 'The wiring diagram of the remote which inspired me to start this project.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/paper_prototype_1.jpeg",
                description: 'The paper prototype of the remote control, which I made to verify if the concept would work.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/paper_prototype_2.jpeg",
                description: 'The paper prototype of the remote control, which I made to verify if the concept would work.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/disassembly_1.jpeg",
                description: 'The cassette deck, disassembled.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/disassembly_2.jpeg",
                description: 'The cassette deck, disassembled.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/disassembly_3.jpeg",
                description: 'The cassette deck, disassembled.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/disassembly_4.jpeg",
                description: 'The cassette deck, disassembled.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/repair_1.jpeg",
                description: 'Repairing the broken bulbs of cassette deck controls.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/repair_2.jpeg",
                description: 'Repairing the broken bulbs of cassette deck controls.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/repair_3.jpeg",
                description: 'Repairing the broken bulbs of cassette deck controls.',
            },
            {
                src: "/slides/1_exploring_passion_and_purpose/repair_4.jpeg",
                description: 'Repairing the broken bulbs of cassette deck controls.',
            },

            
        ],
    }),
}
</script>