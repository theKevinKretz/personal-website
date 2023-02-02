<template>
    <footer class="footer footer-center p-4 bg-base-300 text-base-content">
        <div>
            <p>Copyright © {{ year }} - All right reserved by Mr. Kevin Kretz</p>
        </div>
    </footer>
</template>

<script setup>
const dt = new Date();
const year = (dt.getFullYear()).toString();
</script>