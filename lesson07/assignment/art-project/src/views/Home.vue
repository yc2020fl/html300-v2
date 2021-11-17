<template>

<!-- keep the style from previous lesson 6, items in female artists and paintings are listed in script -->
<div class="text-center">

  <main class="main  bg-success">
    <div class="row mt-5 mb-5">
      <div class="col-xl-3 col-lg-3 col-sm-3 col-12 bg-success p-2 mt-2">
        <h2 class="bg-warning">Females Artists</h2>
        <ul>
          <li v-for="item in femaleArtists" :key="item.message">
            {{ item.message }}
          </li>
        </ul>

        <!-- did v-b-tooltip.hover here, it is easier than the previous lesson of repeative of data-toggle, etc -->
        <!-- did v-for in script for all the data as a list here -->
        <a href="artists.html" v-b-tooltip.hover class="btn btn-light btn-sm active"  title="Learn More about Artists" >See More</a>

      </div>
      <div class="col-xl-9 col-lg-9 col-sm-9 col-12 bg-danger p-2 mt-2">
        <h2 class="bg-warning">Paintings</h2>
        <ul>
          <li v-for="item in paintings" :key="item.message">
            {{ item.message }}
          </li>
        </ul>
        <a href="showcase.html" v-b-tooltip.hover class="btn btn-light btn-sm active" title="See More Paintings">See More</a>

      </div>
    </div>
  </main>

</div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      femaleArtists: [{
          message: 'Berthe Morisot '
        },
        {
          message: 'Adélaïde Labille-Guiard'
        },
        {
          message: 'Rosa Bonheur'
        },
        {
          message: 'Mary Cassatt '
        }
      ],
      paintings: [{
          message: 'A Woman Seated at a Bench on the Avenue du Bois | 1885'
        },
        {
          message: 'The Horse Fair | 1852–55'
        },
        {
          message: 'Madame Élisabeth de France (1764–1794) | ca. 1787 '
        },
        {
          message: 'Lydia Crocheting in the Garden at Marly | 1880'
        }
      ]
    }
  }

}



</script>



<style media="screen">
.main {
  padding: 1em;
}
</style>
