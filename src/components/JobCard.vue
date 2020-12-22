<template>
  <b-col md="4">
    <b-card
      :title="name"
     :img-src="picture"
      img-alt="picture"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2 mt-4"
      :footer="footer"
    >

      <b-card-text v-text="text">
<!--        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, temporibus.-->
      </b-card-text>
      <b-button variant="primary">Apply</b-button>
    </b-card>
  </b-col>
</template>

<script>
export default {
  name: "JobCard",
  props: ['name', "footer", "picture", "text"]
};
</script>

<style scoped>

</style>