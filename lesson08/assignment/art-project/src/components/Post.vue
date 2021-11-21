

<template>
  <div  >
    <!-- <div class="column">
  <div class="post col-xl-3 col-lg-4 col-sm-6 col-12 bg-warning p-2 mt-5" > -->


<!-- child -->
<!-- all these will be pass back to the parent page, and all the data are in this pattern -->
		<h5 class="post__painting">{{ post.painting }}</h5>
		<h6 class="post__name">{{ post.name }} | </h6>
		<h6 class="post__year">{{ post.year }}</h6>
<!-- after click, the image will have a double border, and click again, wil cancel it,
it links to the mixins folder, clickMixin.js, all the clicks can use this style and click event
with the same link to the mixin.js -->
    <img class="img-fluid width: 50% rounded" v-on:click="makeRed" :class="{'red': !isRed}" v-bind:src="post.image" v-bind:alt="post.painting">
    <a v-bind:href="post.link" target="_blank" >Click Me</a>
    <!-- v-on: click can be write as @click -->
    <!-- <button v-on:click="clicked"> -->

</div>

</template>



<script>
import clickMixin from '../mixins/clickMixin';

export default {

//moved this to ..mixins/clickMixin, so it is easier to  apply to other codes
//   methods: {
//
//     makeRed: function() {
//         this.isRed = false;
// }
// },

  mixins: [clickMixin],

//validation
  name: 'post',
  props: {
    post: {
      type: Object,
      default: function () {
        return { }
      },
    }


//if we put type: Number, Array, Boolean, etc. in vue inspect on the page, it says that expecting Object,
//but got a Number/Array, etc.
//Object, it must be capitalize
//lesson8b Codealong is an example
    // post: {
    //   type: Number,
    //   default: true
    //   },
    // }

}


}

</script>


<style lang="scss">


//.image and div means it apply the style to each individual div, not the entire body
  .image div{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(15rem, 1fr));
    grid-gap: 1em;
    padding: 0.5em;
    background: #85a400;
    margin: 0.4em;
    // border-style: solid;

  }

  .image {
    margin: 0.2em;
    padding: 0.1em;
    background: #85a45d;
    border-radius: 0.75em;
  }

  .imageShow  {

    margin: 0.1em;
    object-fit: contain;
    border-radius: 0.75em;
  }

  .imageShow div {
        border-top: 2em solid #5f544a;
  }

//style of the onclick event of the individual image
  .red {
      border-width: medium;
      border-style: double;
      border-color: #042030;
      padding: 1em;

  }

</style>
