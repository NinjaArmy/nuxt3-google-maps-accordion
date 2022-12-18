<script setup>
import 'tw-elements';

const props = defineProps({
    marker: {
        type: Object,
        required: true,
    }
});

</script>
<template>
    <div class="accordion-item border-t-0 border-l-0 border-r-0 rounded-none bg-white border border-gray-200">
        <h2 class="accordion-header mb-0" :id="'heading-' + marker.id">
            <button class="
                    accordion-button
                    collapsed
                    relative
                    flex
                    items-center
                    w-full
                    py-4
                    px-5
                    text-base text-gray-800 text-left
                    bg-white
                    border-0
                    rounded-none
                    transition
                    focus:outline-none" type="button" data-bs-toggle="collapse" :data-bs-target="'#' + marker.id"
                aria-expanded="true" :aria-controls="marker.id">
                {{ marker.headline }}
            </button>
        </h2>
        <div :id="marker.id" class="accordion-collapse border-0 collapse" :aria-labelledby="'heading-' + marker.id"
            data-bs-parent="#accordionFlushExample">
            <div class="accordion-body py-4 px-5">
                {{ marker.text }}
            </div>
        </div>
    </div>
</template>