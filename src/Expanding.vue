<template>
  <transition
    @beforeEnter="beforeEnter"
    @afterEnter="afterEnter"
    @beforeLeave="beforeLeave"
    @afterLeave="afterLeave"
  >
    <slot></slot>
  </transition>
</template>

<script>
export default {
  methods: {
    beforeEnter (el) {
      el.classList.remove('collapse')
      el.style.display = 'block'
      el.classList.add('collapsing')
      el.style.height = `${el.scrollHeight}px`
    },
    afterEnter (el) {
      el.classList.remove('collapsing')
      el.classList.add('collapse', 'in')
    },
    beforeLeave (el) {
      el.classList.add('collapsing')
      el.classList.remove('collapse', 'in')
      el.style.height = 0
    },
    afterLeave (el) {
      el.classList.remove('collapsing')
      el.classList.add('collapse')
      el.style.display = 'none'
    }
  }

}
</script>

<style lang="scss" scoped>
.collapse {
  display: none;

  &.in {
    display: block;
  }
}

.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  transition: height .377s ease;
}
</style>

