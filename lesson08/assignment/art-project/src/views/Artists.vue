<template>
  <div>
    <Header>
      <template #headerontop>
    Artworks and its Relationship to...
    </template>
    <template #headersecond>
    Female Images
    </template>
    </Header>
    <main class="main  bg-success">
      <div class="row mt-5 mb-5">


        <!-- a list of the artists' name -->
        <!-- toke the artists name list out, because it occurs in too mant pages, home, showcase, artists -->
        <!-- <div class="col-xl-12 col-lg-12 col-sm-12 col-12 bg-success p-2 mt-2">
          <h2 class="bg-light">Females Artists</h2>

          <ul >
            <li v-for="item in femaleArtists" :key="item.message">
              {{ item.message }}
            </li>
          </ul>
        </div> -->


<!-- each keywords(items) in script, use v-for to pull the data -->
        <div class="col-xl-3 col-lg-6 col-sm-6 col-12 bg-danger p-2 mt-5">
          <h2 class="bg-warning">Berthe Morisot </h2>
          <ul>
            <li v-for="item in berthemorisot" :key="item.message">
              {{ item.message }}
            </li>

          </ul>
        </div>


        <div class="col-xl-3 col-lg-6 col-sm-6 col-12 bg-danger p-2 mt-5">
          <h2 class="bg-warning">Adélaïde Labille-Guiard</h2>
          <ul>
            <li v-for="item in labille_guiard" :key="item.message">
              {{ item.message }}
            </li>
          </ul>
        </div>
        <div class="col-xl-3 col-lg-6 col-sm-6 col-12 bg-danger p-2 mt-5">
          <h2 class="bg-warning">Rosa Bonheur</h2>
          <ul>
            <li v-for="item in rosabonheur" :key="item.message">
              {{ item.message }}
            </li>
          </ul>
        </div>



        <div class="col-xl-3 col-lg-6 col-sm-6 col-12 bg-danger p-2 mt-5">
          <h2 class="bg-warning">Mary Cassatt</h2>
          <ul>
            <li v-for="item in marycassatt" :key="item.message">
              {{ item.message }}
            </li>
          </ul>
        </div>





      </div>
    </main>



  </div>

</template>

<script>
import Header from '../components/Header';

export default {


  name: 'Artists',

  components: {
    Header
  },

  data() {
    return {

//did not use since Lesosn 8
      // femaleArtists: [{
      //     message: 'Berthe Morisot '
      //   },
      //   {
      //     message: 'Adélaïde Labille-Guiard'
      //   },
      //   {
      //     message: 'Rosa Bonheur'
      //   },
      //   {
      //     message: 'Mary Cassatt '
      //   }
      // ],
      berthemorisot: [{
          message: 'impressionists'
        },
        {
          message: 'French, 1841–1895'
        },
        {
          message: 'Paris Salon '
        },
        {
          message: 'professional artists '
        }
      ],
      labille_guiard: [{
          message: 'Paris guild '
        },
        {
          message: 'Salon'
        },
        {
          message: 'full-scale portraiture'
        },
        {
          message: 'teaching '
        }
      ],
      rosabonheur: [{
          message: 'successful career '
        },
        {
          message: 'moved to Paris'
        },
        {
          message: 'canvas'
        },
        {
          message: 'Paris Salon'
        }
      ],
      marycassatt: [
        {
          message: 'Pennsylvania '
        },
        {
          message: 'Paris'
        },
        {
          message: ' Paris Salon'
        },
        {
          message: 'Impressionism'
        },

      ],
}
}
}
</script>



<style lang="css" scoped>
.main {
  padding: 1em;
}
</style>
