<script setup lang="ts">
import { ref } from 'vue'
import { BooBash } from 'vue-boo-bash'
import 'vue-boo-bash/style.css'

// Optional and reactive game settings
// On change, the game will immediately update
const settings = ref({
    maxGameTime: 40 // specify the game time in seconds - default 30 seconds
    // maxGhosts: 10, // specify the maximum number of ghosts - default 10
    // spawnDuration: 2000, // specify the spawn rate for new ghosts - default 2000ms
    // music: undefined, // specify source for background music
    // debug: true
})
</script>

<template>
    <main class="absolute inset-0 bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500">
        <BooBash :settings="settings" />
    </main>
</template>
