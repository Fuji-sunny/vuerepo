<script>
export default {
  props: {
    value: {
      type: String
    }
  },
  render(h) {
    return h("textarea", {
      on: {
        input: e => {
          this.$emit("update:value", e.target.value);
        }
      }
    }, [this.value]);
  }
};
</script>
