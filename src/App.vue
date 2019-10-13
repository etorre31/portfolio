<template>
  <v-app>
    <v-container fill-height>
      <v-row justify="center" align="center">
        <v-col cols="12" class="text-center">
          <h1 class="display-4">Eric Torres' Portfolio</h1>
        </v-col>
        <v-col cols="12" class="text-center display-1">
          <p>eric00tor@gmail.com</p>
        </v-col>
        <v-col cols="12">
          <v-container>
            <v-row>
              <v-col v-for="(projects, index) in projects" :key="index">
                <v-card max-width="344" class="mx-auto">
                  <v-list-item>
                    <v-list-item-content>
                      <v-list-item-title class="headline">{{projects.name}}</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>

                  <v-img :src="projects.screenshot" contain height="194"></v-img>

                  <v-card-text>{{projects.description}}</v-card-text>

                  <v-card-actions>
                    <v-btn text color="blue accent-4" :href="projects.url" target="_blank">Go to Site</v-btn>
                    <v-btn icon>
                      <v-icon>mdi-share-variant</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>

export default {
  name: "App",
  data: () => ({
    projects: [
      {
        name: 'Vue Todo Application',
        description: 'A simple to do application which handles completed and pending tasks, it also keeps record of total tasks per bucket.',
        screenshot: '/images/todo.PNG',
        url: 'https://todo.eric-torres.site'
      },
      {
        name: 'Marvel Finder',
        description: 'Using Marvel Public API, we have a simple character finder application, with character descriptions and some comics where the character appears.',
        screenshot: '',
        url: 'https://marvelfinder.eric-torres.site'
      },
      {
        name: 'Super Awesome App',
        description: 'The coolest Social Network ever created.',
        screenshot: '/images/super-awesome-app.PNG',
        url: 'https://superawesomeapp.eric-torres.site'
      },
      {
        name: 'Movie Experience',
        description: 'Experience a movie going experience.',
        screenshot: '/images/movie.PNG',
        url: 'https://movie.eric-torres.site'
      }
    ]
  })
};
</script>
