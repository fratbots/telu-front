<template>
  <div>
    <div class="about">
      <h1>Telu is all about interactive text universes</h1>
      <p>
        It's time to rethink storytelling.
        What if the book is not static?
        What if the reader is a part of a story?
      </p>
    </div>
    <el-row>
      <el-col :span="12" class="target">
        <h2>Read the universe. Thousands of them.</h2>
        <p>
          Participate in a journey.
          Make your choices.
          Find the best universe for you.
          Discover classics of new era.
        </p>
        <p class="action">
          <nuxt-link to="/reader">
            <el-link type="primary" icon="el-icon-s-management">Start your journey</el-link>
          </nuxt-link>
        </p>
      </el-col>
      <el-col :span="12" class="target">
        <h2>Tell your story</h2>
        <p>
          Create an interactive journey.
          Share with the world.
          Get in touch with your readers.
          Reinvent the book.
        </p>
        <p class="action">
          <nuxt-link to="/author">
            <el-link type="primary" icon="el-icon-edit">Write your Story</el-link>
          </nuxt-link>
        </p>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.about {
  padding: 28px 0;
  text-align: center;
  background: #FDF6EC;
  border-bottom: 10px solid #FAECD8;
}

.target {
  margin: 48px 0;
}

.action {
  margin: 1em 0;
}
</style>
