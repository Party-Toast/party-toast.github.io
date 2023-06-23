<template>
    <v-card>
        <v-card-text class="pb-0">
            <v-carousel 
                v-model="selectedPicture" 
                hide-delimiters
                cycle
                interval="3000"
            >
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
                        <v-img 
                            :src="picture.src" 
                            contain 
                            max-height="550"
                        />
                    </v-row>
                </v-sheet>
                </v-carousel-item>
            </v-carousel>
        </v-card-text>
        <v-card-text>
            {{ pictures[selectedPicture].description }}
        </v-card-text>
    </v-card>
</template>

<script>
export default {
    props: {
        pictures: {
            type: Array,
            required: true,
        },
    },
    data: () => ({
        selectedPicture: 0,
    })
}
</script>