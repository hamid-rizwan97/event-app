<template>
  <div>
    <header>
      <app-header></app-header>
    </header>
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
    <hr />
    <button v-on:click="DeleteNinja()">Delete ninja</button>
    <hr />
    <footer>
      <app-footer></app-footer>
    </footer>
  </div>
</template>

<script>
import header from "./components/header.vue";
import footer from "./components/footer.vue";
import ninjas from "./components/ninjas.vue";
export default {
  components: {
    "app-header": header,
    "app-footer": footer,
    "app-ninjas": ninjas,
  },
  data() {
    return {
      title: "First vue application",
      ninjas: [
        { name: "Ryan", speciality: "Vue Components", show: false },
        { name: "Crystal", speciality: "Angular", show: false },
        { name: "Hitoshi", speciality: "HTML & Bootstrap", show: false },
        { name: "Tango", speciality: "Magento", show: false },
        { name: "Kami", speciality: "Laravel", show: false },
        { name: "Yoshi", speciality: "React", show: false },
      ],
    };
  },
  methods: {
    DeleteNinja() {
      this.ninjas.pop();
    }
  },
};
</script>

<style></style>
