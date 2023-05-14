<template>
  <div class="accordion">
    <div v-for="(item, index) in items" :key="index" class="accordion__item">
      <button
        class="accordion__button"
        :class="{ 'accordion__button--active': activeIndex === index }"
        :aria-expanded="activeIndex === index ? 'true' : 'false'"
        :aria-controls="'accordion__content-' + index"
        @click="toggleItem(index)"
      >
        {{ item.title }}
        <span
          class="accordion__button__icon"
          :class="{ 'accordion__button__icon--active': activeIndex === index }"
          aria-hidden="true"
        ></span>
      </button>
      <div
        :id="'accordion__content-' + index"
        class="accordion__content"
        :aria-hidden="activeIndex !== index ? 'true' : 'false'"
      >
        <p class="accordion__text">{{ item.content }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Accordion',
  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      activeIndex: 0,
    }
  },
  methods: {
    toggleItem(index) {
      this.activeIndex = this.activeIndex === index ? -1 : index
    },
  },
  mounted() {
    const hash = window.location.hash
    if (hash && hash.startsWith('#accordion__content-')) {
      const index = Number(hash.replace('#accordion__content-', ''))
      if (!isNaN(index)) {
        this.activeIndex = index
      }
    }
  },
}
</script>