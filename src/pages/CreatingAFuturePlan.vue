<template>
    <v-row>
        <v-col cols="5">
            <v-card>
                <v-card-text class="pb-0">
                    <v-carousel v-model="selectedPicture" hide-delimiters>
                        <v-carousel-item
                            v-for="(picture, index) in pictures" :key="index"
                        >
                        <v-sheet
                            height="100%"
                            tile
                        >
                            <v-row
                                class="fill-height"
                                align="center"
                                justify="center"
                            >
                                <v-img :src="picture.src"></v-img>
                            </v-row>
                        </v-sheet>
                        </v-carousel-item>
                    </v-carousel>
                </v-card-text>
                <v-card-text>
                    {{ pictures[selectedPicture].description }}
                </v-card-text>
            </v-card>
        </v-col>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Creating a Future Plan</v-card-title>
                <v-card-subtitle class="pb-0">During your personal purpose project you will develop yourself in numerous directions. Create a future plan where you clarify why these developments are precious and how you are going to implement them in your future.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon>mdi-head-lightbulb</v-icon>
                            In the future, I want to do a lot more with my three main interests of programming, audio/HiFi, and makership. 
                            The insights I've gained during this semester will likely prove vital in my future as I will have more time and resources to pursue my interests.
                            <br>
                            I've already got some plans for future projects, like a multi-room audio system for me and my housemates, intergrate Spotify connect into a vintage HiFi system, and audio visualization using LED strips and electroluminescent wire to create audio-visual experiences.
                            <br><br>
                            <v-icon>mdi-share-variant</v-icon>
                            Although I did not have any time left after completing my personal purpose project, I would like to share my project with fellow makers and audiophiles in the future.
                            There are a lot of communities that might be interested in what I've made and I hope to inspire others to do the same.
                            If desired, I could also send my code, 3D models, and laser cutting files to others so they can recreate my product and iterate upon it themselves.
                            <br><br>
                            <v-icon>mdi-connection</v-icon>
                            While I was researching the 11 pin connector, I found out that multiple brands use the same connector for their products.
                            It turns out that the connector is a standard connector for audio equipment, but it operates slightly differently for each brand.
                            It might be interesting to make some changes to the hardware and software to allow for compatibility with other brands and do some tests with other cassette decks and reel-to-reel recorders.
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
    </v-row>
    
</template>

<script>

export default {
    components: {
    },
    data: () => ({
        selectedPicture: 0,
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