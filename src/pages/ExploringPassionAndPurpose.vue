<template>
    <v-row>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Exploring Passion and Purpose</v-card-title>
                <v-card-subtitle class="pb-0">You can powerfully communicate your passion and indicate how it guided you to your personal purpose. Demonstrating valuable evidence is necessary to support this narrative and see the connection towards the developed product.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.
                        </v-card-text>
                    </v-col>
                    <v-col>
                        <v-card-text>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
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
                <v-img></v-img>
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
                src: "/slides/1_exploring passion_and_purpose/cassette_deck_rear.jpeg",
                description: 'The rear of the cassette deck which inspired me to start this project',
            }
        ],
    }),
}
</script>