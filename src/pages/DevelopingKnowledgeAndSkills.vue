<template>
    <v-row>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Developing Knowledge and Skills</v-card-title>
                <v-card-subtitle class="pb-0">You develop new knowledge and skills that are valuable to your development and your personal purpose. You professionally provide evidence of this relevance and demonstrate your growth.</v-card-subtitle>
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