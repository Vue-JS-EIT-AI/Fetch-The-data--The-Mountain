<template>
  <div>
    <div class="d-flex justify-content-center">
      <button class="btn btn-success" @click="$fetch">Fetch the Data</button>
    </div>
    <p v-if="$fetchState.pending">Fetching mountains...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p>

    <div v-else class="album py-5 bg-light">
      <div class="container">
        <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3">
          <div class="col" v-for="el in posts" :key="el.id">
            <div class="card shadow-sm">
              <img
                :src="el.image"
                class="bd-placeholder-img card-img-top"
                width="100%"
                height="225px"
                :alt="el.title"
              />
              <h5 class="card-title">{{ el.title }}</h5>
              <div class="card-body">
                <p class="card-text">{{ el.description }}</p>
                <p class="card-text">{{ el.countries }}</p>

                <ul>
                  <!-- <li v-repeat="el.countries"> {{$value}}</li> -->
                  <li v-for=" (test,index) in el.countries" :key="test[index] "> {{test }} {{index}}</li>
                </ul>
                
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- <div v-else >
      <div class="card" style="width: 18rem" v-for="el in posts" :key="el.id">
        <img :src="el.image" class="card-img-top" :alt="el.title" />
        <div class="card-body">
          <h5 class="card-title">{{ el.title }}</h5>
          <p class="card-text">
            {{ el.description }}
          </p>
        </div>
      </div>
    </div> -->
  </div>
</template>

<script>

export default {

  data() {
    return {
      posts: [],
    };
  },
  async fetch() {
    this.posts = await fetch("https://api.nuxtjs.dev/posts").then((res) =>
      res.json()
    );
  },
  layout:'fetchLT'
};
</script>