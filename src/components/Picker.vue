<template>
    <div class="my-5">
        <p class="my-2">{{ isColor ? 'Color': nameOfPicker}}:</p>
        <div class="flex gap-2">
            <label v-for="(value, index) in valuesToPick" :key="index" class="cursor-pointer">
                <input
                    type="radio"
                    :name="nameOfPicker"
                    :value="value"
                    class="hidden peer "
                />
                <div
                    v-if="isColor"
                    :style="{ backgroundColor: value.value }"
                    class="w-12 h-8 rounded border-2 border-gray-300 peer-checked:border-black"
                >
                </div>
                <div
                    v-else
                    class="px-6 py-1 border-2 border-gray-300 rounded peer-checked:border-black"
                >
                    {{ value.name }}
                </div>
                
            </label>
        </div>
    </div>
</template>
<script setup>

defineProps({
    nameOfPicker: String,
    isColor: {
        type: Boolean,
        default: false
    },
    valuesToPick: {
        type: Array,
        default: () => []
    }
})
</script>