<script setup>
import HomePageHeader from '../components/HomePageHeader.vue';
import SearchOptions from '@/components/SearchOptions.vue';
import SearchInput from '@/components/SearchInput.vue';
</script>

<template>
  <main>
    <header>
      <div class="wrapper">
        <HomePageHeader msg="Search UI" />
      </div>
    </header>
    <SearchOptions />
    <SearchInput />
  </main>
</template>
