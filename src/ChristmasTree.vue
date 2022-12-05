<script setup lang="ts">
interface Props {
  size: number
}

const props = withDefaults(defineProps<Props>(), {
  size: Number,
})

let dotsArray: number[] = []

for (let i = 0; i < props.size; i++) {
  dotsArray.push(i)
  console.log(i)
}

console.log(dotsArray)
</script>
<template>
  <div>
    <div class="flex flex-row justify-center">
      <!-- This div is styled for the tree sections, but it's not complete -->
      <div
        class="relative rounded-full bg-green w-16 h-16 -m-2 flex justify-center items-center"
        v-for="dot in dotsArray"
      />
    </div>
  </div>
</template>
