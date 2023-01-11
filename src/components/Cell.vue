<template lang="html">
  <div class="cell" :class="classObj"></div>
</template>

<script>
export default {
  name: 'cell',
  props: ['value'],
  computed: {
    classObj: function () {
      return {
        snake: this.value === 1, // Snake lentgh value (Can't change)
        treat: this.value === 2 // Treat quantity value ? (Can't change)
      }
    }
  }// ↓ Snake and treats color 
}
</script>

<style lang="css">
  .cell {
    width: 1em;
    height: 1em;
    float: left; 
  }
  .snake {
    background: rgb(180, 0, 0);
    z-index: 2;
  }
  .treat { 
    background: rgb(150, 0, 0);
    z-index: 2;
  }
</style> 
