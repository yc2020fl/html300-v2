<template>
<!-- Will use this page for the future API project if needed
the following information is just temporary-->


<div>

  <Header>
    <template #headerontop>
  Artworks and its Relationship to...
  </template>
  <template #headersecond>
  Female Images
  </template>
  </Header>

<div class="bg-success m-2 p-2">
  <ul class="bg-light" v-for="person	in	persons" v-bind:key="person.id">
    <li>
      {{person.name}}
    </li>
    <li> {{person.age}}
    </li>
    <li>{{person.style}}</li>
  </ul>
</div>
</div>
</template>

<script>
import Header from '../components/Header';
export default {



  name: 'Statistics',
  components: {
    Header
  },


  data() {
    return {
      persons: [{
          name: 'Berthe Morisot',
          age: 1,
          style: 'impressionism'
        },
        {
          name: 'Adélaïde Labille-Guiard',
          age: 2,
          style: 'impressionism'
        },
        {
          name: 'Rosa Bonheur',
          age: 2,
          style: 'impressionism'
        },
        {
          name: 'Mary Cassatt',
          age: 2,
          style: 'impressionism'
        },

      ],



    }
  }
}
</script>

<style lang="css" scoped>

ul {
  margin: 1em;
}
</style>
