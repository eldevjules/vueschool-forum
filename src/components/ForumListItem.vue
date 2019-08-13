<template>
  <div class="forum-listing">
    <div class="forum-details">
      <router-link
        class="text-xlarge"
        :to="{name: 'Forum', params:{id: forum['.key']}}"
      >
        {{forum.name}}
      </router-link>
      <p>{{forum.description}}</p>
    </div>

    <div class="threads-count">
      <p><span class="count">{{threadsCount}}</span></p>
      {{threadsCount === 1 ? 'thread' : 'threads'}}
    </div>

    <div class="last-thread">
      <!-- TODO: implement later -->
    </div>
  </div>
</template>

<script>
  import {countObjectPropierties} from '@/utils'
  export default {
    props: {
      forum: {
        required: true,
        type: Object
      }
    },

    computed: {
      threadsCount () {
        return countObjectPropierties(this.forum.threads)
      }
    }
  }
</script>

<style scoped>

</style>
