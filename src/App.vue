<template>
  <div>
    <headerList v-bind:listElement="listElement"> </headerList>
    <div class="container">
      <div class="row">
        <div class="col">
          <h1></h1>
          <h2></h2>
          <form class="form-group">
            <label for="list"></label>
            <input
              type="text"
              class="form-control"
              id="list"
              placeholder="écrire ici.."
              v-model="element"
            />
            <button class="btn" v-on:click.prevent="doThat">add</button>
            <div>
              <ul>
                <li v-for="(element, index) in listElement" :key="index">
                  {{ element }}
                  <button class="btn" v-on:click.prevent="deleteThat(index)">
                    x
                  </button>
                </li>
              </ul>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderList from "./components/HeaderList.vue";

export default {
  data() {
    return {
      listElement: [],
      element: "",
    };
  },
  methods: {
    doThat: function () {
      this.listElement.push(this.element);
      console.log(this.listElement);
    },
    deleteThat: function (index) {
      this.listElement.splice(index, 1);
    },
  },
  name: "App",
  components: {
    headerList: HeaderList,
  },
};
</script>

<style>
body {
  background-color: #9cdcc4;
}
button {
  background-color: #41b783 !important;
}
</style>
