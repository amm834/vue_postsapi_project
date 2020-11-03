<template>
  <div>
    <Master>
      <div class="container my-3">
        <div class="jumbotron justify-content-center d-flex">
          <div class="card mb-3">
            <div class="card-header">
              Greeting 😁
            </div>
            <div class="card-body">
              <h5 class="card-title">Thank for visiting to my site!</h5>
              <p class="card-text">
                This blog is deployed on nelify and hosted at github.
              </p>
              <p>
                Develped By : Aung Myat Moe
              </p>
              <p>
                Languages and Technologies
              </p>
              <ul>
                <li>HTML,CSS,JS(Vue Lib)</li>
                <li>API from jsonplaceholder</li>
                <li>Git,Github for Host,Netlify To Deploy</li>
                <li>Linux To Manage</li>
                <li>NPM,Vue-Cli</li>
              </ul>
              <p>
                Conatct To Aung Myat Moe <br>
                <a href="https://github.com/amm834">GitHub Profile</a><br>
                <a href="https://www.facebook.com/aungmyatmoe834">Facebook Profile</a><br>
                <a href="https://www.linkedin.com/in/aungmyatmoe">LinkIn For Work</a>
              </p>
              <div class="alert alert-danger">
                If you think this site is so bad you can check to my Backend Projects and Tranditonal projects!
                <a href="github.com/amm834">Check Here</a>
              </div>
            </div>
          </div>
        </div>
      </div>

    </Master>
  </div>
</template>
<script>
  import Master from '../layouts/Master'
  export default {
    name: "Home",
    components: {
      Master
    }
  };
  </script>