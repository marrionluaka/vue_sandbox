<template lang="pug">
.relative
  img.h-9.w-9.rounded-full.object-cover.my-2(
    :alt="$props.alt"
    :src="$props.src"
  )
  span.absolute.bottom-1.p-1.right-0.rounded-full.border-2(:class="[className]")
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  props: {
    className: {
      type: String,
      default: 'bg-green-400 border-white'
    },
    alt: {
      type: String,
      default: 'Profile Image'
    },
    src: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2.35&w=144&h=144&q=80'
    }
  }
})
</script>
