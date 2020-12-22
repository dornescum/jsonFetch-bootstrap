<template>
  <b-container>
    <b-row align-v="center">
      <job-card v-for="job in jobs" :key="job.id" md="2"
                :name="job.name"
                :footer="job.footer"
                :picture="job.img"
                :text="job.text"
      >
      </job-card>
    </b-row>
  </b-container>
</template>

<script>
import JobCard from "@/components/JobCard";

export default {
  name: "Home",
  data() {
    return {
      jobs: []
    };
  },
  components: {
    JobCard
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      const response = await fetch("jobs.json");
      const value = await response.json();
      this.jobs = value;
      console.log(value);
    }
  }

};
</script>
