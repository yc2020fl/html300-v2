<template>
  <div class="about">


    <section class="container-fluid col-xl-8 col-lg-8 col-sm-12 col-12 bg-success p-2 mt-5 mb-5">
      <div class="d-flex flex-row flex-wrap flex-sm-row flex-md-row flex-lg-row flex-xl-row">
        <p class="m-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>

      </div>

      <div class="bg-light">
        <h3>References Resources</h3>
        <a v-bind:href="link1" >From 1971: Why Have There Been No Great Women Artists?</a>
        <a v-bind:href="link2"  >Great Women Artists</a>
        <a v-bind:href="link3" >The MET</a>
        <a v-bind:href="link4" >Art = Discovering Infinite Connections in Art History</a>
        <a v-bind:href="link5">Public Parks, Private Gardens: Paris to Provence</a>
        <a v-bind:href="link6">Art Books & Media</a>
        <p>For images, Please refer to the link under the images.</p>
      </div>



      <!-- in script, v-if sources is true is to show the links,
      v-if sources is false is not showing the links,
      true is to show the link not have to click on the button
      v-else to show a line asking the user to click to see the sources,
      if the users wants to see less information on the page,
    it creates a better user experiences with less info overwhelming the user
  with v-else, the user learn that by clicking the button it will show the info again-->

      <div class="bg-light">
      <button	type="button" name="button" v-on:click="sources	=	!sources">Sources</button>


      <div v-if="sources">
      <p>https://www.barnesfoundation.org/whats-on/morisot</p>
      <p>https://www.metmuseum.org/toah/hd/lagui/hd_lagui.htm</p>
      <p>https://nmwa.org/art/artists/rosa-bonheur/</p>
      <p>https://nmwa.org/art/artists/mary-cassatt/</p>
      </div>
      <div v-else>Click the button to Show the Sources</div>
    </div>


    </section>








<!-- <h1 v-if="something">showing this sentnece</h1>
<h1 v-else>show not that sentence</h1> -->



  </div>




</template>





<script>
export default {
  name: 'About',
  data () {
    return {

      sources: false,
      link1: 'https://www.artnews.com/art-news/retrospective/why-have-there-been-no-great-women-artists-4201/',
      link2: 'https://www.metmuseum.org/perspectives/articles/2021/7/great-women-artists',
      link3: 'https://www.metmuseum.org/',
      link4: 'https://store.metmuseum.org/art-equals-discovering-infinite-connections-in-art-history-80047004',
      link5: 'https://store.metmuseum.org/public-parks-private-gardens-paris-to-provence-80040790',
      link6: 'https://store.metmuseum.org/books'



    }
  }



}
</script>

<style lang="css" scoped>
.about {
  padding: 1em;
}

a {
  padding: 0.5em;
  font-weight: bolder;
}

div {
  padding: 0.5em;
  margin:1em;
}

button {
  margin: 1em;
}

</style>
