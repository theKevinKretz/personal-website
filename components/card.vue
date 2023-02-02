<template>
    <div class="card w-96 bg-base-100 shadow-xl image-full">
        <figure><img :src="logo_url" alt="Logo" /></figure>
        <div class="card-body">
            <h2 class="card-title">{{ company }}</h2>
            <p>{{ description }}</p>
            <div class="card-actions justify-end">
                <button class="btn btn-primary">Learn more</button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    const props = defineProps({
    company: String,
    description: String,
    logo_url: String
  })
</script>