<template>
  <article>
        <ul id="v-for-object" class="demo">
            <li v-for="value in blogPosts">
                <h2>{{ value.title }}</h2>
                <h5>{{ value.description }}</h5>
                <h5>{{ value.body }}</h5>
            </li>
        </ul>
  </article>
</template>

<script>
    export default {
        computed: {
            blogPosts() {
                return this.$store.state.blogPosts;
            },
        },
    };
</script>