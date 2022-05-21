<template>
  <v-container class="ma-0 pa-0" fluid>
    <v-app-bar color="purple darken-4" dark>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>Our Employees</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group v-model="group">
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Our Employees</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-row class="justify-space-around my-2 mx-2">
      <v-card v-for="user in users" :key="user.name" width="400px" class="my-8">
        <v-card color="purple darken-3" class="py-3 text-center">
          <v-avatar width="100px" height="100px" color="white">
            <img width="100px" :src="user.link" />
          </v-avatar>
        </v-card>
        <v-card-title>{{ user.name }}</v-card-title>
        <v-card-subtitle>{{ user.title }}</v-card-subtitle>
        <v-card-text>
          <p>&emsp;&emsp;{{ descriptions }}</p>
        </v-card-text>
        <v-card-actions class="justify-center">
          <v-row class="pb-4 mx-2">
            <v-col cols="3" class="text-center">
              <v-btn dark fab color="black">
                <v-icon>mdi-github</v-icon>
              </v-btn>
            </v-col>
            <v-col cols="3" class="text-center">
              <v-btn dark fab color="blue">
                <v-icon>mdi-twitter</v-icon>
              </v-btn>
            </v-col>
            <v-col cols="3" class="text-center">
              <v-btn dark fab color="orange">
                <v-icon color="white">mdi-instagram</v-icon>
              </v-btn>
            </v-col>
            <v-col cols="3" class="text-center">
              <v-btn dark fab color="red">
                <v-icon color="white">mdi-email</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-card-actions>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      descriptions:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean accumsan nisl non ligula sagittis pretium. Sed tellus ex, pharetra a sem non, facilisis hendrerit justo. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Praesent libero nisi, tincidunt id massa at, viverra pellentesque lorem.",
      drawer: false,
      group: null,
      users: [
        {
          name: "Sarah",
          title: "Software Engineer",
          icon: "mdi-airplane",
          link: "https://images.unsplash.com/photo-1597223557154-721c1cecc4b0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTR8fGdsb3dpbmclMjBmYWNlfGVufDB8fDB8fA%3D%3D&w=1000&q=80",
        },
        {
          name: "Bill",
          title: "Network Engineer",
          icon: "mdi-dog",
          link: "https://st.depositphotos.com/1008939/1880/i/600/depositphotos_18807295-stock-photo-portrait-of-handsome-man.jpg",
        },
        {
          name: "Jared",
          title: "Business Analyst",
          icon: "mdi-crown",
          link: "https://www.faceapp.com/static/img/content/compare/beard-example-before@3x.jpg",
        },
        {
          name: "Chloe",
          title: "Software Developer",
          icon: "mdi-car",
          link: "https://www.goldennumber.net/wp-content/uploads/2013/08/florence-colgate-england-most-beautiful-face.jpg",
        },
        {
          name: "Jim",
          title: "Cloud Architect",
          icon: "mdi-flower",
          link: "https://www.bethesdaheadshots.com/wp-content/uploads/2020/02/Jonathan-Business-Headshot.jpg",
        },
        {
          name: "Sid",
          title: "Tree Climber",
          icon: "mdi-cat",
          link: "https://www.rainforest-alliance.org/wp-content/uploads/2021/06/three-toed-sloth-teaser-1.jpg.optimal.jpg",
        },
      ],
    };
  },
};
</script>
