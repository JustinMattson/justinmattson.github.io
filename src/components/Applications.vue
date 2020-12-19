<template>
  <div class="applications col-12 col-md-6 col-lg-3 valign p-1">
    <div class="container p-0 shadow-lg">
      <img v-bind:src="require('@/assets/img/' + app.img)" class="image" :title="app.name" alt="screen capture of web app"/>
      <div class="overlay">
        <div class="text text-shadow" aria-label="Application name">{{app.name}}<br />
          <span style="font-size:8px;" class="text-center">Development Stack:<br />
          </span>
            <p style="font-size:13px">{{app.stack}}</p>
          <div>
            <a class="ao" :href="app.githubUrl" style="text-decoration:none;" target="_blank" aria-label="to github repository" title="GitHub Repo">
              <i class="fab fa-github-square fa-2x"><p style="font-size:8px;">Repository</p></i>
            </a>
          </div>
          <div>
            <a class="ao" :href="app.hostUrl" target="_blank" aria-label="to application host site" title="Host Site">
              <span style="font-size:8px;" class="text-center">Hosted on:</span><br />
              {{app.hostName}}
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "applications",
  props: ["app"],
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {},
};
</script>


<style scoped>
a.ao {
  text-decoration: none;
  color: white;
  text-shadow: 1px 1px 5px black;
}
.container {
  position: relative;
  width: 100%;
}
.image {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 10px;
}
.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: 0.5s ease;
  background-color: #35495ecc;
  border-radius: 10px;
}
.container:hover .overlay {
  opacity: 1;
}
.text {
  color: white;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}
</style>