<template>
  <h1>{{ msg }}</h1>

  <p>
    Recommended IDE setup:
    <a
      href="https://code.visualstudio.com/"
      target="_blank"
    >VSCode</a>
    +
    <a
      href="https://marketplace.visualstudio.com/items?itemName=octref.vetur"
      target="_blank"
    >Vetur</a>
    or
    <a
      href="https://github.com/johnsoncodehk/volar"
      target="_blank"
    >Volar</a>
    (if using
    <code>&lt;script setup&gt;</code>)
  </p>

  <p>See <code>README.md</code> for more information.</p>

  <p>
    <a
      href="https://vitejs.dev/guide/features.html"
      target="_blank"
    >Vite Docs</a> |
    <a
      href="https://v3.vuejs.org/"
      target="_blank"
    >Vue 3 Docs</a>
  </p>
  <p>
    counter is {{ counter }}
  </p>
  <button
    class="hello_world__button"
    @click="increaseCounter"
  >
    increase counter
  </button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { mapState, mapActions } from "vuex";

export default defineComponent({
  name: 'Hello',
  props: {
    msg: {
      type: String,
      required: true,
      default: "Hello Vue 3"
    }
  },
  computed: {
    ...mapState(["counter"]),
  },
  methods: {
    ...mapActions(["increaseCounter"]),
  },
})
</script>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
