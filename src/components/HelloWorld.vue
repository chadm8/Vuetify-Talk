<template>
  <v-container class="d-inline-flex">
    <v-row class="justify-space-around">
      <v-card v-for="user in users" :key="user.name" width="400px" class="ma-4">
        <v-system-bar color="blue darken-2" dark> </v-system-bar>
        <v-app-bar dark color="blue">
          <v-avatar color="white">
            <v-icon large color="red">{{ user.icon }}</v-icon>
          </v-avatar>
        </v-app-bar>
        <v-card-title>{{ user.name }}</v-card-title>
        <v-card-subtitle>{{ user.title }}</v-card-subtitle>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          name: "Sarah",
          title: "Software Engineer",
          icon: "mdi-airplane",
        },
        {
          name: "Bill",
          title: "Network Engineer",
          icon: "mdi-dog",
        },
        {
          name: "Jared",
          title: "Business Analyst",
          icon: "mdi-crown",
        },
        {
          name: "Chloe",
          title: "Software Developer",
          icon: "mdi-car",
        },
        {
          name: "Jim",
          title: "Cloud Architect",
          icon: "mdi-flower",
        },
        {
          name: "Alexa",
          title: "Coffee Maker",
          icon: "mdi-cat",
        },
      ],
    };
  },
};
</script>
