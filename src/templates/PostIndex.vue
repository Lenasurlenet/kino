<template>
  <div>

    <h1>{{$page.post.title}}</h1>
    <strong>Author: </strong>{{ $page.post.author }} <br>
    <strong>Published: </strong>{{ $page.post.published }}

    <vueRemarkContent />

  </div>
</template>

<page-query>

  query Post ($id: ID!) {
  post(id: $id) {
    title
    author
    published (format:"DD MMMM YYYY")
  }
}

</page-query>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>

</style>