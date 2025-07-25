<script setup lang="ts">
import Navigation from './components/Navigation/Navigation.vue';

</script>


<template>
  <div class="bg-[#0F141F] h-screen">
    <Navigation />

    <NuxtRouteAnnouncer />
    
    <AboutCard />

    <ProjectCard />
    
    <!-- Skills Card
    <Card>
      
    </Card> -->
    
    <ContactCard />
    
  </div>
</template>

<!-- <script setup>
 TODO: import TAOS for appear on scroll animation
import 'taos/dist/taos.css'
import { useTaos } from 'taos'
useTaos()
</script> -->