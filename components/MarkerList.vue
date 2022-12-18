<script setup>
import { CustomMarker } from 'vue3-google-map';

const props = defineProps({
    marker: {
        type: Object,
        required: true,
    }
});

</script>
    
<template>
    <CustomMarker
        :options="{ position: { lat: marker.lat, lng:  marker.lng }, anchorPoint: 'CENTER' }">
        <img src="/img/marker.svg" width="50" height="50" />
    </CustomMarker>
</template>