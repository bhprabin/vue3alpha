<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="start">Progress</button>
  </div>
</template>

<script>
  export default {
    methods: {
      start () {
          this.$Progress.start()
      },
      set (num) {
          this.$Progress.set(num)
      },
      increase (num) {
          this.$Progress.increase(num)
      },
      decrease (num) {
          this.$Progress.decrease(num)
      },
      finish () {
          this.$Progress.finish()
      },
      fail () {
          this.$Progress.fail()
      },
      test(){
        this.$Progress.start()

        this.$http.jsonp('http://api.rottentomatoes.com/api/public/v1.0/lists/movies/in_theaters.json?apikey=7waqfqbprs7pajbz28mqf6vz')
        .then((response) => {
          console.log(response);
          this.$Progress.finish()
        }, (response) => {
          console.log(response);
          this.$Progress.fail()
        })
      }
    }
  }
</script>
