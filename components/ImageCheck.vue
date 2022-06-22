<template>
    <div>
        This is the image part.
        <img src="~/assets/biriyani.jpeg" width="200px">
        <div class="test">
            <h1> Hello this is Styled in the css</h1>
        </div>
<!-- :style="{ backgroundImage: `url(/_nuxt/${thumbnail})` }" -->
        <!-- <div  :style="require(`~/assets/img/${image}.jpg`)" /> -->
        <div  :style="{backgroundImage: `require(~/assets/${images}.jpeg)`}" >

            <h1> Hello this is Styled in dynamic way</h1>
        </div>

        <!-- <img :src="require(`~/assets/${images}.jpeg`)" /> -->

</div>
    

</template>



<script>
export default {

    props:['images'],

//  data:{
//     images:'asd'
//  }

};
</script>


<style scoped>
.test {
  background-image: url("~assets/biriyani.jpeg");
}
</style>