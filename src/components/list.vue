<template>
  <ul class="list-group">
    <template v-for="(item, key) in items">
      <li :key="key" class="list-group-item d-flex">
        {{ item }}
        <button type="button" class="close ml-auto" @click="remove(key)">&times;</button>
      </li>
    </template>
  </ul>
</template>

<script>
export default {
  props: ["items"],

  methods: {
    remove(index) {
      this.$emit("remove", index);
    }
  }
};
</script>
