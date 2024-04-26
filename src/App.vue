<script setup lang="ts">
import { Navbar } from '@/components/ui/navbar';
import { Sidebar } from '@/components/ui/sidebar';
import { Content } from './components/ui/content';
import { MainHeader } from './components/ui/mainheader'
</script>

<template>
  <!--- Navbar block-->
  <Navbar/>

  <!--- Main Block-->
  <div class="relative overflow-hidden overflow-y-auto h-full">
    <div class="fixed top-8 right-0 left-0 w-full max-w-7xl mx-auto">
      <div class="mb-6 px-4 sm:px-0">
        <div class="flex items-start p-4 space-y-6 sm:space-y-0 mt-6 sm:mt-10">
            <Sidebar/>
            <div class="flex flex-1 flex-col m-6">
              <MainHeader/>
              <Content/>
            </div>
        </div>
      </div>
    </div>
  </div>

</template>

<style scoped>

</style>
