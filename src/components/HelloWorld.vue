<template>
  <div class="hello">
    <p>
      Hello,
      <span
        v-bind:class="['bg-gray', 'text-blue', objectClass]"
      >Vue.js</span>
      <!-- クラスにハイフンがつく場合、シングルコーテーションで囲む必要がある！！ -->
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: () => ({
    objectClass: {
      large: true,
      'text-danger': true
    }
  })
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.large {
  font-size: 32px;
}

.text-danger {
  color: red;
}

.bg-gray {
  background-color: gray;
}

.text-blue {
  color: skyblue;
}
</style>
