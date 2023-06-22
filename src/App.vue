<template>
    <v-app>
        <v-app-bar app dark elevation="5" style="background: linear-gradient(rgb(255, 171, 0), rgb(144, 84, 255))">
            <v-app-bar-title><b>Personal Purpose Track</b> Sytse Walraven</v-app-bar-title>
            <v-spacer/>
            <v-btn 
                @click="showRubric1 = true"
                outlined 
            >
                <span>Rubric</span>
                <v-icon class="ml-2 pr-0">mdi-numeric-1-circle-outline</v-icon>
            </v-btn>
            <v-btn 
                @click="showRubric2 = true"
                outlined 
                class="ml-3"
            >
                <span>Rubric</span>
                <v-icon class="ml-2 pr-0">mdi-numeric-2-circle-outline</v-icon>
            </v-btn>
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
            <v-container fluid style="background: linear-gradient(rgba(144, 84, 255, 0.5), rgb(250, 250, 250))">
                <v-tabs-items v-model="tab" style="background: rgba(0, 0, 0, 0)">
                    <v-tab-item
                        v-for="(item, index) in items" :key="index"
                    >
                        <component :is="item.component" class="ma-auto" />
                    </v-tab-item>
                    </v-tabs-items>
            </v-container>
        </v-main>
        <v-dialog
            v-model="showRubric1"
            width="50%"
        >
            <v-img 
                src="./assets/PPI formative assessment 1.png"
            />
        </v-dialog>
        <v-dialog
            v-model="showRubric2"
            width="50%"
        >
            <v-img 
                src="./assets/PPI formative assessment 2.png"
            />
        </v-dialog>
    </v-app>
</template>

<script>

import ExploringPassionAndPurpose from './pages/ExploringPassionAndPurpose.vue';
import CreatingImpact from './pages/CreatingImpact.vue';
import DevelopingKnowledgeAndSkills from './pages/DevelopingKnowledgeAndSkills.vue';
import CreatingAFuturePlan from './pages/CreatingAFuturePlan.vue';

export default {
    name: 'App',
    created() {
        document.title = 'My Magazine';
    },
    data: () => ({
        showRubric1: false,
        showRubric2: false,
        tab: null,
        items: [
            {
                title: 'Exploring Passion and Purpose',
                icon: 'mdi-heart',
                component: ExploringPassionAndPurpose,
            },
            {
                title: 'Creating Impact',
                icon: 'mdi-bullseye-arrow',
                component: CreatingImpact,
            },
            {
                title: 'Developing Knowledge and Skills',
                icon: 'mdi-flask',
                component: DevelopingKnowledgeAndSkills,
            },
            {
                title: 'Creating a Future Plan',
                icon: 'mdi-calendar',
                component: CreatingAFuturePlan,
            }
        ],
    }),
};
</script>
