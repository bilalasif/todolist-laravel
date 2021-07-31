<template>
  <div>
    <div v-for="(item, index) in items" :key="index">
      <listItem :item="item" class="item" />
    </div>
  </div>
</template>
<script>
import listItem from "./listItem.vue";
export default {
  name: "listView",
  props: ["items"],
  components: { listItem },
};
</script>
<style >
.item {
  background: #e6e6e6;
  padding: 5px;
  margin-top: 5px;
}
</style>