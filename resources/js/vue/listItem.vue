<template>
  <div class="item">
    <input
      type="checkbox"
      class="complted-checkbox"
      @change="updateCheck"
      v-model="item.completed"
    />
    <span :class="[item.completed ? 'completed' : '', 'itemText']">{{
      item.name
    }}</span>
    <button @click="remvoeItem" class="trashcan">
      <font-awesome-icon icon="trash" />
    </button>
  </div>
</template>
<script>
export default {
  name: "listItem",
  props: ["item"],
  methods: {
    updateCheck() {},
    remvoeItem() {},
  },
};
</script>
<style scoped>
.completed {
  text-decoration: line-through;
  color: #999999;
}
.itemText {
  width: 100%;
  margin-left: 20px;
  /* color: #ffff; */
}
.item {
  display: flex;
  justify-content: center;
  align-items: center;
}
.trashcan {
  background: #e6e6e6;
  border: none;
  color: #ff0000;
  outline: none;
  cursor: pointer;
}
.complted-checkbox {
  cursor: pointer;
}
</style>