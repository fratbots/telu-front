<template>
  <div>
    <h1 class="title">Find the next journey</h1>

    <section v-if="error">
      <p>Failed to load stories. Please, try again later.</p>
    </section>

    <section v-else>
      <div v-if="loading"><p>Loading...</p></div>

      <el-card v-else v-for="story in stories" :key="story.id" shadow="hover" class="story">
        <h2>{{ story.title }}</h2>
        <div class="author">
          <p class="el-icon-user-solid">{{ story.author }}</p>
        </div>
        <div class="rating">
          <el-rate
            :value="story.rating"
            disabled
            show-score
            text-color="#ff9900"
            score-template="{value} points">
          </el-rate>
          <span class="downloads">{{ story.games_completed }} journeys completed</span>
        </div>
        <p>
          {{ story.description }}
        </p>
      </el-card>
    </section>
  </div>
</template>

<style scoped>
.story {
  margin: 32px 0;
}

.author {
  margin: -24px 0 24px;
}

.rating {
  margin-bottom: 24px;
}
</style>

<script lang="ts">
import Vue from 'vue'

interface Story {
  id: number,
  author: string,
  title: string,
  description: string,
  rating: number,
  games_completed: number,
}

export default Vue.extend({
  data () {
    let stories: Story[] = [];

    return {
      loading: true,
      stories: stories,
      error: false,
    }
  },
  mounted () {
    this.$axios
      .get<Story[]>('/scenarios')
      .then(response => (this.stories = response.data)).
      catch(error => {
        console.log(error);
        this.error = true
      })
      .finally(() => this.loading = false)
  }
})
</script>
