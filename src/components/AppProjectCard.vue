<script>

export default{
  name: 'AppProjectCard',

  data() {
    return {
     
    }
  },

  props: {

    project: Object,

  },

  created(){
  },

  methods: {
    
  }
}

</script>

<template>
  <router-link :to="{name: 'single-project', params: {slug: project.slug}}" style="text-decoration: none; color: inherit;">
    
  </router-link>
</template>

<style lang="scss">

</style>