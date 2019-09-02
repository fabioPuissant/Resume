<template>
  <v-layout align-content-start>
    <v-flex class="pa-2" xs4>
        <div class="border">
            <span>{{skill}}</span>
        </div>
    </v-flex>
    <v-flex class="ml-3 mt-3 pl-4">
      <v-progress-linear rounded v-model="level" :color="barColor" height="25" reactive>
        <template v-slot="{ value }">
          <strong>{{ Math.ceil(value) }}%</strong>
        </template>
      </v-progress-linear>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: "SkillComponent",
  props: {
    skill: {
      type: String,
      required: true
    },
    level: {
      type: Number,
      required: true,
      validator(value) {
        return value >= 0 && value <= 100;
      },
    },
      barColor: {
          required: true
      },
  }
};
</script>