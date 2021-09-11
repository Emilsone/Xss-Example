<template>
  <section id="app">
    <h1>Welcome to Your Vue.js App</h1>
    <div>
      <p v-html="dummytext" class="dummy-text"></p>
      <p v-html="purify(test)"></p>
    </div>
  </section>
</template>

<script>
import DOMPurify from "dompurify";
export default {
  name: "XssPage",
  data() {
    return {
      dummytext: "This is an xss example ",
      test: `<img src=x onerror=alert(5)>`,
    };
  },
  methods: {
    purify(text) {
      return DOMPurify.sanitize(text);
    },
  },
};
</script>