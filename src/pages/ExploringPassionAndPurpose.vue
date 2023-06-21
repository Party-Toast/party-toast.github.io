<template>
    <v-row>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Exploring Passion and Purpose</v-card-title>
                <v-card-subtitle class="pb-0">You can powerfully communicate your passion and indicate how it guided you to your personal purpose. Demonstrating valuable evidence is necessary to support this narrative and see the connection towards the developed product</v-card-subtitle>
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
                <v-card-text>
                    <v-carousel v-model="model" hide-delimiters>
                        <v-carousel-item
                        v-for="(color, i) in colors"
                        :key="i"
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
                                <v-img :src="generateImage(i)"></v-img>
                            </v-row>
                        </v-sheet>
                        </v-carousel-item>
                    </v-carousel>
                </v-card-text>
                <v-card-text>
                    {{ model }}
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
      model: 0,
      colors: [
        'primary',
        'secondary',
        'yellow darken-2',
        'red',
        'orange',
      ],
    }),
    methods: {
        generateImage(id) {
            return `https://picsum.photos/seed/${id}/300/300`
        }
    },
}
</script>