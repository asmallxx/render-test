

<script>
export default {
  props: {
    level: {
      type: Number,
      required: true
    }
  },

  render: function(createElement) {
    return createElement("h" + this.level, this.$slots.default);
  },

  created() {
    console.log(this.$slots);
  }
};
</script>
<style lang="less" scoped>
</style>
