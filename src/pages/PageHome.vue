<template>
  <div class="col-full push-top">
    <h1>Welcome to the foro</h1>
    <CategoryList :categories="categories"/>
  </div>
</template>

<script>
  import CategoryList from '@/components/CategoryList'

  export default {
    components: {
      CategoryList
    },
    computed: {
      categories () {
        return Object.values(this.$store.state.categories)
      }
    }
  }
</script>
