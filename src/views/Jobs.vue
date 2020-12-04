<template>
  <h2>Job board</h2>
  <div class="job" v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h3>{{ job.title }}</h3>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { id: 1, title: 'Ninja UX designer', description: 'lorem' },
        { id: 2, title: 'Ninja Web designer', description: 'lorem' },
        { id: 3, title: 'Ninja Vue designer', description: 'lorem' },
      ],
    };
  },
};
</script>

<style>
.job a {
  text-decoration: none;
}

.job h3 {
  background: #ddd;
  color: #444;
  padding: 20px 30px;
  text-align: center;
  margin: 10px;
  border-radius: 4px;
}

.job h3:hover {
  background: #aaa;
  cursor: pointer;
}
</style>
