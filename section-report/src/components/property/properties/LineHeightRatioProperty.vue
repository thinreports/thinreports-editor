<template>
  <TextProperty
    :label="$t('label.text.line_height_ratio')"
    placeholder="normal"
    :value="value"
    @change="update"
  />
</template>

<script lang="ts">
import Vue from 'vue';
import TextProperty from './base/TextProperty.vue';

export default Vue.extend({
  name: 'LineHeightRatioProperty',
  components: {
    TextProperty
  },
  props: {
    value: {
      type: [String, Number],
      default: ''
    }
  },
  methods: {
    update (value: string) {
      this.$emit('change', value);
    }
  }
});
</script>

<style scoped></style>
