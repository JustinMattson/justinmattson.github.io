<template>
  <span class="skills">
    <a :href="skill.link" target="_blank" style="text-decoration:none;" :title="skill.title">
      &nbsp;
      <img class="p-2" style="max-height:100px;max-width:100px" :src="skill.imgUrl" />
      &nbsp;
    </a>
  </span>
</template>


<script>
export default {
  name: "skills",
  props: ["skill"],
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {},
};
</script>


<style scoped>
</style>