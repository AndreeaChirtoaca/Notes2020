<template>
  <div>
    <section class="bar_line">
      <div class="bar_create_note">
        <h1 class="name">Dashboard</h1>
        <a class="button" @click="newNote()">NEW NOTE</a>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  name: "Toolbar",
  data: function() {
    return {};
  },
  methods: {
    newNote() {
      this.$router.push({ path: "/new-notes" });
    }
  }
};
</script>
<style scoped>
.dashboard_bar {
  background: #f2f2f2;
  padding: 15px 50px;
  vertical-align: middle;
  margin: 0 auto;
  max-width: 960px;
}

@media screen and (max-width: 500px) {
  .column {
    flex: 50%;
  }
}

.name {
  display: block;
  font-family: "Roboto";
  color: black;
  font-size: 40px;
  font-weight: normal;
  font-style: normal;
}
.button {
  background: #2ea1f8;
  padding: 15px 32px 14px 32px;
  margin: 25px 10px 25px 10px;
  text-decoration: none;
  font-weight: normal;
  font-style: normal;
  font-family: "Roboto";
  font-size: 16px;
  border-radius: 5px;
  line-height: 28px;
  color: #ffffff;
}
.button:hover {
  background-color: #4ab1ff;
}
.bar_create_note {
  display: flex;
  justify-content: space-around;
}
</style>