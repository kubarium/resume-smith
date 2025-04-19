<script setup lang="ts">


</script>

<template>
<div class="flex flex-col min-h-screen">
  <MissionControl />
  <div class="bg-amber-950 p-4 flex flex-grow h-full w-full">

    <!-- <div class="bg-amber-50 flex-grow">Yebebod Content</div> -->
  <Splitter  class="flex-grow mb-8">
    <SplitterPanel class="flex items-center justify-center">
      <MarkdownEditor />
    </SplitterPanel>
    <SplitterPanel class="flex items-center justify-center"> Panel 2 </SplitterPanel>
  </Splitter>
  </div>
  <!-- <footer class="bg-amber-50 dark:bg-amber-900 text-amber-900 uppercase dark:text-amber-50 p-4 shadow-md mb-4">
    Resume Smith
  </footer> -->
</div>
</template>
