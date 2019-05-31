<template>
  <div class="container">
    <Input class="mt-2" @add="add"/>
    <List class="mt-2" :items="items" @remove="remove"/>
  </div>
</template>

<script>
import Input from "@/components/input.vue";
import List from "@/components/list.vue";

export default {
  components: {
    Input,
    List
  },
  data() {
    return {
      items: []
    };
  },
  methods: {
    add(value) {
      this.items.push(value);
    },
    remove(index) {
      this.$delete(this.items, index);
    }
  }
};
</script>
