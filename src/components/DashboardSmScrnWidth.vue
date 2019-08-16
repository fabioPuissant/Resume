<template>
<div>
        <v-col>
            <about />
        </v-col>
        <v-col>
<skills />
        </v-col>
        <v-col>
            <about />
        </v-col>
        <v-col>
<skills />
        </v-col>
        <v-col>
            <about />
        </v-col>
        <v-col>
<skills />
        </v-col>
 
</div>   
</template>

<script>
import about from "../views/About.vue";
import Skills from "../views/Skills.vue";

export default {
    name: "DashboardSmScrnWidth",
    components: {
        about,
        Skills,
    }
}
</script>