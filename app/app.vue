<template>
  <ClientOnly>
    <MglMap
      :map-style="style"
      :center="center"
      :zoom="zoom"
      height="100vh"
      >
      <MglNavigationControl />
    </MglMap>
  </ClientOnly>
</template>

<script setup>
const config = useRuntimeConfig();

const style = `https://api.maptiler.com/maps/streets/style.json?key=${config.public.maptilerKey}`;
const center = [139.622, 35.466];
const zoom = 15;
</script>
