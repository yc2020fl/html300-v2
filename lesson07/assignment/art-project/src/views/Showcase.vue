<template>
<div>

  <h2> Paris Salon Kind of Room</h2>
  <main class="main  bg-success">
    <div class="row mt-5 mb-5">
      <div class="col-xl-12 col-lg-12 col-sm-12 col-12 bg-success p-2 mt-2">
        <h2 class="bg-warning">Females Artists</h2>

        <!-- a list of the female artists names from script, kpt the same style of list-group of the white bg -->
        <ul class="list-group">
          <li class="list-group-item" v-for="item in femaleArtists" :key="item.message">
            {{ item.message }}
          </li>
        </ul>
      </div>

      <!-- 4 artists divided into 4 rows, as if presenting on a wall,
each with their paintings going as a column, with the v-for to the data,
*links need to use v-bind-->

      <div class="col-xl-3 col-lg-3 col-sm-6 col-12 bg-danger p-2 mt-5">
        <div>
          <div v-for="showcasepainting1 in showcasepaintings1" :key="showcasepainting1.name">
            <p class="bg-warning"> {{showcasepainting1.name}}</p>
            <p> {{showcasepainting1.painting}} </p>
            <img class="img-fluid rounded" v-bind:src="showcasepainting1.image">
            <a class="bg-light" v-bind:href="showcasepainting1.link" target="_blank">Click Me</a>
          </div>
        </div>
      </div>


      <div class="col-xl-3 col-lg-3 col-sm-6 col-12 bg-danger p-2 mt-5">
        <div>
          <div v-for="showcasepainting2 in showcasepaintings2" :key="showcasepainting2.name">
            <p class="bg-warning"> {{showcasepainting2.name}}</p>
            <p> {{showcasepainting2.painting}} </p>
            <img class="img-fluid rounded" v-bind:src="showcasepainting2.image">
            <a class="bg-light" v-bind:href="showcasepainting2.link" target="_blank">Click Me</a>
          </div>
        </div>
      </div>


      <div class="col-xl-3 col-lg-3 col-sm-6 col-12 bg-danger p-2 mt-5">
        <div>
          <div v-for="showcasepainting3 in showcasepaintings3" :key="showcasepainting3.name">
            <p class="bg-warning"> {{showcasepainting3.name}}</p>
            <p> {{showcasepainting3.painting}} </p>
            <img class="img-fluid rounded" v-bind:src="showcasepainting3.image">
            <a class="bg-light" v-bind:href="showcasepainting3.link" target="_blank">Click Me</a>
          </div>
        </div>
      </div>

      <div class="col-xl-3 col-lg-3 col-sm-6 col-12 bg-danger p-2 mt-5">
        <div class="pb-5">
          <div class="p-2" v-for="showcasepainting4 in showcasepaintings4" :key="showcasepainting4.name">
            <p class="bg-warning"> {{showcasepainting4.name}}</p>
            <p> {{showcasepainting4.painting}} </p>
            <img class="img-fluid rounded" v-bind:src="showcasepainting4.image">
            <a class="bg-light" v-bind:href="showcasepainting4.link" target="_blank">Click Me</a>
          </div>
        </div>
      </div>


    </div>
  </main>


</div>
</template>

<script>
export default {

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

      //each artist has her own list, name it showcasepainting1 just in case the artists will be changed later
      showcasepaintings1: [{
          name: ' Berthe Morisot, Painting 1 ',
          painting: ' Young Woman Knitting | ca. 1883',
          link: 'https://www.metmuseum.org/art/collection/search/437159',
          image: 'https://collectionapi.metmuseum.org/api/collection/v1/iiif/437159/796162/main-image',

        },
        {
          name: ' Berthe Morisot, Painting 2 ',
          painting: ' A Woman Seated at a Bench on the Avenue du Bois | 1885',
          link: 'https://www.metmuseum.org/art/collection/search/337864',
          image: 'https://collectionapi.metmuseum.org/api/collection/v1/iiif/337864/756828/main-image',

        },
      ],
      showcasepaintings2: [{
          name: 'Adélaïde Labille-Guiard, Painting 1',
          painting: ' Self-Portrait with Two Pupils, Marie Gabrielle Capet (1761–1818) and Marie Marguerite Carreaux de Rosemond (died 1788) | 1785 ',
          link: ' https://www.metmuseum.org/art/collection/search/436840',
          image: 'https://collectionapi.metmuseum.org/api/collection/v1/iiif/436840/1425691/main-image'
        },
        {
          name: 'Adélaïde Labille-Guiard, Painting 2 ',
          painting: ' Madame Élisabeth de France (1764–1794) | ca.1787 ',
          link: ' https://www.metmuseum.org/art/collection/search/439405',
          image: ' https://collectionapi.metmuseum.org/api/collection/v1/iiif/439405/795077/main-image'
        },
      ],
      showcasepaintings3: [{
          name: 'Rosa Bonheur, Painting 1',
          painting: ' The Horse Fair | 1852–55 ',
          link: ' https://www.metmuseum.org/art/collection/search/435702',
          image: 'https://collectionapi.metmuseum.org/api/collection/v1/iiif/435702/796396/main-image'
        },

      ],
      showcasepaintings4: [{
          name: 'Mary Cassatt, Painting 1',
          painting: ' Lydia Crocheting in the Garden at Marly | 1880',
          link: 'https://www.metmuseum.org/art/collection/search/10393',
          image: 'https://images.metmuseum.org/CRDImages/ad/mobile-large/DP165250.jpg'
        },
        {
          name: 'Mary Cassatt Painting 2 ',
          painting: ' Lilacs in a Window (Vase de Lilas a la Fenetre) | ca. 1880–83',
          link: 'https://www.metmuseum.org/art/collection/search/13758',
          image: 'https://images.metmuseum.org/CRDImages/ad/mobile-large/DT254478.jpg'
        },
      ],
    }




  }
}
</script>



<style lang="css" scoped>
</style>
