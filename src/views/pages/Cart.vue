<template>
  <div>
    <Master>
      <div class="container mt-3" v-if="save.length > 0">
        <div class="row row-cols-1 row-cols-md-3 g-4">
          <div class="col" v-for="(bookmark,index) in save" :key="index">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">{{bookmark.title}}</h5>
                <p class="card-text">
                  {{bookmark.body}}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    <div class="text-center" v-else>
      No Added Posts To Show 
    </div>
    </Master>
  </div>
</template>
<script type="text/javascript" charset="utf-8">
  import Master from '../layouts/Master'
  export default {
    name: 'Cart',
    components: {
      Master
    },
    data() {
      return {
        save: []
      }
    },
    created() {
      this.save = this.$root.save
    }
  }
  </script>