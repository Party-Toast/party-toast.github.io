<template>
    <v-app>
        <v-app-bar app color="amber accent-4" dark elevation="10">
            <v-app-bar-title>My Magazine</v-app-bar-title>
            <template v-slot:extension>
                <v-tabs 
                    v-model="tab" 
                    grow
                    center-active
                >
                    <v-tab v-for="(item, index) in items" :key="index">
                        <v-icon class="mr-2">{{ item.icon }}</v-icon>
                        {{ item.title }}
                    </v-tab>
                </v-tabs>
            </template>
        </v-app-bar>

        <v-main>
            <v-container fluid>
                <v-tabs-items v-model="tab">
                    <v-tab-item
                        v-for="(item, index) in items" :key="index"
                    >
                        <v-card class="ma-3"> 
                            <v-card-title>{{ item.title }}</v-card-title>
                            <v-card-text>{{ item.text }}</v-card-text>
                        </v-card>
                    </v-tab-item>
                    </v-tabs-items>
            </v-container>
        </v-main>
    </v-app>
</template>

<script>

export default {
    name: 'App',

    components: {
    },

    data: () => ({
        tab: null,
        items: [
            {
                title: 'Exploring Passion and Purpose',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-heart',
            },
            {
                title: 'Creating Impact',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-rocket',
            },
            {
                title: 'Developing Knowledge and Skills',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-flask',
            },
            {
                title: 'Creating a Future Plan',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-calendar',
            }
        ],
    }),
};
</script>
