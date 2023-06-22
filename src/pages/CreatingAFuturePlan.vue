<template>
    <v-row>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Creating a Future Plan</v-card-title>
                <v-card-subtitle class="pb-0">During your personal purpose project you will develop yourself in numerous directions. Create a future plan where you clarify why these developments are precious and how you are going to implement them in your future.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon color="amber darken-3">mdi-head-lightbulb</v-icon>
                            In the future, I want to do a lot more with my three main interests of programming, audio/HiFi, and makership. 
                            The insights I've gained during this semester will likely prove vital in my future as I will have more time and resources to pursue my interests.
                            <br>
                            I've already got some plans for future projects, like a multi-room audio system for me and my housemates, intergrate Spotify connect into a vintage HiFi system, and audio visualization using LEDs and electroluminescent wire to create audio-visual experiences.
                            <br><br>
                            <v-icon color="amber darken-2">mdi-share-variant</v-icon>
                            Although I did not have any time left after completing my personal purpose project, I would like to share my project with fellow makers and audiophiles in the future.
                            There are a lot of communities that might be interested in what I've made and I hope to inspire others to do the same.
                            If desired, I could also send my code, 3D models, and laser cutting files to others so they can recreate my product and iterate upon it themselves.
                            <br><br>
                            <v-icon color="amber darken-1">mdi-connection</v-icon>
                            While I was researching the 11 pin connector, I found out that multiple brands use the same connector for their products.
                            It turns out that the connector is a standard connector for audio equipment, but it operates slightly differently for each brand.
                            It might be interesting to make some changes to the hardware and software to allow for compatibility with other brands and do some tests with other cassette decks and reel-to-reel recorders.
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
        <v-col cols="5">
            <PictureCarousel :pictures="pictures" />
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
                src: "/slides/4_creating_a_future_plan/multi_audio_room.jpeg",
                description: "An example of a multi-room wireless audio system, powered by Raspberry Pi's. The system would allow you to play music in multiple rooms at the same time, or play different music in each room.",
            },  
            {
                src: "/slides/4_creating_a_future_plan/audio_visualization.jpeg",
                description: "Examples of audio visualization using LEDs, making use of a Raspberry Pi or other microcontroller to process the audio signal and control the lights.",
            },  
            {
                src: "/slides/4_creating_a_future_plan/el_wire.jpeg",
                description: "Electroluminescent wire which I would like to use for audio visualization. It is flexible and can be cut to length, making it easy to use for this purpose.",
            },  
            {
                src: "/slides/4_creating_a_future_plan/sony_remote.jpeg",
                description: "A Sony remote control for cassette decks and reel-to-reel recorders. The remote uses the same 11 pin connector as my controller but is wired differently.",
            },  
        ],
    }),
}
</script>