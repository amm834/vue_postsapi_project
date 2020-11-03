<template>
  <div>
    <Master>
      <Spinner class="text-center mt-3" v-show="isFeched == false"></Spinner>
      <div class="container mt-3" v-show="isFeched">
        <div class="row row-cols-1 row-cols-md-3 g-4">
          <div class="col" v-for="(post,index) in posts" :key="index">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">{{post.title}}</h5>
                <p class="card-text">
                  {{post.body}}
                </p>
              </div>
              <div class="card-footer">
                <button class="btn btn-success float-right" @click.once ="saveIt(post)">Save</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </Master>
  </div>
</template>
<script type="text/javascript" charset="utf-8">
  import Master from '../layouts/Master'
  import Spinner from './Spinner'
  import axios from 'axios'
  export default {
    name: 'Post',
    components: {
      Master,
      Spinner
    },
    data() {
      return {
        posts: [],
        isFeched: false,
      }
    },
    methods: {
      saveIt(post) {
        let save = this.$root.save;
        save.push(post)
      }
    },
    created() {
      axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(res=> {
        this.posts = res.data;
        this.isFeched = true
      })
    }
  }
  </script>