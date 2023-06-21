<template>
    <v-app>
        <v-app-bar app color="amber accent-4" dark elevation="10">
            <v-app-bar-title>Personal Purpose Track: Sytse Walraven</v-app-bar-title>
            <v-spacer/>
            <v-btn outlined>text</v-btn>
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
                        <component :is="item.component" class="ma-auto" />
                    </v-tab-item>
                    </v-tabs-items>
            </v-container>
        </v-main>
    </v-app>
</template>

<script>

import ExploringPassionAndPurpose from './pages/ExploringPassionAndPurpose.vue';
import CreatingImpact from './pages/CreatingImpact.vue';
import DevelopingKnowledgeAndSkills from './pages/DevelopingKnowledgeAndSkills.vue';
import CreatingAFuturePlan from './pages/CreatingAFuturePlan.vue';

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
                component: ExploringPassionAndPurpose,
            },
            {
                title: 'Creating Impact',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-rocket',
                component: CreatingImpact,
            },
            {
                title: 'Developing Knowledge and Skills',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-flask',
                component: DevelopingKnowledgeAndSkills,
            },
            {
                title: 'Creating a Future Plan',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl. Nulla euismod, nisl vitae aliquam ultricies, nunc nisl ultricies nunc, vitae aliquam nisl nisl vitae nisl.',
                icon: 'mdi-calendar',
                component: CreatingAFuturePlan,
            }
        ],
    }),
};
</script>
