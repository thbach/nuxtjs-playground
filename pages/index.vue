<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id">
    </PostPreview>
  </section>
</template>

<script>
import PostPreview from "@/components/Blog/PostPreview";

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: "A New Beggining",
          previewText: "This will be awesome, dont miss it!",
          thumbnailUrl:
            "https://ripeme.com/wp-content/uploads/RV-10070-RIPE-ORGANIC-ORGANIC-TOMATO-BEEF.jpg",
          id: "a-new-beginning"
        },
        {
          title: "A Second Beggining",
          previewText: "This will be awesome, dont miss it!",
          thumbnailUrl:
            "https://ripeme.com/wp-content/uploads/RV-10070-RIPE-ORGANIC-ORGANIC-TOMATO-BEEF.jpg",
          id: "a-second-beginning"
        }
      ]
    };
  }
};
</script>

<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
