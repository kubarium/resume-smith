<script setup lang="ts">
import { Codemirror } from 'vue-codemirror';
import { markdown } from '@codemirror/lang-markdown'
import { ayuLight } from 'thememirror'

const code = ref(`console.log('Hello, world!')`)
const extensions = [markdown(), ayuLight]

// Codemirror EditorView instance ref
const view = shallowRef()
const handleReady = (payload) => {
  view.value = payload.view
}

const getCodemirrorStates = () => {
  const state = view.value.state
  const ranges = state.selection.ranges
  const selected = ranges.reduce((r, range) => r + range.to - range.from, 0)
  const cursor = ranges[0].anchor
  const length = state.doc.length
  const lines = state.doc.lines
  // more state info ...
  // return ...
}
</script>

<template>
  <Codemirror v-model="code" placeholder="Code goes here..." :style="{ height: '400px' }" :autofocus="true"
    :indent-with-tab="true" :tab-size="2" :extensions="extensions" @ready="handleReady"
    @change="console.log('change', $event)" @focus="console.log('focus', $event)" @blur="console.log('blur', $event)" />
</template>

<style scoped>
</style>
