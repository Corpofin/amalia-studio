<template>
<div class="container-fluid mh-100 py-5 text-center">
  <div data-aos="fade">
    <span class="cursive font-weight-bold text-primary">some works</span>
    <h2 class="mb-5">- OUR PROJECTS -</h2>
  </div>

  <div class="row">
    <div class="col-md-6 col-lg-4" v-for="(item, index) in filter(projects, 6)" v-bind:key="index">
      <div class="border-0 card hvr-shadow mb-4 w-100">
        <a v-bind:href="item.link">
          <div class="img-wrapper" data-aos="zoom-in-right">
            <img class="card-img-top hvr-grow" v-bind:src="'img/projects/' + item.img" v-bind:alt="item.title">
          </div>

          <div class="card-body" data-aos="zoom-in-left">
            <small class="text-muted">{{ item.type }}</small>
            <h5 class="card-title">{{ item.title }}</h5>
          </div>
        </a>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import { filter } from "@/assets/js/functions";
import { projects } from "@/assets/js/data";

export default {
  data() {
    return {
      projects
    };
  },
  methods: {
    filter
  }
};
</script>

<style scoped>
</style>
