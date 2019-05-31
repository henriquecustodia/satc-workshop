<template>
  <div class="input-group">
    <input class="form-control" placeholder="Task name" v-model="value" @keydown.enter="add">
    <div class="input-group-append">
      <button class="btn btn-outline-secondary" type="button" @click="add">Add</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: ""
    };
  },

  methods: {
    add() {
      if (!this.value) {
        return;
      }

      this.$emit("add", this.value);

      this.value = "";
    }
  }
};
</script>

